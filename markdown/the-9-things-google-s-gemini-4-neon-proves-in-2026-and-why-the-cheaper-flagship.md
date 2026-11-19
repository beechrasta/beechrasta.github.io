# The 9 Things Google's Gemini 4 Neon Proves in 2026, and Why the Cheaper Flagship Costs More Today

*Google launched a model that beats its own flagship on price, then priced it above the flagship. The catch is a calendar date.*

![Google headquarters](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-19/google-hq-hero.jpg)
*Google's headquarters in Mountain View. The fourth Gemini 4 model in four weeks just landed, and the pricing needs a calendar to understand. Photo: Alban on Unsplash*

Let's stop pretending model launches are about intelligence anymore.

**Google** just shipped **Gemini 4 Neon**, a model it says matches its flagship **Carbon** on coding, reasoning, and agentic work, at Flash speeds and a lower cost. The most interesting part is not the benchmark table.

This article is not a list of benchmark scores. It is about what happens when the frontier becomes a pricing tier, and the "cheaper" model costs more than the flagship until December 1.

## 1. The launch leaked the morning it happened

Google announced **Neon** on November 18, but the price was already public before the announcement. The $3 per million input tokens and $15 per million output tokens pricing surfaced in **Google Cloud's** billing catalog early that morning.

- The documentation page for the model returned a 404 in the morning and described **gemini-4-neon** in full by the evening
- A model card went live on **DeepMind's** site, and the model appeared in the **Vertex AI Model Garden** and **Google AI Studio** the same day
- The launch happened hours after the leak, not days, which means the billing catalog is now a faster press office than the press office

**The leak was the announcement's first draft, and Google shipped the model anyway.**

