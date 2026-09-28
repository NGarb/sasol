# Verified figures: Contract & Spend Leakage

Every figure below came from running the review from a copy of the project folder, and was checked against the generator's own answer key (`tests/fixtures/truth.json`). Your run should show exactly these figures for the decisions you make. Review numbers, times and the record's entry fingerprints differ on every run; **the figures, the fingerprint of the approved figures and the input fingerprints don't.**

## Before the decisions (the same for every choice)

- Purchase orders under R1 million: **5,000** worth **R812,094,562.35**, Jul 2025 to Jun 2026; invoice lines: **288**, worth **R65,421,860.30**
- Agreements read: **12**; confirmed by the independent check: **12**
- Definition A, every purchase with no contract reference: **1,477** purchases worth **R292,948,564.16**
- Definition B, only where a contract exists for the category: **364** purchases worth **R53,185,127.99**; **336** worth **R51,377,498.72** if no agreement not on file is relied on
- A is **4.1** times B, by purchases; categories quoting an agreement: **14**
- Not in the folder, though the spend quotes them: **SAS-2507** (Fabrication), 50 purchases, R14,905,360.34; **SAS-2509** (PPE and Safety), 261 purchases, R15,225,539.36

## The card

One card, 8 items, decided by one person in a role from: Contracts Manager, Category Manager, Procurement Manager, Commercial Manager.

| Item | The evidence on the card | Options | Reference choice |
|---|---|---|---|
| `definition` | A counts 1,477 purchases, R292.9 million · B counts 364, R53.2 million, R1.8 million of it in the categories below | Every purchase with no contract reference · Only where a contract exists for the category · Refer it on | Only where a contract exists for the category |
| `missing:SAS-2507` | 50 purchases quote it, R14.9 million · 1 purchase with no reference, R225,000, counted under B only if it's relied on | Rely on the contract register · Treat as uncontracted until filed · Refer it on | Rely on the contract register |
| `missing:SAS-2509` | 261 purchases quote it, R15.2 million · 27 purchases with no reference, R1.6 million, counted under B only if it's relied on | Rely on the contract register · Treat as uncontracted until filed · Refer it on | Treat as uncontracted until filed |
| `rate:SAS-2512` | Rate up 8.4% from 5 Dec 2025 · CPI allowed 3.3% · 14 lines · R213,000 over | Claim a credit note · Accept the rise · Refer it on | Claim a credit note |
| `rate:SAS-2502` | Rate up 3.1% from 20 Feb 2026 · no notice received · 9 lines · R86,000 over | Claim a credit note · Accept the rise · Refer it on | Claim a credit note |
| `rate:SAS-2501` | Rate up 3.2% from 20 Dec 2025 · notice sent to a buyer on 25 Oct 2025 · 13 lines · R55,000 over | Claim a credit note · Accept the rise · Refer it on | Refer it on |
| `rate:SAS-2511` | Rate up 3.3% from 5 Oct 2025 · anniversary 13 Nov 2025 · 3 lines · R30,000 over | Claim a credit note · Accept the rise · Refer it on | Claim a credit note |
| `rate:SAS-2503` | Rate up 3.2% from 5 Jan 2026 · 5 days' notice, 30 required · 2 lines · R15,000 over | Claim a credit note · Accept the rise · Refer it on | Accept the rise |

## After the decisions

| | Reference (the presenter script) | A | Both on the register | Every rise claimed | All referred |
|---|---|---|---|---|---|
| Off-contract purchases | 337 | 1,477 | 364 | 337 | 0 |
| Off-contract spend | **R51,602,977.01** | **R292,948,564.16** | **R53,185,127.99** | **R51,602,977.01** | **R0.00** |
| Top categories | Electrical and Instrumentation, Bulk Chemicals, Refractory and Linings | Turnaround Support, Scaffolding and Insulation, Rotating Equipment Spares | Electrical and Instrumentation, Bulk Chemicals, Refractory and Linings | Electrical and Instrumentation, Bulk Chemicals, Refractory and Linings | none |
| Notice deadlines passed | 2 | 2 | 2 | 2 | 2 |
| Due within 60 days | 3 | 3 | 3 | 3 | 3 |
| Rate rises outside the terms | 5 | 5 | 5 | 5 | 5 |
| Charged above the terms | R399,787.32 | R399,787.32 | R399,787.32 | R399,787.32 | R399,787.32 |
| Claimed in credit notes | **R329,327.17** | **R329,327.17** | **R329,327.17** | **R399,787.32** | **R0.00** |
| Drafts | 9 | 9 | 9 | 11 | 4 |
| Fingerprint of the approved figures | `3d535a32` | `9f1692a3` | `9df8c7e1` | `2d72beaa` | `77143bd3` |

