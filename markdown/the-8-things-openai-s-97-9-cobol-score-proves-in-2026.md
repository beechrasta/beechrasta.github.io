# The 8 Things OpenAI's 97.9% COBOL Score Proves in 2026

OpenAI just taught its models to read **dead languages**, and the score is honestly rude: **97.9% accuracy** translating ancient COBOL programs into modern code without breaking them.

Let's stop pretending the AI coding revolution is about writing new apps faster. The biggest coding job on the planet is **understanding code that was written before you were born**, running on systems nobody dares to touch.

This article is not about vibe coding. It is about the **trillion-dollar museum** your money lives in, and the AI that just learned to be its tour guide.

![AI chat interface](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-20/oa-chat-interface.jpg)
*An AI chat interface. OpenAI's models just posted a 97.9% score on translating legacy COBOL into modern languages. Photo by Zulfugar Karimov on Unsplash.*

## 1. The number everyone will misread

OpenAI's newest coding model, **GPT-6.1 Sol**, scored **97.9% accuracy** on a test that translates old COBOL programs into **C++, Java, Kotlin, Python, or Rust** without changing what the program does.

That sounds like "problem solved." It is not. Here is what the number actually means:

- The test demands the translated program pass **every hidden test**, including checks comparing its observable outputs to the original program's outputs.
- It is **OpenAI's own test suite**, not a guarantee that real migrations will be error-free.
- It was achieved at **high reasoning effort**, the expensive, slow, think-hard mode. The cheap fast mode is a different story.

<u>A benchmark is a promise made in a lab. Production is where promises go to be audited.</u>

