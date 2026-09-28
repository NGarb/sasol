# Presenter script: Duplicate Vendors & Payments

About 10 minutes. Timings are targets. The presenter drives the screen and makes the decisions as **Thandi Nkosi, Vendor Master Data Manager**, or invites someone in the room to decide in their own name and role. A second person approves the release, in a senior role: a colleague, or someone in the room, as **Lerato Mokoena, Financial Controller**. The person who decides can never approve.

**Before you start**
- The project folder has been reset (`docs/setup.md`, step 3). Finder is open on it beside the Claude app.
- A fresh session in the project has been sent *"Prepare a new review."*, and the dashboard shows **Ready**.
- Keep the eight choices below to hand. The card starts on Claude's recommendation for every pair, with its reason: check each against them, and change any that differs, with a reason of at least three words.

**The opening request:** *"Please run a duplicate-supplier review: is anyone in our supplier list twice, and have we paid anyone twice?"*

| Time | Presenter does | Claude, in the chat | Dashboard | Presenter says |
|---|---|---|---|---|
| 0:00 | Shows the project folder: `02 Data` holds the supplier list and the spend history, while `03 Outputs` and `04 Records` are empty | (Ready) | *Are we paying anyone twice?* | "Every review works from a folder like this. This one needs no documents, only the supplier list and a year of orders under R1 million." |
| 0:20 | Sends the opening request | *"Thank you. I have 1,950 supplier records and 5,000 purchase orders from the project folder to review. …"* | **Updates:** 1,950 suppliers, 1,015 with orders, 5,000 orders, R812.1m, Secunda and Sasolburg | "It'll compare every plausible pair in seconds." |
| 0:40 | Lets it compare | *"I've compared 31,928 plausible pairs. Eight reach the policy line and need a person; fourteen look-alike names stay below it."* | (Unchanged) | "Eight out of thirty-two thousand. That's the queue a person actually sees." |
| 1:10 | Reads the stop aloud | *"Before I count anything, eight pairs need your decision. Four share a tax number, and four share a bank account under different tax numbers … Three already have orders for the same amount on both records: Grootpan, Leeuwpan and Komati. I've set each one on the card below to what I'd recommend, with my reason: keep it or change it, then add your name and role."* The **decision card** appears, one line of evidence per pair, each set to the recommendation with its reason | **Opens on the Overview:** the review queue with a *Same-amount orders* column, and *8 pairs need a decision* in the rail. Open **Candidates** and **drag the review line**: at 0.36 the Mafube / Rietspruit account goes unreviewed; at 0.10 fourteen look-alikes crowd in. Open **Komati**: both R487,350.00 orders, shown before anyone decides | "The evidence is on the table before the decision, including the orders that match. And where the line sits is a policy choice, not an IT setting." |
| 2:30 | On the card, each pair starts on its recommendation, with its reason. Check each against these, keeping those that match and changing any that doesn't, with a reason of your own: Grootpan **The same supplier** (*"same tax number and bank account"*); Kinross **The same supplier** (*"the same company, old record blocked"*); Trichardt **Refer it on** (*"two legal entities, conversion not confirmed"*); Leeuwpan **The same supplier** (*"same tax number and registered name"*); Delmas / Vaalbank **Different suppliers** (*"different companies, tax number captured wrongly"*); Bethal **Different suppliers · bank details verified** (*"group account confirmed with both companies"*); Komati **The same supplier** (*"related names, same account, same order twice"*); Mafube / Rietspruit **Refer it on** (*"a shared account alone doesn't prove it"*). Then **Thandi Nkosi**, **Vendor Master Data Manager**, **Record decisions** | *"Thank you. All eight decisions are recorded, with your reasons, by Thandi Nkosi, Vendor Master Data Manager, at 10:42."* | Open **Decisions**: every pair, with the name and role beside it | "One person, named, in a role that's allowed to make this call. For a shared bank account, 'different suppliers' means the bank details were verified: it's never just waved through." |
| 4:00 | Reads the reveal as it arrives | *"The figures are in. I'm looking at each pair now."* Then: *"Here's what your decisions show: **R820,000** was paid twice, on three pairs you confirmed as one supplier: R139,000 to Grootpan, R194,000 to Leeuwpan, R487,000 to Komati. … Trichardt and Mafube / Rietspruit go for review, not a verdict."* And: *"I've also looked at each pair. … my eleven recommendations are worth about R1.5 million over the next 12 months, starting with Komati Motor Rewinds and Komati Group: recover the amount paid twice."* Then the release card | **Opens on the Overview:** *Paid twice R819,782*, combined spend and paid twice by pair, *Projected gain* and the 12-month projection, and *What to do first*. Open **Payments**: the three pairs of orders, each paid | "Neither record showed it on its own. The decisions made it count." |
| 5:00 | Opens **Recommendations**, then the Trichardt pair | (Waits for the release) | **Recommendations:** the projected gain, *Lost if nothing changes* (dashed) against *Saved with the recommended changes*, and every recommendation with its owner, what it's worth over 12 months and what's at stake. Move the *share of the change achieved* slider. **Trichardt:** the analysis notes the decision differs from the assessment | "Every figure here was checked against the review's own before it was shown, and the values come from the same fixed rules as the findings." |
| 6:00 | Hands over to the approver | (Waits) | *Findings need a second person to release them* | The approver, on the card: it starts on **Approve the release** with the recommended reason; they keep it or write their own (*"evidence reviewed against the records"*), then **Lerato Mokoena**, **Financial Controller**, and tick the confirmation themselves. "If Thandi typed her own name here, the card would stop her." |
| 6:30 | Opens `03 Outputs` in Finder as Claude answers | *"Released, approved by Lerato Mokoena, Financial Controller. The report, a management briefing and a presentation for the next meeting, the evidence pack, the audit trail, the data, the change request and the draft recovery letters are in the project folder under 03 Outputs › DV-0926-1042 …"* | **Published:** the release stamp with the approver's name and role, and the files | "Report, Evidence, Actions: everything filed where the team works. Nothing changes in any system." |
| 7:30 | Opens the **Report** folder: the management briefing and the presentation | None | (Unchanged) | "The pack for the next meeting is already made, from the review's own figures, with the names of the people who decided and approved." |
| 8:30 | Opens the dashboard report from `03 Outputs`, then **Data** and **Audit** | None | **Data:** every supplier record and order, row by row, with *Download as Excel*. **Audit:** every step, each decision with who made it and why, and every control | "Every row it read, and every step it took, in the file you keep." |
| 9:30 | Closes on the folder | None | None | "Thirty-two thousand pairs compared, eight decided by a named person, R820,000 paid twice found because of those decisions, and what to do about each pair, with every figure checked and a second person's approval." |

