# Presenter script: Early Payment Detection

About 10 minutes. Timings are targets. The presenter drives the screen. The decisions on the card are made by someone in a deciding role (a Contracts Manager, say), and the release is approved by a different person in a release role (a Financial Controller): two colleagues, or the presenter and one guest. Each gives their own full name.

**Before you start**
- The project folder has been reset (`docs/setup.md`, step 3). Finder is open on it beside the Claude app.
- A fresh session in the project has been sent *"Prepare a new review."*, and the dashboard shows **Ready**.
- Decide who makes the decisions and who approves, and that they're different people.

**The opening request:** *"Please run an early-payment review: are we paying our suppliers on the right day, and taking the discounts we negotiated?"*

| Time | Presenter does | Claude, in the chat | Dashboard | Presenter says |
|---|---|---|---|---|
| 0:00 | Shows the project folder: `01 Documents` holds the 12 agreements and `02 Data` the payment history, while `03 Outputs` and `04 Records` are empty | (Ready) | *Are we paying suppliers on the right day?*, and how the review works | "Every review works from a folder like this: documents, data, and two folders it may only fill once a second person approves. Quick guess: how many of these payments went out more than five days before they were due?" |
| 0:30 | Sends the opening request | *"Thank you. I have twelve supplier agreements and 679 payments from the project folder to review. …"* | **Updates:** 12 agreements, 679 payments, R320.0m, 12 suppliers | "A year of maintenance and services at Secunda and Sasolburg: a slice, not the group's totals." |
| 0:50 | Lets it read | *"Reading the agreements: six of twelve done."* Then: *"All twelve read. Five are confirmed by an independent check. Seven can each be read two ways, and need your judgement."* | (Unchanged: the chat carries this part) | "It reads each contract and quotes the clause. An independent check reads every term again." |
| 1:50 | Reads the stop aloud | *"Before I go further, I need your decisions. Seven agreements can each be read two ways, and each reading changes the figures. For Vaalkop Industrial Services (SAS-2402), the agreement's 10-day window means 60 discounts not taken … I've set each one on the card below to the reading I'd recommend, with my reason: keep it or change it, then add your name and role."* The **decision card** appears, seven items, each set to the recommended reading with its reason | **Opens on the decisions:** how much each one moves the figures. Open **SAS-2412**: 60 days in clause 3.1, 30 in an annexure that clause 5.1 says prevails, and each reading's early and late payments. **Expand the dashboard to full screen** | "This is the moment. A system that just picked one would be confidently wrong. This one shows you what each reading means, and asks." |
| 2:40 | The decider checks each recommendation against the reference: the annexure's 30 days for SAS-2412, the side letter for SAS-2402, the words for SAS-2406, from the invoice for SAS-2411, the main agreement for SAS-2403 (never countersigned), *paid early by design* for SAS-2405, standard terms for SAS-2410. They keep each that matches, change any that doesn't with a reason of their own, then give their full name and **Contracts Manager**; **Record decisions** | *"Thank you. All seven decisions are recorded, with your reasons, by …, Contracts Manager, at …"* | **Updates:** each decision page and agreement shows *Decided*, with the name, role and time | "A name, a role from the delegation of authority, a reason (the recommendation's, kept, or their own, and the record says which), and a fingerprint of exactly what was on screen, the recommendation included. And a small supplier paid within 15 days is recognised as intended." |
| 3:40 | Reads the findings as they arrive | *"The figures are in. I'm looking at each supplier now."* Then: *"Here's what the review found: **R1.7 million** in early-payment discounts not taken, across 99 payments. R520,000 in cost from paying 141 invoices well before they were due. 39 discounts were taken correctly, which isn't an issue."* And the recommendations, *"worth about R1.1 million over the next 12 months, starting with Vaalkop Industrial Services …"* Then the release card | **Opens on the Overview:** the findings, *Projected gain*, the 12-month projection, and *What to do first*. Open **Findings**: every payment taken, early, on time or late, adding up to 679 | Reveal the guess: 141. "Five of the twelve agreements are clean. The money sits in a handful: Vaalkop's discount, missed by days, and Komati's 90-day terms paid on a shorter run." |
| 4:40 | Opens **Recommendations**, then **Komati Conveyor Maintenance** | (Waits for the release) | **Recommendations:** the projected gain, *Lost if nothing changes* against *Saved with the recommended changes*, and every recommendation with its owner. On Komati, a question to ask in the rail | "Every figure in the analysis was checked against the review's own before it was shown. The values come from the same fixed rules as the findings." |
| 5:40 | Hands over to the approver | (Waits) | The rail says *Findings need a second person to release them* | The approver, on the card: it starts on **Approve the release** with the recommended reason; they keep or change it, give their full name and **Financial Controller**, and tick the confirmation themselves. "The card won't accept anyone who made a decision, or a role that decides." |
| 6:10 | Opens `03 Outputs` in Finder as Claude answers | *"Released, approved by …, Financial Controller. The report, a management briefing and a presentation for the next meeting, the evidence pack, the audit trail and the data are in the project folder under 03 Outputs › EP-…, and the full record of this review is in 04 Records. …"* | **Published:** the release stamp and the files | "Everything is filed where the team works, in OneDrive: the report, the pack for the next meeting, the evidence, the audit trail and the data." |
| 7:00 | Opens `Report` › the management briefing and the presentation | None | The briefing and the presentation open beside the chat | "The pack for the next meeting, in the Sasol design, with only the review's own figures, and the names of the people who decided and approved." |
| 8:30 | Opens the dashboard report's **Data** and **Audit** pages | None | Every payment's outcome, row by row, with *Download as Excel*; the audit trail and its controls | "Every figure traces to the rows behind it, and every step to the person who took it." |
| 9:30 | Closes on the folder | None | None | "Claude read twelve contracts, quoted every clause, stopped where seven could be read two ways, waited for a named person, then told us what to do about it, with every figure checked." |

## A shorter run, 5 minutes

Use a session already run to the decisions. Open SAS-2412's decision page, decide on the card, then the findings, the release and the folder.

## Going deeper, 3 to 5 more minutes (finance and audit audiences)

- *"Why was Komati Conveyor Maintenance paid early so often, and what would paying on day 90 save?"* Claude answers from the review, and says where the dashboard shows it.
- *"How did you value the Vaalkop recommendation?"* Claude gives the rule in a sentence: the discounts not taken, net of the cost of paying sooner, over the period reviewed, carried forward a year and phased in over three months.
- Open the audit trail from `Evidence`: every step with who and why, every decision with the options and roles allowed, how each figure was worked out, and every control re-checked.
- *"Can we check the record hasn't been changed?"* It returns *"Tamper check passed: every entry is intact and in order."*
- In a fresh session, choose **Main agreement · 60 days** for SAS-2412: 199 payments paid early, R675,000 in cost, and its decision page says *Decided against clause 5.1*.

## If something goes wrong

| Situation | Do |
|---|---|
| Claude says a step didn't complete | Start a fresh session and send the opening request again |
| The dashboard doesn't update | Say "Please show my dashboard"; Claude rewrites it with the latest figures |
| The decision card can't send | Copy the text it shows into the chat |
| A decision is refused (a role outside the list, a one-word reason, no surname) | That's the control working: give what it asks for, and the card is recorded whole |
| The files don't appear in `03 Outputs` | Say "Please save the files to the project folder". If that fails too, open them from the chat |
| No connection | Walk through the reference run's screens in `reference-run/screens/` |

The reference run, with every figure and screen, is in `reference-run/`.
