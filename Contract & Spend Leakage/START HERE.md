# Contract & Spend Leakage: setting it up

It answers one question: *are we buying through our contracts, and are their terms being honoured?* Claude reads the panel agreements, confirmed by an independent check, and fixed rules check every invoice line against the agreements' rate terms. Before anything is counted, a person decides, on one card, what counts as off-contract spend, whether to rely on the contract register for agreements not in the folder, and whether to claim each rate rise outside its terms. Fixed rules then find the agreements renewing automatically and value what to act on. A second person, in a senior role, approves the release. Nothing is sent: every letter is a draft for a person to review and send.

This package is version **1.10.0** (28 September 2026). It holds everything a new user needs to set up the review in their own Claude account, with no GitHub access needed: the plugin to upload, the project's instructions and knowledge, the project folder with its files, the guides, and the figures a correct run produces.

## What's in the package

| Folder | What it is | What you do with it |
|---|---|---|
| `1 Claude project` | `instructions.md` and the five files in `knowledge` | Paste and add them to the Claude project (step 3) |
| `2 Project folder` | The folder the review works from: `00 Read me.md`, `01 Documents` (the panel agreements (word)), `02 Data` (the spend history and the invoice lines (excel)), and empty `03 Outputs` and `04 Records` | Copy it to your OneDrive or another local folder (step 2) |
| `3 Plugin to upload` | `sasol-contract-leakage 1.10.0.zip`: the plugin, and in `Skill only` the same review as a single skill | Upload the plugin in the Claude app (step 1) |
| `4 Guides and reference` | How to present it, the test checklist, how to handle the data, and the reference run's figures, transcript and screens | Read before the first run; compare your first run with it |

## What you need

- **The Claude desktop app** (Mac or Windows), on a plan with Projects, signed in to your own account. The review works from a folder on your computer, which only the desktop app can open.
- In **Settings**: **Code execution and file creation** on, and **Artifacts** on. For a demonstration, pause **Memory**, so nothing carries from one chat to the next.
- Only for the catalogue route in step 1 (not needed to upload the plugin): **a GitHub account in the Intellinexus organisation**, with at least read access to the private repository `Intellinexus/sasol-plugin-catalogue`.
- About 20 minutes for the first use case, and 10 for each of the others.

## 1. The plugin

Choose one way, and use only that one: two copies of the same plugin would compete.

**Upload it (no GitHub needed).**
1. In the Claude app, open **Customize → Plugins**, select **Add**, then **Upload plugin**, and choose `3 Plugin to upload/sasol-contract-leakage 1.10.0.zip`. Leave the zip as it is: don't unzip it first.
2. Claude reminds you to install only plugins you trust: this one is Intellinexus's own. Check that **Contract & Spend Leakage** is listed and switched on.
3. An uploaded plugin is added on this computer only, and it doesn't update itself. For a new release, remove this one (open it, then its menu, then **Remove**) and upload the plugin from the new package.
4. If **Upload plugin** isn't offered (an organisation can switch it off), upload `3 Plugin to upload/Skill only/contract-leakage-review.zip` instead, under **Customize → Skills**: the same review, as a skill.

**Or install it from the catalogue (keeps itself up to date; needs GitHub).**
1. Open **Customize → Plugins → Add marketplace**, and enter `Intellinexus/sasol-plugin-catalogue`. When Claude asks, connect GitHub and sign in as your own GitHub user, with access to that repository. If GitHub says it can't see it, an organisation owner adds `sasol-plugin-catalogue` to the Claude GitHub App: on GitHub, **Intellinexus → Settings → GitHub Apps → Claude → Configure → Repository access**.
2. From the **Sasol Plugin Catalogue**, under *Procure to Pay*, install **Contract & Spend Leakage** (`sasol-contract-leakage`).
3. In **Manage marketplaces**, open the catalogue's menu (⋮) and turn on **Sync automatically**: each release then arrives by itself within about an hour.

Either way, check: in a new chat in the project (step 3), the dashboard's *This review* panel shows **Version 1.10.0**. If you also use Claude Code, don't install the plugin there as well.

