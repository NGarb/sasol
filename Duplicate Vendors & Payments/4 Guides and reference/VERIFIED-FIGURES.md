# Verified figures: Duplicate Vendors & Payments

Every figure below came from running the review from a copy of the project folder, and was checked against the generator's own answer key (`tests/fixtures/truth.json`). Your run should show exactly these. Review numbers, times and the record's entry fingerprints differ on every run; **the figures, the fingerprint of the approved figures and the input fingerprints don't.**

## Before the decisions

- Supplier records: **1,950** (1,803 active, 147 blocked, none of them with an order in the year)
- Purchase orders: **5,000** worth **R812,094,562.35** (excluding VAT), Jul 2025 to Jun 2026, every one under R1 million
- Plausible pairs compared: **31,928**; pairs scoring 0.10 or more: **22**; in the review queue at the 0.35 policy line: **8**

| Pair | Shares | Match | On the card |
|---|---|---|---|
| Grootpan Vacuum Services / Grootpan Vacuum Services (Pty) Ltd | tax number and bank account | 1.00 (queued) | Same tax number and bank account · names 100% alike · R1.8 million combined spend · R138,915.60 ordered on both, 9 days apart |
| Kinross Crane Hire / Kinross Crane Hire CC | tax number | 0.65 (queued) | Same tax number, different bank accounts · names 100% alike · Kinross Crane Hire blocked on 16 Sep 2024 · R2.6 million combined spend |
| Trichardt Welding Supply / Trichardt Welding Supplies | bank account and name and city | 0.54 (queued) | Same bank account and town, different tax numbers · names 92% alike · R1.1 million combined spend |
| Leeuwpan Refractory Services / Leeuwpan Industrial Holdings | tax number | 0.50 (queued) | Same tax number, different bank accounts · names 47% alike · R3.3 million combined spend · R193,516.20 ordered on both, 14 days apart |
| Delmas Instrument Calibration / Vaalbank Bulk Chemicals | tax number | 0.45 (queued) | Same tax number, different bank accounts · names 23% alike · R3.5 million combined spend |
| Bethal Pump Works / Bethal Valve and Seal | bank account and city | 0.40 (queued) | Same bank account and town, different tax numbers · names 47% alike · R5.5 million combined spend |
| Komati Motor Rewinds / Komati Group | bank account and city | 0.40 (queued) | Same bank account and town, different tax numbers · names 50% alike · R2.2 million combined spend · R487,350.00 ordered on both, 2 days apart |
| Mafube Access Solutions / Rietspruit Hydraulics | bank account only | 0.35 (queued) | Same bank account, different tax numbers · names 18% alike · Mafube Access Solutions blocked on 14 Mar 2025 · R557,000 combined spend |
| Lothair Lining / Lothair Linings | similar names only | 0.19 |  |
| Pullenshope Motor Rewinding / Pullenshope Motor Rewinds | similar names only | 0.19 |  |
| Doornkop Transport / Doornkop Transporters | similar names only | 0.19 |  |
| Goedehoop Seals / Goedehoop Seal | similar names only | 0.19 |  |
| Ermelo Compressors / Ermelo Compressor | similar names only | 0.15 |  |
| Rooikoppies Pumping Solution / Rooikoppies Pumping Solutions | similar names only | 0.15 |  |
| Koppies Pumping Solution / Koppies Pumping Solutions | similar names only | 0.15 |  |
| Morgenzon Lifting Services / Morgenzon Lifting Service | similar names only | 0.15 |  |
| Breyten Bearing / Breyten Bearings | similar names only | 0.15 |  |
| Meyerton Valve Service / Meyerton Valve Services | similar names only | 0.15 |  |
| Ogies Process Chemical / Ogies Process Chemicals | similar names only | 0.15 |  |
| Lothair Electrical Engineering / Lothair Electrical Engineers | similar names only | 0.14 |  |
| Bronkhorstspruit Motor Rewinds / Bronkhorstspruit Motor Rewinding | similar names only | 0.14 |  |
| Rooikoppies Safety Supply / Rooikoppies Safety Supplies | similar names only | 0.14 |  |

## The review line (the what-if on Candidates)

| Line | Reviews needed | Would go unreviewed | Look-alikes queued |
|---|---|---|---|
| 0.10 | 22 | 0 | 14 |
| 0.20 | 8 | 0 | 0 |
| 0.35 | 8 | 0 | 0 |
| 0.36 | 7 | 1 | 0 |
| 0.41 | 5 | 3 | 0 |
| 0.46 | 4 | 4 | 0 |
| 0.51 | 3 | 5 | 0 |
| 0.55 | 2 | 6 | 0 |
| 0.66 | 1 | 7 | 0 |
| 0.90 | 1 | 7 | 0 |

## After the decisions

| Decisions | Paid twice | Payments | Possible duplicates | Fingerprint of the approved figures |
|---|---|---|---|---|
| The presenter script: Grootpan, Kinross, Leeuwpan and Komati the same; Trichardt and Mafube / Rietspruit referred; Delmas / Vaalbank and Bethal different | **R819,781.80** | 3 pairs of orders | none | `ad8901e4` |
| As the presenter script, but Komati referred | **R332,431.80** | 2 pairs of orders | R487,350.00 (pending forensic review) | `6b65c05e` |
| As the presenter script, but Komati different suppliers (bank details verified) | **R332,431.80** | 2 pairs of orders | R487,350.00 (decided as different suppliers) | `333d61ad` |
| As the presenter script, but Mafube / Rietspruit different suppliers (bank details verified) | **R819,781.80** | 3 pairs of orders | none | `9a0a2bb7` |

