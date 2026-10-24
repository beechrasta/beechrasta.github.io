# The 9 Things Canva's Craft Proves in 2026, and Nobody Expected a Design App to Win

*Forget prettier pixels. The real war in AI images is about who controls the layout, and Canva just made its move.*

![Canva homepage under a magnifying glass](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-23/canva-site-homepage.jpg)
*Canva's homepage, up close. The design giant just stopped renting other labs' models and built its own. Photo: Jernej Furman, CC BY 2.0, via Wikimedia Commons*

Let's stop pretending the AI image race is about who makes the prettiest picture.

Here is the uncomfortable truth: **most AI-generated images are useless the moment you need to change the headline.** They look great and edit terribly.

This article is not a list of Craft's features. It is about why a design app building its own image model changes who wins.

## 1. Canva stopped renting and started owning

- On **October 22, 2026**, Canva launched **Craft**, the first image generation model it built and trained from scratch
- It comes from **Canva Research**, the company's in-house AI lab, and it is live for every Canva user inside **Dream Lab**, plus a public API for developers
- Until now, Canva leaned on other companies' models. Dream Lab launched in October 2024 running on **Phoenix**, the model from **Leonardo.ai**, the Sydney startup Canva acquired that year. Researchers from Leonardo worked on Craft too

So what: **the landlord just became a homeowner.** When you serve hundreds of millions of users, renting someone else's model is a tax you eventually refuse to pay.