## 2. The project folder

1. Copy `2 Project folder/Contract & Spend Leakage` to where the project will read it. In OneDrive, use `Jumpstarts/Sasol/Contract & Spend Leakage`, so the released files reach SharePoint and the team. Keep the folder names exactly as they are.
2. On a Mac with OneDrive, right-click the folder in Finder and choose **Always Keep on This Device**, so no file is ever online-only.
3. For a fresh run later, move everything inside `03 Outputs` and `04 Records` to the Trash, or copy the package's folder again. Never change `01 Documents` or `02 Data`.

## 3. The Claude project

1. Create a project named **Sasol - Contract & Spend Leakage**.
2. **Instructions:** paste the whole of `1 Claude project/instructions.md`.
3. **Files:** add the five files in `1 Claude project/knowledge/`.
4. **Folder:** choose the folder from step 2.
5. **Permission mode:** Auto.

## 4. A first run (about 10 minutes)

1. Start a new chat in the project and send **"Go"**, or the full request:
   > Please run a contract-leakage review: are we buying through our contracts, and are their terms being honoured?
   The review reads the files, shows its dashboard on the right, and stops at the **decision card** in the chat. (*"Prepare a new review."* opens the dashboard and waits for you to say when to begin: useful before a demonstration.)
2. **The decisions.** Each item on the card starts on the recommended option, with its reason. Keep it or change it, then give your full name and choose your role: Contracts Manager, Category Manager, Procurement Manager or Commercial Manager.
3. **The release** needs a second person: a different name, in a release role (Chief Procurement Officer, Financial Controller, Commercial Director or Chief Financial Officer). The approval card starts on the recommendation too; the approver keeps or changes it, and ticks the confirmation.
4. **The results.** In the folder, `03 Outputs` now holds a folder for the review with **Report**, **Evidence** and **Actions**, and `04 Records` holds its record. Ask *"Can we check the record hasn't been changed?"*
5. **Compare** the figures with `4 Guides and reference/VERIFIED-FIGURES.md` (they match exactly for the same decisions), and the screens with `4 Guides and reference/screens`. `uat.md` is the full test checklist.

## Good to know

- **The data is invented**: every agreement, supplier, person and figure in `01 Documents` and `02 Data`. Never use real Sasol data. See `4 Guides and reference/handling.md`.
- **The Sasol design is built into the plugin**: the dashboard, the cards, the report, and the Word and PowerPoint pack carry it themselves. The *Sasol Design System* in Claude Design isn't needed. With it set as your default in Claude Design, anything extra you ask for in the chat (a one-slide version, say) follows it too; ask its owner to share it with you if you want that.
- **One catalogue for all three.** Step 1 is once; each use case then needs its own project (step 3) and folder (step 2).
- **Updates:** an uploaded plugin stays at 1.10.0 until you upload a newer one; from the catalogue, updates arrive by themselves. Either way, the project's instructions and knowledge files change only now and then: each release's notes (`CHANGELOG.md`) say when, and which files to replace.

## If something isn't right

| You see | Do this |
|---|---|
| The plugin upload fails | Choose the `.zip` exactly as it came in the package. If your organisation doesn't allow uploaded plugins, upload the skill instead (step 1.4), or use the catalogue |
| The catalogue can't be added, or GitHub can't find it | Check your GitHub user can open `Intellinexus/sasol-plugin-catalogue`, and that the Claude GitHub App has access to it (step 1) |
| The dashboard shows an older version | Start a new chat: an open chat keeps the version it started with. From the catalogue, **Check for updates** in its menu first |
| The review can't find the files | Check the project's folder is the one holding `00 Read me.md`, `01 Documents` and `02 Data`. If Claude works from a copy instead, that's the designed fallback |
| The card doesn't appear, and Claude asks in the chat instead | Answer in the chat, in one reply: that's the designed fallback |
| A decision or the release is refused | That's a control working: give what it asks for (a full name, a role from the list, a reason of three words or more, a different approver) |
