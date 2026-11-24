# The 9 Things Cisco and OpenAI's Shirudo Proves in 2026, and Why Linux Just Learned to Defend Itself

Let's stop pretending patching is a plan. A critical vulnerability drops, and the clock starts: somebody has to write the fix, test it, ship it, and get it onto every machine before attackers weaponize it. That gap has always been the whole game.

**Cisco** and **OpenAI** launched **Shirudo** on November 23, 2026, an open source project that puts a shield on a running **Linux** system while the real patch is still being built. No reboot. No downtime. An **AI agent** writes the protection, and a human still holds the keys.

This article is not a product announcement. It is about the moment defense stopped being something humans do at human speed.

![Cisco headquarters in San Jose](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-24/cisco-hq.jpg)

*Cisco's headquarters in San Jose, California. Image: Computerworld*

## 1. The patch gap is the whole game now, and attackers know it

- A defender has to protect every machine, all the time. An attacker only needs one machine that has not been patched yet.
- **AI** tools now help attackers find and weaponize flaws faster than most teams can patch. In some cases exploitation starts before a flaw is even publicly disclosed.
- **Shirudo** exists for exactly that stretch: the days or weeks between disclosure and a patch landing everywhere.

**The patch was never the defense. The window was always the battlefield.** **Shirudo** is the first tool built to fight in it.

