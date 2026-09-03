# Module 13 — Order Fulfilment

**Days 74–80 of ~120.**
This module turns "how the business works" into a documented, repeatable pipeline — the exact sequence from quote to reorder, an order tracker to run it through, and the SOPs (standard operating procedures) that make quality, delivery, and payment collection consistent every time, not just when you're paying close attention.

---

### DAY 74 — MAPPING THE FULL FULFILMENT PIPELINE

**Module 13: Order Fulfilment — Lesson 1**

### TODAY'S OBJECTIVE

Lay out the complete order pipeline, stage by stage, from the moment a quote is accepted to the moment a customer reorders — so every later day in this module is filling in detail on a map you already understand end-to-end.

### WHAT YOU NEED TO LEARN

**1. The full pipeline.**

```
QUOTE ACCEPTED
     ↓
DEPOSIT COLLECTED (50%, before anything is ordered — your Day 1 rule, still non-negotiable)
     ↓
ORDER PLACED WITH SUPPLIER (blank garments, using deposit funds)
     ↓
BRANDING (embroidery/print applied by your decorator)
     ↓
QUALITY CONTROL (you personally inspect — Day 76)
     ↓
PACKAGING
     ↓
DELIVERY (Day 77)
     ↓
BALANCE PAYMENT COLLECTED (Day 78)
     ↓
FOLLOW-UP (confirm satisfaction, log the relationship)
     ↓
REORDER (triggered months later — Day 79, and fully automated in Module 17)
```

**2. What happens at each stage, and who's involved:**

| Stage | What actually happens | Tag |
|---|---|---|
| Quote accepted | Customer confirms via your sales process (Module 9) | [ME] |
| Deposit collected | 50% paid via EFT before any supplier spend | [ME] to confirm, [AUTOMATION] can log it once confirmed |
| Order placed with supplier | You order blank garments + arrange branding, using your qualified supplier(s) from Module 4 | [ME] |
| Branding | Supplier/decorator embroiders or prints the logo — lead time depends on your supplier agreement | Supplier's job, but you're tracking it |
| Quality control | You personally inspect every order before it leaves your hands (roadmap rule, non-negotiable at this stage) | [ME] |
| Packaging | Sorted by size/recipient if the customer needs that, bagged/boxed | [ME] or [EMPLOYEE] later |
| Delivery | Handed off to the customer, signed for | [ME] |
| Balance payment | Remaining 50% collected on delivery | [ME] |
| Follow-up | Quick check-in that everything's correct and fits well | [ME], reminder [AUTOMATION] |
| Reorder | Triggered 6-12 months later based on the delivery date | [AUTOMATION] reminder, [ME] does the actual conversation |

**3. Why mapping it matters before building the tracker.** Day 75 builds a tracker whose status stages need to match reality exactly — if the pipeline map is fuzzy, the tracker will be too, and it'll drift out of sync with what's actually happening on real orders within the first month.

### WHAT YOU NEED TO UNDERSTAND

Every stage in this pipeline exists because skipping it has already been identified as a real risk (Module 1, roadmap section 7): skip the deposit and you fund the customer's order yourself; skip QC and a bad batch reaches a customer; skip the follow-up and a happy customer quietly drifts to a competitor at reorder time instead of coming back to you. The pipeline isn't bureaucracy — every stage is there because something bad happens if it's missing.

### EXERCISES

1. **Walk through the pipeline using a realistic order** (make up plausible numbers: e.g. a security company orders 50 golf shirts). Write one or two sentences for each stage describing exactly what you personally would do at that point. A strong answer is specific enough that someone else could follow it without asking you questions.
2. **Identify the single riskiest stage** in the pipeline for your business specifically, and explain why in 2-3 sentences. A strong answer references a real risk from Module 1 (cash flow, quality, supplier reliability) rather than a generic worry.
3. **True or false, and explain why:** "Once the deposit is collected, the order is basically done and just needs producing." (Think about how much can still go wrong between deposit and delivery.)

