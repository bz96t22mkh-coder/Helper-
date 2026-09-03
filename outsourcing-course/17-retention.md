# Module 17 — Customer Retention

**Days 98–102 of ~120.**
The last module showed why new-customer channels are ranked the way they are — this one shows, with real numbers, why the customers you already have are worth more of your attention than most beginners realize, and builds the systems that keep them coming back without you having to chase them.

---

### DAY 98 — WHY RETENTION MATTERS MORE THAN CONSTANT NEW-CUSTOMER HUNTING

**Module 17: Customer Retention — Lesson 1**

### TODAY'S OBJECTIVE

Understand, with a real worked example, why this specific business's economics make a reordering customer far more valuable than the effort of winning a new one — and why that should shape where your time goes.

### WHAT YOU NEED TO LEARN

**1. The core driver: staff turnover.** Security and cleaning companies typically see staff turnover somewhere in the 30-50%/year range (roadmap section 3) — guards and cleaners come and go, and every new hire needs uniform kit. This means an existing customer doesn't just *maybe* reorder someday — their own staffing reality creates recurring, semi-predictable demand for uniforms, on a cycle of roughly **6-12 months** (roadmap section 2), without you having to generate a new lead from scratch each time.

**2. Customer lifetime value (LTV)**, plain language: the total gross profit a customer is worth to you across the whole relationship, not just their first order. A customer who only ever places one order and never returns has an LTV equal to that one order's profit. A customer who reorders repeatedly has an LTV that compounds over years, often for very little additional effort on your part beyond staying in touch.

**3. A fully worked LTV example.** Say a security company places an initial order of **R20,000** at your business's typical **45% gross margin** — gross profit **R9,000** (COGS R11,000). Staff turnover then drives smaller top-up reorders (replacing kit for new hires, not a full re-supply) averaging **R6,000** each, at the same 45% margin — gross profit **R2,700** per reorder (COGS R3,300).

Over a 3-year relationship, reordering roughly every 9 months, that's 4 reorders after the initial order (at months 9, 18, 27, and 36):

| | Revenue | Gross profit |
|---|---|---|
| Initial order | R20,000 | R9,000 |
| Reorder 1 | R6,000 | R2,700 |
| Reorder 2 | R6,000 | R2,700 |
| Reorder 3 | R6,000 | R2,700 |
| Reorder 4 | R6,000 | R2,700 |
| **Total (3 years)** | **R44,000** | **R19,800** |

