# The 8 Things Kimi K3.1 Pro's 3 Trillion Parameters Prove in 2026, and the Open Weights Are Still a Promise

*A Beijing lab just dropped a 2.8-trillion-parameter monster that out-codes almost everything. The weights land November 4. Probably.*

![Kimi chatbot example screenshot](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-24/kimi-chatbot-hero.jpg)
*Kimi in conversation. Moonshot AI's K3.1 Pro claims 2.8 trillion parameters, with only 104 billion firing per token. Screenshot: VulcanSphere, public domain, via Wikimedia Commons (software by Moonshot AI)*

Let's stop pretending the AI race is a two-horse sprint between San Francisco labs.

**On October 23, 2026, Moonshot AI unveiled Kimi K3.1 Pro**, the first model in the K3.1 series, and the numbers are the kind that make benchmark leaderboards look lopsided.

This article is not a spec sheet. It is about what a 3-trillion-parameter open-weight promise does to the balance of power, and why the most interesting number in the launch is not a benchmark at all.

## 1. This is not a new model, it is a new training philosophy

- K3.1 Pro is a **post-trained version of Kimi K3** (the July 2026 model whose weights shipped July 27), not a fresh base model
- Moonshot pushed it through **much larger post-training compute**: joint reinforcement learning across "hundreds of downstream domains," plus an optimized RL framework, long-context inference, and new sandbox infrastructure
- One open-models watcher, **Nathan Lambert** of the Interconnects newsletter, put it plainly on X: "it looks like they figured out their RL, where the initial release was a very impressive base model with lighter post-training"

So what: **the base model was the rough draft; the RL was the product.** The frontier is moving from pretraining scale to post-training grind.

