# Module 12 — AI & Automation

**Days 67–73 of ~120.**
You've now built a website, a sales playbook, a lead-gen system, and a full CRM — this module makes them work together with less manual typing, while drawing a hard line around anything that touches money or talks to a customer.

---

### DAY 67 — THE AUTOMATION AUDIT

**Module 12: AI & Automation — Lesson 1**

### TODAY'S OBJECTIVE

Go through every recurring task in the business you've built so far (Modules 1-11) and classify it [ME], [AUTOMATION], or [EMPLOYEE] using a clear, repeatable framework — before you automate anything, you need to know what's actually safe to automate.

### WHAT YOU NEED TO LEARN

**1. Why order matters.** It's tempting to automate whatever is most annoying first. That's backwards. A task that's annoying but low-risk (typing the same CRM fields twice) is a good automation candidate. A task that's rare but high-risk (confirming a big supplier order) is not — even if automating it would "feel" efficient. You need a framework that checks risk before it checks convenience.

**2. The five-question framework, in priority order.** For every recurring task, ask these in this exact order and stop at the first one that says "keep a human in it":

| Priority | Question | If the answer is bad news |
|---|---|---|
| 1. Reliability | If this is done wrong and nobody catches it, how much damage does it do? | High damage (wrong price quoted, wrong size ordered) → stays [ME] or gets a mandatory human check |
| 2. Security | Does this touch money, customer data, or a message that leaves the business? | Yes → needs an approval step before it can run (this becomes Day 72's whole subject) |
| 3. Simplicity | Can this be automated with the tools you already have (your CRM, pricing calculator, Claude Code), or does it need new infrastructure? | Needs something heavy/new → not worth it yet, per the roadmap's "complexity you don't need yet is a cost, not a feature" |
| 4. Cost | Is the time it takes to build and maintain this automation actually less than the time it saves you over the next few months? | No → skip it for now, revisit later |
| 5. Scalability | Will the volume of this task grow as you add customers? | Yes → prioritize automating it sooner, because the time saved compounds |

Notice the order: reliability and security come *before* simplicity, cost, and scalability. A task can be cheap and easy to automate and still fail question 1 or 2 — in that case it stays manual or gets an approval gate, full stop. This is the same logic behind the roadmap's tag system: [AUTOMATION] is for things that can run with zero human step *because* they've already passed reliability and security, not because they're convenient.

**3. Worked mini-example, applying the framework:**
- *Task: calculating a quote's total price, deposit, and balance from garment counts and pricing rules.* Reliability — the pricing calculator already does this deterministically (same inputs, same output, every time), so it's reliable. Security — it doesn't send anything to a customer or spend money by itself. Simplicity — you already have the calculator. Cost/scalability — you'll do this often and it grows with your lead volume. **Verdict: [AUTOMATION]** for the calculation itself, but the *sending* of that quote to a customer is a separate task (see below).
- *Task: sending a quote to a customer.* Reliability — if it goes out with a mistake, that mistake is now in front of a paying customer and hard to take back. Security — yes, it's a customer-facing message. **Verdict: stays [ME]**, even though the number-crunching behind it is automated.
- *Task: deciding whether to redo a damaged order for free or offer a partial refund.* This is a judgment call about a specific relationship. **Verdict: [ME]**, permanently — no framework question past #1 even needs asking.

### WHAT YOU NEED TO UNDERSTAND

Automation in this business is not "make everything hands-off." It's "make the repetitive, low-risk parts hands-off so your limited hours go to the parts that need a human — selling, judgment calls, and relationships." Every task you'll audit today either saves you time safely, or it doesn't, and the framework above is how you tell the difference before you build anything, not after something goes wrong.

### EXERCISES

This exercise is about your real business — there's no single correct answer, so here's what a strong answer looks like instead of an answer key.

1. **List every recurring task currently happening in your business**, drawing from Modules 1-11: e.g. adding a new lead to the CRM, calculating a quote, sending a quote, following up with a non-responsive lead, updating a lead's stage, placing a supplier order, inspecting goods, scheduling delivery, collecting payment, chasing a late payment, posting on your website/socials, reviewing your prospect list, running a weekly numbers check. Aim for at least 12-15 real tasks — pull from what you actually do, not a generic list.
2. **Run each one through the five-question framework** and assign it a tag: [ME], [AUTOMATION], or [EMPLOYEE] (you don't have employees yet, so [EMPLOYEE] here just means "not now, but this is the kind of task I'd hand off first once I hire").
3. **A strong answer**: every task that touches a customer message, money leaving the business, or a committed order stays [ME] or gets flagged for an approval step; every task that's pure calculation, data entry, or internal reporting with no customer/money exposure is a real [AUTOMATION] candidate; nothing is tagged [AUTOMATION] just because "it would save time" without passing questions 1 and 2 first. If your list has more than two or three things tagged [AUTOMATION] that involve sending something to a customer or spending money, go back — that's the mistake this exercise exists to catch.

### BUSINESS IMPLEMENTATION

1. **[ME]** Write your full task audit (from the exercise) into a working document — this becomes the checklist we automate against for the rest of this module, in order of priority.
2. **[ME]** Circle the top 3-4 tasks that are clearly [AUTOMATION] candidates (pass questions 1 and 2 cleanly, and are either high-cost-in-time or growing in volume). These become Days 68-71.
3. **[ME]** Separately, list every task you circled as "touches money/customer/committed order" — you'll formalize approval rules for these on Day 72, but start naming them now.

### TODAY'S DELIVERABLES

- [ ] A written audit of 12-15+ real recurring tasks, each tagged.
- [ ] Top automation candidates for Days 68-71 identified.
- [ ] A running list of "needs approval" tasks started, ready for Day 72.

### END-OF-DAY CHECK

1. Can I explain, without looking it up, why reliability and security come before cost and simplicity in the framework?
2. Did I tag anything [AUTOMATION] that actually sends a message to a customer or spends money? (If yes, fix it now.)
3. Do I have a clear, ranked list of what to automate first, and why those four?

### NEXT DAY

**Day 68** takes the highest-priority [AUTOMATION] candidate from today's audit — quote generation — and actually builds it, linking the Module 6 pricing calculator to the Module 11 CRM.

---

### DAY 68 — AUTOMATING QUOTE GENERATION

**Module 12: AI & Automation — Lesson 2**

### TODAY'S OBJECTIVE

Stop calculating quotes in one tool and re-typing them into another. Link your Module 6 pricing calculator to your Module 11 CRM so a quote generates directly from a lead or customer record, using the exact same pricing rules every time.

### WHAT YOU NEED TO LEARN

**1. The gap you're closing.** Right now, generating a quote likely means: open the pricing calculator, work out the numbers, then manually type the result into the CRM as a new quote record. Every manual re-entry is a chance for a typo — a wrong total, a wrong deposit — to reach a customer. Linking the two tools means the CRM calls the same pricing logic directly, so the numbers can never drift apart.

**2. What "linked" means here, concretely.** From a lead or customer record in the CRM, you should be able to trigger "generate a quote," enter the order specifics (garment type(s), quantities, branding type, any discount tier), and get back: COGS, unit sell price, total order value, 50% deposit amount, balance amount — computed with your real pricing rules, saved as a new quote record attached to that lead/customer.

**3. Where the human step stays.** Per the framework from Day 67, *calculating* a quote is safe to automate — it's deterministic and doesn't leave the business. *Sending* it to the customer is not: that's a customer-facing message and stays [ME], gated behind your review. So every auto-generated quote saves as a **draft**, never as "sent."

### WHAT YOU NEED TO UNDERSTAND

This is the pattern for almost every automation you'll build from here: automate the calculation, keep the human decision. A tool that "generates and sends" in one uncontrolled step is not an upgrade — it's a new way to make a mistake in front of a customer, faster. A tool that "generates and waits for your yes" gives you the exact same time savings with none of the risk.

### EXERCISES

1. **Before building anything, decide on paper**: what fields does a quote actually need to auto-generate correctly? List them (garment type, quantity, branding type, discount tier, customer name/contact, delivery estimate...). A strong answer includes every field the pricing calculator currently needs as an input, plus whatever the CRM needs to file the quote against the right lead/customer.
2. **Decide your default quote status.** A strong answer: every auto-generated quote defaults to "Draft," never "Sent" — and you can explain why in one sentence (referencing the framework from Day 67).

### BUSINESS IMPLEMENTATION

1. **[ME]** Confirm the exact fields and pricing rules the calculator currently uses (garment costs, markup rules, discount tiers if any) so the CRM integration reuses them exactly, not a re-typed approximation.
2. **[CLAUDE CODE]** Build the link between the pricing calculator and the CRM (prompt below).
3. **[ME]** Test it against at least 2 real or realistic scenarios and confirm the numbers match what the standalone calculator produces.
4. **[AUTOMATION]** Once tested, quote calculation for any new lead/customer runs through this linked flow going forward — but sending stays [ME], every time.

### CLAUDE CODE / AI BUILDING

**What we're building:** a "Generate Quote" action inside the CRM that reuses the pricing calculator's exact logic.

**The exact prompt:**
```
Read how our pricing calculator (business/pricing/) and our CRM (business/crm/)
are currently built before changing anything, and keep the same file/data
conventions already in place.

Add a "Generate Quote" action to the CRM, usable from any lead or customer
record. It should:
- Let me enter: garment type(s), quantity per type, branding type
  (embroidery/print), and any discount tier that applies.
- Calculate COGS, unit sell price, total order value, the 50% deposit
  amount, and the balance amount, using the exact same pricing rules and
  formulas as the pricing calculator — do not duplicate or re-derive the
  logic, reuse it directly so the two tools can never disagree.
- Save the result as a new quote record linked to that lead/customer, with
  status "Draft" by default. Never set it to "Sent" automatically — I always
  review and send quotes myself.
- Show me a clear summary (all the numbers above) before confirming the
  quote is saved.

Explain what you built in plain language and tell me exactly how to test it.
```

**How to test it:** pick a real lead from your CRM, generate a quote for a plausible order (e.g. 40 shirts, embroidered, no discount), and confirm: the total, deposit, and balance match what you'd get running the same numbers through the pricing calculator directly; the quote saved with status "Draft"; it's correctly linked to that lead's record. Try a second scenario with a discount tier applied, if you have one, to confirm that logic carries through too.

### TODAY'S DELIVERABLES

- [ ] Quote-generation fields confirmed and documented.
- [ ] "Generate Quote" action built and linked to the CRM.
- [ ] At least 2 test quotes generated and manually verified against the standalone calculator.
- [ ] Confirmed every generated quote defaults to "Draft."

### END-OF-DAY CHECK

1. Do the numbers from the linked quote tool match the standalone pricing calculator exactly?
2. Does every generated quote require my review before it's marked "Sent"?
3. Could I explain to someone else why calculation is automated but sending isn't?

### NEXT DAY

**Day 69** automates the next biggest recurring task from your Day 67 audit: keeping leads and reorder-due customers from going cold, using reminders instead of messages that send themselves.

---

### DAY 69 — AUTOMATING FOLLOW-UP REMINDERS

**Module 12: AI & Automation — Lesson 3**

### TODAY'S OBJECTIVE

Automate the *reminding*, not the *messaging*: build a system that tells you exactly who needs a follow-up today — cold leads per your Module 10 cadence, and customers approaching their reorder window — without ever sending anything to a customer on its own.

### WHAT YOU NEED TO LEARN

**1. Two different reminder types, one system.**
- **Lead follow-up reminders**: based on the follow-up cadence you set in Module 10 (e.g. a first follow-up a few days after no response, a second a bit later, then a move to "cold"). The trigger is *time since last contact* on a lead that hasn't converted yet.
- **Reorder reminders**: based on the *delivery date* of a completed order plus the typical 6-12 month reorder window this business runs on (staff turnover means uniforms wear out or new hires need kit on a predictable-ish cycle). The trigger is *time since last delivery* on a closed order.

Both are really the same shape of automation: "watch a date, and tell me when it's time to act" — which is exactly why they belong in the same build.

**2. What "automated" means here.** The system checks dates and produces a list — it does not draft or send a WhatsApp message, an email, or anything else to a customer. That step stays [ME] (and gets formalized on Day 72). What's automated is the *noticing*: you no longer have to manually scroll the CRM every morning wondering who's overdue for contact.

### WHAT YOU NEED TO UNDERSTAND

The value of this automation isn't "the computer talks to my customers for me" — it's "the computer never forgets, so I never have to hold every follow-up date in my head." That's a meaningfully different, much safer thing to build, and it removes the actual bottleneck (your memory and time), not the actual relationship (which still needs your voice).

### EXERCISES

1. **Write out your real lead follow-up cadence** (from Module 10) as explicit day-counts (e.g. "day 3 after no response, day 8, then mark cold at day 15" — use your real numbers, not these). A strong answer is specific enough that a reminder system could literally check against it.
2. **Decide your reorder-reminder trigger point.** The window is 6-12 months; a strong answer picks a concrete trigger (e.g. "flag as due starting at 8 months since delivery, so I have a comfortable runway before the 12-month edge") and can explain the reasoning in one sentence.

### BUSINESS IMPLEMENTATION

1. **[ME]** Finalize your real cadence numbers and reorder-trigger point (from the exercise) — these become the rules Claude Code builds against.
2. **[CLAUDE CODE]** Build the reminder system (prompt below).
3. **[AUTOMATION]** Once built, the reminder list itself refreshes with no human step.
4. **[ME]** Acting on the list — actually contacting the person — stays yours, every time.

### CLAUDE CODE / AI BUILDING

**What we're building:** a daily/weekly "who to contact today" list inside the CRM, covering both cold-lead follow-ups and reorder-due customers.

**The exact prompt:**
```
Read how the CRM (business/crm/) currently stores leads, customers, and
orders before changing anything.

Build a follow-up reminder view that surfaces two kinds of items, each
clearly labelled:
1. Lead follow-ups: any lead not yet converted, where time since last
   contact has crossed my cadence thresholds [give your real day-counts
   from today's exercise]. Show how overdue each one is.
2. Reorder reminders: any customer whose most recent delivered order's
   delivery date is at or past [your trigger point, e.g. 8 months] from
   today, up to the 12-month outer edge. Show how long it's been.

This view should only ever read and summarize existing CRM data — it must
never send a message, email, or notification to a lead or customer, and it
must never change a lead's or order's status on its own. It's a checklist
for me, nothing more.

Explain what you built and tell me exactly how to check it's picking up
the right leads and customers.
```

**How to test it:** manually pick 2-3 leads and 1-2 delivered orders in your CRM, adjust their last-contact/delivery dates (or use real ones you already know are overdue), and confirm the reminder list correctly flags them — and correctly does *not* flag ones that aren't due yet.

### TODAY'S DELIVERABLES

- [ ] Real cadence and reorder-trigger numbers documented.
- [ ] Follow-up reminder view built and linked to the CRM.
- [ ] Tested against at least 2 lead cases and 1 reorder case, confirmed correct.
- [ ] Confirmed the system does not send anything on its own.

### END-OF-DAY CHECK

1. Does my reminder list correctly separate lead follow-ups from reorder reminders?
2. Did I verify it flags overdue items and stays quiet on ones that aren't due?
3. Am I still the one sending every actual message?

### NEXT DAY

**Day 70** cuts the time it takes to get a new lead or update into the CRM in the first place, so the reminder system on Day 69 always has accurate dates to work from.

---

### DAY 70 — AUTOMATING CRM DATA ENTRY

**Module 12: AI & Automation — Lesson 4**

### TODAY'S OBJECTIVE

Replace slow, field-by-field CRM data entry with a quick-add flow — one simple input that fills out a full lead, customer, or update record — so the system stays accurate without eating your time.

### WHAT YOU NEED TO LEARN

**1. Why this matters even though it seems minor.** Every automation you've built this week (quote generation, reminders) depends on the CRM data being complete and current. If entering a new lead or logging a call takes five minutes of clicking through fields, you'll skip it on a busy day — and then Day 69's reminder system is working off stale data. Fast, low-friction data entry is what keeps the rest of the automation honest.

**2. What "quick-add" means.** Instead of opening a form and filling in company name, contact, industry, source, notes, and status one field at a time, you type (or dictate) one short, natural line — e.g. "New lead: Thabo, ops manager at [company], security company, got the number from a referral, interested in 80 shirts" — and the system parses it into the right CRM fields, prompting you only if something critical is missing (like a contact method).

**3. Where judgment still lives.** Fields that require actual judgment — lead score/priority, deal stage — should still default to a sensible starting value (e.g. new leads start at "New," lowest priority tier) rather than have the quick-add tool guess at scoring. You confirm or adjust those, the tool just removes the *typing*, not the *thinking*.

### WHAT YOU NEED TO UNDERSTAND

This is the same principle as Day 68 in a different shape: automate the mechanical part (typing structured data into the right fields), keep the judgment part (how to score or prioritize this lead) with you. A quick-add tool that also auto-scores leads without you looking is a shortcut that quietly degrades your pipeline quality — don't build that.

### EXERCISES

1. **Draft 3 example quick-add lines** you'd realistically type for: a new lead, a note added to an existing customer after a call, and a status update on an order. A strong answer is short, natural, and contains enough information (names, what happened, next step) that a person reading it later would understand what happened without more context.
2. **List which fields should always default to a safe starting value** rather than be guessed from your quick-add text (e.g. lead score, deal stage). A strong answer explains why guessing these would be risky (ties back to the Day 67 framework — reliability).

### BUSINESS IMPLEMENTATION

1. **[ME]** Write your 3 example quick-add lines (from the exercise) — these become test cases.
2. **[CLAUDE CODE]** Build the quick-add flow (prompt below).
3. **[ME]** Test it with real entries, correct anything mis-parsed, and use it going forward instead of full manual entry.

### CLAUDE CODE / AI BUILDING

**What we're building:** a single quick-add input in the CRM that parses a short natural-language line into a properly structured lead, customer note, or order-status update.

**The exact prompt:**
```
Read how the CRM (business/crm/) currently structures leads, customers,
notes, and order records before changing anything.

Add a "quick add" input that takes one short line of plain text and turns
it into the right kind of CRM entry — a new lead, a note on an existing
customer, or an order status update — inferring which one from what I
typed. For a new lead, pull out whatever is present (company name, contact
name, industry, source, quantity/interest if mentioned) and set anything
judgment-based (lead score, deal stage) to a safe default rather than
guessing. If something essential is missing (like how to contact them),
ask me instead of leaving it blank silently.

Always show me what it parsed before saving, so I can fix anything wrong
in one step. Explain what you built and how to test it.
```

**How to test it:** run your 3 example lines from the exercise through it, check the parsed result against what you actually meant, and correct the prompt/logic with Claude Code for anything it got wrong (e.g. mixing up which field the quantity belongs in).

### TODAY'S DELIVERABLES

- [ ] Quick-add flow built and tested with 3+ real examples.
- [ ] Confirmed judgment fields default safely rather than being guessed.
- [ ] Adopted quick-add as your default way of logging new CRM activity going forward.

### END-OF-DAY CHECK

1. Is quick-add actually faster than the old field-by-field entry, for a real example?
2. Did it correctly leave lead scoring/stage to me rather than guessing?
3. Would I trust this to keep my CRM accurate on a busy day?

### NEXT DAY

**Day 71** builds on accurate, up-to-date CRM data (thanks to today's quick-add) to automate a weekly view of the whole business — leads, quotes, orders, and revenue — in one summary.

---

### DAY 71 — AUTOMATING WEEKLY REPORTING

**Module 12: AI & Automation — Lesson 5**

### TODAY'S OBJECTIVE

Build a weekly summary that pulls leads, quotes, orders, and revenue into one view automatically — so you always know where the business stands without manually digging through the CRM.

### WHAT YOU NEED TO LEARN

**1. Why this is a safe, high-value automation.** Run it back through the Day 67 framework: reliability — it's just reading and summarizing data that already exists, nothing new is created or sent; security — it doesn't touch money or a customer message, it's an internal report for you; simplicity — your CRM already holds all the data it needs; cost/scalability — the time this saves grows every week as your pipeline grows. It clears every question cleanly. This is exactly the kind of task that should be fully [AUTOMATION].

**2. What the report should actually show.** At minimum: new leads this week, quotes generated (and how many are still sitting as "Draft," unreviewed — tying back to Day 68), orders moved forward a stage, revenue collected (deposits + balances), and anything overdue from your Day 69 reminder list. The goal is a two-minute read that tells you if the week was healthy.

### WHAT YOU NEED TO UNDERSTAND

A report nobody reads is wasted automation. Keep it short and specific to decisions you actually make weekly (do I need more leads in the pipeline? are quotes sitting too long unreviewed? is revenue tracking where I expect?) rather than a dump of every number the CRM can produce. More data isn't more useful if you stop reading it.

### EXERCISES

1. **List the 5-6 numbers you'd actually want to see every week** to know if the business is healthy. A strong answer is specific (e.g. "new leads added," "quotes still in Draft after 3+ days," "orders delivered," "total revenue collected") rather than vague ("how things are going").
2. **Decide how you'll receive it** (e.g. a view inside the CRM you check each Monday, or emailed to yourself). A strong answer notes that either is fine *because it's going to you, not a customer* — this is a "runs freely" case per the approval rule you'll formalize tomorrow.

### BUSINESS IMPLEMENTATION

1. **[ME]** Confirm the exact metrics you want (from the exercise).
2. **[CLAUDE CODE]** Build the weekly report (prompt below).
3. **[AUTOMATION]** Once built, it generates with no human step — you just read it.
4. **[ME]** Acting on what it shows (chasing draft quotes, following up on stalled leads) stays yours.

### CLAUDE CODE / AI BUILDING

**What we're building:** a weekly summary view/report pulling from the CRM's leads, quotes, orders, and revenue data.

**The exact prompt:**
```
Read how the CRM (business/crm/) currently stores leads, quotes, orders,
and payment/revenue data before changing anything.

Build a weekly business summary that shows:
- New leads added this week
- Quotes generated this week, and how many quotes are still sitting as
  "Draft" for more than 3 days (unreviewed)
- Orders that moved forward a stage this week (e.g. deposit received,
  delivered)
- Total revenue collected this week (deposits + balances combined, shown
  separately)
- Anything currently overdue on the follow-up/reorder reminder list from
  Day 69

This is a read-only internal report for me — it must never send anything
to a lead or customer, and it must not change any CRM data. Make it
something I can read in under two minutes. Explain what you built and how
to generate it each week.
```

**How to test it:** generate it now against your real current CRM data, and manually cross-check 2-3 of the numbers (e.g. count new leads yourself) to confirm they match.

### TODAY'S DELIVERABLES

- [ ] Weekly summary built, covering leads/quotes/orders/revenue/overdue items.
- [ ] Numbers manually cross-checked against the CRM at least once.
- [ ] A routine set for when you'll read it each week.

### END-OF-DAY CHECK

1. Does the report cover the 5-6 numbers I actually decided I need?
2. Did I confirm the numbers are accurate against the CRM directly?
3. Is this something I'll actually read weekly, or did I over-build it?

### NEXT DAY

**Day 72** takes everything built this week (Days 68-71) and formalizes the one rule that's been running underneath all of them: nothing that touches a customer or money moves without your okay first.

---

### DAY 72 — APPROVAL STEPS FOR ANYTHING RISKY

**Module 12: AI & Automation — Lesson 6**

### TODAY'S OBJECTIVE

Write down, formally, the one rule that's protected every automation you've built this week — and check every system from Days 68-71 actually enforces it.

### WHAT YOU NEED TO LEARN

**1. The rule.** Nothing sends a customer a message, spends money, or changes a committed order without a human okay first. Not "usually" — always. This is the line between "automation that saves you time" and "automation that can quietly damage a customer relationship or the business's cash while you weren't looking."

**2. What needs approval (a human must say yes before it happens):**
- Sending a quote, invoice, or any message to a lead or customer (WhatsApp, email, or otherwise)
- Placing or confirming an order with a supplier
- Any refund, discount, or price change on a quote or committed order
- Marking an order as delivered or as paid (these are real state changes with money/relationship consequences)
- Anything posted publicly (website updates, social content) that represents the business

**3. What can run freely (no approval needed, because it fails the "customer or money" test):**
- Calculating a quote's numbers (Day 68) — but not sending it
- Generating the follow-up/reorder reminder list (Day 69) — a checklist for you, nothing more
- Quick-adding a lead or note into the CRM (Day 70) — internal data, not customer-facing
- Generating the weekly summary report (Day 71) — read-only, goes to you
- Backing up data, tagging/organizing internal records, drafting (not sending) a message for your review

**4. "Draft, then approve" is the pattern, not "block everything."** Notice the risky list is entirely about the *outbound* or *committing* action — the underlying calculation or preparation is still automated. A drafted WhatsApp follow-up message is fine to auto-generate; it just can't auto-send. This keeps almost all the time-saving while keeping 100% of the risky actions behind you.

### WHAT YOU NEED TO UNDERSTAND

An approval step isn't friction for its own sake — it's the difference between an automation mistake costing you two minutes to fix (you catch it before it goes out) versus costing you a customer relationship (it already reached them). Every extra second an approval step costs is cheap insurance against the one mistake that would actually hurt.

### EXERCISES

1. **Go through your Day 67 audit list again** and mark, for each task tagged [AUTOMATION], whether it needs an approval gate. A strong answer: anything customer-facing or money-moving gets flagged, even if it felt "automated" in your earlier pass.
2. **Write one sentence explaining, in your own words, why "calculating a quote" and "sending a quote" get different treatment** even though they're part of the same task. A strong answer references the reliability/security priority from Day 67, not just "because it feels safer."

### BUSINESS IMPLEMENTATION

1. **[ME]** Finalize the written approval rule and the two lists (needs-approval / runs-freely) as an actual reference document you can point Claude Code back to for every future automation in this course.
2. **[CLAUDE CODE]** Audit and harden Days 68-71's builds against this rule (prompt below).
3. **[ME]** Spot-check each system once more after hardening to confirm nothing sends or commits without you.

### CLAUDE CODE / AI BUILDING

**What we're building today:** not a new feature — a safety pass over everything built this week, closing any gap against the approval rule.

**The exact prompt:**
```
Review everything built in the CRM this week: the quote generator, the
follow-up/reorder reminder list, the quick-add flow, and the weekly
report.

Confirm, and fix if not already true, that:
- The quote generator never sets a quote's status to "Sent" automatically
  — only "Draft," and only I can change it to "Sent."
- The reminder list only reads and displays data — it never sends a
  message to a lead or customer, and never changes any record's status.
- Quick-add only writes internal CRM records — it never sends anything
  externally.
- The weekly report only reads and summarizes — it never changes CRM data
  or sends anything externally.
- Nowhere in any of these does the system place a supplier order, apply a
  discount/refund, or mark an order as delivered/paid without me
  explicitly confirming that action.

If you find any place where an automated step could send a customer
message, spend money, or change a committed order without my confirmation
first, stop and tell me — do not silently fix it in a way that changes
behavior I haven't approved; describe the gap and the fix you propose.
```

**How to test it:** try to make each system take a risky action end-to-end (generate a quote and check it can't be marked "Sent" without you; check the reminder list truly can't message anyone) and confirm each one stops at the human step, exactly as designed.

### TODAY'S DELIVERABLES

- [ ] Written approval rule and needs-approval / runs-freely lists finalized.
- [ ] Days 68-71's automations audited against the rule.
- [ ] Any gaps found and fixed, confirmed by re-testing.

### END-OF-DAY CHECK

1. Can I state the approval rule from memory, in one sentence?
2. Did I actually verify — not just assume — that each automation respects it?
3. Do I know exactly what's allowed to run with zero human step, and why?

### NEXT DAY

**Day 73** is the capstone: run the full automation suite end-to-end for real, define a simple weekly habit for keeping an eye on it, and take the module quiz before moving to Module 13 (Order Fulfilment).

---

### DAY 73 — AUTOMATION SUITE CAPSTONE

**Module 12: AI & Automation — Lesson 7 (Capstone)**

### TODAY'S OBJECTIVE

Run everything built this module — quote generation, follow-up/reorder reminders, quick-add, weekly reporting, and the approval gates — end-to-end on a real or realistic case, define your ongoing monitoring habit, and confirm you're ready for Module 13.

### WHAT YOU NEED TO LEARN

**A simple weekly monitoring habit.** Automation isn't "build it once and forget it" — it needs a light, regular check that it's still doing what you expect. Once a week (the same time you read the Day 71 report is a natural anchor), check:
1. **Any drafts piling up unreviewed** — quotes sitting in "Draft" too long, meaning you're the bottleneck now, not the tool.
2. **Any reminders that look wrong** — a lead flagged that shouldn't be, or a real overdue one that didn't show up.
3. **Anything in the weekly report that looks off** — a number that doesn't match your gut sense of the week.
4. **Nothing risky slipped through** — a spot-check that no message, order, or status change happened without your say-so.

This is a 5-10 minute habit, not a rebuild. Its whole job is catching drift early.

### WHAT YOU NEED TO UNDERSTAND

The automation you've built this module doesn't replace you running the business — it removes the parts of running it that were pure repetition, so your 2 hours a day go further. If you ever find yourself spending more time double-checking an automation than the manual task used to take, that's a signal to simplify or roll it back, not push through — this is the same "cost" question from Day 67, applied continuously.

### EXERCISES — MODULE QUIZ

1. In your own words, state the five-question framework from Day 67, in order.
2. What's the one rule from Day 72 that governs every automation in this business?
3. Name two tasks that are safe to fully automate, and two that must always stay [ME], with a one-sentence reason each.
4. Why does "calculating a quote" and "sending a quote" get treated differently, even though a customer sees the same document either way?

**Check your work:**
1. Reliability → Security → Simplicity → Cost → Scalability, checked in that order for every task.
2. Nothing sends a customer message, spends money, or changes a committed order without a human okay first.
3. Safe to automate (examples): calculating quote numbers, generating the follow-up/reorder reminder list, quick-add data entry, weekly reporting — all internal, read/calculate-only, no money or customer message involved. Always [ME] (examples): sending any customer-facing message, judgment calls on complaints/refunds, supplier negotiation, final quality inspection — because a mistake here reaches a customer or commits money directly.
4. Calculating is internal and reversible if wrong (you catch it before anyone sees it); sending is external and effectively irreversible once a customer has read it — the risk profile is completely different even though the end document looks the same.

### BUSINESS IMPLEMENTATION

1. **[ME]** Run one real lead through the full automated flow: quick-add the lead → generate a quote → confirm it's in "Draft" → review and send it yourself → confirm it shows correctly in next week's report.
2. **[ME]** Write down your weekly monitoring habit (the 4 checks above) somewhere you'll actually see it weekly — this is the start of your SOP library (formalized fully in Module 19).
3. **[CLAUDE CODE]** Fix anything that broke or behaved unexpectedly during today's end-to-end test.

### CLAUDE CODE / AI BUILDING

Not a new build today — if today's end-to-end test surfaces a bug or gap in any of Days 68-71's systems, describe exactly what you expected vs. what happened, and have it fixed before moving on. Don't carry a known-broken automation into Module 13, where the order tracker will depend on some of these same CRM foundations.

### TODAY'S DELIVERABLES

- [ ] Full flow tested end-to-end on one real case: lead → quote (draft) → your review/send → shows in weekly report.
- [ ] Weekly monitoring habit written down.
- [ ] Module 12 quiz completed and understood.
- [ ] Any bugs found today fixed and re-tested.

### END-OF-DAY CHECK

1. Did the full flow work end-to-end without me having to manually re-enter anything?
2. Do I have a concrete weekly habit for checking on the automation, not just a vague intention to "keep an eye on it"?
3. Am I confident nothing in this suite can send a message or spend money without me?

### NEXT DAY

**Module 13 (Order Fulfilment)** starts Day 74 by mapping your full pipeline — quote through reorder — end-to-end, then Day 75 builds an order tracker on top of the same CRM foundations you just automated around.
