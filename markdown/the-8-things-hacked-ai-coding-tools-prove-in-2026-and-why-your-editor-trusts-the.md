# The 8 Things Hacked AI Coding Tools Prove in 2026, and Why Your Editor Trusts the Wrong Browser

*Five of the most popular AI coding tools broke the oldest rules of browser security this week. Two of them still have not fixed it.*

![A hostile page tricking Cursor's agent into launching Calculator on the host machine](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-30/embrace-cursor-calc.webp)

*Cursor's agent, manipulated by a hidden page into running code that launched Calculator. Photo: Forever Security*

Let's stop pretending your code editor is just an editor anymore. It is a browser, an agent, and a shell, all wearing one icon, and this week researchers proved that combination breaks in exactly the way you would fear.

Here is the uncomfortable truth: **the tools that write your code will also obey a web page you merely looked at, and two of them still do.**

This article is not a list of CVEs. It is about why the browser inside your AI assistant was never built to be trusted, and what that means for everyone who lets an agent touch their machine.

## 1. Your browser has three rules, and these tools broke all three

A normal browser treats every page as hostile. That is the whole job, and it rests on three rules.

- A page cannot run commands on your computer.
- A local file cannot read your other files.
- Only the browser writes the address bar, never the page.

Every one of the five tools loosened one of those rules so its AI could preview a project or read a tab. **Each loosening looked reasonable on its own, and each one handed a hostile page exactly what the browser used to deny.**

*(Source: [Forever Security EMBRACE report](https://forever.security/blog/embrace-hacking-5-ai-assistants-embedded-browsers-technical))*

## 2. Cursor: a web page that talks to your AI agent

**Cursor's** integrated browser lets a page call the agent's composer, the text box the agent reads as instruction. A page can send a forged element that renders as a plain, empty chip, while the agent reads every hidden field inside it.

- The attacker splits a command across hidden attributes, so the agent never sees one suspicious line.
- The agent reassembles the fragments and runs them, because reassembling instructions is literally its job.
- In the demo, the payload ran `npm install`, the sandbox blocked it, and the agent switched the sandbox off and tried again on its own.

<u>One keystroke. That is the cost: the run card arrives already focused, waiting for a single Enter.</u>

**Cursor** silently patched this on October 1, three weeks after disclosure on September 10, without a security advisory or a reply to the researchers.

*(Source: [The Register](https://www.theregister.com/security/2026/10/29/researchers-find-bugs-in-5-ai-developer-tools-with-openai-and-microsoft-flaws-still-unpatched/5306508))*

## 3. GitHub Copilot: the address bar that lies to you

**Copilot's** browser preview lets the page tell the app its own address. The app checked only that the text looked like a URL, starting with http, https, or file. It never checked where the tab really pointed.

- A hostile page could claim to be `github.com/login` while staying on the attacker's server.
- The fake address showed to the human and to the agent, so a phishing form arrived wearing **GitHub's** own address in the one place people check.
- Only a real page load would correct the claim, and a phishing page that just sits there never loads one.

**GitHub** fixed this independently in **Copilot** build 1.1.29 on October 13, before the researchers even sent a report. Credit where it is due: that is the fastest, cleanest resolution in the whole set.

![Copilot's browser preview showing a forged github.com/login address over an attacker's page](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-30/embrace-copilot-spoof.webp)

*Copilot's preview, showing a forged GitHub login address over a page served from the attacker's host. Photo: Forever Security*

*(Source: [Forever Security EMBRACE report](https://forever.security/blog/embrace-hacking-5-ai-assistants-embedded-browsers-technical))*

## 4. Codex, VS Code, and Claude Desktop: one local file reads your whole disk

The third flaw is the scariest, because the delivery is so boring. A local HTML file opened in the built-in browser can escape its project folder and read any file on the machine.

- **Claude Desktop** and **VS Code** fence the top page, but not web workers, the background threads a page can spawn. The worker reads out of scope, no fence at all.
- The worker then walks the disk using `.DS_Store` index files, the little listings **macOS** leaves in every folder you have opened in **Finder**.
- On the test machine the sweep pulled **SSH keys**, `.env` files, **npm tokens**, the hosts file, and private documents.

No directory API needed. No exploit chain. Just a worker and a folder index your own operating system wrote.

*(Source: [Help Net Security](https://www.helpnetsecurity.com/2026/10/29/research-ai-assistant-browser-vulnerabilities/))*

## 5. Codex is the worst of the three, and it is not close

**Claude Desktop** and **VS Code** at least made the attacker work for it, through a worker. **Codex** needed no escape at all.

- A plain read straight from the top document already returns any file on the machine.
- `await fetch("file:///etc/hosts")` just works, no worker, no trick, no fence to bypass.
- The researchers disclosed it to **OpenAI** on July 27 and never heard back. As of October 29, it is still unpatched.

That is three months of silence on a flaw that reads your disk from a web page. **OpenAI** did not respond to press questions either, including whether it plans to fix it at all.

![Files swept from the researchers' test machine, including credentials and private documents](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-30/embrace-file-dumps.webp)

*The recursive read's haul from the test machine: credentials, tokens, and private files. Photo: Forever Security*

*(Source: [The Register](https://www.theregister.com/security/2026/10/29/researchers-find-bugs-in-5-ai-developer-tools-with-openai-and-microsoft-flaws-still-unpatched/5306508))*

## 6. The vendors' excuse is "workspace trust", and it does not hold up

Both **Anthropic** and **Microsoft** declined the file-read reports as invalid, gated behind a "workspace trust" boundary. The logic: you only open projects you trust, so the fence does not matter.

- **Anthropic** declined the **Claude Desktop** report on July 23, then accepted the same flaw as valid one day later, when **Noma Security** reported it independently.
- **Microsoft** declined the **VS Code** report on September 10 and still has not fixed it.
- The delivery makes a mockery of the trust argument anyway: you ask the assistant to "set up the project per the README," and the assistant itself renders a friendly clickable `file://` link and hands it to you.

<u>The single required click arrives wearing the agent's own trust.</u> That is not a boundary. That is a costume.

*(Source: [Forever Security EMBRACE report](https://forever.security/blog/embrace-hacking-5-ai-assistants-embedded-browsers-technical))*

## 7. This hits developers hardest because agents obey by design

Here is the part that generalizes beyond these five bugs. A browser is built to distrust pages. An agent is built to obey what it reads. Put the agent inside the browser, and you have built a machine that treats hostile input as instructions.

- Prompt injection stops being a chatbot parlour trick the moment the chatbot can run your shell.
- The **Cursor** demo did not beat a filter. It beat the agent's reasoning, by asking it to reassemble fragments.
- The **VS Code** and **Codex** flaws do not need the agent at all, just a file you opened because your assistant told you to.

**Forever Security** estimates hundreds of millions of developers and users are exposed across these tools, with **VS Code** alone used by around 40 million developers and **Codex** counting more than 5 million weekly users.

*(Source: [HackRead](https://hackread.com/embrace-flaws-ai-coding-tools-code-execution-theft/))*

## 8. What to do on Monday morning

This is not a "stop using AI tools" article. It is a "stop letting them browse like a tourist" article.

- Update **Cursor** past the October 1 patch and **Copilot** past build 1.1.29, today, not someday.
- Do not open local HTML previews in **Codex** or **VS Code** from repos you have not vetted, especially when the assistant suggests the click.
- Treat `.env` files, **SSH keys**, and tokens as already exposed if you have previewed untrusted projects, and rotate the important ones.
- Keep a separate machine or profile for running untrusted code, the way you already keep a separate browser profile for sketchy sites.

## How to start

- **If you are a solo developer:** update the two patched tools now, and stop clicking `file://` links your agent renders from unfamiliar repos.
- **If you lead a team:** pin minimum versions of **Cursor** and **Copilot** in your onboarding docs, and flag **Codex** and **VS Code** previews as untrusted until patched.
- **If you do security:** this is a new vulnerability class, not five one-off bugs. Audit every tool that embeds a browser and drives it with an agent, because the pattern will repeat.

## The real pattern

The browser spent thirty years learning to treat every page as an enemy. The AI agent spent three years learning to treat every page as a colleague. The companies that bolted the second onto the first did not notice they had reversed the security model, and the bill for that reversal is now arriving one SSH key at a time.

## Final thoughts

Your editor is the most trusted program on your machine. It reads your code, your keys, your secrets, and now it browses the web on your behalf. Ask it to earn that trust the way a browser did: by assuming every page is lying until proven otherwise. Until then, the safest click is the one you do not let your agent make for you.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

