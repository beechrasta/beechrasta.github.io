# The Microsoft Outage That Took Down Outlook, Teams and Copilot in 74 Countries in 2026

*It was not a hack. It was a routine upgrade, and that is the scary part.*

![A Microsoft building under a clear blue sky](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-15/microsoft-building.jpg)

*A Microsoft building in Redmond, Washington. Photo: Sammamish Washington.*

Let's stop pretending the cloud is always there.

On Thursday, **Microsoft 365** went down across **74 countries**, and it stayed down for **more than a day**. **Outlook**, **Teams** and **Copilot** all went dark together.

This article is not about one bad Thursday. It is about what happens when the whole world rents its office from one landlord.

## 1. Thursday, midday: how it unfolded

The timeline is short and brutal.

- First reports surfaced around **midday Thursday, November 12**, in the US, when users could not open their **Exchange Online** mailboxes
- **Microsoft** first acknowledged the issue at **5:54 pm GMT**, 11:24 pm IST
- The incident records list **EX1550543** for Exchange Online, starting 4:17 pm UTC, and **MO1550821** for the wider Microsoft 365 disruption, starting 6:26 pm UTC
- Services were **fully restored on Saturday, November 14**, more than 24 hours later

Microsoft's own words on Saturday: "We have completed our efforts to address the underlying issue of the incident and restored service to the remaining impacted customers and regions."

More than a day without email. In 2026, that is not an inconvenience. That is a shutdown.

