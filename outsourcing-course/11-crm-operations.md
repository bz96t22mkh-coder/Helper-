# Module 11 — CRM & Operations

**Days 59–66 of ~120.**
Build your real CRM — leads, customers, quotes, orders, suppliers, and basic inventory linkage — as one lightweight system, tested against real data.

---

### DAY 59 — What a CRM Actually Needs to Do for This Business

**Module 11: CRM & Operations — Lesson 1**

### TODAY'S OBJECTIVE

Define, precisely, what a CRM needs to do for this specific business before building anything — so Day 61's build starts from a clear, correct requirement instead of a generic "build me a CRM" guess.

### WHAT YOU NEED TO LEARN

**1. What CRM means here, plainly.** CRM stands for customer relationship management — in practice for this business, it's the one system that replaces your spreadsheet tracker (Module 10) and holds the full picture: every lead, every customer, and (added later this module) every quote, order, supplier link, and basic inventory note, all connected instead of scattered across separate files.

**2. Why your Module 10 spreadsheet tracker isn't enough long-term.** A spreadsheet is excellent for a list you sort and filter — it struggles once you need records to connect to each other (this customer came from this lead, this order came from this quote, this quote used this supplier) and once you want a simple, repeatable way to move a record through stages by clicking rather than manually editing a status column. That connected structure and stage-based workflow is what a real CRM adds.

