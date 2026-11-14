# The 9 Things Humanoid Robots on a Real Car Line Prove in 2026, and Why 96 Percent Is Not the Point

*Google's robots sorted car parts on a live Mercedes line at 96 percent. The number is real. The denominator is missing.*

![Humanoid robots on a factory floor, with the humans still watching](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-14/humanoid-robots-factory.jpg)

*Humanoid robots on a factory floor, with the humans still watching. Photo: Mongoose HQ*

Let's stop pretending humanoid robots are a demo video. This week one worked a real shift, on a real car line, while the line kept running.

**Google DeepMind** says **Apptronik's Apollo 2** sorted car parts at **Mercedes-Benz** plants with a 96 percent success rate. The number sounds like a verdict. It is not. It is a progress report with the fine print missing.

This article is not a victory lap for robots. It is about what actually happened on that line, what the number hides, and who this hits first.

## 1. A robot did kitting on a live line, and the line did not stop

- On active production lines in Kecskemét, Hungary, and Sindelfingen, Germany, **Apollo 2** humanoids autonomously performed automotive kitting.
- The job: reach into supply bins, pick up individual metal brackets, and place them into sequencing containers in the exact order each vehicle on the line needs.
- This was a real-world proof-of-concept, announced November 10 with **Gemini Robotics 2.5**, **DeepMind's** most capable vision-language-action model to date. Not a lab, not a staged video, a working factory.

**That is the news. Everything else in this article is about how much it does and does not mean.**

