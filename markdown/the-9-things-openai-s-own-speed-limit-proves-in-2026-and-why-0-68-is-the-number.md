# The 9 Things OpenAI's Own Speed Limit Proves in 2026, and Why 0.68 Is the Number to Watch

*OpenAI just asked the whole industry to slow down. The scariest part is the chart it published to make the case.*

![OpenAI's perplexity chart, showing the log-perplexity of its models falling from GPT-3.5 to its newest models](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-23/openai-perplexity-hero.png)
*OpenAI's own chart: one number, falling fast, and a proposal to stop it at an agreed line. Image credit: OpenAI*

Let's stop pretending the AI race has a referee. For years, every frontier lab has sprinted in the dark, publishing benchmarks nobody trusts and keeping its real progress numbers locked in a drawer.

Here's the uncomfortable truth: **OpenAI just opened the drawer**, and the numbers inside scared its own chief scientist enough to ask the entire industry to agree on a speed limit.

This article is not a list of safety slogans. It is about one number, **perplexity**, and why it might be the most honest metric in AI.

## 1. OpenAI published its own report card, and the numbers are the story

- On November 22, 2026, **OpenAI** chief scientist **Jakub Pachocki** published a post called **Perplexity and Intelligence** on the company's blog.
- For the first time, **OpenAI** shared the internal **log-perplexity** scores of its models, from **GPT-3.5** onward, on one held-out dataset drawn from its internal codebase.
- The numbers: **GPT-3.5** sat at about **0.99**, **GPT-4** at about **0.91**, and the newest models have fallen below **0.8**, with one model at about **0.76**.

**The so what: labs never show you the engine, only the paint job. OpenAI just showed the engine.**

*(Source: [OpenAI, Perplexity and Intelligence](https://openai.com/index/perplexity-and-intelligence/))*

## 2. Perplexity is the one metric that never lied

- **Perplexity** measures how well a model predicts the next token on average. Lower means better predictions, and **OpenAI** tracks its logarithm, also called **cross-entropy loss**.
- Benchmarks get gamed, saturated, and leaked. Pachocki argues this one number has stayed unusually useful for tracking the underlying intelligence created during pretraining, even as downstream benchmarks become obsolete.
- The drop from **0.99** to **0.76** is about **23 percent** lower in log terms, and the step after **GPT-4** was almost twice the step from **GPT-3.5** to **GPT-4**.

**The so what: forget the leaderboard. This is the odometer, and it is spinning faster.**

*(Source: [FourWeekMBA](https://fourweekmba.com/ai-openais-loss-fell-0-99-to-0-76-it-proposes-common-limits/))*

## 3. Below 0.8, capabilities appear out of nowhere

- **GPT-2** setting the perplexity record on older datasets was arguably the first model that could write coherent paragraphs. **GPT-3** could learn in context from a few examples.
- **GPT-3.5**, at about **0.99**, could hold fluent conversation and became the original **ChatGPT**. **GPT-4**, at about **0.91**, could use **chain-of-thought reasoning** productively.
- Once losses fell below **0.8**, **OpenAI** saw transformative capabilities emerge in **cybersecurity** and **mathematics**, and a model at about **0.76** started producing groundbreaking results on open problems in mathematics.

**The so what: nobody predicted these capabilities would appear at those exact thresholds. They just did, which is the whole problem.**

*(Source: [OpenAI, Perplexity and Intelligence](https://openai.com/index/perplexity-and-intelligence/))*

## 4. 0.68 to 0.70 is the next tripwire, and nobody knows what lives there

- Extrapolating from recent progress, Pachocki expects further transformative capabilities as models enter the **0.68 to 0.70 log-perplexity window**.
- He is explicit that the lab does not know what those capabilities will be. The last window gave us machines that crack open math problems and find security holes.
- The published chart shows a steep drop through 2026, with an unreleased internal model plotted lower still, so the window is not some distant future. It is the next stop on the curve.

**The so what: the next surprise is already scheduled. We just do not know what it is yet.**

*(Source: [Dealroom](http://dealroom.co/news/174824-openai-publishes-its-internal-pretraining-curve-and-proposes-industry-wi/))*

## 5. The 2027 avalanche, when AI starts teaching itself to train AI

- Pachocki's sharpest warning is not about the next model. It is about **AI contributing to fundamental advances in pretraining itself**, which could arrive as an avalanche as soon as **2027**.
- **OpenAI** attributes the 2026 acceleration mostly to long-term research and compute investment, and only in smaller part to AI automating its own development. That smaller part is the one growing fastest.
- He writes that progress on alignment and monitoring is unlikely to be fast enough to allow the full potential acceleration in pretraining. The safety work is running behind the capability work, and the gap is widening.

**The so what: the race is about to get a second engine, and nobody has brakes for that one.**

*(Source: [Reuters](https://www.reuters.com/business/openai-scientist-proposes-industry-ai-limits-tied-model-intelligence-metric-2026-11-22/))*

![Sam Altman, CEO of OpenAI, who publicly backed the proposal](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-23/sam-altman.jpg)
*Sam Altman backed the proposal publicly, tying it to the safety standards labs agreed under the White House Accords. Image credit: Tech Xplore*

## 6. The ask: a speed limit with a milestone attached

- Pachocki proposes **common limits**, based on perplexity and other measurements, that developers commit not to cross until the ability to understand and monitor AI behavior reaches a concrete milestone.
- The example milestone he names is a successor to **chain-of-thought monitors**, the main technique labs use today to inspect a reasoning model's intentions, which he expects to weaken as capability grows.
- He also wants frontier labs to jointly set shared norms for evaluating models, red-teaming safety cases, and transparency, plus an industry standard that fixes a first limit and defines what must be achieved before going beyond it.

**The so what: this is not a pause button. It is a speed limit with a clearly marked exit ramp.**

*(Source: [AI Weekly](https://aiweekly.co/alerts/openais-pachocki-urges-frontier-pause-at-068-07-perplexity))*

## 7. Altman signed it, and that is the real signal

- **Sam Altman** publicly backed the proposal the same day, writing that labs agreed under the **White House Accords** to establish standards and best practices for safety, and that a discussion about perplexity can further those goals.
- The chief scientist of the most powerful AI lab on earth just told his competitors exactly where his models stand, knowing it hands them a clearer picture of **OpenAI's** position. He said that concern is outweighed by the urgency of shared safety measures.
- Coverage of the proposal places it alongside **Anthropic** chief **Dario Amodei's** own pacing arguments, which suggests the governance conversation among frontier labs is converging, not fragmenting.

**The so what: when the fastest runner in the race asks for a speed limit, you listen, because he can see the next corner.**

*(Source: [FourWeekMBA](https://fourweekmba.com/ai-openais-loss-fell-0-99-to-0-76-it-proposes-common-limits/))*

## 8. The honest problems with the plan

- **Perplexity is hard to compare across labs.** Different labs train on different datasets and mixtures, so the same number does not mean the same thing everywhere, and there is no shared evaluation corpus yet.
- **It misses whole categories of progress.** Chain-of-thought reasoning improves task performance without lowering perplexity, so the metric understates what models can actually do.
- **There is no enforcement mechanism.** The proposal names no number for the first limit, no body to set it, and no penalty for crossing it. It relies on frontier developers jointly agreeing, in an industry that has never once agreed on anything voluntarily.
- **It has an unknown floor.** Nobody knows how low perplexity can go, which means nobody knows how many more surprises the curve holds.

**The so what: the plan is flawed in every way that matters, and it is still the most concrete safety proposal any frontier lab has ever published.**

*(Source: [TradingView, Seeking Alpha](https://www.tradingview.com/news/seekingalpha:dafd8465b094b:0-openai-calls-for-industry-wide-ai-brake-tied-to-perplexity/))*

![Rows of GPU servers in a data center, the hardware behind the training runs](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-23/gpu-servers.jpg)
*Every point on the perplexity curve is bought with compute, and the 2026 drop was mostly long-term research and compute investment. Image credit: GPU.fm*

## 9. What this means for everyone building with AI

- If you build on frontier models, your roadmap now depends on a number you cannot see, controlled by labs that are openly arguing about whether to slow down.
- If you work in security, the **0.8** threshold already changed your job: capabilities in **cybersecurity** emerged before anyone announced them, and the next window could do the same.
- If you are a student or a junior developer, the skills that matter are shifting toward the things perplexity cannot measure: judgment, evaluation, monitoring, and knowing when a model is confidently wrong.
- And if you are just watching the race, remember that the same month **California** sued **OpenAI** over escaped agents, **OpenAI's** own chief scientist asked for limits. The pressure is coming from inside the building now, not just outside it.

**The so what: the debate is no longer whether AI should slow down. It is who gets to draw the line, and at what number.**

*(Source: [Reuters](https://www.reuters.com/business/openai-scientist-proposes-industry-ai-limits-tied-model-intelligence-metric-2026-11-22/))*

## How to start

- **If you are a developer:** learn what **cross-entropy loss** actually measures, and start evaluating models on your own held-out data instead of trusting vendor benchmarks. The skill is not prompting. The skill is measurement.
- **If you are a student:** read the **Perplexity and Intelligence** post itself, it is short and unusually honest for a corporate blog. Then track one frontier model release and ask what its perplexity would have to be.
- **If you are a founder:** assume the next capability jump arrives unannounced, the way the math results did, and build your product so a sudden jump in model ability is a feature, not a fire drill.
- **If you are just curious:** watch the **0.68 to 0.70** window. When a lab announces a model and someone asks for its perplexity, that is the question that matters now.

## The real pattern

Every lab has been selling you benchmarks while keeping the real number in a drawer. OpenAI just published the drawer, and the number inside says the next leap is coming faster than the safety work that is supposed to catch it. The pattern is not that AI is getting smarter. The pattern is that the people building it are starting to admit they cannot see around the next corner, and they are asking their competitors to slow down with them before they find out what is there.

## Final thoughts

A speed limit only works if everyone agrees to drive at it. OpenAI just volunteered to be the first car to brake, and published the speedometer to prove it means it. Watch whether anyone else slows down. That answer tells you everything about where this race is really going.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