*(Source: [Interesting Engineering](https://interestingengineering.com/ai-robotics/openai-coding-models-software-modernization))*

## 2. The low-effort number is the real story

Everyone will quote 97.9%. The number that actually matters is **86.6%**.

- At **low reasoning effort** (fast, cheap mode), GPT-6.1 Sol hit 86.6% accuracy. The previous model, **GPT-5.6 Sol**, managed **5.4%**. *That is not an improvement. That is a different species.*
- OpenAI also reported a **39% reduction in API costs** at that setting.

Think about what 5.4% to 86.6% means in one generation. The old model was **useless** at this task. The new one is **deployable**. Somewhere between those two numbers, an entire profession's bottleneck moved. The jump from "toy" to "tool" happened in the boring middle of the settings panel, not at the headline number.

*(Source: [Interesting Engineering](https://interestingengineering.com/ai-robotics/openai-coding-models-software-modernization))*

![Old computer hardware](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-20/oa-old-computer.jpg)
*Banks still run on decades-old code. IBM estimates COBOL supports 40% of online banking systems and 95% of ATM transactions. Photo by Yuheng Ouyang on Unsplash.*

## 3. Your money runs on a museum

Why does anyone care about COBOL, a language from **1959**? Because your bank does.

- **IBM estimates** COBOL supports more than **40% of online banking systems**, **80% of in-person credit card transactions**, and **95% of ATM transactions**.
- **Fortran** still runs **weather forecasting and nuclear reactor safety analysis**.
- These languages have **far less training material** than Python or JavaScript, which is exactly why AI struggled with them until now.

Every time you tap your card, you are trusting arithmetic written when computers filled rooms and programmers wore ties. *The financial system is a heritage building with excellent plumbing and no fire exits.*

Banks cannot just rewrite this stuff. The business rules live **only in the original code**, the documentation is incomplete, and one wrong decimal can move real money to the wrong place.

*(Source: [Interesting Engineering](https://interestingengineering.com/ai-robotics/openai-coding-models-software-modernization))*

## 4. The rounding trap (or: how code runs clean and still steals money)

Here is the detail that should terrify every engineering manager. A rewritten program can **run without a single error** and still be wrong.

- **COBOL silently discards excess decimal digits** unless the program explicitly asks for rounding.
- Translate that logic into Python or Java naively, and the new program **rounds where the old one truncated**. Every calculation drifts. Pennies become dollars become lawsuits.
- The old code's quirks are not bugs. They are **undocumented business rules** that have been correct-by-accident for 40 years.

This is why "the AI rewrote our core banking system" is not a press release you want to read without a very long testing chapter attached. **Behavioral equivalence is the whole game**, and it is measured in hidden tests, not vibes.

*(Source: [Interesting Engineering](https://interestingengineering.com/ai-robotics/openai-coding-models-software-modernization))*

## 5. Twenty languages, one database engine

The COBOL score was not the only flex. OpenAI also ran **MultiLangBench**, where models must build a **database engine compatible with SQLite** across **20 programming languages**.

- **GPT-6 Astra** averaged **87.4%** test pass rate, up from **26.8%** for GPT-5.6 Sol. Every single language improved.
- **Fortran** jumped from 21.4% to **83.5%**. Visual Basic went from 27.5% to **89.4%**.
- **COBOL stayed the hardest language**, but even it climbed from 10.9% to **72.1%**.

Building a working database engine in Fortran is the kind of task that used to require a specialist who is probably retired and unreachable. *The bus factor of legacy systems just got a whole lot less scary, which is great news for everyone except the consultants charging by the hour.*

*(Source: [Interesting Engineering](https://interestingengineering.com/ai-robotics/openai-coding-models-software-modernization))*

![Laptop screen](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-10-20/oa-laptop.jpg)
*A developer's laptop. MultiLangBench tested building a SQLite-compatible database engine across 20 programming languages. Photo by Sunrise King on Unsplash.*

## 6. Luna, the cheap one

Buried in the announcement is the model that might matter most: **GPT-6 Luna**.

- Luna averaged **40.3%** pass rate, much lower than Astra's 87.4%.
- But it costs roughly **78% less per sample** than GPT-5.6 Sol. OpenAI pegged average API costs at **$0.77 versus $3.48**.

40% accuracy sounds bad until you realize what it is for: **running hundreds of experiments cheaply**, generating candidate migrations, and letting the expensive model or a human verify the winners. *Luna is the intern. Astra is the senior engineer. You need both, and the intern costs less than your coffee.*

The honest framing: cheap-but-mediocre models are how you afford to attempt migrations at all. Nobody greenlights a modernization project that costs more than the mainframe it replaces.

*(Source: [Interesting Engineering](https://interestingengineering.com/ai-robotics/openai-coding-models-software-modernization))*

## 7. The unglamorous goldmine

Nobody brags about modernizing a 30-year-old payroll system at parties. But look at the economics:

- The world's banks, insurers, and governments are **trapped on legacy code** they cannot rewrite by hand. There are not enough COBOL programmers left, and the ones who remain can name their price.
- AI that translates legacy code at 86%+ accuracy, **39% cheaper than before**, turns a decade-long rewrite into a project a normal team can attempt.
- This is the **least sexy, most lucrative** application of coding AI. No hackathon demos. Just trillions of dollars of infrastructure finally becoming maintainable.

*Everyone is building AI to write the next app. The money is in AI that reads the last one.*

## 8. Trust, but verify (the part OpenAI also says)

Credit where it is due: OpenAI is not claiming victory. Their own writeup says developers must still **verify rewritten applications against real workloads and undocumented dependencies**.

- The 97.9% is on a test suite, not your bank's actual codebase with its 40 years of patches.
- Astra's scores **varied considerably across languages**. COBOL is still the hardest.
- Production deployments need **careful validation** before migrated software touches anything critical.

That honesty is the whole ballgame. The teams that win with this will be the ones who treat the AI as a **brilliant translator with no common sense**, and build the testing harness to prove every translation. The model does the typing. **You do the trusting, carefully, with receipts.**

## How to start (developer edition)

**This week:**
- Pick **one legacy file or module** in your codebase that everyone is afraid to touch. Read it. That is step one.
- Try translating a small, well-tested piece with a coding model, then run the **existing test suite** against the translation. The tests are the truth.

**This month:**
- Build a **differential testing harness**: run the old and new code on the same inputs, compare outputs. This is the single highest-leverage practice in modernization work.
- Price the experiment: use a cheap model for bulk attempts, the strong model for the final pass. **The Luna/Astra split is a strategy, not just a product lineup.**

**This quarter:**
- Document the **undocumented behaviors** you find (the rounding, the truncation, the magic numbers). That document is worth more than the migration itself.

## The real pattern

The future of coding is not writing new code faster. It is understanding old code that nobody dares to touch. Every industry runs on software its builders have forgotten, and the bottleneck was never typing speed. It was comprehension. The model that reads the museum is worth more than the model that paints a new wing.

## Final thoughts

Your bank runs on code older than the internet. For decades, that was a risk nobody could afford to fix.

Now a machine can read the dead language at 97.9% accuracy, and the price of trying keeps falling. The museum is finally getting renovated. Just make sure someone checks the arithmetic before the doors reopen.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