*(Source: [Google DeepMind, Gemini Robotics 2.5](https://deepmind.google/blog/gemini-robotics-2-5-accelerates-real-world-physical-intelligence/))*

## 2. Kitting is the most boring job in the factory, which is exactly the point

- Kitting is repetitive, physically taxing prep work: sorting parts into trays so the assembly line never waits.
- **DeepMind** is explicit about why it picked this task. Offloading the monotonous work keeps the line moving and frees technicians to focus on complex build tasks.
- Robots are not starting with the skilled work. They are starting with the work humans are tired of doing, which is also the work nobody defends at a union meeting.

**Watch which jobs go first. It is never the interesting ones.**

*(Source: [Google DeepMind, Gemini Robotics 2.5](https://deepmind.google/blog/gemini-robotics-2-5-accelerates-real-world-physical-intelligence/))*

## 3. 96 percent is a real number with a missing denominator

- **DeepMind** reports a 96 percent success rate, but the announcement does not say how many picks that covers, what counts as a success, or how often a human stepped in.
- 24 successes in 25 attempts and 960 in 1,000 both round to 96 percent, and they mean very different things on a production line.
- No **Mercedes** statement confirms the figure independently, and the pilot is a proof-of-concept, not a deployment. There is no confirmed timetable or quantity for a factory-wide rollout.

**A percentage without a denominator is a vibe, not a measurement. Treat it like one.**

*(Source: [TechTimes](https://www.techtimes.com/articles/330432/20261111/gemini-robotics-25-reports-96-success-sorting-mercedes-car-parts-publishes-no-trial-count.htm))*

## 4. The hand is the story, not the brain

- **Apollo 2** carries the **SharpaWave** hand: five fingers, 22 degrees of freedom, built to handle delicate, flexible objects with finesse.
- **Gemini Robotics 2.5** was evaluated across more than 200 distinct tasks, including serving food with tongs, tying a bow on a gift box, and pipetting a liquid. Those are dexterity tests, not compute tests.
- Compared with previous baselines, **DeepMind** reports 30 to 100 percent higher success depending on the task type, and tasks completed 20 to 30 percent faster.

**Everyone talks about robot brains. The bottleneck was always fingers.**

*(Source: [Google DeepMind, Gemini Robotics 2.5](https://deepmind.google/blog/gemini-robotics-2-5-accelerates-real-world-physical-intelligence/))*

![Orange robot arms working on car bodies on an assembly line](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-14/kuka-car-factory.jpg)

*Orange robot arms working on car bodies on an assembly line. Photo: ITC*

## 5. Two models run the robot, one thinks and one moves

- **Gemini Robotics ER**, the embodied reasoning model, keeps track of the workflow: which car is next, which parts it needs, what goes where.
- **Gemini Robotics 2.5**, the actions model, controls the hands and arms, reaching into bins and correcting for gaps while placing brackets.
- The split matters. Reasoning about a multi-step job and moving a hand through a cluttered bin are different problems, and **DeepMind** solved them with different models working together.

**The robot does not have one brain. It has a planner and a pair of hands that take orders from it, which is suspiciously like how a factory already works.**

*(Source: [Google DeepMind, Gemini Robotics 2.5](https://deepmind.google/blog/gemini-robotics-2-5-accelerates-real-world-physical-intelligence/))*

## 6. Sindelfingen tried this in 2016 and gave up

- The Sindelfingen plant is a pointed place to claim a humanoid milestone. In 2016, **Mercedes** said robots could not cope with the individualization and number of variants in its vehicles, and moved some work back to human workers.
- The plant produces about 400,000 cars a year. Variant complexity is the whole game there.
- Ten years later, the same plant is the test site, and the robot that is supposed to handle the variants is shaped like the humans who replaced the last robots.

**History does not repeat, but it does run the same experiment twice and wait to see if the hardware caught up.**

*(Source: [TechTimes](https://www.techtimes.com/articles/330432/20261111/gemini-robotics-25-reports-96-success-sorting-mercedes-car-parts-publishes-no-trial-count.htm))*

## 7. The safety numbers are the ones I actually believe

- **Gemini Robotics 2.5** uses inference-time reasoning guidance to steer around physical hazards in real time, like a safety classifier for movement instead of words.
- In **DeepMind's** evaluations, that lifted safe task completion around obstacles by 33 percent and around nearby people by 43 percent.
- The lab also released **ASIMOV-Jailbreak**, an open benchmark of adversarial prompts that try to trick robots into unsafe actions. **Gemini 4 Argon** scores 99.5 percent jailbreak resistance on it, against 82 percent for the previous baseline.

**A robot that can be jailbroken into dropping a car part on someone is a liability, not a product. The safety work is the product.**

*(Source: [Google DeepMind, Gemini Robotics 2.5](https://deepmind.google/blog/gemini-robotics-2-5-accelerates-real-world-physical-intelligence/))*

## 8. You cannot buy this, and that is deliberate

- **Gemini Robotics 2.5** is rolling out to **DeepMind's** robotics partners only. There is no public API, no price, and no general availability date.
- More than 100 trusted testers, from industrial automation firms to robotics startups, are working with the models.
- The training itself was accelerated by **Gemini 4 Argon**, which acts as a simulation engine, generating thousands of varied practice runs from a real camera scene and building digital twins. **Apptronik's** CEO **Jeff Cardenas** said the models improved dramatically within a few weeks of post-training and carried over to the **Mercedes** lines with very little drop-off.

**The robot is not a product yet. It is a partner program with a press release attached.**

*(Source: [Humanoids Daily](https://www.humanoidsdaily.com/news/gemini-robotics-2-5-apollo-2-mercedes-benz-argon))*

![A humanoid service robot, the same wave in a different uniform](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-14/pepper-humanoid-robot.jpg)

*A humanoid service robot, the same wave in a different uniform. Photo: Unsplash*

## 9. Mercedes is not a neutral test site

- **Mercedes** signed a commercial agreement with **Apptronik** in March 2024, announced an investment in March 2025, and joined **Google** and **B Capital** as a repeat investor in **Apptronik's** 520 million dollar Series A-X extension in February 2026.
- The customer, the investor, and the test site are the same company. That does not make the 96 percent false, but it does make it interested.
- When the company grading the exam also funded the student and owns the classroom, read the score with both eyes open.

**None of this makes the pilot fake. It makes it a pilot, run by believers, on a friendly line, and the honest version of the story says exactly that.**

*(Source: [TechTimes](https://www.techtimes.com/articles/330432/20261111/gemini-robotics-25-reports-96-success-sorting-mercedes-car-parts-publishes-no-trial-count.htm))*

## How to start

- **If you build robots:** read the **DeepMind** post and the **Gemini Robotics** evaluations, and join the waitlist for early access. The interesting work right now is in VLA models, dexterous manipulation, and safety evals like **ASIMOV-Jailbreak**, not in building another arm.
- **If you work in a factory:** audit your kitting and prep work, the repetitive sorting and staging nobody likes doing. That is where the first humanoids will show up, not on the skilled line.
- **If you are just watching:** follow the denominator, not the headline. The next pilot that publishes its trial count, its failure taxonomy, and its human intervention rate will be the first one worth fully believing.

## The real pattern

Robots are leaving the lab the same way AI left the lab: not with a single breakthrough, but with a demo that works just well enough, in just friendly enough conditions, that the money starts moving before the measurement catches up. The 96 percent is not a lie and it is not a proof. It is a signal that the factory floor is now a software problem, and software problems get solved in public, messily, one pilot at a time.

## Final thoughts

A robot sorted car parts on a live line and the line kept running. That sentence would have sounded like science fiction five years ago, and like a press release two years ago. Today it is a progress report with missing footnotes, which is the most honest kind of progress there is. Keep watching the footnotes. They are where the future actually lives.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