*(Source: [The Verge](https://www.theverge.com/ai-artificial-intelligence/1017151/canva-craft-in-house-ai-model); [madrobot.blog](https://madrobot.blog/2026/10/22/canva-craft-ai-image-model-dream-lab-canva-research/))*

## 2. It plans the picture before it paints it

- Most image models turn a prompt straight into pixels. Craft splits the job in two
- First, a **planning model** reads your prompt and writes a detailed plan: which elements appear, where they sit, their relative sizes, what matters most, and any text that must appear
- Then a separate **rendering model** turns that plan into a finished image at up to **2K resolution**, in more than **30 aspect ratios** or a custom size

So what: **an architect who sketches before building beats a painter who improvises.** Planning first is why Craft can place objects where you asked instead of where it felt like.

*(Source: [Digital Trends](https://www.digitaltrends.com/computing/canva-craft-ai-image-generation-model-launch/); [XenoSpectrum](https://xenospectrum.com/en/canva-craft-image-planning-editable-layers/))*

## 3. Text is the whole game, and photos were the wrong teacher

- Ask any image model for a poster with a headline and watch it spell like a tired toddler. **Legible text** is the hardest problem in image generation
- Craft was trained on **millions of human-made Canva templates**, posters, social posts, presentations, infographics, menus, diagrams, instead of mainly photographs
- It can write text into images in **55 languages**, and you can prompt it in any language

<u>Photos teach a model what things look like. Templates teach it how information is arranged. That is the entire difference.</u>

Honest caveat, straight from Canva: **small text and technical drawings** are still areas to improve. They said it themselves, which is more than most labs do.

*(Source: [XenoSpectrum](https://xenospectrum.com/en/canva-craft-image-planning-editable-layers/); [Digital Trends](https://www.digitaltrends.com/computing/canva-craft-ai-image-generation-model-launch/))*

## 4. Designers trained it, not just data centers

- After pretraining, Canva applied supervised fine-tuning and reinforcement learning with feedback from **professional designers**
- In internal evaluation, designers and researchers compared more than **25,000 pairs of images** head to head
- Where automated metrics and human judgment disagreed, **Canva gave priority to the designers' judgment**

So what: **benchmarks measure what is easy to measure.** Canva let working designers overrule the scoreboard, which is exactly the kind of heresy the industry needs.

*(Source: [XenoSpectrum](https://xenospectrum.com/en/canva-craft-image-planning-editable-layers/))*

![The Canva logo](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-23/canva-logo.jpg)
*The Canva logo. Craft is the first image model Canva Research built from scratch instead of licensing. Photo: KaiLEK54, CC0, via Wikimedia Commons*

## 5. The image is not the product. The layers are.

- Craft generates the image, then **Magic Layers**, an existing Canva feature, breaks it into editable pieces: text, objects, background
- Canva Research trained a **learned decomposition model** that understands the elements and layers inside a composition, and pairs it with a font library so text returns to editable form instead of staying a cluster of pixels
- Change one element and the surrounding areas do not need to be redrawn, which is the thing every marketer has screamed at their screen about

So what: **a flat image is a dead end. A layered design is a starting point.** Canva is selling the edit, not the render.

*(Source: [XenoSpectrum](https://xenospectrum.com/en/canva-craft-image-planning-editable-layers/); [AI Daily Post](https://aidailypost.com/news/canvas-craft-first-ai-image-model))*

## 6. It is built for the revision loop, not the wow loop

- Real production work is generate, revise, repeat. Every round costs **waiting time and compute**, and at Canva's scale, more than **one billion designs a month**, a few cents per generation adds up fast
- Canva used **model distillation** to cut the inference steps needed, and built its own engine for the planning stage
- Faster versions, **Craft-fast and Craft-ultrafast**, are already on the roadmap

<u>Owning the model means owning the cost curve.</u> That is the sentence that should worry every API reseller in the design space.

Fair note: Canva gave **no specific generation times and no user-facing pricing** for Craft yet. Speed and cost claims are roadmap, not receipts.

*(Source: [XenoSpectrum](https://xenospectrum.com/en/canva-craft-image-planning-editable-layers/))*

## 7. The leaderboard claim, decoded honestly

- Canva says it is now the world's **second-best AI lab for images** on DesignArena's public leaderboard, behind only OpenAI
- As a single model, Craft sits **fourth**, behind three OpenAI models: GPT-Image-2.5 Sunburst, GPT-Image-2.5 Flare, and GPT-Image-2
- Both can be true at once: lab ranking counts the stable, model ranking counts the horse

So what: **read leaderboard claims the way you read a resume.** The fine print is where the truth lives, and to Canva's credit, the numbers are public enough to check.

*(Source: [madrobot.blog](https://madrobot.blog/2026/10/22/canva-craft-ai-image-model-dream-lab-canva-research/); [Tech News Vision](https://technewsvision.co.uk/canvas-first-ai-image-model-plans-designs-before-generating-them/))*

## 8. The API and the MCP play are the real story for builders

- Craft is available through **Canva's public API** for developers right now
- Canva plans to let **AI agents plug into Craft through the open Model Context Protocol**, so assistants can generate on-brand images inside workflows
- It also ships with input and output moderation, privacy and safety controls, and reporting tools

My angle, personally: **my daily poster pipeline runs on image models, and Petra renders them through my PosterBuilder API.** A design-first model with an API and future MCP support is exactly the kind of brick I want in that wall. I will be testing Craft against my current stack this week.

So what: **models win benchmarks, platforms win workflows.** Canva is playing the second game.

*(Source: [Tech News Vision](https://technewsvision.co.uk/canvas-first-ai-image-model-plans-designs-before-generating-them/); [madrobot.blog](https://madrobot.blog/2026/10/22/canva-craft-ai-image-model-dream-lab-canva-research/))*

![Wood letterpress type](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-23/letterpress-type.jpg)
*Wood letterpress type. Craft's whole bet is that text and layout are the hard part of image generation, not pixels. Photo: Michellecornelison, CC BY-SA 4.0, via Wikimedia Commons*

## 9. What to do on Monday

- **Creators and marketers:** open Dream Lab from the three-dot menu in Canva and try a text-heavy poster. Compare the headline spelling against whatever you used last week. That single test tells you everything
- **Developers:** look at the public API docs and ask whether your image pipeline needs pixels or needs editable designs. If it is the second, this is your model
- **Everyone:** check the plan limits before you fall in love. Available to all users does not mean free and unlimited, and Canva has not published Craft pricing yet

So what: **try the thing that annoys you most about current tools.** If Craft fixes your headline problem, it earned its place. If not, you lost ten minutes.

*(Source: [Tech News Vision](https://technewsvision.co.uk/canvas-first-ai-image-model-plans-designs-before-generating-them/); [XenoSpectrum](https://xenospectrum.com/en/canva-craft-image-planning-editable-layers/))*

## The real pattern

Every AI image lab spent two years racing to make prettier pictures, and Canva noticed that nobody's actual job is "make a pretty picture." The job is "make the poster, then change the date, then change the headline, then ship it." Craft is the first frontier image model designed around the revision, not the render. The labs optimizing for wow are about to learn what every designer already knows: the money was never in the first draft.

## Final thoughts

Canva did not need to build a model. It chose to, because renting intelligence at its scale is just paying someone else to own your future.

The design app grew teeth. Watch what it bites next.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

