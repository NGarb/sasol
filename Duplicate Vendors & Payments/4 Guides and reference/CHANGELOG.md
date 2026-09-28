# Changelog

All notable changes to this plugin. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow [Semantic Versioning](https://semver.org/).

## [1.10.0] - 2026-09-28

### Changed
- **The approval card starts on a recommendation too.** The analysis now ends with a recommendation for the release (approve or return, a confidence and a reason of one or two sentences, whose figures must be the review's own), and the approval card starts on it, with the reason in the box. The approver keeps it or changes it, and still gives their own full name and role and ticks the confirmation themselves. The request for release records the recommendation, the release records whether the approver followed it and whose reason it gives, and the recommended reason is refused for returning the findings. The audit trail's Approval sheet gains a *Recommendation* column.
- **A shorter line beside the button.** Instead of a paragraph, the card lists only what's still needed, under *Still needed* (*Full name · role · the confirmation*), and says *Ready to send* when nothing is. Each item still says what it lacks under it.
- The project knowledge changed: replace `02-governance-policy.md` in the Claude project.

## [1.9.0] - 2026-09-28

### Added
- **The decision card starts on a recommendation.** The assessment Claude already writes for each pair, citing only its evidence, is now what the card starts on: its recommendation, with the assessment as the reason. The card starts on each recommendation, with its reason in the box, and the person keeps it or changes it, then adds their name and role. Choosing another option clears the recommended reason, since it argues for the option recommended; choosing the recommendation again brings it back.
- **The record keeps the recommendation.** Each recommendation (its option, reason and confidence) is recorded when the decision is requested, before anyone decides, and is part of the fingerprint of what was shown. Each decision records whether it followed the recommendation, and whether the reason is the person's own or the recommended one they kept. The recommended reason is refused for a different option. The audit trail's Decisions sheet gains *Recommended* and *Followed the recommendation*, the evidence pack's gains *Followed the recommendation*, and the dashboard's decisions show what was recommended.
- The approval to release is never pre-filled: the approver's reason is always their own.

### Changed
- **The reason box grows with its text,** so a longer reason can be read in full.
- **The same two stops in every review.** Only a request to prepare a review (*"Prepare a new review."*) pauses before starting; any other opening, such as *"Go"*, runs straight to the decisions. After that the review stops only for the decisions and for approval to release.
- **Showing the card.** Claude shows it with `show_widget`, called by the exact name the tool list gives it, reading its guide first if asked. It uses no other display tool, never to try one out, and never with placeholder content: the first thing shown is the card itself.
- The project knowledge changed: replace `02-governance-policy.md` in the Claude project.

## [1.8.1] - 2026-09-27

### Changed
- Version only, to confirm the Claude app picks up a release on its own after a push. Nothing else changes.

## [1.8.0] - 2026-09-27

### Removed
- **Obsidian.** A release no longer files a review note (`Review <number>.md`) or a review map (`.canvas`), and the folder no longer has a register (`00 Reviews.base`); the installer no longer adds a home page, a register or vault settings above the use-case folders. Each review's folder in `03 Outputs` holds only `Report`, `Evidence` and `Actions`, and `04 Records` the record.
- **The line about the last review.** It read the last review's note, so it goes with it: every review starts afresh. Questions about an earlier review are answered from its one-page summary, and its record in `04 Records` remains the evidence.

## [1.7.2] - 2026-09-27

### Fixed
- **Tables fit, with columns sized to their content.** Every table on the dashboard and in the filed report now shares one set of columns across its rows, sized to what's in them: a column's width is the most it takes, numbers stay on one line, and the text columns share the rest. No column is squeezed into a sliver, runs off the table or lands on the side panel, and the rows line up.
- The design audit checks every table at the narrowest layout, 1,280 pixels wide (a narrower panel scales the page down): none wider than its space, no column off its edge, no text squeezed into a sliver.
- **The decision card, in any chat.** Claude looks for the tool that shows the card, loading it first if it has to, before concluding there's none; if there's truly none, it asks in the chat without saying a card can't be shown.

## [1.7.1] - 2026-09-27

### Fixed
- **The decision card says what's missing.** A decision counts only with a choice and a reason of three words or more, and the card now says so: under each item that's been started ("Give a reason of three words or more.", "Choose an option."), in the reason box, and in the line beside the button. It asks for a first name and surname when only one name is typed. The rule itself is unchanged.

## [1.7.0] - 2026-09-27

### Changed
- **Nothing Claude reads knows what the folder holds.** The project instructions, the knowledge files, the skill and its references no longer name any supplier, agreement, ID, count, total, site or period from the files in the folder, and their examples are made up. The review works on whatever files are in the folder, and every name, count and figure Claude gives comes from those files and the review's own results.
- The project instructions say so: never assume what the folder contains, how many files there are, the period or sites they cover, or what the review will find. The voice guide's examples are patterns, with the review's own results in braces.
- The management pack's scope and basis are worked out from the data (the sites, and the period the spend history covers) instead of a fixed description of one set of files, and no longer say the orders are under R1 million.
- A check fails the build if anything Claude reads names a supplier, reference, ID, site, city or period, or in prose a row count or total, from the sample files in the folder template.

## [1.6.1] - 2026-09-26

### Changed
- Version aligned with the other two reviews, so all three read 1.6.1. The presentation fixes that Early Payment Detection 1.6.1 lists were already in 1.6.0 here. Nothing else changes.

## [1.6.0] - 2026-09-26

### Added
- **Named sign-off in realistic roles.** Every decision records the person's full name and a role from this review's delegation of authority: Vendor Master Data Manager, Creditors Manager, Procurement Manager or Supplier Risk Manager. The release is approved by a different person, in a senior role (Financial Controller, Head of Internal Control, Chief Risk Officer or Chief Financial Officer), who confirms they reviewed the findings, the decisions and the recommendations. Anyone who decided, by name, or any deciding role, is refused.
- **Eight pairs on one decision card.** Five more likely duplicates join the three, with a realistic mix of evidence: the same tax number and bank account; a trading name against a registered name; a dormant duplicate of a blocked record; a close corporation that became a company; a group paid through one treasury account; a tax number captured on the wrong record; and a blocked supplier's bank account on a new supplier. Each item carries a one-line summary of its evidence, the card is recorded whole or not at all (`decide --name --role --file`), and the rail reads *8 pairs need a decision*.
- **Orders for the same amount are evidence before the decision.** Every pair in the queue is checked for an order on each record for the same amount within 30 days, shown on the card and on the pair's page before anyone decides.
- **Possible duplicates.** A match on a pair referred on, or decided as different suppliers, is listed with its status (for example *pending forensic review*) and never counted as paid twice. The review never says R0 or "nothing was paid twice" while one is open.
- **The full release, filed at once:** the dashboard report (with its Data and Audit pages and Excel downloads), a management briefing and a presentation in the Sasol Design System, the one-page summary, the evidence pack, the audit trail, the data and the review's own drafts, in `03 Outputs/<review>/Report`, `Evidence` and `Actions`. The record ends with a fingerprint of every file released.
- **Data and Audit tabs** on the dashboard, and questions to ask on every page, written from its own figures.
- **Draft recovery letters on the letterhead**, one per supplier paid twice, asking for the amount excluding VAT and the VAT charged on it.

### Changed
- **More realistic data**, shared with the contract-leakage review: 1,950 supplier records, about half with orders in the year; 7.5% blocked, each with the date, and none with an order; 5,000 orders under R1 million worth R812.1 million; Secunda 71% of spend; the top fifth of suppliers holding three quarters of it; every supplier's name matching its category; a payment date on every paid order; supplier numbers in the order records were created.
- **Paid twice** now needs both orders paid: R819,781.80 on three pairs in the presenter script's decisions (Grootpan, Leeuwpan and Komati).
- **A shared bank account is never simply recorded as distinct.** For a pair sharing a bank account under different tax numbers, the option is *Different suppliers · bank details verified*, and its recommendation keeps the confirmation on both records. New levers value what each decision leaves at stake: confirming a registration, holding a possible duplicate, checking matching orders. Where a decision differs from the assessment, the analysis says so.
- **The evidence pack and the change request name both records of every pair**, with every order on the queued pairs and a header row on every sheet; the change request shows who decided and who approved, by name and role. The evidence pack's record uses plain step names and South African time.
- **The record fingerprints what each step produced** (the scored pairs, the evidence, the assessment and the findings), not just their counts.
- **Neutral wording everywhere:** "the analysis", "the assessment" and "Analysis and recommendations"; nothing on a screen or in a file is attributed to Claude.
- With nothing to gain, the review says "No gain is projected: these actions protect R… at stake", and mentions the recovery letters only when there are some.
- The management pack is filed with the release instead of being offered afterwards.
- Recommendations shows what's gained over 12 months and what's at stake in separate columns; a page shows a chart only when it has something to compare, and a single chart spans the page.

### Fixed
- Look-alike names read as people type them, never as generated ("Heat Exchangerss").
- No two orders share an amount unless they were paid twice, so nothing looks like a missed duplicate.
- A blocked record's story is coherent: it says when it was blocked, and it has no orders after it.

## [1.5.1] - 2026-09-26

### Fixed
- **The decision and release cards look the same in every chat.** A chat shows each card inside its own page, which styles headings, buttons and form fields for its own light or dark theme: in a dark chat the card's question turned grey and its buttons took the chat's look. The card now draws inside a shadow root, which the chat's styles can't reach. *Record decision ›* stays white with a grey outline until a choice, a reason and a role are given, then turns navy.

## [1.5.0] - 2026-09-26

### Added
- **Every review records its version.** The version of the review that ran it is in the record's first entry, on the dashboard's *This review* panel, in the management-pack briefing and in the review note's properties, so the evidence always says what produced it and a new chat shows which version it runs.

## [1.4.0] - 2026-09-26

### Added
- **Claude's analysis.** After the findings, Claude analyses every pair in the review queue and recommends what to act on, with an owner. The review's own rules value each recommendation:
  - recovering a payment made twice (one-off, counted in the third month);
  - merging the two records, at the pace duplicates were paid over the period reviewed, phased in over three months;
  - verifying a shared bank account (the spend at stake, never counted as a gain).

  The review accepts the analysis only when every figure in it is one of its own. It is recorded as Claude's, and the second person approves it with the findings.
- On the dashboard:
  - Claude's analysis and the recommended actions on every pair's page and on its payments;
  - a 12-month projection of what's lost if nothing changes against what the changes save;
  - a Projected gain card and *What to do first* on the overview;
  - a Recommendations tab, with a what-if for the share of the change achieved. It shows what's at stake instead when nothing has a rand value.
- In the files:
  - a Recommendations sheet in the evidence pack;
  - the recommended actions in the one-page summary;
  - Claude's analysis in the review note;
  - the recommendations in the management pack. The recovery request and the forensic referral stay listed whenever they aren't recommended.
- **A dashboard report with every release.** Publishing files `Dashboard report <review>.html` into `03 Outputs` with the other files: the completed dashboard, every page, with the released figures and the logo, to open in any browser. The review note links it.

### Changed
- The findings step no longer asks for the release: the analysis step does, once Claude's analysis passes the check. The release card asks to release the findings and recommendations.
- Each dashboard update sends only what changed, so the updates after the findings are far smaller. The dashboard budget is 56 KiB.

### Fixed
- The briefing says "1 pair was confirmed", not "1 pairs were confirmed".
- The management-pack briefing lists every released file (it listed none before).
- The menu fits seven or more tabs in the 1280px layout the side panel scales to, hiding the keys hint when space is short.
- The projection counts a one-off that isn't recovered as lost in the same month, so the saved line never rises above it, and its curve never overshoots.

## [1.3.2] - 2026-09-26

### Fixed
- The dashboard shows Sasol's logo at the top left again. The chat's artifacts can't load images from other sites, so the logo is now embedded in the page (a 2 KB image), and the dashboard's size budget is 48 KiB.
- The review note and its map say "approved by Operations", not "approved by the Operations".

## [1.3.1] - 2026-09-26

### Fixed
- The decision and release cards: shown with the conversation's inline-visual tool when it has one. Without one, Claude never pastes the card's code: it asks for the choice, the reason and the role in one reply. Found in the live test.

## [1.3.0] - 2026-09-26

### Changed
- Claude speaks as the live system: nothing it reads or says calls the review a demonstration, a demo or a test, mentions an event, or calls the data invented. It never says the files are Sasol's own records, and says plainly that they aren't if asked.
- The first knowledge file is now `01-about-this-review.md` (it was `01-about-this-demo.md`), and the working-context file no longer describes an event.
- The checks enforce it: what Claude reads, and what the reference run has Claude say, fail on that wording.

## [1.2.0] - 2026-09-26

### Added
- The register, for Obsidian: each release also files the review's note (properties, the answer, the decisions, the actions, how AI helped, and links to every file, with the summary embedded) and a map of the review (JSON Canvas) in its folder in `03 Outputs`.
- `00 Reviews.base` in the folder, and a client-wide `Reviews.base` and `Home.md` above it, installed by `tools/install_folder.py` with the vault's starting settings.
- Memory without chat memory: `start` reports the last review whose record passes the tamper check, and Claude mentions it in one sentence. Questions about earlier reviews are answered from their notes.

## [1.1.0] - 2026-09-26

### Fixed
- Working from a copy of the project folder: the results are never filed into the copy, and Claude is told exactly what to save where in the real folder (`start --copy`).
- Filing only ever writes into a complete standard folder, and the working space moves out of the skill's folder or a read-only one.
- Messages about Claude's own reading or assessment start "Fix and run again" and never crash, so a slip is corrected quietly instead of read out.
- The supplier pair is quoted in the decision step, so a shell can't split it at the `|`.
- An answer ready for "is this fraud?", and the Candidates pointer moved to the decisions, when the dashboard has the candidates.

### Changed
- The skill: clearer triggers ("prepare a new review" in this project), a working folder outside the project and skill folders, carrying straight on between steps, a safe dashboard refresh, a fresh review in a new chat, and the second approver's reason and role.
- The project instructions name the skill, and use this review's own answer to "How does this work?" and its own kinds of money.
- The management-pack briefing carries this review's own Assist · Augment · Automate wording (`ai_help`), and the decisions are plural.
- The plugin's description no longer repeats its name.

## [1.0.0] - 2026-09-26

### Added
- The duplicate-supplier review as a Claude plugin, `sasol-duplicate-vendors`, listed in the Sasol Plugin Catalogue under Procure to Pay.
- Reading from and filing to the project folder in the standard structure (`01 Documents`, `02 Data`, `03 Outputs`, `04 Records`), with a fallback when the folder can't be written.
- The management pack: a two-page briefing and a six-slide presentation in the Sasol Design System, made only from the review's own figures.
- The Claude project's instructions and knowledge, the folder template, the presenter script, the UAT checklist and a full reference run.