**Check your work (question 3):** False. Between deposit and delivery there are at least five more stages where things can go wrong — supplier delay, branding error, a QC failure, a delivery mishap, or the customer not being ready to pay the balance on time. Treating "deposit collected" as "done" is exactly the kind of complacency that leads to a rushed, unchecked delivery.

### BUSINESS IMPLEMENTATION

1. **[ME]** Write out the pipeline map above with your own real specifics filled in (your actual supplier's typical lead time, your actual delivery method, etc.) — this becomes the backbone of the SOP document you'll finish assembling on Day 80.
2. **[ME]** Identify any stage where you don't yet have a clear real-world process (e.g. you haven't actually decided how packaging/sorting works for a multi-size order) — flag it, it gets solved over the next several days.

### TODAY'S DELIVERABLES

- [ ] Full pipeline map written with your real business's specifics.
- [ ] Riskiest stage identified and reasoning documented.
- [ ] Any pipeline gaps flagged for the days ahead.

### END-OF-DAY CHECK

1. Can I list all the pipeline stages in order, from memory, without looking?
2. Do I know exactly what "done" means at each stage, not just roughly?
3. Have I flagged every stage I'm still unsure how to actually execute?

### NEXT DAY

**Day 75** builds the order tracker directly on top of today's map — one status field per stage, linked to your CRM, so every real order's position in the pipeline is always visible at a glance.

---

### DAY 75 — BUILDING THE ORDER TRACKER

**Module 13: Order Fulfilment — Lesson 2**

### TODAY'S OBJECTIVE

Have Claude Code build an order tracker inside your CRM using the exact pipeline stages from Day 74, so every order's real-world status is always one glance away — and generate a proper invoice automatically once an order is placed, closing the loop the roadmap promised for this module.

### WHAT YOU NEED TO LEARN

**1. The exact status stages the tracker will use**, matching Day 74's map one-to-one:
`Quote Accepted → Deposit Received → Order Placed with Supplier → In Branding → Quality Check → Packaged → Out for Delivery → Delivered → Balance Paid → Follow-Up Sent → Reordered`

**2. Why it lives inside the CRM, not as a separate tool.** An order is already a record type in your Module 11 CRM (leads → customers → quotes → orders). The tracker isn't a new system — it's a status field and a clear view on the order records you already have, so it never falls out of sync with your customer and quote data.

**3. Invoicing, folded in here.** The roadmap always planned for auto-generated PDF invoices to arrive at this stage (Module 13), once you have a real order pipeline to attach them to. When an order reaches "Deposit Received," you should be able to generate a proper invoice (or deposit receipt) and, at "Balance Paid," a final receipt — using the same order data the tracker already holds, so amounts always match what's actually in the CRM.

### WHAT YOU NEED TO UNDERSTAND

A tracker only works if updating it is *faster* than not updating it. If moving an order to the next stage takes longer than just remembering it in your head, you'll stop using it within two weeks. Keep the update step to one click/one status change per stage — the value is in always having an honest, current view, not in capturing extra detail you won't maintain.

### EXERCISES

1. **Match each Day 74 pipeline stage to one of the 11 tracker statuses above** — confirm nothing's missing and nothing's redundant. A strong answer notices these are the same 10 pipeline stages from Day 74, just phrased as trackable statuses (with "Order Accepted" split into "Quote Accepted" then "Deposit Received," since those are two separate real events).
2. **Decide what "generate invoice" should actually produce** — what fields does a customer expect to see on a deposit invoice vs. a final receipt? A strong answer includes: your business details, customer details, itemized order (garment/qty/price), amount due at this stage, and the order/quote reference number.

### BUSINESS IMPLEMENTATION

1. **[ME]** Confirm the 11 status stages match your real process (adjust wording if your actual workflow differs slightly).
2. **[CLAUDE CODE]** Build the order tracker and invoice generation (prompt below).
3. **[ME]** Test it on a realistic order, moving it through every stage and generating both documents.
4. **[AUTOMATION]** Once built, moving an order forward and generating its paperwork takes one action each — but sending an invoice to a customer still needs your review, per the Module 12 approval rule.

### CLAUDE CODE / AI BUILDING

