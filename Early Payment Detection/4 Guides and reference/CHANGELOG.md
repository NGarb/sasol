# Changelog

All notable changes to this plugin. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow [Semantic Versioning](https://semver.org/).

## [1.10.0] - 2026-09-28

### Changed
- **The approval card starts on a recommendation too.** The analysis now ends with a recommendation for the release (approve or return, a confidence and a reason of one or two sentences, whose figures must be the review's own), and the approval card starts on it, with the reason in the box. The approver keeps it or changes it, and still gives their own full name and role and ticks the confirmation themselves. The request for release records the recommendation, the release records whether the approver followed it and whose reason it gives, and the recommended reason is refused for returning the findings. The audit trail's Approval sheet gains a *Recommendation* column.
- **A shorter line beside the button.** Instead of a paragraph, the card lists only what's still needed, under *Still needed* (*Full name · role · the confirmation*), and says *Ready to send* when nothing is. Each item still says what it lacks under it.
- The project knowledge changed: replace `02-governance-policy.md` in the Claude project.

## [1.9.0] - 2026-09-28

### Added
- **The decision card starts on a recommendation.** Before the card is shown, Claude recommends a reading for each agreement from its own clauses, with a confidence and a reason (`references/assessment-guide.md`): `gate` now prints the agreements for that assessment, and `gate --assessment assessment.json` gives the card. The card starts on each recommendation, with its reason in the box, and the person keeps it or changes it, then adds their name and role. Choosing another option clears the recommended reason, since it argues for the option recommended; choosing the recommendation again brings it back.
- **The record keeps the recommendation.** Each recommendation (its option, reason and confidence) is recorded when the decision is requested, before anyone decides, and is part of the fingerprint of what was shown. Each decision records whether it followed the recommendation, and whether the reason is the person's own or the recommended one they kept. The recommended reason is refused for a different option. The audit trail's Decisions sheet gains *Recommended* and *Followed the recommendation*, the evidence pack's gains *Followed the recommendation*, and the dashboard's decisions show what was recommended.
- The approval to release is never pre-filled: the approver's reason is always their own.

### Changed
- **The reason box grows with its text,** so a longer reason can be read in full.
- **The same two stops in every review.** Only a request to prepare a review (*"Prepare a new review."*) pauses before starting; any other opening, such as *"Go"*, runs straight to the decisions. After that the review stops only for the decisions and for approval to release.
- **Showing the card.** Claude shows it with `show_widget`, called by the exact name the tool list gives it, reading its guide first if asked. It uses no other display tool, never to try one out, and never with placeholder content: the first thing shown is the card itself.
- The project knowledge changed: replace `02-governance-policy.md` and `01-about-this-review.md` in the Claude project.

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
- The reading guide, the rules, the data dictionary and the glossary describe each term by what an agreement says, not by one set of agreements' clause numbers and layout: agreements are numbered and laid out in their own ways.
- The management pack's scope and basis name the sites and the period from the data, instead of a fixed description of the work the payments were for.
- A check fails the build if anything Claude reads names a supplier, reference, ID, site, city or period, or in prose a row count or total, from the sample files in the folder template.

## [1.6.1] - 2026-09-26

### Changed
- The presentation's decisions slide fits any number of decisions: one person's name is given once, as many decisions as fit are shown, and a line says how many more there are and where they're recorded.
- The Assist · Augment · Automate tiles show whole sentences, never a sentence cut mid-list.
- The projection's two end values sit above and below their lines, so they never overlap.
- Scorecard labels are three words or fewer ("Projected gain", "Discounts taken").

## [1.6.0] - 2026-09-26

### Added
- **Seven decisions on one card.** Seven of the twelve agreements can each be read two ways, and the review stops for all of them together: an annexure that prevails (SAS-2412), words and figures that disagree ("45 (thirty) days"), an annexure only the supplier signed, a side letter that widens the discount window, 60 days counted "from statement", an agreement that ended while payments continued, and a qualifying small enterprise the purchaser aims to pay within 15 days (enterprise and supplier development). Each item shows what each reading means for that agreement's payments, early and late, with the dates that matter, and always offers *Refer it on*. The card is recorded whole or not at all.
- **Named sign-off.** Every decision records the person's full name and a role allowed to decide agreement terms (Contracts Manager, Category Manager, Procurement Manager, Legal Counsel). The release needs a different person, named, in a release role (Financial Controller, Group Treasurer, Financial Manager, Chief Financial Officer), who confirms they reviewed the findings, the decisions and the recommendations.
- **The full release pack, filed as files.** Publishing files the dashboard report, a management briefing (Word) and a presentation (PowerPoint), the one-page summary, the evidence pack, an audit trail and the data, in `Report` and `Evidence` folders, with the review note and map, and the record ends with a fingerprint of every file released.
- **Data and Audit pages.** The report shows every payment as read, every agreement term, every payment's outcome against its terms and the decisions applied, row by row, with downloads to Excel, and the full audit trail.
- **On time**, as an outcome: each payment reviewed is taken with its discount, paid early, on time or paid late, so the outcomes add up to the payments reviewed. Discounts not taken are counted alongside.
- **Ask about this:** questions written from each page's own figures, to copy into the chat.
- A decision page that goes against the clause that settles it (an annexure clause 5.1 says prevails, an annexure clause 5.2 says isn't effective unsigned, terms clause 4.2 replaces) says so plainly.

### Changed
- **Realistic scale:** 679 invoices worth R320.0 million across the 12 agreements, with Vaalkop Industrial Services and Komati Conveyor Maintenance the largest; 30, 45, 60 and 90-day terms; discounts on two agreements only; five agreements with no finding at all. Figures cover only the agreements and invoices in the review and say so.
- **The rate for paying early** is the Treasury's short-term funding rate, 9.5%, not a cost of capital.
- **Late means more than five days late**, the same tolerance as early, because days are counted from the invoice date while the agreements count from receipt. The Paid late page shows how late.
- **The on-time lever** is offered only where late payments are material, so the recommendations don't repeat it for every supplier.
- Quotes are whole clauses. After a decision, the agreements, their terms and the Contracts table show the outcome with the name, role and time, never "Needs a decision" or "Confirmed" for a clause that reads two ways.
- The record fingerprints what was read and what the comparison found, not just the counts; the analysis is recorded as a step of the review. Times in the files are South African time.
- Charts: a key on every chart with more than one series, each supplier's payments against its own terms, and no empty or hard-coded bars.
- The one-page summary lists every decision with its person, and "the top 5 of" the recommended actions.

### Removed
- The management-pack offer after the release: the pack is filed with it.
- "Claude's analysis", "Claude read" and every other attribution, on every screen and in every file.

## [1.5.1] - 2026-09-26

### Fixed
- **The decision and release cards look the same in every chat.** A chat shows each card inside its own page, which styles headings, buttons and form fields for its own light or dark theme: in a dark chat the card's question turned grey and its buttons took the chat's look. The card now draws inside a shadow root, which the chat's styles can't reach. *Record decision ›* stays white with a grey outline until a choice, a reason and a role are given, then turns navy.

## [1.5.0] - 2026-09-26

### Added
- **Every review records its version.** The version of the review that ran it is in the record's first entry, on the dashboard's *This review* panel, in the management-pack briefing and in the review note's properties, so the evidence always says what produced it and a new chat shows which version it runs.

## [1.4.0] - 2026-09-26

### Added
- **Claude's analysis.** After the findings, Claude analyses every supplier and recommends what to act on, with an owner. The review's own rules value each recommendation over the next 12 months, with each change phased in over three months. The levers are paying on the due date, taking a discount net of the cost of paying sooner, and paying on time. The review accepts the analysis only when every figure in it is one of its own. It is recorded as Claude's, and the second person approves it with the findings.
- On the dashboard:
  - Claude's analysis and the recommended actions on every supplier page;
  - a 12-month projection of what's lost if nothing changes against what the changes save;
  - a Projected gain card and *What to do first* on the overview;
  - a Recommendations tab, with a what-if for the share of the change achieved.
- In the files:
  - a Recommendations sheet in the evidence pack;
  - the recommended actions in the one-page summary;
  - Claude's analysis in the review note;
  - the recommendations in the management pack.
- **A dashboard report with every release.** Publishing files `Dashboard report <review>.html` into `03 Outputs` with the other files: the completed dashboard, every page, with the released figures and the logo, to open in any browser. The review note links it.

### Changed
- The findings step no longer asks for the release: the analysis step does, once Claude's analysis passes the check. The release card asks to release the findings and recommendations.
- Each dashboard update sends only what changed, so the updates after the findings are about a third of their old size. The dashboard budget is 56 KiB.

### Fixed
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

### Changed
- The skill: clearer triggers ("prepare a new review" in this project), a working folder outside the project and skill folders, carrying straight on between steps, a safe dashboard refresh, a fresh review in a new chat, and the second approver's reason and role.
- The project instructions name the skill, and use this review's own answer to "How does this work?" and its own kinds of money.
- The management-pack briefing carries this review's own Assist · Augment · Automate wording (`ai_help`), and the decisions are plural.
- The plugin's description no longer repeats its name.

## [1.0.0] - 2026-09-26

### Added
- The early-payment review as a Claude plugin, `sasol-early-payment`, listed in the Sasol Plugin Catalogue under Procure to Pay.
- Reading from and filing to the project folder in the standard structure (`01 Documents`, `02 Data`, `03 Outputs`, `04 Records`), with a fallback when the folder can't be written.
- The management pack: a two-page briefing and a six-slide presentation in the Sasol Design System, made only from the review's own figures.
- The Claude project's instructions and knowledge, the folder template, the presenter script, the UAT checklist and a full reference run.