## A shorter run, 5 minutes

Use a session already run to the decisions. Move the review line, show Komati's matching orders, decide on the card, then the reveal and the recommendations, the release and the folder.

## Going deeper, 2 to 3 more minutes (finance and audit audiences)

- *"How did you value the Komati recommendations?"* Claude gives the rule in a sentence: the amount paid twice is recovered once, and merging the two records stops it recurring at the pace of the period reviewed, carried forward a year and phased in over three months. The evidence pack's Recommendations sheet has every value and its basis.
- *"What if we'd referred Komati?"* In a fresh chat, refer it: R332,000 is paid twice, and Komati's R487,350.00 stays on the dashboard as a possible duplicate, pending forensic review. It's never shown as nothing.
- *"Why isn't Kinross worth anything?"* Nothing was paid twice on it, so its spend is shown as at stake: the risk that closing the blocked record removes, never counted as a saving.

## If something goes wrong

| Situation | Do |
|---|---|
| Claude says a step didn't complete | Start a fresh session and send the opening request again |
| The dashboard doesn't update | Say "Please show my dashboard" |
| The card refuses a name, a role or a reason | Give a first name and surname, choose a role from the list, and write a reason of at least three words |
| The decision card can't send | Claude asks for the choices and reasons, the name and the role in the chat: give them in one reply |
| The files don't appear in `03 Outputs` | Say "Please save the files to the project folder". If that fails too, open them from the chat |
| Someone asks whether it's fraud | "That isn't something the review decides. Shared bank details go to forensic review, and people with the authority decide." |
| No connection | Walk through the reference run's screens in `reference-run/screens/` |

The reference run, with every figure and screen, is in `reference-run/`.