That single customer relationship is worth **R19,800 in gross profit over 3 years** — more than double the R9,000 the first order alone produced — for the cost of a handful of low-pressure check-ins (Day 79's reorder-trigger SOP) and good service, not a fresh sales campaign each time.

### WHAT YOU NEED TO UNDERSTAND

Compare that R19,800 lifetime value to the actual cost of winning a brand-new customer from scratch — the hours of outreach, discovery calls, and quoting from Modules 9-10, plus whatever Module 16 marketing spend contributed. Even a fairly time-intensive acquisition process is dwarfed by what one retained relationship is worth within a year or two. This doesn't mean stop finding new customers — new-customer growth still matters, especially early on — but it does mean a business that only chases new leads and neglects the reorder relationship is leaving most of its long-term profit on the table.

### EXERCISES

1. **Recompute the worked LTV example by hand** and confirm you reach R44,000 total revenue and R19,800 total gross profit over 3 years.
2. **A different customer**: initial order R30,000, same 45% margin, reorders averaging R8,000 every 8 months. Calculate the initial order's gross profit, one reorder's gross profit, how many reorders occur in a 2-year (24-month) relationship, and total gross profit over those 2 years.

**Check your work (exercise 2):**
- Initial gross profit: 30,000 × 0.45 = **R13,500**
- Reorder gross profit: 8,000 × 0.45 = **R3,600**
- Reorders in 24 months at 8-month intervals: month 8, 16, 24 → **3 reorders**
- Total gross profit: 13,500 + (3 × 3,600) = 13,500 + 10,800 = **R24,300**

### BUSINESS IMPLEMENTATION

1. **[ME]** Estimate a rough LTV for your own real early customers using their actual first-order numbers and your best estimate of reorder timing — even a rough estimate reframes how much attention that relationship deserves.
2. **[ME]** Look at how you've actually been splitting your time between new-lead outreach and staying in touch with delivered customers so far — an honest gap here is common and exactly what this module fixes.

### TODAY'S DELIVERABLES

- [ ] Worked LTV example hand-calculated and confirmed.
- [ ] Exercise 2 completed correctly.
- [ ] Rough real LTV estimated for at least one of your actual early customers.

### END-OF-DAY CHECK

1. Can I explain, with real numbers, why a reordering customer is worth more than a single sale?
2. Did I get exercise 2's numbers right?
3. Am I honest with myself about whether I've been neglecting existing customers in favor of only chasing new leads?

### NEXT DAY

**Day 99** takes the reorder-trigger SOP from Module 13 and has Claude Code build it into a fully automated reminder system, so no reorder window is ever missed simply because you forgot.

---

### DAY 99 — AUTOMATING THE REORDER-REMINDER SYSTEM

**Module 17: Customer Retention — Lesson 2**

### TODAY'S OBJECTIVE

Extend the reminder system built in Module 12 (Day 69) and defined in Module 13 (Day 79) into a complete, reliable reorder-management feature — so every delivered customer gets a genuine check-in inside their real reorder window, automatically surfaced, every time.

### WHAT YOU NEED TO LEARN

**1. What already exists.** Day 69 built a reminder view that flags leads needing follow-up and orders approaching their reorder window. Day 79 defined the trigger timing (starting around 8 months since delivery, per the 6-12 month window). Today isn't a new system — it's making that reorder-specific piece more complete and useful now that you understand its real value (Day 98).

**2. What "more complete" means.** Beyond just flagging that a customer is due, a genuinely useful reorder view should also show: the customer's original order details (so your check-in message can reference specifics — garment types, quantities), the estimated LTV pattern if they've reordered before (has this happened before, at what cadence), and a simple way to mark a check-in as "sent" so you don't accidentally double-message someone.

**3. The approval rule still applies, fully.** Per Module 12, this system surfaces *who* to contact and *when* — it never drafts and sends the actual reorder check-in message on its own. That message stays personal and stays [ME], because a generic auto-sent "time to reorder!" message to a real B2B relationship undermines exactly the trust this whole module is about.

### WHAT YOU NEED TO UNDERSTAND

The system's whole value is reliability — catching every customer inside their real window without depending on your memory, especially as your customer count grows past what you can track in your head. A reorder system that only works when you happen to remember to check it defeats its own purpose; today's build should make checking it a five-second glance, not a task you can put off.

### EXERCISES

1. **List what information you'd want visible for each customer flagged as reorder-due**, beyond just their name and how overdue they are. A strong answer includes original order specifics and prior reorder history, since both make the actual check-in conversation better and faster to have.

### BUSINESS IMPLEMENTATION

1. **[ME]** Confirm your real reorder-trigger timing (from Day 79) is still right, now that you understand the LTV reasoning behind it.
2. **[CLAUDE CODE]** Extend the reminder system (prompt below).
3. **[ME]** Test it against your real delivered orders and confirm it surfaces the right customers with the right context.
4. **[ME]** Continue sending every actual reorder check-in message yourself, personalized using the context the system now surfaces.

### CLAUDE CODE / AI BUILDING

**What we're building:** an extended reorder view inside the existing reminder system, adding order context, reorder history, and a "check-in sent" marker.

**The exact prompt:**
```
Read how the existing follow-up/reorder reminder view (built in Module 12,
Day 69) and the order tracker (business/crm/) currently work before
changing anything.

Extend the reorder-due section of the reminder view so that, for each
customer flagged as reorder-due (delivery date at or past [your real
trigger point, e.g. 8 months] since their most recent delivered order),
it also shows:
- That order's details: garment type(s) and quantities delivered
- Whether this customer has reordered before, and if so, how many times
  and at roughly what interval
- A "check-in sent" marker I can set myself after I've actually reached
  out, so the same customer doesn't keep showing as newly due once I've
  already contacted them

This stays a read-only, internal checklist — it must never draft or send
any message to a customer on its own. Explain what you built and how to
test it against real delivered orders.
```

**How to test it:** pick 2-3 real delivered orders (adjusting dates if needed to simulate being past the trigger point), confirm they appear correctly with accurate order details and reorder history, mark one as "check-in sent," and confirm it stops showing as newly due afterward.

### TODAY'S DELIVERABLES

- [ ] Reorder-trigger timing reconfirmed.
- [ ] Extended reorder view built, showing order context and reorder history.
- [ ] "Check-in sent" marker tested and working.
- [ ] Confirmed the system still never sends anything on its own.

### END-OF-DAY CHECK

1. Does the reorder view now give me enough context to write a genuinely personal check-in message quickly?
2. Did I confirm the "check-in sent" marker actually prevents duplicate flags?
3. Am I still the one sending every real check-in message?

### NEXT DAY

**Day 100** looks at what happens once a customer has reordered reliably several times: when and how to move them onto more formal corporate contract terms.

---

### DAY 100 — MOVING TRUSTED CUSTOMERS TO CORPORATE CONTRACTS & 30-DAY TERMS

**Module 17: Customer Retention — Lesson 3**

### TODAY'S OBJECTIVE

Define concretely what "trust earned" means before extending 30-day payment terms or a more formal corporate contract to a customer — moving off the deposit-first default only when a real track record justifies it, not just because a relationship feels comfortable.

### WHAT YOU NEED TO LEARN

**1. Why this is a real risk decision, not just a relationship reward.** The deposit-first rule (Day 1, non-negotiable early on) exists specifically to protect your cash flow from non-payment risk. Extending 30-day terms means you *are* funding that order out of your own cash until payment arrives — exactly the risk deposits were designed to prevent. This should only happen once a customer's track record makes that risk genuinely low, not as a casual favor.

**2. Concrete criteria for "trust earned"** — a customer should meet all of these before you extend formal terms, not just a couple:
- A **minimum number of completed orders** on the standard deposit-first model — a reasonable starting bar is **at least 3-4 completed, fully paid orders** over a meaningful period (not all placed in a rushed cluster).
- **A clean payment record** — balances paid on time, every time, with no history of needing to move past a friendly reminder (Day 78/84's stage 1) on any of those orders.
- **Consistent, predictable order volume** — a company that orders somewhat regularly (tied to their real staffing needs) is a safer bet for extended terms than one with sporadic, unpredictable ordering.
- **A real, verifiable business** — an established company (verifiable registration, a real operating history, not a brand-new entity with no track record of its own) reduces the risk further.

**3. What the terms actually look like when extended.** A simple, written agreement: an agreed credit limit (tied to their typical order size — don't extend a limit larger than what you could comfortably absorb if it went unpaid), a clear 30-day payment window from delivery/invoice date, and an explicit statement that missing that window reverts them to deposit-first on future orders. Put this in writing — the same discipline as your original quote terms (Module 6), not a verbal understanding.

**4. This can be revoked.** Extended terms are a privilege earned by track record, not a permanent status — if a customer who's been on 30-day terms starts paying late, it's reasonable and appropriate to revert them to deposit-first, communicated respectfully (per Module 14's tone) rather than treated as a punishment.

### WHAT YOU NEED TO UNDERSTAND

The temptation with a good, friendly relationship is to extend trust based on how the relationship *feels*, rather than on an actual track record. The criteria above exist precisely so that decision isn't made on a good mood — a real business risk deserves a real, consistent bar, applied the same way to every customer, however much you like them personally.

### EXERCISES

1. **Apply the criteria to a realistic scenario**: a cleaning company has placed 4 orders over 14 months, all paid in full, with balance paid within 2-3 days of delivery each time (never needing even a friendly reminder), and has a registered, established business. Should they qualify for 30-day terms? A strong answer says yes — they meet the order-count, clean-payment, consistency, and verifiability bars — and can state what credit limit would be reasonable relative to their typical order size.
2. **Second scenario**: a security company has placed 2 large orders in the last 3 months, both eventually paid but only after a firm reminder (Day 84 stage 2) each time. Should they qualify? A strong answer says no — despite order volume, the payment record isn't clean, which is the specific criterion this decision protects, and extending terms here increases real risk rather than rewarding a track record that doesn't yet exist.

### BUSINESS IMPLEMENTATION

1. **[ME]** Write your own real criteria (using the guidance above, adjusted if you want a stricter or different bar) as a formal internal policy.
2. **[ME]** Draft a simple written 30-day-terms agreement template, ready for the first customer who qualifies.
3. **[PROFESSIONAL]** For any credit-terms agreement above a size that would meaningfully hurt the business if unpaid, have a qualified professional review the written terms before you rely on them — a verbal or informal agreement offers you far less protection than a signed one.

### TODAY'S DELIVERABLES

- [ ] Written trust-earned criteria finalized as internal policy.
- [ ] 30-day-terms agreement template drafted.
- [ ] Both exercise scenarios worked through correctly.

### END-OF-DAY CHECK

1. Do I have concrete, written criteria for extending terms, rather than a gut feeling?
2. Could I correctly apply those criteria to a real customer today?
3. Do I understand that extended terms can and should be revoked if the payment record changes?

### NEXT DAY

**Day 101** looks at growing revenue from customers you've already earned trust with — systemizing referrals (building on Module 16) and identifying real upsell and cross-sell opportunities.

---

### DAY 101 — SYSTEMIZING REFERRALS, UPSELLS & CROSS-SELLS

**Module 17: Customer Retention — Lesson 4**

### TODAY'S OBJECTIVE

Build a repeatable process for turning existing, satisfied customers into two additional sources of growth: referrals to new customers, and upsells/cross-sells within the relationship you already have.

### WHAT YOU NEED TO LEARN

**1. Referrals — the retention-stage version.** Module 16, Day 95 already built the referral ask into your delivery/follow-up process. At the retention stage, add a second natural moment: the reorder check-in itself (Day 99) is another genuine, low-pressure opportunity — a customer who's reordering is by definition still satisfied, which is exactly when a referral ask lands best.

**2. Upsells — more from the same customer, same relationship.** Ideas specific to this niche:
- Seasonal additions (jackets, beanies, rain gear for winter months, alongside their core shirt/uniform order)
- Adjacent PPE or accessories a security or cleaning company might also need (subject to the compliance considerations flagged for construction-style PPE in the roadmap — stay within what you're actually set up to source and qualify properly, don't overreach into a category needing certifications you haven't verified)
- Branded items beyond core uniforms for the same company (e.g. a small run of branded items for a client event, if the customer's own business does client-facing work)

**3. Cross-sells — extending into an adjacent niche via an existing relationship.** The roadmap flags restaurants/hospitality as a natural **third niche** to add once your sourcing and fulfilment process is proven, using the same sales motion but different SKUs (aprons, chef wear). If an existing security or cleaning company customer has any connection to that space (rare, but possible — some larger operators diversify), it's worth a mention; more realistically, this cross-sell mostly matters for your Module 16 referral network, not this specific customer's own order.

**4. Discipline: don't oversell a good relationship.** An upsell or cross-sell offer should be genuinely relevant to what the customer's business actually needs — a pushy, irrelevant add-on offer risks the trust this whole module has been building. Offer once, clearly, and let them decide; don't repeat an offer they've already declined.

### WHAT YOU NEED TO UNDERSTAND

Referrals, upsells, and cross-sells all draw on the same underlying asset: trust built through consistent, reliable fulfilment (Module 13) and honest service (Module 14). None of these techniques work as a substitute for that — they work *because* of it. If delivery and service aren't consistently solid, none of this module's systems will produce much, regardless of how well they're built.

### EXERCISES

1. **Draft one realistic upsell offer** for a real or realistic existing customer (e.g. adding winter jackets to a security company's next reorder). A strong answer is specific to a real, plausible seasonal or operational need, not a generic "want to buy more?"
2. **Identify where in your fulfilment/retention process each of these asks now lives**: referral ask, review ask, upsell offer. A strong answer names a specific trigger point for each (e.g. referral/review at follow-up, upsell at reorder check-in) rather than leaving any of them undefined.

### BUSINESS IMPLEMENTATION

1. **[ME]** Finalize your upsell/cross-sell ideas relevant to your real product range and real customers.
2. **[ME]** Confirm each ask (referral, review, upsell) has a specific, defined trigger point in your process, not left to memory.
3. **[ME]** Draft your reorder-check-in referral ask (building on Day 95's script) for use at that second natural moment.

### TODAY'S DELIVERABLES

- [ ] Real upsell/cross-sell ideas documented.
- [ ] Referral ask added at the reorder check-in trigger point.
- [ ] All three asks (referral, review, upsell) mapped to specific trigger points in the process.

### END-OF-DAY CHECK

1. Do I have real, relevant upsell ideas rather than generic ones?
2. Does every ask (referral, review, upsell) have a defined moment it happens, not left to chance?
3. Am I confident these asks stay genuine and low-pressure, not pushy?

### NEXT DAY

**Day 102** is the capstone: confirm the full retention system is live end-to-end, take the module quiz, and move to Module 18 (Hiring & Scaling).

---

### DAY 102 — RETENTION SYSTEM CAPSTONE

**Module 17: Customer Retention — Lesson 5 (Capstone)**

### TODAY'S OBJECTIVE

Confirm the full retention system — LTV understanding, the automated reorder-reminder system, terms-extension criteria, and the referral/upsell process — is live and working together, and that you're ready to move into Module 18.

### WHAT YOU NEED TO LEARN

**Why retention is the hinge between Modules 1-16 and what comes next.** Everything before this module was about winning and fulfilling individual orders well. Everything from Module 18 onward (hiring, SOP library, dashboard, scaling) assumes a business that's already retaining customers reliably — you can't scale a leaky bucket. This module is what turns first customers into a durable base the rest of the course builds on top of.

### EXERCISES — MODULE QUIZ

1. In the Day 98 worked example, why was the 3-year LTV more than double the initial order's gross profit?
2. What does the reorder-reminder system do automatically, and what does it deliberately never do on its own?
3. Name the four criteria a customer should meet before being extended 30-day terms.
4. Why do referrals, upsells, and cross-sells all depend on the same underlying thing?

**Check your work:**
1. Because staff turnover drove multiple smaller reorders (4, at ~9-month intervals) on top of the initial order, and each reorder added its own gross profit — the relationship's total value compounds well beyond the first sale.
2. It automatically surfaces which customers are reorder-due, with order context and history; it never drafts or sends the actual check-in message to the customer — that stays personal and manual, per the Module 12 approval rule.
3. A minimum number of completed, fully paid orders (e.g. 3-4); a clean payment record with no history of needing more than a friendly reminder; consistent, predictable order volume; a real, verifiable business.
4. Because all three only work when trust has already been built through consistent, reliable fulfilment and honest service — they amplify a good relationship, they don't create one.

### BUSINESS IMPLEMENTATION

1. **[ME]** Confirm the extended reorder-reminder system (Day 99) is live and correctly surfacing real customer data.
2. **[ME]** Confirm your written terms-extension criteria (Day 100) and referral/upsell trigger points (Day 101) are documented in one place alongside the rest of your SOPs.
3. **[ME]** Review your real customer base against the LTV lens from Day 98 — are you giving retained relationships the attention their real value justifies?

### TODAY'S DELIVERABLES

- [ ] Reorder-reminder system confirmed live and accurate.
- [ ] Terms-extension criteria and referral/upsell trigger points documented together.
- [ ] Module 17 quiz completed and understood.
- [ ] Honest review of time/attention given to existing vs. new customers completed.

### END-OF-DAY CHECK

1. Is my reorder-reminder system genuinely live and trustworthy, not just built and forgotten?
2. Do I have clear, written criteria for extending terms, and clear trigger points for referral/upsell asks?
3. Am I confident retention is now a real system in this business, not just good intentions?

### NEXT DAY

**Module 18 (Hiring & Scaling)** starts next, looking at when to make your first hire, who to hire first, and what stays automated instead of staffed — now that the business has a proven pipeline, a full automation suite, and a retention system holding it all together.
