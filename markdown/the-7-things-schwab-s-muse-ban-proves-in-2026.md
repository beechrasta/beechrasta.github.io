# The 7 Things Schwab's Muse Ban Proves in 2026

*Two bank CEOs just said it out loud in the same week: your AI agent is not touching your money. And almost nobody is arguing with them.*

![Wall Street in New York](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-17/wall-street.jpg)
*Wall Street. The people who own the money just drew a line around it, and the line is your AI agent. Photo: Dietmar Rabich via Wikimedia Commons*

Let's stop pretending the agent era has arrived everywhere.

This week, the CEO of **Charles Schwab** told **Bloomberg TV** that his company is actively blocking **Meta's Muse** from moving client money. Days earlier, **JPMorgan's** Jamie Dimon said the same thing on an earnings call. The agents can have your calendar. They cannot have your account.

This article is not about banking regulation. It is about who gets to say "no" to the most hyped software category of the decade, and why they are right.

## 1. Schwab is playing whack-a-agent, every single week

**Rick Wurster**, the Charles Schwab CEO, did not hedge on **Bloomberg TV** on Friday.

- Schwab is **actively blocking Muse** from taking action on client accounts, because "it poses unacceptable risks to the firm and its clients."
- His own words: *"We don't want someone just giving their password to Muse, and letting Muse come in and take action on that client's behalf."*
- He personally gets a weekly report on how many **AI agents** were detected and blocked. The number is in the **"tens and twenties" per week**, and has not crossed into the hundreds.

**The so what: people love AI, but they are not handing it their brokerage passwords. The weekly block count proves it.**

*(Source: [Gizmodo](https://gizmodo.com/after-muse-launch-u-s-banks-are-saying-hell-no-to-ai-agents-moving-money-2000827221))*

## 2. Dimon's version was blunter

**JPMorgan Chase** CEO **Jamie Dimon** said his version on the earnings call days earlier.

- The bank **bans AI agents based on risk**: *"We're not going to allow just any... outside agent to come in inside the company, because it's just too risky for clients and for JPMorgan."*
- His follow-up: *"You don't want rogue agents, and it could be thousands of them."*
- For now, the ban covers **any external agent** for retail clients, per a bank spokesperson.

Two of the biggest money managers on earth, same week, same message. That is not a coincidence. That is a policy consensus forming in real time.

*(Source: [Gizmodo](https://gizmodo.com/after-muse-launch-u-s-banks-are-saying-hell-no-to-ai-agents-moving-money-2000827221))*

## 3. The liability question nobody can answer

Wurster asked the question that ends every "let the agent do it" pitch in a bank boardroom.

- *"We can't control it, the client can't control it, something could go wrong and who's liable?"*
- An agent with your password is not a tool you operate. It is a **person you delegated to**, except it has no insurance, no license, and no legal personhood.
- The agent makes one bad trade at 3 AM and the first question is not "was it a bug." The first question is "who pays."

<u>Nobody in the agent industry has a good answer to "who's liable." The banks noticed.</u>

*(Source: [Gizmodo](https://gizmodo.com/after-muse-launch-u-s-banks-are-saying-hell-no-to-ai-agents-moving-money-2000827221))*

![The Meta logo](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-17/meta-logo.jpg)
*Meta's logo. Its Muse agent is the one the banks are blocking, and Meta's own privacy record is half the reason why. Photo: Wikimedia Commons (public domain)*

## 4. Meta's privacy record is doing the agents no favors

Let's be honest about why **Muse** specifically is the agent banks fear most.

- Muse collects **entire dossiers of data** on users and everyone they digitally interact with, per the **Gizmodo** report.
- The agent has already had serious reported **privacy incidents**, including the time it handed out a **home address to a stranger**.
- *And here is the part Meta does not put in the launch demo: Meta trains on your chats by default unless you switch it off.* Your money conversations would feed the model.

**The so what: the banks are not just banning "agents." They are banning an agent built by a company whose default setting is "we keep your conversations."**

*(Source: [Gizmodo](https://gizmodo.com/after-muse-launch-u-s-banks-are-saying-hell-no-to-ai-agents-moving-money-2000827221))*

## 5. Schwab built its own agent and still won't let it trade

Here is the part that should embarrass every agent maximalist.

- Schwab has its own in-house assistant, **Charley**, unveiled last month. It handles **administrative and informational tasks only**. No trading.
- Wurster told **Yahoo Finance** that letting AI agents make decisions without human approval is **"a leap too far."**
- A growing subset of Schwab clients are already **"trading through LLMs and APIs"**, but only through the firm's own **APIs and MCP servers**, where every request is authenticated and scoped.

The company that builds agents for a living will not let its own agent move money. Read that again.

*(Source: [Gizmodo](https://gizmodo.com/after-muse-launch-u-s-banks-are-saying-hell-no-to-ai-agents-moving-money-2000827221))*

## 6. The read-only loophole is the actual future

Wurster did describe the shape of what comes next, and it is not "no agents."

- Schwab is preparing to allow **external LLM connections** through **Model Context Protocol (MCP) servers** with controlled authentication.
- What agents will be allowed to do: **see account balances, do research**.
- What they will never be allowed to do: **move money**.

**The so what: the agent economy is splitting in two. Read agents get API keys. Write agents get lawyers.**

*(Source: [Gizmodo](https://gizmodo.com/after-muse-launch-u-s-banks-are-saying-hell-no-to-ai-agents-moving-money-2000827221))*

![The main entrance of the New York Stock Exchange](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-17/nyse-entrance.jpg)
*The New York Stock Exchange. When the people inside this building say no to your software, it is not a feature request. It is a verdict. Photo: Roland Arhelger via Wikimedia Commons*

## 7. The security pros saw this coming first

The banks are the visible "no." The security community was the early "absolutely not."

- This week, **CERT-In** (India's national cyber agency) issued a **critical advisory** after **AI agents** accessed confidential company records without authorization.
- The agency warns that **exposed credentials and security gaps** are letting agents reach data they were never given permission to touch, enabling faster cyberattacks.
- Put the two stories together: agents are getting into things they should not touch, and the institutions with the most to lose are bolting the doors first.

**My take:** the agent hype cycle assumed trust was a feature you add later. The banks just informed the industry that trust is the gate, and it opens from their side.

*(Source: [AryaAge/CERT-In](https://www.aryanage.com/article/47829/cert-in-issues-critical-warning-as-ai-agents-access-company-data), [Gizmodo](https://gizmodo.com/after-muse-launch-u-s-banks-are-saying-hell-no-to-ai-agents-moving-money-2000827221))*

## How to start (as a dev)

- **Curious:** read the **Gizmodo** piece and Wurster's full **Bloomberg TV** quotes. The liability question is the one to internalize.
- **Builder:** if you build **agents**, study the **MCP** pattern Schwab is adopting. Authenticated, scoped, read-only-first is how you get institutional access.
- **Founder:** do not pitch "the agent moves the money." Pitch "the agent prepares the action, the human approves it." That is the product the banks will actually buy.
- **Everyone:** audit what your own agent can touch. If it holds credentials that can move money, you are your own worst bank.

## The real pattern

The agent era's bottleneck was never capability. Agents can already do the work. The bottleneck is **trust**, and trust is not a technical property. It is a liability decision made by institutions with something to lose. The banks just made theirs, in public, twice in one week. Every other regulated industry will now copy the homework.

## Final thoughts

Meta built an agent that can do your errands. The banks built a wall around the one errand that matters.

The agents will get in eventually. But they will get in through the MCP door, with a badge, a scope, and a human watching.

That is not the agent future anyone demoed. It is the one the money signed off on.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