## Off contract by category (the reference decisions)

| Category | Purchases | Spend |
|---|---|---|
| Electrical and Instrumentation | 36 | R6,548,271.15 |
| Bulk Chemicals | 13 | R4,956,948.47 |
| Refractory and Linings | 18 | R4,562,488.84 |
| Pumps | 18 | R4,534,212.66 |
| Valves and Seals | 24 | R4,394,231.11 |
| Conveyor Maintenance | 19 | R4,370,359.80 |
| Bulk Logistics | 27 | R4,268,971.42 |
| Lifting and Rigging | 20 | R3,994,353.83 |
| Bearings and Drives | 37 | R3,807,851.89 |
| Analytical Services | 29 | R3,616,747.47 |
| Calibration | 49 | R3,181,653.21 |
| Welding Consumables | 46 | R3,141,408.87 |
| Fabrication | 1 | R225,478.29 |

## The renewal calendar (review date 29 Sep 2026, as the answer key was verified)

| Agreement | Category | Period ends | Notice by | Days left | Status |
|---|---|---|---|---|---|
| SAS-2500 | Analytical Services | 10 Nov 2026 | 12 Aug 2026 | -48 | passed |
| SAS-2501 | Bearings and Drives | 7 Dec 2026 | 8 Sep 2026 | -21 | passed |
| SAS-2502 | Bulk Chemicals | 6 Feb 2027 | 9 Oct 2026 | 10 | due within 60 days |
| SAS-2503 | Bulk Logistics | 28 Dec 2026 | 29 Oct 2026 | 30 | due within 60 days |
| SAS-2504 | Calibration | 18 Feb 2027 | 20 Nov 2026 | 52 | due within 60 days |
| SAS-2505 | Conveyor Maintenance | 24 Jul 2027 | 25 Jan 2027 | 118 | later |
| SAS-2506 | Electrical and Instrumentation | 6 Jun 2027 | 8 Mar 2027 | 160 | later |
| SAS-2508 | Lifting and Rigging | 21 Jul 2027 | 22 Apr 2027 | 205 | later |
| SAS-2510 | Pumps | 6 Aug 2027 | 7 Jun 2027 | 251 | later |
| SAS-2511 | Refractory and Linings | 13 Nov 2027 | 16 Jul 2027 | 290 | later |
| SAS-2512 | Valves and Seals | 26 Nov 2027 | 28 Aug 2027 | 333 | later |
| SAS-2513 | Welding Consumables | 23 Dec 2027 | 24 Sep 2027 | 360 | later |

## Rate checks (clause 2.3: the published headline CPI for the second month before the notice)

| Agreement | Supplier | Result | Rise | CPI allowed | Notice | First invoiced at the new rate | Above the terms | Lines | Decision |
|---|---|---|---|---|---|---|---|---|---|
| SAS-2500 | Parys Analytical Labs | Within the terms | 3.3% | 3.5%, July 2025 | 26 Sep 2025, 45 days, Contracts office, supplier portal | 20 Nov 2025 | R0.00 | 0 | – |
| SAS-2501 | Arnot Gearbox Services | Notice outside the terms | 3.2% | 3.3%, August 2025 | 25 Oct 2025, 43 days, Email to a buyer at Secunda | 20 Dec 2025 | R55,098.41 | 13 | Refer it on |
| SAS-2502 | Vaalpark Chemicals | No notice | 3.1% | 3.6%, December 2025 | none | 20 Feb 2026 | R85,510.20 | 9 | Claim a credit note |
| SAS-2503 | Rietkuil Transport | Late notice | 3.2% | 3.6%, October 2025 | 23 Dec 2025, 5 days, Contracts office, supplier portal | 5 Jan 2026 | R15,361.74 | 2 | Accept the rise |
| SAS-2504 | Parys Metrology | Within the terms | 3.4% | 3.5%, November 2025 | 9 Jan 2026, 40 days, Contracts office, supplier portal | 20 Feb 2026 | R0.00 | 0 | – |
| SAS-2505 | Pullenshope Belt Splicing | Fixed rates | 0.0% | – | none | – | R0.00 | 0 | – |
| SAS-2506 | Sandspruit Drives and Automation | Fixed rates | 0.0% | – | none | – | R0.00 | 0 | – |
| SAS-2508 | Leslie Crane Hire | Fixed rates | 0.0% | – | none | – | R0.00 | 0 | – |
| SAS-2510 | Blesbokspruit Pumping Solutions | Fixed rates | 0.0% | – | none | – | R0.00 | 0 | – |
| SAS-2511 | Villiers Refractory Services | Before the anniversary | 3.3% | 3.5%, July 2025 | 1 Sep 2025, 30 days, Contracts office, supplier portal | 5 Oct 2025 | R30,338.32 | 3 | Claim a credit note |
| SAS-2512 | Morgenzon Valve Services | Above CPI | 8.4% | 3.3%, August 2025 | 17 Oct 2025, 40 days, Contracts office, supplier portal | 5 Dec 2025 | R213,478.65 | 14 | Claim a credit note |
| SAS-2513 | Amersfoort Metal Supply | Within the terms | 3.0% | 3.4%, September 2025 | 13 Nov 2025, 40 days, Contracts office, supplier portal | 5 Jan 2026 | R0.00 | 0 | – |

