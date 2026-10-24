# The 9 Things Anthropic's AI Worm Proves in 2026

Forget antivirus. The next malware does not need you to click anything, and it learns while it spreads.

![Dario Amodei, CEO of Anthropic](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-19/dario-amodei.jpg)
*Dario Amodei, Anthropic's CEO. His offensive research team built the worm as a warning. (Photo: UK Prime Minister's office, CC BY 2.0, via Wikimedia Commons)*

Let's stop pretending AI malware is a future problem.

Anthropic's own red team just built a self-replicating AI program that spread by itself through internet-connected smart TVs. No phishing email, no shady download, no human trickery required. The uncomfortable truth: the only thing stopping a real one is compute power, and that excuse expires this year.

This article is not a list of scary predictions. It is about the 9 things this demo actually proves, and what each one means for you.

## 1. The worm split itself across 15 TVs and kept working

Anthropic's offensive research team built a malicious AI program that spread autonomously through internet-connected smart TVs.

- It "split parts of itself" among **15 televisions**
- Each TV donated a sliver of computing power, and the worm still functioned
- The team compared it to Voldemort's horcruxes, the nerdiest and most accurate security metaphor of 2026

The **so what**: this proves the architecture works, not just the theory.

*(Source: [Guardian](https://www.theguardian.com/technology/2026/oct/18/anthropic-ai-worm-worries))*

## 2. Sharding is the whole trick

Normal AI needs serious compute, which is why nobody took AI malware seriously until now.

- The worm shards its model across many weak devices instead of needing one strong one
- Fifteen TVs, each contributing a little, equals one working malicious mind
- Your living room is now a **distributed compute cluster** for whoever gets there first

![Anthropic logo](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-19/anthropic-logo.jpg)
*The Anthropic logo. The warning comes from the company's own offensive research team. (Image: Anthropic, public domain, via Wikimedia Commons)*

<u>The attacker does not need a data center. They need your gadgets.</u>

## 3. "By year's end" is the timeline

Anthropic's researchers were blunt about how close this is.

- A truly capable worm needs more capability on weaker devices than exists today
- Current trends make it feasible **by the end of 2026**, roughly ten weeks away, not ten years
- Chris Inglis, former NSA deputy director, says the plausibility question "has been settled by several breakout events over the past six months"

The **so what**: this is a this-Christmas problem, not a sci-fi problem.

*(Source: [Guardian](https://www.theguardian.com/technology/2026/oct/18/anthropic-ai-worm-worries))*

## 4. AI worms learn, old viruses just execute

This is what separates an AI worm from every piece of malware you have ever met.

- Classic viruses follow fixed instructions; AI models **learn as they go**
- Anthropic theorizes a worm could keep adapting to new hardware by researching newly disclosed vulnerabilities itself
- A worm that reads vulnerability databases for fun is a new species of attacker

The **so what**: static defenses assume a static enemy. That assumption just died.

*(Source: [Anthropic research](https://www.anthropic.com/research/self-replicating-ai))*

## 5. Your smart devices never get patched

The worm's favorite habitat is the device you forgot has an IP address.

- Smart TVs, ovens, and cameras get patched far less often than phones or laptops
- Anthropic warned days earlier that models are "months away" from self-replication on smart devices
- Every unpatched gadget is a **free hotel room** for a worm

![Server rack with networking equipment](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-19/server-rack.jpg)
*Networked equipment like this is what worms spread through. Your TV is quietly part of the same club. (Photo: Federal Bureau of Investigation, public domain, via Wikimedia Commons)*

The **so what**: the patch gap is the real vulnerability, not the AI.

## 6. We have seen this movie, it was called 1988

The Morris worm is the direct ancestor of everything Anthropic just demoed.

- In 1988, a graduate student released the Morris worm, exploiting software flaws and weak passwords
- Infected machines slowed to a stop; it was an accident that became a legend
- The difference now: the 1988 worm could not **think about its next move**

The **so what**: history rhymes, but this time the worm has a brain.

## 7. The damage math is already in the tens of billions

State actors industrialized worms decades ago, and the receipts are public.

- Stuxnet (US and Israel, late 2000s): sabotaged Iranian nuclear centrifuges, stealthily
- NotPetya (Russian) and WannaCry (North Korean-attributed): **tens of billions of dollars** in global damage
- Those were dumb worms following scripts. Add learning and the ceiling lifts.

The **so what**: we already know how bad worms get. Now make them smart.

## 8. The skeptics are not wrong, just early

Not everyone is buying the panic, and the pushback deserves a hearing.

- Juan Andres Guerrero-Saade, SentinelOne's VP of research, dismissed the demo as "nifty stunt hacking"
- A University of Toronto paper from months earlier infected a full-size computer and spread faster than the TV worm
- Joshua Saxe, who led Meta's AI security effort, and Ariel Herbert-Voss, an early OpenAI security expert now running RunSybil, are taking it seriously
- For the record: Anthropic did not respond to the Guardian's interview request

<u>Skepticism is healthy. "Nifty stunt hacking" is what every real attack looked like first.</u>

## 9. What developers actually do about this

Enough fear. Here is the builder's checklist.

- Treat every smart device on your network as **untrusted by default**
- Segment IoT onto its own VLAN; your TV does not need to see your laptop
- Patch aggressively, and buy devices from vendors with a real update policy
- If you ship agents, assume a hostile environment: least privilege, signed actions, human approval for anything irreversible

The **so what**: the defense is boring and it works. Boring is underrated.

## How to start

- **If you are a developer:** put your home IoT on a separate network this weekend. Twenty minutes of router config kills the easiest attack path.
- **If you build agents:** add an approval gate before any irreversible action. Your agent will thank you when the worm comes knocking. *(It will not thank you. It has no feelings. Add the gate anyway.)*
- **If you just own a smart TV:** check for a firmware update tonight. Yes, really.

## The real pattern

Every defensive assumption in security was built for enemies that follow scripts. AI worms do not follow scripts, they write new ones. The entire industry is about to re-learn the Morris worm lesson, except this time the adversary improves between infections.

## Final thoughts

Your TV was a screen. Then it was a computer. Now it might be a horcrux.

Patch your stuff.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