Paid twice, in the presenter script's decisions (each order paid; found only because a person confirmed the pair):

- **R138,915.60**: PO-702936 (2025-11-11, paid 2025-12-23) and PO-703173 (2025-11-20, paid 2026-02-03), 9 days apart: Grootpan Vacuum Services / Grootpan Vacuum Services (Pty) Ltd
- **R193,516.20**: PO-704067 (2026-01-20, paid 2026-03-24) and PO-704425 (2026-02-03, paid 2026-04-07), 14 days apart: Leeuwpan Refractory Services / Leeuwpan Industrial Holdings
- **R487,350.00**: PO-705272 (2026-03-09, paid 2026-05-05) and PO-705364 (2026-03-11, paid 2026-05-22), 2 days apart: Komati Motor Rewinds / Komati Group

## The analysis (the presenter script's decisions)

Every lever the rules value, and what it's worth over the next 12 months (a recovery counted once, in the third month; a recurring change phased in over its first three months; an amount at stake shown, never counted). The reference analysis recommends 11 of them: **R1,537,090.88** in all, with R9,781,892.69 at stake. A live analysis may choose differently; the values of the levers don't change.

| Pair | Lever | What it does | Kind | 12 months | Recommended |
|---|---|---|---|---|---|
| Komati Motor Rewinds / Komati Group | `recover` | Recover the amount paid twice | one-off | R487,350.00 | yes |
| Komati Motor Rewinds / Komati Group | `merge` | Merge the two records into one | recurring | R426,431.25 | yes |
| Leeuwpan Refractory Services / Leeuwpan Industrial Holdings | `recover` | Recover the amount paid twice | one-off | R193,516.20 | yes |
| Leeuwpan Refractory Services / Leeuwpan Industrial Holdings | `merge` | Merge the two records into one | recurring | R169,326.68 | yes |
| Grootpan Vacuum Services / Grootpan Vacuum Services (Pty) Ltd | `recover` | Recover the amount paid twice | one-off | R138,915.60 | yes |
| Grootpan Vacuum Services / Grootpan Vacuum Services (Pty) Ltd | `merge` | Merge the two records into one | recurring | R121,551.15 | yes |
| Bethal Pump Works / Bethal Valve and Seal | `keep-proof` | Keep the bank confirmation on both records | risk | R5,517,190.75 at stake | yes |
| Kinross Crane Hire / Kinross Crane Hire CC | `merge` | Merge the two records into one | risk | R2,593,324.49 at stake | yes |
| Trichardt Welding Supply / Trichardt Welding Supplies | `verify-bank` | Confirm each supplier's bank details before paying either again | risk | R1,114,467.97 at stake | yes |
| Mafube Access Solutions / Rietspruit Hydraulics | `verify-bank` | Confirm each supplier's bank details before paying either again | risk | R556,909.48 at stake | yes |
| Delmas Instrument Calibration / Vaalbank Bulk Chemicals | `mark-distinct` | Record that the two are different suppliers | risk | not valued | yes |

Decided differently, a pair offers other levers (the other pairs' don't change):

- As the presenter script, but Komati referred: `verify-bank` (confirm each supplier's bank details before paying either again), R2,168,188.45 at stake; `hold` (hold the possible duplicate for the forensic review), R487,350.00 at stake
- As the presenter script, but Komati different suppliers (bank details verified): `keep-proof` (keep the bank confirmation on both records), R2,168,188.45 at stake; `check-orders` (confirm the orders for the same amount were separate work), R487,350.00 at stake
- As the presenter script, but Mafube / Rietspruit different suppliers (bank details verified): `keep-proof` (keep the bank confirmation on both records), R556,909.48 at stake

## Input fingerprints (the files in the project folder)

| File | Fingerprint (first 16 characters) |
|---|---|
| spend.xlsx | `0cb26d16a223644d` |
| vendor_master.xlsx | `145584d457747d26` |

## The controls, as demonstrated in the reference run

- Counting before every pair is decided: *"This step needs a decision first. Nothing has been calculated."*
- Deciding in a role the delegation of authority doesn't allow, or with a first name only: refused, and **nothing** on the card is recorded.
- Asking for the release before the analysis, or publishing before approval: refused. `03 Outputs` and `04 Records` stay empty.
- Thandi Nkosi, who decided the pairs, approving the release: *"A different person must approve the release: Thandi Nkosi made a decision in this review, so can't also release it."*
- Lerato Mokoena approving as a Procurement Manager (a deciding role): *"Only these roles can approve the release: Financial Controller, Head of Internal Control, Chief Risk Officer or Chief Financial Officer. Please choose one of them."*
- Approving without confirming the review: *"Please confirm the review before approving: \"I have reviewed the findings, the decisions and the recommendations.\""*
- The analysis quoting a figure that isn't the review's own, or recommending another pair's lever: *"Fix and run again: …"*, corrected before anything is shown.
- The tamper check on the record in `04 Records`: *"Tamper check passed: every entry is intact and in order."* On the altered copy in `tamper-demo/`: *"The record was altered at entry 13."*
- The record's last entry fingerprints every released file, so a file changed after the release shows against it.