**3. Requirements gathering — the right way to define this before building.** Rather than guessing what a CRM "should" have, work backward from your real, already-established process:
- What information do you already collect about a lead (Module 10's tracker)? All of that needs to carry over.
- What happens between a lead and a paying customer (Module 9's buyer journey — discovery, quote, deposit)? Each of those needs a place to live.
- What happens after a customer pays a deposit (Module 1's money flow — supplier order, inspection, delivery, balance)? The CRM needs to at least reference this, even if full fulfilment tracking is built properly later (Module 13).
- Who uses this system — just you, for now, on your laptop/phone? That shapes how simple it can stay (no multi-user login system needed yet).

### WHAT YOU NEED TO UNDERSTAND

The biggest risk at this stage isn't building too little — it's over-scoping, trying to spec a CRM with every feature you can imagine before you've used a working version for a single real day. The right approach, matching the course's Claude Code Business Builder Workflow (roadmap, section 10), is the smallest useful first version: leads and customers, tested with real data, before adding quotes, orders, suppliers, or inventory in later days this module.

### EXERCISES

1. **List every field you currently track about a lead** (from your Module 10 CSV tracker) — this is your minimum viable "leads" requirement.
2. **List every field you'd want to track about a customer** once a lead converts (company details, contact person, order history summary, any special notes) — this is your minimum viable "customers" requirement.
3. **Write one sentence** describing what "working" will mean for CRM v1 specifically — the concrete test you'll run on Day 61 (hint: adding one real lead and moving it through real stages).

A strong requirements list is grounded entirely in what you actually already do (from Modules 9-10), not a wishlist of features you've seen in other tools you don't actually need yet.

### BUSINESS IMPLEMENTATION

1. **[ME]** List required lead fields and customer fields.
2. **[ME]** Write the concrete "what does working look like" test for CRM v1.
3. **[ME]** Record all of this in `business/decisions-log.md` as the spec for tomorrow's pipeline design and Day 61's build.

### TODAY'S DELIVERABLES

- [ ] Lead fields listed, based on your real Module 10 tracker.
- [ ] Customer fields listed.
- [ ] A concrete "working" test written for CRM v1.
- [ ] Requirements recorded in the decisions log.

### END-OF-DAY CHECK

1. Is every field I listed something I actually use today, not something I imagine I might want someday?
2. Do I have a clear, specific test in mind for "does this CRM actually work"?
3. Am I resisting the urge to spec every possible feature before building anything?

### NEXT DAY

**Day 60** designs the pipeline stages — the exact path a lead moves through on its way to becoming a repeat customer — using today's requirements as the foundation.

---

### DAY 60 — Designing the Pipeline Stages

**Module 11: CRM & Operations — Lesson 2**

### TODAY'S OBJECTIVE

Design the exact pipeline stages your CRM will use, so every lead and customer has one clear, current stage at all times, and moving between stages reflects something real that happened, not an arbitrary label.

### WHAT YOU NEED TO LEARN

**1. What a pipeline is.** An ordered set of stages a record moves through, left to right (or top to bottom), representing real progress — the CRM equivalent of your Module 9 buyer's journey, but built as an actual system field instead of a mental model.

**2. A pipeline that fits this business's real process:**

```
Lead → Contacted → Quoted → Deposit Paid → In Production → Delivered → Repeat Customer
```

- **Lead** — a real prospect exists in the system (matches Module 10's "unaware/aware" stages, before real engagement).
- **Contacted** — first outreach has happened (Module 9's cold outreach), awaiting response.
- **Quoted** — a discovery call has happened and a real quote has been sent (Module 9, Days 48-49).
- **Deposit Paid** — the 50% deposit has been collected; this is the moment a lead becomes a real customer and production can start (Module 1's money flow).
- **In Production** — the order is with your supplier/decorator (Module 4), being produced.
- **Delivered** — the order has been inspected and delivered, balance collected.
- **Repeat Customer** — has ordered more than once; this stage exists specifically because repeat orders (driven by staff turnover, per Module 1) are core to this business's economics, and your CRM should make it easy to see who's in this category for follow-up and referral requests (Module 17, later).

**3. Why every stage needs a clear, objective trigger.** A stage that's ambiguous (when exactly does someone move from "Contacted" to "Quoted"?) leads to inconsistent, unreliable data. Each stage transition should map to one specific, observable event — a quote sent, a deposit received, an order marked delivered — not a feeling.

### WHAT YOU NEED TO UNDERSTAND

Pipeline stages are only useful if they're few enough to be meaningful at a glance and precise enough that you'd never argue with yourself about which stage a record is in. Seven stages, each with an unambiguous trigger, is enough structure to be genuinely useful without becoming its own admin burden.

### EXERCISES

1. **Confirm or adjust the seven-stage pipeline above** for your business — if your real process differs meaningfully (for instance, if you sometimes skip a formal discovery call), note the variation, but keep the total stage count small.
2. **Write the exact trigger event for each stage transition** — the specific, observable thing that means a record has moved forward.
3. **Decide what happens to a "Contacted" lead that never responds** — does it stay in "Contacted" indefinitely, or does your Module 10 cadence/nurture logic eventually mark it differently? Write your rule.

A strong pipeline definition means you could hand this to someone else (a future employee, Module 18) and they'd move records through it exactly the way you would, with no ambiguity.

### BUSINESS IMPLEMENTATION

1. **[ME]** Finalize the seven pipeline stages and their trigger events for your business.
2. **[ME]** Decide the rule for stalled "Contacted" leads.
3. **[ME]** Record the finalized pipeline spec in `business/decisions-log.md` — this is what Claude Code builds tomorrow.

### TODAY'S DELIVERABLES

- [ ] Pipeline stages finalized (seven, or your adjusted version) with a written trigger event for each.
- [ ] Stalled-lead rule decided.
- [ ] Pipeline spec recorded in the decisions log.

### END-OF-DAY CHECK

1. Could I state the exact trigger for every stage transition without hesitating?
2. Is my pipeline short enough to take in at a glance, but complete enough to reflect my real process?
3. Am I ready to hand this exact spec to Claude Code tomorrow?

### NEXT DAY

**Day 61** hands this pipeline spec and Day 59's requirements to Claude Code to build CRM v1 — bring both.

---

### DAY 61 — Claude Code Builds CRM v1: Leads and Customers

**Module 11: CRM & Operations — Lesson 3**

### TODAY'S OBJECTIVE

Get a working first version of your CRM built — leads and customers, moving through your real pipeline stages — and test it immediately with one real lead.

### WHAT YOU NEED TO LEARN

**1. Why this is a single lightweight local web app, not a paid CRM service.** Per the roadmap's technology approach, this business does not need a monthly-fee CRM platform at this stage — a self-contained tool built by Claude Code, with no ongoing cost, no account to manage, and no dependency on a third party staying in business, does the job. The build today is one self-contained HTML file with the interface and logic built in, storing your data in the browser's local storage (so it works fully offline, with zero setup) and including an export function so your data is never trapped — you can always get a plain CSV backup out of it.

**2. What "v1" scope means today**: leads and customers only, moving through your real pipeline stages, with the fields you specified Day 59. Quotes, orders, supplier links, and inventory (Days 63-64) come later, deliberately, once this base layer is proven to work.

**3. What "working" looks like, concretely**: you can add a real lead with real fields, move it forward through pipeline stages with a simple action (a dropdown or a button, not manual re-entry), see it correctly reflected in the interface at every stage, and it's still there — correctly saved — after closing and reopening the file in your browser.

### WHAT YOU NEED TO UNDERSTAND

Local storage means this data lives in one specific browser, on one specific device, until you export it — this is a deliberate, acceptable v1 tradeoff for a single-operator business at this stage, not an oversight. Know this limitation going in: back up by exporting regularly (this becomes a habit worth building from day one with this tool), and don't open the CRM in a different browser or device expecting your data to follow automatically.

### EXERCISES

Before the build, confirm your inputs are ready:
1. Your Day 59 lead and customer field lists.
2. Your Day 60 pipeline stages and their triggers.
3. Your real Module 10 CSV tracker, ready to reference (not migrated yet — that happens properly on Day 66's capstone, once the CRM is fully built and tested).

### BUSINESS IMPLEMENTATION

1. **[ME]** Confirm requirements and pipeline spec are ready.
2. **[CLAUDE CODE]** Build CRM v1 — leads and customers, with pipeline stages.
3. **[ME]** Add one real lead and move it through every pipeline stage as a test.

### CLAUDE CODE / AI BUILDING

**What we're building today:** CRM v1, a single self-contained HTML file (`business/crm/index.html`) with leads and customers, moving through your real pipeline — no server, no framework, no account, no monthly cost, opens directly in any browser.

**The exact prompt to give Claude Code:**
```
Build CRM v1 for my business as a single self-contained HTML file at
business/crm/index.html — no build tools, no external dependencies, no
server required, works fully offline by opening the file directly in a
browser. Store all data in the browser's localStorage, and include an
"export to CSV" button so data can always be backed up or moved out.

Records: Leads/Customers, one unified record type, with these fields:
[paste your Day 59 field list — company name, contact person, phone/
WhatsApp, email, staff size, source, notes, etc.]

Pipeline stage field, using exactly these stages in this order:
Lead → Contacted → Quoted → Deposit Paid → In Production → Delivered →
Repeat Customer

Interface requirements:
- A simple list/table view of all records, filterable by pipeline stage
- Click a record to see full details and edit any field
- Move a record's pipeline stage forward (and backward, in case of a
  mistake) via a clear dropdown or button — not manual re-typing
- Add-new-record form with all the fields above
- Export-to-CSV button that downloads all current data
- Clean, simple styling — no design requirements beyond readable and
  usable, this is an internal tool

Explain in plain language, after building, exactly how data is stored
and what I need to know about backing it up.
```

**What to expect:** one HTML file you open directly in your browser (no installation) showing a working leads/customers list with add, edit, and stage-move functionality, plus a working CSV export.

**How to test it:** add one real lead with real details, move it through every pipeline stage one at a time confirming the interface updates correctly each time, close the browser tab entirely and reopen the file to confirm the data was actually saved (not lost), and run the CSV export to confirm you get a real, readable backup file. Report anything that doesn't work exactly as expected back to Claude Code specifically (what you did, what you expected, what actually happened).

### TODAY'S DELIVERABLES

- [ ] `business/crm/index.html` built.
- [ ] One real lead added and moved through every pipeline stage successfully.
- [ ] Data confirmed to persist after closing and reopening the file.
- [ ] CSV export tested and confirmed working.

### END-OF-DAY CHECK

1. Did my test lead correctly move through every pipeline stage without data loss?
2. Do I understand exactly where and how this tool stores my data, and its local-storage limitation?
3. Does the CSV export actually give me a real, usable backup?

### NEXT DAY

**Day 62** puts CRM v1 through a real testing pass and teaches you how to describe a bug to Claude Code clearly and specifically, so fixes happen fast and correctly.

---

### DAY 62 — Testing Thoroughly and Reporting Bugs Clearly

**Module 11: CRM & Operations — Lesson 4**

### TODAY'S OBJECTIVE

Test CRM v1 thoroughly with realistic (not just one happy-path) usage, and learn how to describe any bug you find clearly enough that Claude Code can fix it correctly on the first try.

### WHAT YOU NEED TO LEARN

**1. Why one successful test yesterday isn't the same as "tested."** Day 61's test proved the basic happy path works. Real usage is messier: fields left blank, records edited after creation, moving a record backward as well as forward, adding several records in a row, using it on a phone browser as well as a desktop one. Today finds the edges the happy path didn't touch.

**2. A practical test checklist for CRM v1:**
- [ ] Add multiple records in a row — do they all save correctly, with no data bleeding between records?
- [ ] Edit an existing record's details — does the change save and stick after reopening?
- [ ] Move a record's stage forward through all seven stages, then backward — does it behave correctly both directions?
- [ ] Leave optional fields blank — does the record still save without breaking?
- [ ] Filter the list by each pipeline stage — does the filter show exactly the right records?
- [ ] Open the tool on a phone browser — is it still usable, not just technically loading?
- [ ] Export to CSV after adding several records — does every record appear correctly in the export?
- [ ] Close and fully reopen the browser (not just the tab) — does everything persist correctly?

**3. How to describe a bug clearly** — the skill that determines whether a fix takes one round-trip or five:
- **What you did**, specifically (the exact action, not "I was using the CRM").
- **What you expected** to happen.
- **What actually happened** instead.
- **Whether it's consistent** (happens every time) or intermittent (happened once).

A weak bug report: "the CRM is broken." A strong bug report: "I added a new lead with the company name field left blank, expecting it to either save with a blank name or show a validation message — instead the record disappeared entirely from the list after I clicked add, and it's not in the CSV export either. This happened both times I tried it."

### WHAT YOU NEED TO UNDERSTAND

This bug-reporting skill isn't just for today — it's the exact skill you'll use for every future Claude Code build in this course (and honestly, for reporting any issue to any technical person for the rest of the business's life). A specific report gets a correct fix quickly; a vague one costs an extra round-trip of "can you say more about what's happening," which is genuinely avoidable friction.

### EXERCISES

1. **Work through the full test checklist above**, checking off each line and noting exactly what happened for any that failed.
2. **Write a properly structured bug report** for anything that failed, using the four-part structure (what you did, what you expected, what happened, consistent or not).
3. **If nothing failed** (possible, but test honestly rather than rushing to that conclusion), write one deliberately tricky edge case you haven't tried yet and test it for real.

A strong bug report is specific enough that someone who has never seen your screen could reproduce the exact problem from your description alone.

### BUSINESS IMPLEMENTATION

1. **[ME]** Work through the full test checklist.
2. **[ME]** Write properly structured bug reports for anything found.
3. **[CLAUDE CODE]** Fix every reported issue.
4. **[ME]** Re-test each fix specifically to confirm it's actually resolved.

### TODAY'S DELIVERABLES

- [ ] Full test checklist completed.
- [ ] Any bugs found, reported using the four-part structure.
- [ ] All reported bugs fixed and re-tested.

### END-OF-DAY CHECK

1. Did I test realistic messy usage, not just the one happy path from yesterday?
2. Could someone else reproduce any bug I found purely from how I described it?
3. Is CRM v1 now genuinely solid for leads and customers, not just "seemed fine at a glance"?

### NEXT DAY

**Day 63** extends this tested CRM with quotes and orders tracking — the next real layer of your process.

---

### DAY 63 — Claude Code Extends the CRM: Quotes and Orders

**Module 11: CRM & Operations — Lesson 5**

### TODAY'S OBJECTIVE

Extend your working CRM to track quotes and orders linked to each customer, so the full path from "quote sent" to "order delivered" lives in one connected system instead of separate documents.

### WHAT YOU NEED TO LEARN

**1. Why quotes and orders are a natural next layer, not a rebuild.** Your CRM already has real, tested customer records and a pipeline (Days 60-62). Quotes and orders are new record types that link to those existing customer records — extending the same tool, not starting over. This is exactly the smallest-useful-next-increment approach from the roadmap's build workflow.

**2. What a quote record needs** (drawing directly on Module 9, Day 49's quote structure): linked customer, date, line items (garment, quantity, unit price), total, deposit amount, balance amount, status (draft/sent/accepted/expired).

**3. What an order record needs** once a quote is accepted and the deposit is paid: linked customer and linked quote, order date, expected turnaround/delivery date (from your real supplier lead times, Module 4), current pipeline stage (reusing your existing In Production / Delivered stages from Day 60), and a notes field for anything relevant during fulfilment.

**4. Why linking matters more than the new fields themselves.** The real value here isn't just "a place to type quote numbers" — it's that opening a customer record now shows you their quote and order history in one place, without hunting through separate files. That connected view is the actual reason a CRM earns its place over a spreadsheet.

### WHAT YOU NEED TO UNDERSTAND

Resist the temptation to over-build this into a full invoicing or accounting system today — that's Module 13 (fulfilment) and Module 15 (finance) territory, built properly later with their own real requirements. Today's job is specifically: can I create a quote for a customer, mark it accepted, and see it become an order I can track through delivery, all inside the CRM.

### EXERCISES

Before the build, confirm your inputs:
1. Your real quote structure (Module 9, Day 49) — the exact fields you use.
2. Your real order/turnaround information (Module 4's supplier lead times).

### BUSINESS IMPLEMENTATION

1. **[ME]** Confirm quote and order field requirements.
2. **[CLAUDE CODE]** Extend the CRM with quotes and orders, linked to customers.
3. **[ME]** Test by creating one real (or realistic practice) quote through to an order.

### CLAUDE CODE / AI BUILDING

**What we're building today:** an extension to the existing `business/crm/index.html` adding Quotes and Orders, each linked to a customer record — same file, same no-dependency approach, no new tool to learn.

**The exact prompt to give Claude Code:**
```
Extend business/crm/index.html (the existing CRM) with two new linked
record types, keeping everything in the same file, same localStorage
approach, same export-to-CSV pattern extended to cover the new data.

Quotes: linked to a customer record, with fields: date, line items
(garment, quantity, unit price — allow multiple line items per quote),
auto-calculated total, deposit amount (50% of total), balance amount,
status (Draft / Sent / Accepted / Expired).

Orders: linked to a customer record and to the quote it came from, with
fields: order date, expected delivery date, pipeline stage (reuse the
existing In Production / Delivered stages), notes.

Add a way to view a customer's full quote and order history from their
record. Add a button on an Accepted quote to generate a linked order
from it, pre-filled with the quote's details, rather than re-entering
everything.

Test that existing lead/customer data and pipeline functionality from
before still work correctly after this change.
```

**What to expect:** the same CRM tool you already know how to use, with quotes and orders now available, linked to customers, and a customer's record now showing their real quote/order history.

**How to test it:** create one full test quote for a real or realistic customer with multiple line items, confirm the total/deposit/balance calculate correctly, mark it Accepted, generate the linked order from it, and confirm it's pre-filled correctly and appears in that customer's history. Also re-run a few checks from Day 62's checklist to confirm nothing existing broke.

### TODAY'S DELIVERABLES

- [ ] CRM extended with Quotes and Orders, linked to customers.
- [ ] One full test quote created, calculated correctly, and converted to an order.
- [ ] Confirmed existing lead/customer/pipeline functionality still works.

### END-OF-DAY CHECK

1. Does a quote's total, deposit, and balance calculate correctly from its line items?
2. Can I see a customer's full quote and order history from their record?
3. Did I confirm nothing from Days 61-62 broke as a result of this extension?

### NEXT DAY

**Day 64** extends the CRM again with supplier and basic inventory linkage — connecting orders to who's actually producing them.

---

### DAY 64 — Claude Code Extends the CRM: Supplier and Inventory Linkage

**Module 11: CRM & Operations — Lesson 6**

### TODAY'S OBJECTIVE

Extend the CRM once more so an order shows which supplier is producing it and a basic record of what was ordered from them — closing the loop between your sales side and your Module 4 supplier relationships.

### WHAT YOU NEED TO LEARN

**1. Why this stays "basic" linkage, not full inventory management.** This business doesn't hold significant stock (per the roadmap's low-inventory model) — you order blanks from a wholesaler and send them to a decorator per order, rather than managing a warehouse of SKUs. "Inventory" here means a simple record of what was ordered from which supplier for which order, not a full stock-tracking system with reorder points and stock levels — that level of complexity isn't justified by how this business actually operates.

**2. What supplier linkage needs**: each order can reference which supplier(s) it used (your blank-garment wholesaler and your decorator, from Module 4's supplier database), so you can see, per order, exactly who produced it — useful for quality issues, lead-time tracking, and comparing suppliers over time.

**3. What basic inventory linkage needs**: a simple note per order of what was ordered from the supplier (garment, quantity) — not a running stock count, just a record tied to that specific order, since you don't hold ongoing stock.

### WHAT YOU NEED TO UNDERSTAND

It's tempting, once you're on a roll extending a working tool, to keep adding "while we're at it" features. Stay disciplined here: today's scope is specifically linking orders to suppliers and recording what was ordered from them — full supplier performance dashboards, automatic reorder-point alerts, and multi-supplier cost comparison are all legitimate future features, but they belong to a later module (or a later, evidence-based request) once the business has real data to justify them.

### EXERCISES

Before the build, confirm:
1. Your real supplier list (Module 4's supplier database — names/roles, e.g. your blank-garment wholesaler and decorator).
2. What you actually want visible per order regarding supplier and what was ordered — keep this list short.

### BUSINESS IMPLEMENTATION

1. **[ME]** Confirm supplier list and required per-order fields.
2. **[CLAUDE CODE]** Extend the CRM with supplier and basic inventory linkage on orders.
3. **[ME]** Test by linking one real (or realistic) order to a supplier with what was ordered.

### CLAUDE CODE / AI BUILDING

**What we're building today:** a further extension to `business/crm/index.html` adding supplier linkage and a basic per-order inventory note — same single-file, no-dependency approach.

**The exact prompt to give Claude Code:**
```
Extend business/crm/index.html again, adding to the existing Orders:

Supplier linkage: a field (or two, if you use separate blank-garment
and decorator suppliers per order) on each Order to select which
supplier(s) were used, from this list: [paste your real Module 4
supplier list — names and roles].

Basic inventory note: a simple field or small table on each Order for
what was ordered from the supplier (garment, quantity) — not a running
stock count, just a record tied to that specific order.

Add a simple way to see, from a supplier's perspective, which orders
have used them (e.g. filter orders by supplier) — useful later for
comparing suppliers.

Test that all previously built functionality (leads, customers,
pipeline, quotes, orders) still works correctly after this change.
```

**What to expect:** orders that now show which supplier produced them and what was ordered from that supplier, plus a simple way to filter orders by supplier.

**How to test it:** link one real or realistic order to a real supplier from your Module 4 list, record what was ordered, confirm it displays correctly on the order and that filtering orders by that supplier correctly shows it. Re-check a few things from Days 61-63 to confirm nothing broke.

### TODAY'S DELIVERABLES

- [ ] CRM extended with supplier linkage and basic per-order inventory notes.
- [ ] One order linked to a real supplier with items recorded.
- [ ] Filtering orders by supplier confirmed working.
- [ ] Confirmed previous functionality (leads, customers, pipeline, quotes) still works.

### END-OF-DAY CHECK

1. Can I see, for any order, exactly which supplier produced it and what was ordered?
2. Can I filter orders by supplier?
3. Am I confident I haven't over-built this into a stock-management system this business doesn't need yet?

### NEXT DAY

**Day 65** runs one complete mock order through the entire CRM end to end — lead through delivery — to catch anything that only shows up when the whole system is used together.

---

### DAY 65 — Full End-to-End Test: One Complete Mock Order

**Module 11: CRM & Operations — Lesson 7**

### TODAY'S OBJECTIVE

Run one complete, realistic mock order through the entire CRM from lead to delivery, fixing whatever breaks — the test that catches problems individual feature tests (Days 62-64) can't, because it exercises everything connected together the way real use actually will.

### WHAT YOU NEED TO LEARN

**1. Why end-to-end testing matters even after each piece was tested individually.** Days 62-64 each tested one layer in relative isolation. Real usage moves through every layer in sequence, and problems sometimes only appear at the handoffs between them — a quote that converts to an order correctly but loses its supplier link, say, or a customer whose history view doesn't update correctly once an order reaches "Delivered." Only a full run-through surfaces these.

**2. The mock order to run, start to finish, using invented (practice, not real) details**:
1. Add a new lead.
2. Move it to Contacted.
3. Move it to Quoted, and create a real quote with multiple line items.
4. Mark the quote Accepted, generate the linked order.
5. Move the record through Deposit Paid.
6. Link the order to a real supplier and record what was ordered.
7. Move the order through In Production.
8. Move it to Delivered.
9. Confirm the customer's full history (quote, order, supplier, final stage) is all visible correctly from their record.
10. Export everything to CSV and confirm the mock order's full data appears correctly in the export.

**3. How to treat anything that breaks.** Exactly like Day 62 — a specific, structured bug report (what you did, what you expected, what happened, consistent or not) for each issue, rather than a general "something's off around the orders section."

### WHAT YOU NEED TO UNDERSTAND

This full run-through is also your first real rehearsal of how you'll actually use this tool in daily operation — pay attention not just to whether it technically works, but whether the flow feels efficient enough for you to genuinely want to use it every day. A CRM that's technically correct but clunky enough that you'll be tempted to skip steps has still failed its real purpose.

### EXERCISES

Run the full ten-step mock order above, checking off each step, and note both:
1. Anything that broke (structured bug report for each).
2. Anything that worked correctly but felt clunky or slower than it should (not a bug, but worth noting as a possible future refinement).

### BUSINESS IMPLEMENTATION

1. **[ME]** Run the full ten-step mock order end to end.
2. **[ME]** Write structured bug reports for anything broken.
3. **[CLAUDE CODE]** Fix every reported issue.
4. **[ME]** Re-run the full mock order once more after fixes, start to finish, to confirm everything now works cleanly together.

### TODAY'S DELIVERABLES

- [ ] Full ten-step mock order run end to end.
- [ ] Any issues reported with structured bug reports and fixed.
- [ ] Full mock order re-run successfully after fixes, with no remaining issues.

### END-OF-DAY CHECK

1. Did I run every step of a real order's life cycle through the actual CRM, not just individual features in isolation?
2. Are all issues found actually fixed and re-confirmed, not just reported and assumed fixed?
3. Does using this tool feel efficient enough that I'll actually use it daily, not just technically functional?

### NEXT DAY

**Day 66** is Module 11's capstone: the CRM goes live for real, your actual prospect data gets migrated in, the quiz, and the bridge to Module 12 (AI & Automation).

---

### DAY 66 — Capstone: CRM Goes Live, Real Data Migrated

**Module 11: CRM & Operations — Lesson 8**

### TODAY'S OBJECTIVE

Migrate your real prospect and customer data from `business/prospect-list.csv` into the now fully-tested CRM, retire the spreadsheet tracker, and confirm the CRM is genuinely your single system of record going forward.

### WHAT YOU NEED TO LEARN

**1. Why migration happens now, not earlier.** Moving real data into an unfinished, untested system risks corrupting or losing it. Now that CRM v1 has been built (Day 61), extended twice (Days 63-64), and proven end to end (Day 65), it's safe to treat as the real system of record — today's the day your actual business data moves in for good.

**2. What a clean migration looks like**: every real lead and customer from your CSV tracker present in the CRM afterward, with correct pipeline stages reflecting their real current status (not everything reset to "Lead") and no duplicates.

### WHAT YOU NEED TO UNDERSTAND

From today onward, `business/prospect-list.csv` becomes a historical record, not your active tracker — the CRM is where you work daily going forward. Make this a clean, deliberate switch (confirm the migration is complete and correct before you stop updating the old file), not a gradual, confusing overlap where some leads live in one place and some in the other.

### EXERCISES

**Module 11 review quiz:**
1. What are the seven pipeline stages, in order?
2. Why was CRM v1 (Day 61) scoped to just leads and customers, instead of building everything at once?
3. What's the difference between what this CRM calls "inventory linkage" and full stock/inventory management, and why doesn't this business need the latter yet?
4. What are the four parts of a properly structured bug report?

**Check your work:**
1. Lead → Contacted → Quoted → Deposit Paid → In Production → Delivered → Repeat Customer.
2. Matching the roadmap's build workflow (section 10): the smallest useful first version, tested with real data, before adding complexity — reduces risk and gets a working tool in use faster.
3. This business doesn't hold ongoing stock (low-inventory, order-per-customer model) — "inventory linkage" here just records what was ordered from a supplier for a specific order, not a running stock count with reorder points, which would be unjustified complexity for how the business actually operates.
4. What you did, what you expected, what actually happened, and whether it's consistent or intermittent.

### BUSINESS IMPLEMENTATION

1. **[CLAUDE CODE]** Migrate all real data from `business/prospect-list.csv` into the CRM.
2. **[ME]** Verify every real lead/customer is present, correctly staged, and not duplicated.
3. **[ME]** Update `business/decisions-log.md` marking Module 11 complete and the CRM as the live system of record, and update `business/crm/README.md` accordingly.

### CLAUDE CODE / AI BUILDING

**What we're building today:** a one-time migration of your real prospect/customer data from `business/prospect-list.csv` into the live CRM, plus a short note documenting the switch.

**The exact prompt to give Claude Code:**
```
Migrate all real records from business/prospect-list.csv into
business/crm/index.html's data. For each row: create a Lead/Customer
record with the matching fields, and set its pipeline stage based on
its real current status in the CSV (map [describe your CSV's status
values] to the correct CRM pipeline stage — ask me if any mapping is
unclear rather than guessing). Check for and flag any likely duplicates
before finalizing rather than silently merging them.

After migration, update business/prospect-list.md with a short note
that active lead tracking has moved to the CRM (business/crm/index.html)
as of today's date, and that the CSV is now a historical record only.
```

**What to expect:** every real prospect and customer you've built up since Day 1 now living inside the CRM, correctly staged, with a clear note in the old file pointing forward to the new system.

**How to test it:** open the CRM and manually spot-check at least 10-15 migrated records against the original CSV — correct company details, correct stage, no duplicates. If your CSV had a status value that doesn't map cleanly to a pipeline stage, resolve that explicitly rather than letting it default silently.

### TODAY'S DELIVERABLES

- [ ] All real data migrated from the CSV into the CRM.
- [ ] Spot-check of 10-15 migrated records confirmed accurate.
- [ ] `business/prospect-list.md` updated noting the switch to the CRM.
- [ ] `business/decisions-log.md` and `business/crm/README.md` updated, Module 11 marked complete.
- [ ] Module 11 quiz answered and checked.

### END-OF-DAY CHECK

1. Is every real lead and customer I had correctly present in the CRM, with no data lost?
2. Am I clear that the CRM, not the old spreadsheet, is now my daily working system?
3. Do I feel confident operating this CRM day to day going forward — adding leads, moving stages, creating quotes and orders — without needing to relearn it each time?

### NEXT DAY

**Module 12 (AI & Automation), Day 67** starts automating pieces of the process you've been running manually through Modules 9-11 — outreach, follow-ups, CRM updates, quote generation, and reporting — always with approval steps on anything that spends money or speaks to a customer.
