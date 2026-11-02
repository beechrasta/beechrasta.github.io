# The 8 Things Google and NASA Building a Robot Doctor Proves in 2026, and Why Mars Needs Hands, Not Just Chat

A chatbot cannot fetch an ultrasound machine. On a trip to Mars, that simple fact could kill someone, and **Google** and **NASA** just tested a robot that can.

![Robonaut 2 aboard the International Space Station](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-02/robonaut-iss.jpg)
*Robonaut 2, a humanoid robot tested aboard the International Space Station. Credit: NASA via Science Friday.*

Let's stop pretending deep space medicine is a video call with a doctor.

On a future Mars mission, a radio signal takes up to **44 minutes** for a round trip. There is no real time advice, no second opinion on demand, and no ambulance. **Google Public Sector** and **NASA** are building a robot to fill that gap, and its first job is gloriously unglamorous: carry the bag, fetch the machine, hold still.

This article is not about a robot surgeon. It is about why the most useful space robot of the next decade might be an extra pair of hands for an overworked human doctor.

## 1. The 44 minute problem changes everything about medical help

- **Google** public sector vice president **Jim Kelly** wrote in an October 27 blog post that a Mars astronaut could face round trip communication latencies of up to 44 minutes.
- That delay makes real time medical guidance from mission control nearly impossible, according to **Google** and **NASA** reporting of the project.
- The partners are **NASA's Human Research Program**, the **Johnson Space Center** robotics team, and the **Jet Propulsion Laboratory**, working with **Google Public Sector**.

**When help is 44 minutes away, autonomy is not a luxury.** It is the treatment plan.

