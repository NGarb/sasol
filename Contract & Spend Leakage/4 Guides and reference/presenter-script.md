# Presenter script: Contract & Spend Leakage

About 9 minutes. Timings are targets. The presenter drives the screen and makes the decisions on the card, or invites someone in the room to, as a named person in one of the deciding roles (*Thandi Nkosi, Contracts Manager* in the reference run). A second person approves the release, in a release role (*Lerato Mokoena, Financial Controller*).

**Before you start**
- The project folder has been reset (`docs/setup.md`, step 3). Finder is open on it beside the Claude app.
- A fresh session in the project has been sent *"Prepare a new review."*, and the dashboard shows **Ready**.

**The opening request:** *"Please run a contract-leakage review: are we buying through our contracts, and are their terms being honoured?"*

| Time | Presenter does | Claude, in the chat | Dashboard | Presenter says |
|---|---|---|---|---|
| 0:00 | Shows the project folder: `01 Documents` holds 12 panel agreements and `02 Data` the spend history and the invoice lines, while `03 Outputs` and `04 Records` are empty | (Ready) | *Are we buying through our contracts?* | "Every review works from a folder like this. Before we start: what share of our spend do you think is off contract?" |
| 0:20 | Sends the opening request | *"Thank you. I have 5,000 purchase orders, 12 panel agreements and 288 invoice lines from the project folder to review. I'll read the agreements first …"* | **Updates:** 5,000 orders, R812.1m, 12 agreements | "Hold on to your guess." |
| 0:40 | Waits while the agreements are read | *"Reading the agreements: six of twelve done."* Then *"All twelve read. Twelve are confirmed by an independent check."* | The agreements, each with its term, notice and rate clause, confirmed; two more marked **Not on file** | "Every term is quoted from its clause. Notice the agreements differ: one runs 60 months with 180 days' notice." |
| 1:30 | Reads the stop aloud | *"Before I count anything, a few things need your decision, on one card … I've set each one on the card below to what I'd recommend, with my reason: keep it or change it, then add your name and role."* The **decision card** appears with **8 items**, each set to the recommendation with its reason | **Opens on Decisions:** each item with its evidence; the overview shows both definitions' totals and the rises charged above the terms | "It didn't pick a number. Definition A is R292.9 million, B is R53.2 million: that's a judgement, so it asks." |
| 2:00 | On the card, each item starts on the recommendation. Check each against the reference: **B**; SAS-2507 **Rely on the contract register**; SAS-2509 **Treat as uncontracted until filed**; claim SAS-2512, SAS-2502 and SAS-2511; accept SAS-2503; refer SAS-2501. Keep each that matches, change any that doesn't with a reason of your own, then a full name and **Contracts Manager**; **Record decisions** | *"Thank you. All eight decisions are recorded, with your reasons, by Thandi Nkosi, Contracts Manager, at 10:42."* | Decisions: each item decided, with the name and role | "One person, eight judgements, each with a reason, on the record. The role list is the delegation of authority." |
| 3:00 | Reads the result as it arrives | *"The figures are in. I'm looking at each agreement and category now."* Then: *"Here's what the review found. Under your definition, **R51.6 million** … Two agreements' notice deadlines have passed, so they will renew … Three rate rises are claimed as credit notes, R329,000 to recover …"* And the recommendations: *"… worth about R2.9 million over the next 12 months: R650,000 measured, and R2.2 million resting on the 5% planning assumption."* Then the release card | **Overview:** off contract R51.6m, renewals due 3, rate rises 5, *Projected gain* split into measured and assumed, the 12-month projection and *What to do first* | "How close was your guess? And look at the split: it tells you which part is measured and which part is an assumption." |
| 4:00 | Opens **Escalation › SAS-2512**, then **Decisions › SAS-2507**, then **Recommendations** | (Waits for the release) | SAS-2512: +8.4% against August 2025's published 3.3%, the rate charged against the rate allowed, clause 2.3 quoted, the decision stamped with the name. SAS-2507: quoted by 50 purchases but not on file. Recommendations: measured against assumed, every action with its owner | "Every rand traces to a clause and a published CPI figure. And where an agreement isn't on file, it says so instead of pretending it read it." |
| 5:00 | Hands over to the approver | (Waits) | *Findings need a second person to release them* | The approver, on the card: it starts on **Approve the release** with the recommended reason; they keep it or write their own (*"drafts reviewed against the evidence"*), give their full name and **Financial Controller**, and tick the confirmation themselves. "Only a release role can approve, and never the person who decided." |
| 5:30 | Opens `03 Outputs` in Finder as Claude answers | *"Released, approved by Lerato Mokoena, Financial Controller. The report, a management briefing and a presentation for the next meeting, the evidence pack, the audit trail and the data are in the project folder …"* | **Published:** the release stamp and the files | "That's Monday morning for a category manager: the letters are drafted, the pack is ready for the meeting, and everything is filed where the team works." |
| 6:30 | Opens **Report › Presentation** and the **Management briefing**, then the dashboard report's **Data** and **Audit** pages | None | The presentation's scorecards and charts; the Data page row by row with **Download as Excel**; the audit trail | "Every row read and every result, and every step with who and why. Nothing here is a black box." |
| 8:30 | Closes on the folder | None | None | "It asked what we meant before it counted, every date and rand traces back to a clause, and a named person owns every decision." |

## A shorter run, 5 minutes

Use a session already run to the card. Take the guess, decide on the card, read the result, open SAS-2512 and the Recommendations split, then the release and the folder.

## If something goes wrong

| Situation | Do |
|---|---|
| Claude says a step didn't complete | Start a fresh session and send the opening request again |
| The dashboard doesn't update | Say "Please show my dashboard" |
| The decision card can't send | Copy the message it shows into the chat |
| Claude asks for items the card didn't cover | Answer those items in the chat, with a reason each |
| The files don't appear in `03 Outputs` | Say "Please save the files to the project folder". If that fails too, open them from the chat |
| Someone asks where the 5% comes from | "It's the review's planning assumption: buying on contract costs 5% less than buying off it. Every value that rests on it says so, and the gain is split into measured and assumed." |
| Someone asks where the CPI comes from | "Statistics South Africa's published headline CPI, for the month clause 2.3 names: the second month before the supplier's notice. The escalation page shows the month and the figure." |
| No connection | Walk through the reference run's screens in `reference-run/screens/` |

The reference run, with every figure and screen, is in `reference-run/`.