## The drafts (the reference decisions)

- Notice of non-renewal · SAS-2502: Send by 9 Oct 2026
- Notice of non-renewal · SAS-2503: Send by 29 Oct 2026
- Notice of non-renewal · SAS-2504: Send by 20 Nov 2026
- Rate query · SAS-2512 · Morgenzon Valve Services: R213,478.65 to recover
- Rate query · SAS-2502 · Vaalpark Chemicals: R85,510.20 to recover
- Rate query · SAS-2511 · Villiers Refractory Services: R30,338.32 to recover
- Request for the agreement · SAS-2507: Fabrication · quoted by 50 purchases
- Request for the agreement · SAS-2509: PPE and Safety · quoted by 261 purchases
- Referral note: Hotspots: Electrical and Instrumentation, Bulk Chemicals, Refractory and Linings · Referred: SAS-2501

## The analysis (the reference decisions)

Every lever the rules value, and what it's worth over the next 12 months (each change phased in over its first three months; a one-off counted once, in the third). Moving spend onto contract is valued at the review's planning assumption that it costs 5% less. The reference analysis recommends 23 of them: **R2,897,310.60** in all, of which **R649,545.15** is measured (credit notes and paying the agreed rate) and **R2,247,765.45** rests on the 5% assumption, with R217,582,069.86 of annual spend at stake. A live analysis may choose differently; the values of the levers don't change.

| Item | Lever | What it does | Kind | 12 months | Recommended |
|---|---|---|---|---|---|
| Analytical Services (SAS-2500) | `SAS-2500:renegotiate` | Renegotiate the terms before the renewal | risk | R38,405,790.20 at stake, not counted | yes |
| Analytical Services (SAS-2500) | `SAS-2500:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R158,232.69 | yes |
| Bearings and Drives (SAS-2501) | `SAS-2501:renegotiate` | Renegotiate the terms before the renewal | risk | R34,222,355.32 at stake, not counted | yes |
| Bearings and Drives (SAS-2501) | `SAS-2501:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R166,593.52 | yes |
| Bulk Chemicals (SAS-2502) | `SAS-2502:notice` | Renegotiate or give notice by 9 October 2026 | risk | R52,579,051.54 at stake, not counted | yes |
| Bulk Chemicals (SAS-2502) | `SAS-2502:credit` | Claim a credit note for the amount charged above the terms | one-off | R85,510.20 | yes |
| Bulk Chemicals (SAS-2502) | `SAS-2502:hold-rate` | Pay the old rate until a proper notice has run | one-off | R17,102.04 |  |
| Bulk Chemicals (SAS-2502) | `SAS-2502:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R216,866.48 | yes |
| Bulk Logistics (SAS-2503) | `SAS-2503:notice` | Renegotiate or give notice by 29 October 2026 | risk | R37,915,629.01 at stake, not counted | yes |
| Bulk Logistics (SAS-2503) | `SAS-2503:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R186,767.49 | yes |
| Calibration (SAS-2504) | `SAS-2504:notice` | Renegotiate or give notice by 20 November 2026 | risk | R24,328,344.09 at stake, not counted | yes |
| Calibration (SAS-2504) | `SAS-2504:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R139,197.35 | yes |
| Conveyor Maintenance (SAS-2505) | `SAS-2505:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R191,203.22 | yes |
| Electrical and Instrumentation (SAS-2506) | `SAS-2506:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R286,486.83 | yes |
| Lifting and Rigging (SAS-2508) | `SAS-2508:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R174,752.97 | yes |
| Pumps (SAS-2510) | `SAS-2510:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R198,371.77 | yes |
| Refractory and Linings (SAS-2511) | `SAS-2511:credit` | Claim a credit note for the amount charged above the terms | one-off | R30,338.32 | yes |
| Refractory and Linings (SAS-2511) | `SAS-2511:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R199,608.88 | yes |
| Valves and Seals (SAS-2512) | `SAS-2512:credit` | Claim a credit note for the amount charged above the terms | one-off | R213,478.65 | yes |
| Valves and Seals (SAS-2512) | `SAS-2512:hold-rate` | Pay only the rate the agreement allows | recurring | R320,217.98 | yes |
| Valves and Seals (SAS-2512) | `SAS-2512:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R192,247.65 | yes |
| Welding Consumables (SAS-2513) | `SAS-2513:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R137,436.60 | yes |
| Fabrication (SAS-2507, not on file) | `SAS-2507:obtain` | Obtain the signed agreement and check its terms | risk | R14,905,360.34 at stake, not counted | yes |
| Fabrication (SAS-2507, not on file) | `SAS-2507:on-contract` | Buy on the agreement, not off it, at an assumed 5% saving | recurring | R9,864.65 |  |
| PPE and Safety (SAS-2509, not on file) | `SAS-2509:obtain` | Obtain the signed agreement and check its terms | risk | R15,225,539.36 at stake, not counted | yes |