*(Source: [Nextgov, NASA, Google test AI-powered medical robot for deep space missions](https://www.nextgov.com/emerging-tech/2026/10/nasa-google-test-ai-powered-medical-robot-deep-space-missions/416874/))*

## 2. It is a payload handler first, and a doctor second

- The system is designed as a versatile payload handler that manages cargo, logistics, and equipment on routine days.
- When it is not organising tools or securing compartments, it pivots to medical support.
- **Kelly** described it as a general purpose helper for a lean crew, not a replacement crew member.

<u>The boring job is the point.</u> A robot that only works during emergencies will be untested, untrusted, and in the way when the emergency actually arrives.

**Use it every day for cargo, and it will be ready on the day someone is in pain.**

*(Source: [The Register, Google is building a robot medic for NASA](https://www.theregister.com/offbeat/2026/10/28/please-state-the-nature-of-the-medical-emergency-google-is-building-a-robot-medic-for-nasa/5306130))*

## 3. The kidney stone test case is deliberately ordinary

- **Google** gives one example: an astronaut with extreme back pain, a possible sign of kidney stones.
- The robot would retrieve and prepare the ultrasound machine, leaving the human crew medical officer to interpret the scan and decide on treatment.
- The robot might also capture basic vitals or simple ultrasounds, but only under the strict guidance of that human officer.

**Notice what the robot does not do.** It does not diagnose, it does not prescribe, and it does not decide. It fetches, preps, and assists.

*(Source: [Nextgov, NASA, Google test AI-powered medical robot for deep space missions](https://www.nextgov.com/emerging-tech/2026/10/nasa-google-test-ai-powered-medical-robot-deep-space-missions/416874/))*

![Astronauts aboard the International Space Station](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-02/iss-crew.jpg)
*Astronauts working aboard the International Space Station. Credit: NASA.*

## 4. A chatbot doctor came first, and it runs locally for a reason

- The robot builds on the **Crew Medical Officer Digital Assistant**, or **CMO-DA**, which **Google** and **NASA** have developed since 2025.
- **CMO-DA** is an AI powered clinical decision support system, designed to run models locally rather than sending data to a distant data center.
- It is already being evaluated on Earth bound copies of computers used aboard the **International Space Station**, and it runs on the Red Hat supported open source tool **RamaLama**.

**Local matters in space for the same reason it matters on Earth.** When the connection is slow, censored, or gone, the model on the machine is the only model you have.

*(Source: [The Register, Google is building a robot medic for NASA](https://www.theregister.com/offbeat/2026/10/28/please-state-the-nature-of-the-medical-emergency-google-is-building-a-robot-medic-for-nasa/5306130))*

## 5. 85 percent is a baseline, not a pass mark, and Google says so

- In early laboratory demonstrations, the robot achieved an **85 percent** baseline success rate in locating and moving a medical bag.
- The tests ran at **Johnson Space Center's iMETRO** facility, after movements were rehearsed in **Google DeepMind's MuJoCo** physics simulator.
- **Google** calls that result an initial baseline ahead of further training and safety refinement, not a finished medical capability.

**85 percent sounds good until you flip it.** It also means the robot failed to find or move the bag 15 percent of the time, in a lab, on a simple task.

<u>That honesty is the most trustworthy part of the whole announcement.</u>

*(Source: [ExecutiveBiz, Google Public Sector, NASA test robotic space assistant](https://www.executivebiz.com/articles/google-public-sector-nasa-test-robotic-assistant-deep-space-missions))*

## 6. The brain is Pi0, trained in just 2.5 hours

- The system used the open source **Pi0** model, developed by **Physical Intelligence** and run on **Google Cloud** infrastructure.
- **Google** fine tuned the **4 billion parameter** model on **Google Cloud G4** instances in just 2.5 hours.
- The demonstration used an eye to hand camera configuration to find and move the medical bag.

**Fast fine tuning is the real story for builders.** If a space robot's brain can be retrained in an afternoon, the same trick applies to warehouses, hospitals, and labs back on Earth.

*(Source: [Nextgov, NASA, Google test AI-powered medical robot for deep space missions](https://www.nextgov.com/emerging-tech/2026/10/nasa-google-test-ai-powered-medical-robot-deep-space-missions/416874/))*

## 7. NASA borrowed satellite tracking to help a robot walk a corridor

- **JPL** adapted satellite situational awareness tools, originally built to track objects in orbit, to help the robot navigate tight spacecraft spaces.
- That is a beautiful piece of reuse: software that watches satellites now helps a robot avoid bumping into a wall.
- The **MuJoCo** simulator let the team practice movements virtually before running them on real hardware, which matters when hardware mistakes are expensive and far away.

**Space engineering has always been recycling with better excuses.** This time the recycled part is vision, not metal.

*(Source: [TechDefused, NASA and Google test robot for deep-space medical support](https://techdefused.com/a/SmXnQj2/nasa-and-google-test-robot-for-deep-space-medical-support))*

![NASA robotics work](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-02/nasa-robotics.jpg)
*NASA robotics work in preparation for human spaceflight. Credit: NASA.*

## 8. No space ready robot exists yet, and that caveat matters

- The project remains at the **proof of concept** stage, with early laboratory demonstrations completed.
- **Google** has not confirmed whether a fully integrated, space ready robot exists, and **NASA** declined to give specifics when asked.
- **NASA** said only that it is working on a range of AI projects with partners and assessing them for future applications.

**Do not let the headlines upgrade this into a Mars hospital.** It is a lab demo with a good reason to exist, a clear human in charge, and a long road to flight.

*(Source: [The Register, Google is building a robot medic for NASA](https://www.theregister.com/offbeat/2026/10/28/please-state-the-nature-of-the-medical-emergency-google-is-building-a-robot-medic-for-nasa/5306130))*

## How to start

- If you are a builder, start with the pieces that are actually public: **MuJoCo** for physics simulation and open vision language action models like **Pi0**.
- If you are a student, read the **CMO-DA** story before the robot story. The local model problem is the foundation, the robot is the hands on top.
- If you work in healthcare, steal the design rule: the robot assists, the human decides. That boundary is the product.
- First step this week: pick one dull, repeated physical task in your own work and ask what an 85 percent helper would do to it. That is how this robot earns its place.

## The real pattern

The future of AI in high stakes places is not a smarter chatbot giving orders, it is a dumber, safer pair of hands that shows up on time, under human command, when the expert is 44 minutes away and the patient cannot wait.

## Final thoughts

Mars will not be saved by a robot that pretends to be a doctor. It will be saved by a robot that knows it is not one, fetches the right machine, and gets out of the human's way. That humility, built into hardware, is worth more than any demo.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