*(Source: [AI Frontier Post](https://aifrontierpost.com/articles/gemini-4-neon-google-release-live/))*

## 2. Four models in four weeks

**Neon** is the fourth **Gemini 4** model in about four weeks. **Argon** arrived in late September, **Carbon** in late October, **Hydrogen** on November 12, and **Neon** on November 18.

- **Hydrogen** is the everyday model, the Flash replacement for fast daily work
- **Argon** was the code and analysis model, the one Google called ideal for the majority of software engineering and knowledge work
- **Carbon** is the flagship for the hardest, long-horizon work that tests the limits of a model's intelligence
- **Neon** sits between **Hydrogen** and **Carbon**, built for complex work that also has to be fast

**Google is shipping model tiers the way phone companies ship data plans, and the lineup changes monthly.**

*(Source: [9to5Google](https://9to5google.com/2026/11/18/gemini-4-neon-announcement/))*

## 3. The headline number: 61, third in the world

Google's headline claim is that **Neon** scores 61 on the **Artificial Analysis Intelligence Index** at its highest thinking level, ranking third overall. The two models ahead of it are larger, slower ones: **GPT-6.2 Astra** and **Claude Fable 5.2**.

- The score is one point above **Carbon's** 60 at its high setting, so the middle child outscored the flagship on the composite index
- **Neon** also ranks second on the **Vals Index** at 70.9 percent, landing on the Pareto frontier, which means no evaluated model is both cheaper and more accurate on that index
- It debuts second globally on **Arena's** new **Agent Arena Index** with a score of 1336 across more than 4,200 real-world agent sessions

**A mid-tier model ranking third in the world is the whole point of Neon, and also the reason to read the fine print.**

*(Source: [Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/))*

## 4. The coding crown, and why agents are the real customer

The benchmark Google leads with is not general intelligence. It is coding, and specifically coding by agents. **Neon** ranks first overall on the **Artificial Analysis Coding Agent Index** with a score of 58.6.

- It scores 65.2 percent on **Terminal-Bench 4.1** and 46.2 percent at its default high setting on **FrontierCode 2.0**
- It ranks first on both the **Legal Research Bench** and the **Tax Agent Bench**, and first on **Zapier's AutomationBench** at 56.3 percent
- On **Andon Labs' Vending-Bench 2**, a long-horizon simulation of running a business, it scored $16,843, the top result

**Neon is built for agents that do the work, not chat about it, and the benchmarks Google picked all measure doing.**

*(Source: [9to5Google](https://9to5google.com/2026/11/18/gemini-4-neon-announcement/))*

## 5. The price paradox: cheaper than Carbon, except right now

Here is the detail Google's announcement does not shout about. **Neon** costs $3 per million input tokens and $15 per million output tokens. **Carbon** and **Argon** currently cost $2 and $10 under introductory pricing that runs until November 30.

- At today's prices, the "cheaper than Carbon" model costs 50 percent more than **Carbon** on input tokens
- After the promotion ends on December 1, **Carbon** and **Argon** rise to $4 and $20, and **Neon** becomes 25 percent cheaper than the flagships
- **Neon** is exactly twice the price of **Hydrogen**, which costs $1.50 and $7.50, though cached input on **Neon** is discounted 95 percent to $0.15 per million tokens

**The cheaper flagship is a December product wearing a November price tag, so check the calendar before you check the invoice.**

*(Source: [Android Headlines](https://www.androidheadlines.com/2026/11/google-gemini-4-neon-release-pricing-features.html))*

## 6. The picker is now the product

The quietest change in the launch is the one most users will actually feel. **Neon** replaces **Argon**, the older **3.1 Pro** model is retired, and **3.5 Flash-Lite** becomes **Auto** in the model picker for paid users.

- The refreshed picker now offers four choices: **Auto**, which adapts to the task
- **Everyday help**, powered by **4 Hydrogen**; **Deeper analysis**, powered by **4 Neon**; **Code and complex work**, powered by **4 Carbon**
- **Neon** is also rolling out in the **Gemini API** in **Google AI Studio**, in **Gemini for business**, and in **Google Antigravity** for paid **AI Pro** and **AI Ultra** subscribers

**Google is quietly taking the model choice away from you, one picker redesign at a time.**

*(Source: [9to5Google](https://9to5google.com/2026/11/18/gemini-4-neon-announcement/))*

![Developer coding at night](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-19/developer-coding-night.jpg)
*A developer working late with code on two monitors. Neon is aimed squarely at this person, and at the agents doing this work on their behalf. Photo: Mohammad Rahmani on Unsplash*

## 7. You are now paying for how hard the model thinks

**Neon** has the same 1 million-token context window as **Hydrogen**, with four thinking levels: **Low**, **Medium**, **High**, and **Extra High**. The default is **High**, and the thinking level is the dial that trades intelligence against cost.

- Google says **Neon** costs 32 percent less per task than **Carbon** at its default high setting
- Google also says **Neon** recorded its lowest fabrication rate yet in internal **Google Antigravity** testing, which is a polite way of saying it hallucinates less than its siblings
- On **Terminal-Bench Science** it scores 70.5 percent, on **RiemannBench** 84 percent, and on **HLE-Diamond** 71.3 percent, all best-in-class figures from Google's own tables

**The product is no longer just the model. It is a slider, and every notch has a price.**

*(Source: [Google Antigravity](https://antigravity.google/blog/gemini-4-neon-in-google-antigravity/))*

## 8. What it can and cannot do

**Neon** is a workhorse, not a media model, and the capability list makes that obvious. It supports **Computer Use**, live code execution, grounding through **Google Search** and **Maps**, function calling, and structured outputs.

- It can direct **Hydrogen** subagents on big coding jobs, which is Google's way of saying the mid-tier model can boss around the fast model
- It takes text, image, video, audio, and PDF inputs, with outputs up to 1 million tokens when long decode is enabled
- It does not generate images or audio, and it does not support the **Live API**, so this is a model for agents and long tasks, not for talking to your phone

<u>The spec sheet tells you who the customer is: developers running agents, not people chatting with a bot.</u>

*(Source: [AI Frontier Post](https://aifrontierpost.com/articles/gemini-4-neon-google-release-live/))*

## 9. The honest caveats, because the benchmarks are Google's own

Every number in this article so far comes from Google's announcement, its model card, or its selected benchmark tables. That is the honest caveat, and it matters more than any single score.

- Google has published no independent benchmarks for **Neon** yet, and the model card describes capabilities, not scores
- At launch, **OpenRouter's** comparison pages still listed **Neon's** Intelligence Index score as unavailable, so third-party tracking had not caught up
- The "close to Carbon" claim rests on Google's own framing, and Google's own comparison table has **Neon** leading 16 of 19 reported results against the mid-tier **Claude Opus 5.5** and **GPT-6.2 Sol** models, which is a table Google itself chose

**Trust the price, because the price is a fact. Verify the benchmarks, because the benchmarks are a pitch.**

*(Source: [AlphaSignal](https://alphasignal.ai/news/google-deepmind-s-gemini-4-neon-targets-complex-agent-workflows-at-61))*

![Google logo letters](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-19/google-logo-letters.jpg)
*The Google logo in colorful 3D letters. The brand is the same, the model lineup changes every few weeks. Photo: BoliviaInteligente on Unsplash, 3D render*

## How to start

Pick your lane, and check the date before you commit to a price.

- **Developers:** try **Neon** through the **Gemini API** in **AI Studio**. Cached input at $0.15 per million tokens makes long-context work cheap, but compare against **Carbon's** $2 promotional rate before December 1, because the flagship is the bargain until then.
- **AI Pro subscribers:** pick **Deeper analysis** in the Gemini app for research, multi-step tasks, and anything where **Hydrogen** feels too shallow and **Carbon** feels too slow.
- **Everyone else:** wait for December 1. That is the day the pricing story Google is telling actually becomes true, and the day the comparisons stop needing an asterisk.

You don't need all four models. Pick one, and let **Auto** pick for you when you are not sure.

## The real pattern

Google is not selling a smarter model. It is selling the middle of the price curve, and the launch calendar has become a pricing strategy. Every few weeks a new tier appears, the old tier gets a new price, and the picker quietly relearns what "good enough" means. The intelligence race is still running, but the race that decides your bill is the one between the tiers.

## Final thoughts

Four models in four weeks is not a roadmap, it is a subscription strategy with a changelog. The model that wins your work will not be the smartest one. It will be the one that is fast enough, cheap enough, and already sitting in the picker when you open the app. **Neon** is Google's bet that the middle is where most of the work lives. Use it, but read the price like a calendar, not a promise.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