*(Sources: [MarkTechPost](https://www.marktechpost.com/2026/10/23/moonshot-ai-kimi-k3-1-pro-open-weight-model/), [WebProNews](https://www.webpronews.com/moonshot-kimi-k3-1-pro-open-weights-cyber-data/))*

## 2. Decoding the 3T: only 104 billion brains fire at once

- **2.8 trillion total parameters**, but just **104 billion active per token**, in a sparse mixture-of-experts design: **896 experts**, only 16 awake per token, routed by a "Stable LatentMoE" framework
- Custom **Kimi Delta Attention** (a Gated DeltaNet linear-attention implementation) plus "Attention Residuals" carried over from K3
- **1-million-token context window**, multimodal across text and images, with video input referenced in the API docs

So what: **the headline number is marketing; the active number is engineering.** 104B active per token is the part your GPU bill actually feels.

*(Sources: [SiliconANGLE](https://siliconangle.com/2026/10/23/moonshot-ai-launches-new-flagship-kim-k3-1-pro-model-with-3t-parameters/), [Kimi launch post](https://www.linkedin.com/posts/kimi-ai-linkedin_introducing-kimi-k31-pro-our-most-capable-activity-7519448212529934336-UB0h))*

## 3. It is trading punches with Claude Opus 5.5

- Moonshot's own numbers (company-reported, mostly unaudited): **Terminal-Bench 4.0 at 65.7%**, against Claude Opus 5.5's 66.4% and GPT-6 Astra's 58.2%; **OfficeQA Pro v2 at 64.4**, claimed as the top score anywhere; **BenchCAD 92.7%** with tools
- Claim-level hallucination rate fell from **23.4% on K3 to 8.3%** on K3.1 Pro, per Moonshot's internal measures
- The independent check matters more: **Artificial Analysis** scores it **55 on its Intelligence Index, 4th overall**, behind only Claude Opus 5.5 (58), Claude Sonnet 5.5 (56), and Muse Wonder Full (56). That is **up 11 points** from K3's 44
- Where it shines is agentic work: **Terminal-Bench 4.0 at 67%** (the highest of any model, independently measured), GDPval-AA at 1,846 Elo (3rd, up 312), AutomationBench at 73% (up from 58%)

So what: **a lab from Beijing is now within 3 points of the best proprietary model on earth.** The gap between open and closed weights just shrank from 12 points to 3.

*(Sources: [Artificial Analysis](https://artificialanalysis.ai/articles/kimi-k3-1-pro-launch-benchmarks), [SiliconANGLE](https://siliconangle.com/2026/10/23/moonshot-ai-launches-new-flagship-kim-k3-1-pro-model-with-3t-parameters/))*

![Kimi interface screenshot](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-24/kimi-screenshot-body.jpg)
*The Kimi interface. K3.1 Pro is live on Kimi.ai, Kimi Work, Kimi Code, and the API. Screenshot: Rodrigo Padula, CC BY 4.0, via Wikimedia Commons*

## 4. The pricing is a knife fight

- API pricing: **$2 per million input tokens, $10 per million output, $0.20 cached input**, a full **33% cheaper than K3** across all three rates
- A **K3.1 Pro Highspeed** variant runs 2 to 3 times faster at **$4/$20** per million in/out, same cached price, with no separate benchmarks published for it

So what: **frontier-adjacent coding at a third off.** If you are an indie dev or a startup in India watching every token, this is the price war working for you.

*(Sources: [Artificial Analysis](https://artificialanalysis.ai/articles/kimi-k3-1-pro-launch-benchmarks), [pasqualepillitteri.it](https://pasqualepillitteri.it/en/news/26667/kimi-k3-1-pro-launches-open-weights-nov-4))*

## 5. The open weights are a promise, not a fact

- The weights are **not published yet**. Moonshot promises full weights by **November 4, 2026**, and the license has not even been specified
- Lambert's verdict, with the caveat doing heavy lifting: the scores "look to be clearly the strongest current open weight model, **if the weights are released as they claim by November 4th**"

<u>Never celebrate an open model before the weights land. Announcements are cheap; torrents are truth.</u>

*(Sources: [SiliconANGLE](https://siliconangle.com/2026/10/23/moonshot-ai-launches-new-flagship-kim-k3-1-pro-model-with-3t-parameters/), [WebProNews](https://www.webpronews.com/moonshot-kimi-k3-1-pro-open-weights-cyber-data/))*

## 6. They deliberately dulled its hacking skills

- Ahead of the open-weight release, Moonshot **stripped cybersecurity-related data** from the post-training set, on purpose, for safety
- Their own honesty about the cost: on an in-house exploit benchmark, the filtered model solves **81.0%** of tasks versus **90.5%** for an unfiltered build. A 9.5-point self-inflicted wound
- Future models will get "more advanced vulnerability analysis features," which reads like: we will figure out the safety story later

So what: **this is the new normal for open weights.** The model you download is the model minus its teeth, and the lab is telling you exactly how many teeth it pulled.

*(Sources: [WebProNews](https://www.webpronews.com/moonshot-kimi-k3-1-pro-open-weights-cyber-data/), [SiliconANGLE](https://siliconangle.com/2026/10/23/moonshot-ai-launches-new-flagship-kim-k3-1-pro-model-with-3t-parameters/))*

## 7. The lab is named after a Pink Floyd album

- **Moonshot AI** is Beijing-based (Haidian district HQ), founded in **March 2023** by Tsinghua schoolmates **Yang Zhilin** (CEO, ex-Google Brain and Meta, co-author of Transformer-XL and XLNet), Zhou Xinyu, and Wu Yuxin
- The name comes from Pink Floyd's **Dark Side of the Moon**
- The **Kimi chatbot** launched in October 2023 and made its name on absurd long context (2 million tokens) before the open-weight pivot with the K2, K2.5, and K3 series

So what: **the founder co-wrote two of the papers your transformer runs on.** This is not a hype lab; it is a research lab that learned to ship.

*(Source: [Wikipedia](https://en.wikipedia.org/wiki/Moonshot_AI))*

![Zhongguancun, Beijing tech hub](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-24/zhongguancun.jpg)
*Zhongguancun, Beijing's tech corridor. Moonshot AI builds from Haidian district, a short walk from Tsinghua, where its founders studied. Photo: N509FZ, CC BY-SA 4.0, via Wikimedia Commons*

## 8. Why developers should care this weekend

- If the weights land November 4, this becomes the **highest-scoring open-weights model in existence**, and the open-versus-proprietary gap collapses to 3 points
- Moonshot is positioning it for **full-project coding** (games in Unreal, Unity, and Godot), parametric 3D modeling in **Blender and CAD**, and finance work with hallucination "down 65%" (their claim, treat as marketing until verified)
- The agentic scores are the real story: Terminal-Bench and AutomationBench measure **work**, not trivia. This thing does jobs

So what: **your next coding agent's brain might be downloadable.** Start planning your eval harness now, not after the torrent drops.

*(Sources: [Artificial Analysis](https://artificialanalysis.ai/articles/kimi-k3-1-pro-launch-benchmarks), [OfficeChai](https://officechai.com/ai/moonshot-ai-releases-kimi-k3-1-pro-beats-opus-5-5-gpt-astra-6-on-some-benchmarks/))*

## How to start

- **If you build with LLMs:** try K3.1 Pro on the API this weekend at the $2/$10 rates. Benchmark it against whatever you use now on your own tasks, not theirs.
- **If you run open models:** mark November 4 on your calendar, and watch for the license terms. A great model with a hostile license is a demo, not a tool.
- **If you just follow the race:** stop counting parameters. Start counting active parameters per token, post-training compute, and agentic benchmarks. That is where the frontier moved.

## The real pattern

The moat was never the parameter count. It was who could afford the post-training. Moonshot just proved a focused RL grind can take a July base model within 3 points of the best closed lab on earth, and once those weights drop, that grind becomes everyone's starting line.

## Final thoughts

Three trillion parameters, and the bravest number in the launch is 9.5.

That is how many points of hacking skill Moonshot cut out of its own model, on purpose, in public.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