**What we're building:** an order status tracker with 11 defined stages, linked to existing CRM order records, plus auto-generated PDF invoices/receipts tied to two of those stages.

**The exact prompt:**
```
Read how the CRM (business/crm/) currently structures orders before
changing anything, and keep the same conventions already in place.

Add an order status field with exactly these stages, in this order:
Quote Accepted, Deposit Received, Order Placed with Supplier, In Branding,
Quality Check, Packaged, Out for Delivery, Delivered, Balance Paid,
Follow-Up Sent, Reordered.

Requirements:
- Updating an order's status should be a single action, not a multi-step
  form.
- Give me a view that shows all active orders grouped by current status,
  so I can see the whole pipeline at a glance.
- When an order reaches "Deposit Received," let me generate a PDF deposit
  invoice from the order's existing data (my business details, customer
  details, itemized garments/quantities/prices, amount due = the deposit,
  order reference number).
- When an order reaches "Balance Paid," let me generate a final PDF
  receipt the same way, showing the balance amount and confirming the
  order is fully paid.
- Generating these documents must not automatically send them anywhere —
  per our approval rule, I review and send every customer-facing document
  myself.

Explain what you built and how to test moving an order through every
stage and generating both documents.
```

**How to test it:** create or pick a real test order, move it through all 11 statuses one at a time, generate the deposit invoice at "Deposit Received" and the final receipt at "Balance Paid," and check both documents' numbers against the order record manually.

### TODAY'S DELIVERABLES

- [ ] Order tracker built with all 11 stages, linked to the CRM.
- [ ] Pipeline-view (orders grouped by status) confirmed working.
- [ ] Deposit invoice and final receipt generation built and tested.
- [ ] One real order moved end-to-end through the tracker as a test.

### END-OF-DAY CHECK

1. Can I see, at a glance, exactly which stage every active order is in?
2. Did I test both invoice/receipt generation and check the numbers by hand?
3. Is updating an order's status actually fast enough that I'll keep doing it?

### NEXT DAY

**Day 76** builds the quality-control SOP that gives real, concrete meaning to the "Quality Check" stage the tracker now has a slot for.

---

### DAY 76 — THE QUALITY-CONTROL SOP

**Module 13: Order Fulfilment — Lesson 3**

### TODAY'S OBJECTIVE