*(Source: [YourStory](https://yourstory.com/2026/11/one-outage-millions-affected-what-went-wrong-at-microsoft))*

## 2. 74 countries in one hour

Speed is the detail that tells you how centralised everything has become.

- Within an hour of the first problems, outage tracker **Downdetector** had logged reports from **74 countries and territories**
- The services hit: **Outlook, Teams, Copilot, OneDrive and SharePoint**
- Governments, courts, healthcare services, businesses, airlines and banks, all in the same boat, at the same time

One company's bad afternoon became 74 countries' bad day. That is not a bug in the system. That is the system.

*(Source: [Firstpost](https://www.firstpost.com/tech/microsoft-says-services-fully-restored-after-global-outage-hit-governments-banks-and-airlines-14059984.html))*

## 3. When email dies, governments start texting

This is where the outage stops being a tech story and becomes a civilisation story.

- In **Japan**, government email became completely unavailable, forcing staff to resort to **text messaging** for communications
- The governments of **Japan, Singapore, Australia, Greece, Norway and India** all reported disrupted operations
- In **Britain**, a trial in **Manchester** was halted after technical problems affected court proceedings
- The British government said it was working closely with Microsoft while maintaining contingency arrangements

Hospitals fell back on phone lines and paper records. Some offices dug out the fax machine.

*Italics aside: the richest companies on earth run on email, and email runs on one vendor, and one vendor had a bad upgrade. The fax machine was the backup plan.*

*(Source: [Outlook India](https://www.outlookindia.com/international/microsoft-fixes-24-hour-global-outage-that-silenced-outlook-and-teams-worldwide))*

![A dimly lit server room with rows of illuminated racks](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-15/server-room-dark.jpg)

*A dimly lit server room. When the core process that handles secure connections stops, nothing else matters. Photo: GBSower.*

## 4. It was not a hack, and that matters more

Everyone's first guess was a cyberattack. Microsoft ruled it out fast, and the real answer is worse.

- The incident was **"introduced by an issue during an earlier network capacity upgrade that surfaced"** after a recent network change
- Engineers traced part of the fault to a **core process responsible for secure connections** that became overwhelmed and stopped processing requests
- Microsoft said the outage was **"not related to cyber"** or **AI agents**, and apologised on Friday, saying it was **"deeply sorry"**
- Restoration was gradual, validating stability at each stage. **Asia Pacific** stabilised first on November 13, followed by Europe and North America
- A full **post-incident report** is promised

A hacker is an enemy you can fight. A routine capacity upgrade that quietly breaks your core connection process is an enemy that lives inside your own change pipeline.

*(Source: [The Guardian](https://www.theguardian.com/technology/2026/nov/14/microsoft-says-services-fully-restored-after-global-outage))*

## 5. The CrowdStrike parallel nobody wanted

We have seen this movie before, and it was also not a hack.

- On **July 19, 2024**, a faulty **CrowdStrike Falcon** update crashed roughly **8.5 million Windows computers** worldwide
- **Delta** cancelled more than **7,000 flights over five days**, disrupting around 1.3 million passengers, at a cost of about **$550 million**
- In 2025, an **Amazon Web Services** outage disrupted thousands of businesses and took more than 15 hours to resolve

The Guardian called this week's failure **"one of worst IT failures in years."** The pattern across all three: a routine update, a single point of failure, and a blast radius measured in countries, not customers.

<u>The two biggest IT failures in recent years were both self-inflicted updates, not hackers.</u>

*(Source: [SFG Media](https://sfg.media/en/a/microsoft-outage-global-dependence-tech-giants/))*

## 6. Even Copilot went down with the ship

Here is the irony that deserves its own section.

**Copilot**, the AI assistant sold as the thing that makes work resilient and effortless, died at exactly the same moment as the email it was supposed to help you manage.

- Your AI assistant lives on the same cloud it is meant to save you from
- When the platform goes, the assistant goes with it, no matter how smart the model is
- The **AI tools** did not cause this outage, Microsoft was clear about that, but they were the first casualty of it

Every AI productivity pitch assumes the infrastructure underneath is permanent. Thursday proved it is a Tuesday upgrade away from gone.

*(Source: [Financial Express](https://www.financialexpress.com/life/technology/microsoft-365-services-fully-restored-company-shares-latest-update/4384428/))*

![A modern Microsoft campus building with the company logo](https://raw.githubusercontent.com/beechrasta/medium-images/main/2026-11-15/microsoft-campus.jpg)

*Microsoft's campus in Redmond. The same infrastructure that serves governments and hospitals also serves your Copilot. Photo: Peter Reinold.*

## 7. One landlord, everybody's office

Step back from the incident reports and look at the shape of the thing.

- A handful of providers underpin email, documents, meetings and AI assistance for most of the working world
- Governments, hospitals and courts run on the **same infrastructure** as your startup's standup notes
- The question nobody prices into the contract: **what is your plan B when the landlord's lights go out**

Redundancy used to mean a second server in the next room. Now it means a second vendor, a second continent, and a runbook that works when the tools the runbook describes are all down at once.

*(Source: [Gulf News](https://gulfnews.com/technology/companies/microsoft-says-global-outage-fully-resolved-after-disrupting-services-in-over-70-countries-1.500747167))*

## How to start

**If you are an everyday worker:** keep an offline list of your team's phone numbers and your IT helpdesk number. Know where your files live outside the cloud. It takes ten minutes and saves a day.

**If you are a developer or IT lead:** test your failover before you need it, keep a status page habit, and write runbooks that work **without the tools they describe**. If your incident response plan lives in the system that just died, you do not have a plan.

**If you are a founder:** SLA credits are not a business continuity plan. Ask your team one question on Monday: what do we do if Outlook and Teams are both gone until tomorrow?

## The real pattern

The cloud did not fail because it is fragile. It failed because it is centralised. Every efficiency gain from putting the world's office in one place is also a concentration of risk in one place, and the bill for that risk arrives on a random Thursday, all at once, in 74 countries.

## Final thoughts

Nobody hacks the cloud anymore. They do not have to.

We hand it the keys, schedule the upgrade, and wait for the capacity change to do the job for them. Build your plan B on a quiet day, because the loud ones are already taken.

* * *

If this saved you money or taught you something, [buy me a coffee](https://buymeacoffee.com/rachitasthana). It keeps the articles coming.

Follow along. Clap if it earned it.