*(Source: [Cisco Newsroom](https://newsroom.cisco.com/c/r/newsroom/en/us/a/y2026/m11/cisco-and-openai-launch-shirudo-a-new-project-to-safeguard-agentic-ai.html))*

## 2. Shirudo is not a patch, it is a shield, and the difference matters

- A patch fixes the vulnerable code permanently. A shield blocks the path to the vulnerable code temporarily.
- Shields go live only when the evidence says they are safe, after testing against the exploit and against legitimate traffic.
- **Shirudo** is Japanese for "shield", and the name is the design: a narrow, targeted protection that leaves everything else running.

**A patch says the bug is gone. A shield says the attack cannot reach the bug.** One of those you can deploy today, the other takes a release cycle.

*(Source: [Cisco Newsroom](https://newsroom.cisco.com/c/r/newsroom/en/us/a/y2026/m11/cisco-and-openai-launch-shirudo-a-new-project-to-safeguard-agentic-ai.html))*

## 3. eBPF is the trick that makes any of this possible

- **eBPF** lets small programs run at specific points inside the **Linux** kernel without changing its source code and without restarting anything.
- A kernel verifier checks every program before it is allowed to run, and kernel security controls restrict who can load changes at all.
- **Shirudo** uses **eBPF** to load a shield into a running system, then removes it cleanly once the real patch arrives.

<u>If you run Linux, eBPF has been quietly sitting in your kernel for a decade waiting for a job exactly like this one.</u> It was built to evolve a running system without interrupting it, and that is precisely what patching cannot do.

*(Source: [Isovalent](https://isovalent.com/blog/post/cisco-openai-shirudo/))*

## 4. Codex writes the shield, humans hold the keys

- The agent workflow runs as a loop: ingest the vulnerability details, build a reproducer for the exploit, pick a mitigation point, and test that the fix blocks the attack without breaking normal use.
- **OpenAI's Codex** generated the shield in the project's reference demonstration.
- **AI agents** do the legwork across the full stack, while people keep the keys and set the boundaries. Nothing loads without human approval.

**The agent is the intern who works at machine speed. The human is still the boss.** That division of labor is the entire bet.

*(Source: [Pandromeda](https://pandromeda.com/ai/openai-and-cisco-launch-shirudo-an-open-source-ebpf-shield-for-linux))*

## 5. Java4Shell proved it on a live Elasticsearch box

- In a controlled demonstration, a **Codex**-generated shield blocked a **Java4Shell** exploit attempt against a running **Elasticsearch** service, with no restart.
- **Java4Shell** is **CVE-2026-114938**, a flaw in the **OpenJDK Base64** decoder that attackers began probing earlier in November.
- The shield added an input check to the **Java** decoder inside the running process. The exploit was rejected, **Elasticsearch** kept serving requests.
- **Cisco** says **Shirudo** also wrote code that detected and blocked attempts to exploit a recent **PHP** flaw.

**A demo against a real CVE on a real service is worth a hundred architecture diagrams.** This one stopped the exploit and the service never blinked.

*(Source: [Interesting Engineering](https://interestingengineering.com/ai-robotics/openai-cisco-shirudo-linux-security-runtime))*

![Server racks in a data center](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-24/linux-server-room.jpg)

*The Linux servers Shirudo is built to protect, running while the shield goes in. Image: LinuxClouds*

## 6. It is Tetragon, rewritten for the agent era

- **Shirudo** has its roots in **Tetragon**, the **eBPF**-based security platform **Isovalent** open sourced back in 2022.
- **Tetragon's** policy language was designed for humans. **Shirudo** is a ground-up rewrite that lets agents interact in their natural language: code.
- The crucial learning, per **Isovalent** engineers **Thomas Graf** and **Liz Rice**: to unlock defense at machine speed with agents, you have to let agents speak code, not fill in policy forms.

**The rewrite is the story.** **Cisco** did not bolt an agent onto a human tool. It rebuilt the tool so the agent is the native operator.

*(Source: [Isovalent](https://isovalent.com/blog/post/cisco-openai-shirudo/))*

## 7. Signed shields and a TPM receipt, because the shield itself is code

- Every shield is cryptographically signed, and the host verifies the signature before it runs, even if an attacker has gained administrator access.
- Shields are delivered as signed **.bee** packages through an **OCI** registry, and a **Trusted Platform Module (TPM)** keeps a verifiable record of what was loaded and removed.
- The architecture splits into a one-shot CLI, so no permanently running daemon is needed, and an **eBPF** control plane loaded at boot.

**Think about what that trust model means: even root cannot sneak in an unsigned shield.** The moment you let agents write kernel code, the signature check stops being a feature and becomes the whole product.

*(Source: [Cisco Blog](https://blogs.cisco.com/news/expanding-the-defenders-window-with-self-defending-infrastructure))*

## 8. It is pre-release and honest about it, which is rarer than it sounds

- The **GitHub** project calls itself pre-release, and the README says it is not ready for production fleets.
- Production targets need a **Linux** kernel with the signed-loader interface and **Shirudo's** kernel patches, plus a **TPM 2.0** chip.
- The code is on **GitHub** at **shirudo-dev/shirudo** (390 stars on day one) under a **BSD 2-Clause** license, with the **BPF** programs dual-licensed **BSD** and **GPL**.

**A security project that tells you it is not production-ready on launch day is a security project you can trust.** The ones that oversell are the ones that get people breached.

*(Source: [cybersixt](https://cybersixt.com/originals/openai-cisco-shirudo))*

![Linux server racks](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-24/linux-racks.jpg)

*Linux runs most of the internet's servers, which is why a Linux shield matters at this scale. Image: Ars Technica*

## 9. The open source bet: shields ship with disclosures

- **OpenAI** says its aim is to publish tested shields alongside vulnerability disclosures, so operators can deploy a temporary protection while they prepare the permanent patch.
- **Cisco** and **OpenAI** are inviting developers, researchers, and enterprises to contribute: a test that reproduces a vulnerability, a shield run against a kernel build you use, a report of where it breaks legitimate traffic.
- A deep-dive technical webinar is scheduled for December 15.

**When one team finds a better way to protect a system, others should not have to start from scratch.** That sentence, from **Greg Brockman**, is the whole open source argument in one line.

*(Source: [MLQ.ai](https://mlq.ai/news/cisco-and-openai-release-shirudo-an-open-source-tool-that-shields-linux-systems-until-patches-land/))*

## How to start

- **Security engineer or kernel developer:** clone **shirudo-dev/shirudo** on **GitHub**, read the README, and run the virtual-machine quickstart. It is built to be tried in a VM, not on your production fleet.
- **Infrastructure operator:** check whether your fleet kernels support the signed-loader interface and whether your machines carry **TPM 2.0**. Those two answers decide whether **Shirudo** is a this-quarter project or a next-year one.
- **Security researcher:** the highest-value contribution is a reproducer test for a vulnerability you know well. The project is explicitly asking for them.
- **Everyone else:** register for the December 15 technical webinar. The **Isovalent** team is doing the deep dive there, and the architecture is worth an hour of your time even if you never touch a kernel.

## The real pattern

Defense is moving from patch faster to defend while you patch. The window between disclosure and a patch landing everywhere is now the battlefield, and the side that automates that window wins it. Shirudo is the first serious attempt to put an agent in that window, with a signature check and a human in charge.

## Final thoughts

Every security team already knows the patch will be late. The honest ones admit the window is where breaches happen. **Shirudo** does not pretend the window will close. It just puts a shield in it, and dares the next exploit to get through.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

