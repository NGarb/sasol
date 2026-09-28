# About this review: Duplicate Vendors & Payments

## The question it answers

*Are we paying the same company twice, under two different supplier numbers?* Duplicate supplier records creep in over years of onboarding and system changes, and a payment can land on both records without either showing anything wrong.

## What happens

1. The review reads the supplier list and the spend history (purchase orders, each with the date it was paid, where it was) in the project folder, whatever they hold, and reports what it found: how many records and orders, their value and the period they cover.
2. Fixed rules compare every plausible pair on tax number, bank account, name and city, and score each pair from 0 to 1. For each pair at or above the **policy line (0.35)**, they also look for orders for the same amount on both records within 30 days. The dashboard's what-if shows what a higher or lower line would change.
3. Claude assesses each pair, citing only the evidence, and recommends: the same supplier, different suppliers, or refer it on.
4. **One person decides every pair on one card:** a choice and a reason for each, their full name, and a role the delegation of authority allows (Vendor Master Data Manager, Creditors Manager, Procurement Manager or Supplier Risk Manager). Only then does the review count what was paid twice, and only for pairs the person confirmed.
5. After the findings, each pair is analysed and what to act on is recommended, each valued by the review's own rules.
6. **A different person approves the release**, in a senior role (Financial Controller, Head of Internal Control, Chief Risk Officer or Chief Financial Officer), confirming they reviewed the findings, the decisions and the recommendations. Only then does the review file its results in the project folder's `03 Outputs`: the dashboard report, a management briefing and a presentation, the one-page summary, the evidence pack, the audit trail, the data, a draft change request and draft recovery letters. The tamper-evident record goes to `04 Records`. Nothing is merged, blocked or recovered.

## What makes it different

- **The finding depends on a person's decision.** A payment only counts as made twice once someone takes responsibility for saying two records are one supplier. Until then, it's a possible duplicate, shown but not counted.
- **There isn't always a right answer.** A shared bank account with different tax numbers is common (payment agents, group treasuries), so the honest answer can be "refer it on". Where a person decides the two are different suppliers, they confirm the bank details were verified.
- **The threshold is policy, not an IT setting.** Moving the line trades review effort against what goes unseen, and the dashboard makes that visible.
- **Two named people, in two roles.** The person who decides can never approve the release.

## The limits, stated plainly

- It covers the supplier records and the orders in this project's folder, over the period the spend history covers, in rand excluding VAT. The figures are not group totals, and it makes no claim beyond them.
- It changes nothing in any system. The change request and the letters are drafts for the people who own those processes.
- It never draws a conclusion about wrongdoing. Shared bank details go to forensic review, and people with the authority decide.