Turn "you personally inspect before delivery" (the roadmap's non-negotiable rule) into a concrete, repeatable inspection checklist you actually run on every order.

### WHAT YOU NEED TO LEARN

**1. Why "inspect before delivery" needs a checklist, not just intent.** "I'll check it carefully" is not a process — it's a hope. On a rushed day, or once you're not personally embroidering every garment yourself, an informal glance will miss things a checklist catches every time. The checklist exists so quality doesn't depend on how alert you happen to be that day.

**2. The inspection checklist, item by item:**

| Check | What you're actually looking for |
|---|---|
| **Count** | Does the delivered quantity exactly match the order — right sizes, right quantities per size, nothing missing or extra? |
| **Stitching** | Loose threads, uneven seams, puckering around the collar/hem, any visibly weak stitching that would fail with wear |
| **Sizing** | Spot-check against the size chart/order spec — pull a few garments per size and physically confirm the label matches actual measurements, don't just trust the tag |
| **Logo placement** | Consistent position across every garment (same spot, same size, same orientation) — a logo that's centered on one shirt and off-center on the next is an instant giveaway of sloppy work |
| **Logo quality** | Clean edges, correct colors matching the customer's actual branding, no smudging, no loose threads on embroidery, no cracking/peeling on print |
| **General condition** | No stains, no damage from the branding process (scorch marks from heat transfer, snags from embroidery), garment itself free of defects |
| **Packaging** | Folded/bagged neatly, sorted by size if the order requires it, ready to hand over looking professional |

**3. How much of the batch to check.** For small orders, check every single item. For larger orders, a full 100% check on stitching/logo quality plus a full recount is still worth the time (miscounts and misplaced logos are the two most common real failures) — but you don't need to physically remeasure every single garment's sizing if the run is large and consistent; spot-check a sample across each size represented.

### WHAT YOU NEED TO UNDERSTAND

A QC failure caught by you costs you a redo conversation with your supplier — annoying, but recoverable and invisible to the customer. A QC failure that reaches the customer costs you trust you may never fully get back, on an account you're hoping will reorder for years. The checklist is cheap. A failed corporate account is not.

### EXERCISES

1. **Run the checklist mentally against a realistic scenario**: an order of 60 branded golf shirts arrives from your decorator. Describe, item by item, exactly what you'd physically do to check each line of the checklist. A strong answer is specific and physical (e.g. "lay out one shirt per size on a table, measure chest width against the size chart") not vague ("check it looks right").
2. **Decide your rule for full-check vs. spot-check by order size.** A strong answer names an actual threshold (e.g. "under 30 units, check every item; 30+ units, full logo/stitch pass but a per-size sample for sizing") and explains the reasoning.

### BUSINESS IMPLEMENTATION

1. **[ME]** Adopt the checklist above (adjusted for your real garment types) as your standard inspection process, effective on the next real order.
2. **[ME]** Decide your full-check vs. spot-check threshold from the exercise and write it down.
3. **[EMPLOYEE]** (flagged for later, not now) — once you hire fulfilment help, this checklist is exactly the document you hand them; QC judgment stays [ME] far longer than most tasks, but the checklist itself makes eventual delegation possible.

### TODAY'S DELIVERABLES

- [ ] Inspection checklist adopted, adjusted for your real garment types.
- [ ] Full-check vs. spot-check threshold decided and written down.
- [ ] Checklist walked through mentally against a realistic order.

### END-OF-DAY CHECK

1. Could I run this checklist on a real order right now without having to think about what to check next?
2. Do I know my own threshold for full-check vs. spot-check?
3. Do I understand why a caught QC failure is cheap and a delivered one is expensive?

### NEXT DAY

**Day 77** picks up right where QC leaves off: the delivery and handoff SOP for getting a passed-inspection order safely and professionally into the customer's hands.

---

### DAY 77 — DELIVERY LOGISTICS & CUSTOMER HANDOFF SOP

**Module 13: Order Fulfilment — Lesson 4**

### TODAY'S OBJECTIVE

Build a repeatable delivery and handoff process — so the last physical touchpoint with the customer before payment is smooth, professional, and leaves a clean paper trail.

### WHAT YOU NEED TO LEARN

**1. Scheduling the delivery.** Confirm the delivery slot with the customer in advance (don't just show up) — B2B customers, especially ops managers at security/cleaning companies, often need to coordinate who's available to receive and sign for the goods. Confirm the delivery address and contact person again at this point, even if it was set at quoting — details drift over a multi-week order.

**2. What to bring.**
- The order itself, already through QC (Day 76) and packaged
- The deposit invoice (for reference) and a final invoice/receipt for the balance
- A delivery note or simple sign-off sheet listing exactly what's being delivered, for the customer's representative to sign

**3. The handoff, step by step:**
1. Confirm you're handing the order to the right person (the contact on file, or someone they've authorized).
2. Do a quick joint count/visual check with the customer present — this protects both of you; any discrepancy is caught immediately, not discovered after you've left.
3. Get the delivery note signed and dated.
4. Take a photo of the delivered goods and the signed note for your own records (this matters more than it seems — it's your evidence if a dispute ever comes up later).
5. Request the balance payment on the spot (Day 78 covers this in detail) — the delivery moment is when payment is easiest to collect, because the customer has the goods in hand and every reason to close the loop.

**4. Update the tracker.** Move the order to "Delivered" in your Module 13 tracker as soon as handoff is confirmed — this is also what starts the reorder-window clock (Day 79, Module 17).

### WHAT YOU NEED TO UNDERSTAND

The delivery moment is not just logistics — it's the point where trust either gets confirmed (goods match what was promised, professionally handed over) or damaged (a rushed drop-off with no verification, no paperwork, no clear next step). A five-minute proper handoff is what makes the balance-payment conversation on Day 78 easy instead of awkward.

### EXERCISES

1. **Write your real delivery SOP**, filling in your actual likely method (you deliver personally, a courier, customer collects) for a typical order size. A strong answer names who physically does the handoff, what document gets signed, and what you do with the signed copy afterward.
2. **Scenario: you arrive and the customer's contact isn't available, but a receptionist offers to "just take it."** What do you do? A strong answer says you don't hand off an unverified order to someone not authorized to receive/sign for it — reschedule with the actual contact rather than risk a dispute over what was or wasn't delivered.

### BUSINESS IMPLEMENTATION

1. **[ME]** Write your real delivery SOP (from the exercise) into your growing SOP document.
2. **[ME]** Create a simple delivery note/sign-off template if you don't already have one (can be built with Claude Code alongside the invoice templates from Day 75, or kept as a simple document).
3. **[AUTOMATION]** Moving the order to "Delivered" in the tracker, and the reorder-window clock that starts from it, is already covered by Days 75 and 79 — no new automation needed today, just the discipline of updating status at the moment of handoff.

### TODAY'S DELIVERABLES

- [ ] Real delivery SOP written and documented.
- [ ] Delivery note/sign-off template ready to use.
- [ ] Photo-and-signature habit for every delivery adopted.

### END-OF-DAY CHECK

1. Do I have a clear, written process for who hands off, what gets checked, and what gets signed?
2. Do I know what I'd do if the right contact isn't there to receive the order?
3. Does my process end with the tracker updated to "Delivered," not just the goods dropped off?

### NEXT DAY

**Day 78** covers the conversation that happens right at the end of today's handoff process: collecting the balance payment, and what to do if it doesn't happen on the spot.

---

### DAY 78 — PAYMENT COLLECTION SOP

**Module 13: Order Fulfilment — Lesson 5**

### TODAY'S OBJECTIVE

Build a respectful, staged process for collecting the balance payment on delivery — and for what to do when a customer doesn't pay on the spot.

### WHAT YOU NEED TO LEARN

**1. The ideal case: collect on delivery.** As covered Day 77, the moment of handoff is the best time to collect the balance — goods are in hand, the final receipt is ready, and you can process an EFT confirmation or request an immediate transfer before you leave. Ask directly and matter-of-factly: "The balance is R[X] — happy to wait a few minutes if you want to do the transfer now, or can you confirm when it'll go through today?"

**2. If it doesn't happen on the spot — a respectful, staged approach:**

| Stage | Timing | Tone | What you actually do |
|---|---|---|---|
| 1. Friendly reminder | Day of delivery, end of day, if not yet paid | Warm, assumes good faith | A short message confirming delivery went well and reminding them the balance of R[X] is due — most delays are simple admin, not refusal |
| 2. Firm reminder | 3-5 days overdue | Professional, clear | Restate the amount, the original agreed terms (from your quote/invoice), and ask directly when to expect payment |
| 3. Hold future orders | 7-10+ days overdue with no response or commitment | Firm but not hostile | No new orders are placed for this customer until the outstanding balance clears — say this plainly, don't just quietly stop responding to them |
| 4. Last resort | Extended non-payment despite the above | Formal | A written formal demand, and if it stays unresolved, this moves to **[PROFESSIONAL]** — a lawyer or a small-claims/debt-collection process, not something to handle informally past this point |

**3. Why deposits matter even more here.** Because you always collect 50% upfront, your worst-case exposure on any single non-paying customer is capped at the unpaid balance on goods already delivered — never the full order value, and never a supplier payment you made with your own uncovered cash. This is the deposit-first rule protecting you again, at the other end of the order.

### WHAT YOU NEED TO UNDERSTAND

Respectful and firm are not opposites. Staying warm in stage 1 costs you nothing and preserves a relationship that's usually just dealing with normal admin delay. Being clearly firm by stage 3 — actually holding future orders, not just thinking about it — is what protects you from becoming the supplier everyone knows they can pay late. Do both, in the right order, every time.

### EXERCISES

1. **Draft your stage 1 friendly reminder message**, in your own words, for a real or realistic scenario. A strong answer is warm, specific (names the amount and references the delivery), and doesn't sound like a threat.
2. **Draft your stage 2 firm reminder message.** A strong answer is clearly more direct than stage 1 — restates the original terms plainly — while still being professional, not hostile.
3. **Scenario: a long-standing, normally reliable customer is 12 days late on a balance for the first time ever.** Do you go straight to "hold future orders"? A strong answer says no — context matters; a first-time delay from an otherwise reliable account probably warrants one more direct conversation before escalating, whereas a new or already-shaky account might reach stage 3 faster. The staged process is a default, not a rule applied blindly regardless of relationship history.

### BUSINESS IMPLEMENTATION

1. **[ME]** Write your real stage 1 and stage 2 message templates (from the exercise) — keep them ready to personalize and send.
2. **[ME]** Decide your real timing thresholds (the table above uses example day-counts — set your own if you want different ones) and document them.
3. **[PROFESSIONAL]** Know in advance, before you ever need it, roughly what a formal demand/collections process would involve in South Africa for a B2B debt of this size — you don't need to engage a lawyer today, but know that stage 4 is where you'd start that conversation, not further down the line.

### TODAY'S DELIVERABLES

- [ ] Stage 1 and stage 2 message templates written.
- [ ] Real timing thresholds for each stage documented.
- [ ] Clear understanding of when (and why) this moves to [PROFESSIONAL].

### END-OF-DAY CHECK

1. Do I have ready-to-use templates for both the friendly and firm reminder stages?
2. Do I know exactly when I'd hold future orders for a non-paying customer?
3. Do I know where the line is past which this stops being something I handle myself?

### NEXT DAY

**Day 79** looks forward past a successfully paid, delivered order to the next thing that should happen months later: a reorder check-in, triggered automatically off the delivery date this module's tracker now records.

---

### DAY 79 — THE REORDER-TRIGGER SOP

**Module 13: Order Fulfilment — Lesson 6**

### TODAY'S OBJECTIVE

Define exactly when and how a completed order becomes a reorder check-in, closing the loop of the pipeline you mapped on Day 74 — and set up the connection this SOP has to Module 17 (Retention), where it gets built out fully.

### WHAT YOU NEED TO LEARN

**1. Why this is part of fulfilment, not an afterthought.** The reorder trigger only works because the delivery date was recorded accurately back on Day 77, and the reminder logic already exists from Day 69 (Module 12). Fulfilment doesn't end at "delivered and paid" — it ends when the relationship is set up to naturally continue, which is what makes this a genuinely repeat business instead of one-off sales.

**2. The trigger, concretely.** Using the 6-12 month reorder window this business runs on (driven by staff turnover in security and cleaning companies): a check-in reminder fires starting around the 8-month mark since delivery (giving you comfortable runway before the 12-month outer edge), surfaced on your Day 69 reminder list alongside lead follow-ups.

**3. What the check-in actually is — not a hard sell.** A simple, low-pressure message: confirming how the uniforms have held up, asking if headcount has changed (new hires need kit — that's often a smaller, easier reorder than a full re-supply), and reminding them you're one message away when they're ready. This is [ME] — a real, personal touch, not an automated blast (per the Module 12 approval rule: the reminder is automated, the actual message is not).

### WHAT YOU NEED TO UNDERSTAND

The reorder trigger is where the whole deposit-first, quality-controlled, relationship-first approach pays off financially — a reordering customer costs you almost nothing to "acquire" a second time and already trusts your quality. Module 17 builds this into a full retention system; today's job is just making sure the fulfilment pipeline hands off a clean, accurate delivery date for that system to work from.

### EXERCISES

1. **Draft a reorder check-in message** for a realistic delivered order (e.g. 60 shirts delivered 8 months ago to a security company). A strong answer is short, specific to that customer's order, and asks a genuine question (about fit, wear, headcount changes) rather than just "want to reorder?"
2. **Explain in 2-3 sentences why the check-in timing (8 months, not 12) matters.** A strong answer notes that waiting until the 12-month edge risks the customer already sourcing from a competitor out of urgency, while checking in earlier gives you a natural opening before that pressure exists.

### BUSINESS IMPLEMENTATION

1. **[ME]** Confirm your real reorder-trigger timing (adjust the 8-month default if your niche mix or typical order type suggests differently).
2. **[AUTOMATION]** Confirm the Day 69 reminder system correctly uses each order's "Delivered" date from the Day 75 tracker as its trigger input (test with a real or adjusted-date order if needed).
3. **[ME]** Draft your reorder check-in message template (from the exercise) — ready for Module 17 to build fully into the retention system.

### TODAY'S DELIVERABLES

- [ ] Reorder-trigger timing confirmed and documented.
- [ ] Confirmed the reminder system correctly reads delivery dates from the tracker.
- [ ] Reorder check-in message template drafted.

### END-OF-DAY CHECK

1. Do I know exactly when a reorder check-in should fire for a given delivered order?
2. Have I confirmed (not assumed) that the reminder system pulls the right date?
3. Do I have a genuine, non-pushy check-in message ready to personalize?

### NEXT DAY

**Day 80** is the capstone: assemble the full written fulfilment SOP from Days 74-79 into one document, confirm the order tracker is fully live, take the module quiz, and move to Module 14 (Customer Service).

---

### DAY 80 — FULFILMENT SOP CAPSTONE

**Module 13: Order Fulfilment — Lesson 7 (Capstone)**

### TODAY'S OBJECTIVE

Assemble everything from Days 74-79 into one complete, usable fulfilment SOP document, confirm the order tracker and invoicing are fully working, and take the module quiz before moving into Module 14.

### WHAT YOU NEED TO LEARN

**Why one assembled document matters.** Right now the pipeline map, QC checklist, delivery SOP, payment SOP, and reorder trigger exist as separate day-by-day pieces. A real SOP document — one file, organized in pipeline order — is what you'd actually hand a future employee (Module 18-19) or refer back to yourself six months from now when a detail's gone fuzzy. This is your first real entry in what becomes the full SOP library in Module 19.

### EXERCISES — MODULE QUIZ

1. List the full pipeline in order, from "Quote Accepted" to "Reordered."
2. What are the two things you personally verify during quality control that most beginners skip?
3. What's the correct order of the payment-collection escalation stages, and what changes about the tone as you move through them?
4. Why does the reorder-trigger fire around month 8, not month 12?

**Check your work:**
1. Quote Accepted → Deposit Received → Order Placed with Supplier → In Branding → Quality Check → Packaged → Out for Delivery → Delivered → Balance Paid → Follow-Up Sent → Reordered.
2. Count accuracy (matches the order exactly) and logo placement consistency across every garment — both are easy to assume are fine and are exactly where sloppy batches actually fail.
3. Friendly reminder → firm reminder → hold future orders → last resort ([PROFESSIONAL]); tone moves from warm/assuming good faith to professional/clear to firm-but-not-hostile to formal.
4. To give runway before the 12-month outer edge of the reorder window, so you reach the customer before they've already started sourcing elsewhere out of urgency.

### BUSINESS IMPLEMENTATION

1. **[ME]** Assemble Days 74-79's content into one fulfilment SOP document, organized in pipeline order: pipeline map → QC checklist → delivery SOP → payment SOP → reorder-trigger SOP.
2. **[ME]** Run one final real (or realistic) order fully through the live tracker, generating both the deposit invoice and final receipt, to confirm the whole system works together.
3. **[CLAUDE CODE]** Fix anything that surfaced as broken or unclear during today's full run-through.

### TODAY'S DELIVERABLES

- [ ] Complete fulfilment SOP document assembled from Days 74-79.
- [ ] One order run fully through the live tracker as an end-to-end test.
- [ ] Module 13 quiz completed and understood.

### END-OF-DAY CHECK

1. Do I have one document I could hand someone else that explains the whole fulfilment process?
2. Did I confirm the tracker and invoicing genuinely work end-to-end, not just in pieces?
3. Am I confident in every SOP in this module, not just the ones I found interesting?

### NEXT DAY

**Module 14 (Customer Service)** starts Day 81, building the complaint-handling and communication frameworks for when something in this pipeline doesn't go perfectly — because eventually, something won't.