## Input fingerprints (the files in the project folder)

| File | Fingerprint (first 16 characters) |
|---|---|
| SAS-2500 Analytical Services panel agreement.docx | `1eccd573aec22fe4` |
| SAS-2501 Bearings and Drives panel agreement.docx | `65a10d9d6d7f4bd3` |
| SAS-2502 Bulk Chemicals panel agreement.docx | `97148b745628d4f5` |
| SAS-2503 Bulk Logistics panel agreement.docx | `950594f5d697f54b` |
| SAS-2504 Calibration panel agreement.docx | `1d7f1a6f37979e7d` |
| SAS-2505 Conveyor Maintenance panel agreement.docx | `ad24c790b38046c0` |
| SAS-2506 Electrical and Instrumentation panel agreement.docx | `3ac136edaaa1703d` |
| SAS-2508 Lifting and Rigging panel agreement.docx | `c2b8bff9ea0b5493` |
| SAS-2510 Pumps panel agreement.docx | `b0e1652247c867d1` |
| SAS-2511 Refractory and Linings panel agreement.docx | `fdab41a651a43bc0` |
| SAS-2512 Valves and Seals panel agreement.docx | `7e7b432dfc0e4386` |
| SAS-2513 Welding Consumables panel agreement.docx | `29984b9eefd4df18` |
| invoice_lines.xlsx | `32ecebbec48ac89e` |
| spend.xlsx | `0cb26d16a223644d` |

## The controls, as demonstrated in the reference run

- Asking for the card before the agreements are read and checked: *"The agreements haven't been read and checked yet."*
- Asking for the findings before the card is decided: *"This step needs every decision on the card first. Nothing has been calculated."*
- Recording the card with an item left out: *"Every item on the card needs a choice and a reason before any is recorded. Still to decide: SAS-2503 · Rietkuil Transport: late notice."*
- Recording the card in a role that can't make these decisions: *"Only these roles can make this decision: Contracts Manager, Category Manager, Procurement Manager or Commercial Manager. Please choose one of them."*
- Asking for the release before the analysis: *"Fix and run again: write the analysis and run analysis first; it asks for the release."* The analysis is written and checked; the release is asked for with it.
- The analysis quoting a figure that isn't the review's own, recommending another item's lever, or valuing buying on contract without saying it's assumed: *"Fix and run again: …"* It's corrected before anything is shown.
- Publishing before approval: *"Nothing can be released without an approver's decision."* `03 Outputs` and `04 Records` stay empty.
- Thandi Nkosi, who made the decisions, approving the release: *"A different person must approve the release: Thandi Nkosi made a decision in this review, so can't also release it."*
- An approver in a deciding role: *"Only these roles can approve the release: Chief Procurement Officer, Financial Controller, Commercial Director or Chief Financial Officer. Please choose one of them."*
- An approval without the confirmation: *"Please confirm the review before approving: "I have reviewed the findings, the decisions and the recommendations.""*
- The tamper check on the record in `04 Records`: *"Tamper check passed: every entry is intact and in order."* On the altered copy in `tamper-demo/`: *"The record was altered at entry 12."*
