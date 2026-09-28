# Verified figures: Early Payment Detection

Every figure below came from running the review from a copy of the project folder, and was checked against the generator's own answer key (`tests/fixtures/truth.json`). Your run should show exactly these figures for the choices you make. Review numbers, times and the record's entry fingerprints differ on every run; **the figures, the fingerprint of the approved figures and the input fingerprints don't.**

## Before the decisions (the same whatever is chosen)

- Agreements read: **12**; confirmed by the independent check: **5**; can each be read two ways, so a person decides: **7**
- Payments: **679** worth **R320,022,513.96** (rand excluding VAT), invoices dated Jul 2025 to Jun 2026, sites Secunda, Sasolburg
- Paying early is valued at the Treasury's short-term funding rate, **9.5%** a year; on time is within **5 days** either side of the due date, counted from the invoice date

## The decisions on one card

Ordered as the card shows them, by how much money the choice moves. Each reading's effect is on that agreement's own payments. The card starts on the reference choice for each, the recommendation in `tests/fixtures/claude-assessment.json`, with its reason.

| Agreement | Why a person decides | Options | Reference choice | Effect of each reading |
|---|---|---|---|---|
| SAS-2402 Vaalkop Industrial Services | A later side letter widens the discount window | Agreement · 2% in 10 days / Side letter · 2% in 15 days / Refer it on | Side letter · 2% in 15 days | *Side letter · 2% in 15 days*: none early, 11 late, 53 discounts not taken (R1,349,585.05); *Agreement · 2% in 10 days*: 7 early (R146,167.19), 11 late, 60 discounts not taken (R1,586,317.83) |
| SAS-2412 Blesbokspruit Crane Hire | Clause 3.1 gives one period and Annexure B, signed by both, another; clause 5.1 says the annexure prevails | Main agreement · 60 days / Annexure · 30 days / Refer it on | Annexure · 30 days | *Annexure · 30 days*: none early, 9 late; *Main agreement · 60 days*: 58 early (R155,510.44), none late |
| SAS-2406 Grootpan Electrical Contractors | Clause 3.1's words and figures disagree | Figures · 45 days / Words · 30 days / Refer it on | Words · 30 days | *Words · 30 days*: none early, none late; *Figures · 45 days*: 60 early (R66,382.03), none late |
| SAS-2411 Steelpoort Fabrication Works | Clause 3.1 counts from statement; clause 3.4 from the invoice | From the invoice · 60 days / From the statement · 60 days / Refer it on | From the invoice · 60 days | *From the invoice · 60 days*: none early, 17 late; *From the statement · 60 days*: 38 early (R58,464.23), 1 late |
| SAS-2403 Mpumalanga Valve and Seal | Annexure B changes the period, but only the supplier signed it; clause 5.2 needs both signatures | Main agreement · 60 days / Unsigned annexure · 45 days / Refer it on | Main agreement · 60 days | *Main agreement · 60 days*: 48 early (R48,450.89), none late; *Unsigned annexure · 45 days*: none early, none late |
| SAS-2405 Sandspruit Analytical Labs | A qualifying small enterprise the purchaser aims to pay within 15 days (clause 3.4), on 30-day terms in clause 3.1 | Paid early by design: not a finding / Count its early payments (30 days) / Refer it on | Paid early by design: not a finding | *Paid early by design: not a finding*: none early, none late; *Count its early payments (30 days)*: 48 early (R39,717.11), none late |
| SAS-2410 Leeuwpan Industrial Gases | The agreement ended on 31 March 2026 and payments continued; clause 4.2 sets the terms after it ends | Keep the agreement's 60 days / Standard 30 days after it ended / Refer it on | Standard 30 days after it ended | *Standard 30 days after it ended*: none early, none late; *Keep the agreement's 60 days*: 13 early (R33,388.03), none late |

## After the decisions

The reference run's choices, then each decision switched to its other reading on its own (everything else as the reference run), then every agreement that can be read two ways referred on.

| Reading | Payments assessed | Paid early | Cost of paying early | Discounts not taken | Value not taken | Discounts taken | Value taken | Paid late | On time | Set aside | Fingerprint |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **Reference run** | 679 | 141 | R519,547.69 | 99 | R1,672,556.43 | 39 | R732,352.74 | 45 | 454 | none | `fb93912c` |
| SAS-2402: agreement | 679 | 148 | R665,714.88 | 106 | R1,909,289.21 | 32 | R495,619.96 | 45 | 454 | none | `686f3891` |
| SAS-2403: annexure | 679 | 93 | R471,096.80 | 99 | R1,672,556.43 | 39 | R732,352.74 | 45 | 502 | none | `0614c012` |
| SAS-2405: count | 679 | 189 | R559,264.80 | 99 | R1,672,556.43 | 39 | R732,352.74 | 45 | 406 | none | `7c548b50` |
| SAS-2406: figures | 679 | 201 | R585,929.72 | 99 | R1,672,556.43 | 39 | R732,352.74 | 45 | 394 | none | `d8d34347` |
| SAS-2410: keep | 679 | 154 | R552,935.72 | 99 | R1,672,556.43 | 39 | R732,352.74 | 45 | 441 | none | `71debef3` |
| SAS-2411: statement | 679 | 179 | R578,011.92 | 99 | R1,672,556.43 | 39 | R732,352.74 | 29 | 432 | none | `aa15fbd9` |
| SAS-2412: main | 679 | 199 | R675,058.13 | 99 | R1,672,556.43 | 39 | R732,352.74 | 36 | 405 | none | `9796008c` |
| All referred on | 285 | 93 | R471,096.80 | 46 | R322,971.38 | 20 | R126,167.72 | 8 | 164 | SAS-2402, SAS-2403, SAS-2405, SAS-2406, SAS-2410, SAS-2411, SAS-2412 | `3ae86074` |

## The analysis (reference run)

Every lever the rules value, and what it's worth over the next 12 months (each change phased in over its first three months). The reference analysis recommends 6 of them: **R1,102,509.52** in all, 0.34% of the invoice value reviewed. A live analysis may choose differently; the values of the levers don't change.

| Lever | What it does | Kind | 12 months | Recommended |
|---|---|---|---|---|
| `SAS-2402:discount` | Take the 2% discount by paying within 15 days | recurring | R471,824.98 | yes |
| `SAS-2402:on-time` | Pay within the agreed 60 days, not after | risk | not valued |  |
| `SAS-2404:due-date` | Pay on the agreed due date (90 days) | recurring | R326,298.69 | yes |
| `SAS-2407:due-date` | Pay on the agreed due date (30 days) | recurring | R10,048.03 |  |
| `SAS-2407:discount` | Take the 1.5% discount by paying within 10 days | recurring | R186,128.34 | yes |
| `SAS-2407:on-time` | Pay within the agreed 30 days, not after | risk | not valued |  |
| `SAS-2408:due-date` | Pay on the agreed due date (60 days) | recurring | R75,862.98 | yes |
| `SAS-2403:due-date` | Pay on the agreed due date (60 days) | recurring | R42,394.53 | yes |
| `SAS-2412:on-time` | Pay within the agreed 30 days, not after | risk | not valued |  |
| `SAS-2411:on-time` | Pay within the agreed 60 days, not after | risk | not valued | yes |

## Input fingerprints (the files in the project folder)

| File | Fingerprint (first 16 characters) |
|---|---|
| SAS-2401 Highveld Rotating Solutions.docx | `a2010af1abe13c01` |
| SAS-2402 Vaalkop Industrial Services.docx | `6774dc519b9f21b1` |
| SAS-2403 Mpumalanga Valve and Seal.docx | `43750e60da308647` |
| SAS-2404 Komati Conveyor Maintenance.docx | `9404698ef6bfb682` |
| SAS-2405 Sandspruit Analytical Labs.docx | `be5b195a7a6a7c3a` |
| SAS-2406 Grootpan Electrical Contractors.docx | `14c7b420c7902d27` |
| SAS-2407 Riverhorse Bulk Chemicals.docx | `5aefc390e8c578f4` |
| SAS-2408 Delmas Catalyst Handling.docx | `4d9f7e7ddadf1481` |
| SAS-2409 Witbank Refractory Services.docx | `a939c1777a5439db` |
| SAS-2410 Leeuwpan Industrial Gases.docx | `73265d83076155b5` |
| SAS-2411 Steelpoort Fabrication Works.docx | `830aa25115c9b8da` |
| SAS-2412 Blesbokspruit Crane Hire.docx | `2c356ccc6267feca` |
| payment_history.xlsx | `8ae7059c5d24adf4` |

## The controls, as shown in the reference run

- Asking for the findings before the decisions: *"This step needs a decision first. Nothing has been calculated."*
- A decision in a role outside the delegation (Finance): *"Only these roles can make this decision: Contracts Manager, Category Manager, Procurement Manager or Legal Counsel. Please choose one of them."*
- A first name only: *"Please give your full name, a first name and a surname: every decision is recorded against the person who made it."*
- A one-word reason ("Test"): *"Please give the reason in a sentence of your own, three words or more: a decision without one isn't recorded."* The card is recorded whole or not at all.
- The recommended reason given for the other reading: *"That reason is the one recommended for a different option. Please give the reason for your choice in your own words."*
- Publishing before approval: *"Nothing can be released without an approver's decision."* `03 Outputs` and `04 Records` stay empty.
- Thandi Nkosi, who made the decisions, approving the release: *"A different person must approve the release: Thandi Nkosi made a decision in this review, so can't also release it."* A deciding role is refused too, and so is an approval without the confirmation.
- The analysis quoting a figure that isn't the review's own, or recommending another supplier's lever: *"Fix and run again: …"*, corrected before anything is shown.
- The tamper check on the record in `04 Records`: *"Tamper check passed: every entry is intact and in order."* On the altered copy in `tamper-demo/` (a decision's role changed): *"The record was altered at entry 11."*
