# Module 1 — Understanding the Outsourcing Business

**Days 1–5 of ~120.**

This module gets the fundamentals locked in before any money moves: how the business actually makes money, the model you're running versus the alternatives, the mistakes that sink beginners, the real economics of one order worked end to end, and a first-draft business name — so Module 2 starts with a real foundation, not a guess.

---

### DAY 1 — What Outsourcing Actually Is & How This Business Makes Money

**Module 1: Understanding the Outsourcing Business — Lesson 1**

### TODAY'S OBJECTIVE

Understand exactly how your business will make money before you spend a single rand, learn the handful of terms you'll use every day from now on, and get your real workspace set up so tomorrow starts with a business, not a blank page.

### WHAT YOU NEED TO LEARN

**1. What "outsourcing" means for this business.** You will not own a factory, embroidery machine, or warehouse. You take an order from a customer (say, a cleaning company that needs 60 branded polo shirts), then you "outsource" the actual production to two specialists: a **blank-garment wholesaler** (who supplies the plain polo shirts in bulk, cheaper than retail) and a **decorator** (who embroiders or prints your customer's logo onto them). You manage the relationship, the quality, and the money. This is exactly how most uniform/workwear suppliers actually operate — very few of them own their own garment factories.

**2. The money flow, step by step:**

```
1. Customer agrees to an order and pays you a 50% DEPOSIT
2. You order blank garments from your wholesaler (paid for out of the deposit — never your own savings)
3. You send them to your decorator for branding (embroidery/print)
4. You personally inspect quality before delivery
5. You deliver to the customer
6. Customer pays the remaining 50% BALANCE
7. Your profit = total customer payment − (blank garments + branding + delivery costs)
```

Notice: your own cash is never at risk for the *production cost* of an order, because the deposit funds it. This single rule is what separates a business that survives from one that gets crushed by cash-flow problems in month two. You'll build this into every quote from Module 6 onward.

**3. Core money terms, explained simply:**

| Term | Plain-English meaning |
|---|---|
| **COGS** (cost of goods sold) | What it actually cost you to produce what you sold — blanks + branding + any packaging, for that specific order |
| **Gross profit** | Customer payment − COGS, for one order |
| **Gross margin** | Gross profit expressed as a % of what the customer paid (not of your cost — this trips up almost every beginner, see the exercise below) |
| **Markup** | How much you add on top of your cost, expressed as a % of your *cost* |
| **MOQ** (minimum order quantity) | The smallest quantity a supplier (or you) will accept for an order — below this, per-unit cost is too high to be worth it |
| **Lead time** | How long, from order to ready-for-delivery, production actually takes |
| **Blank garment** | An unbranded plain item (shirt, golfer, overall) before any logo/embroidery is added |
| **Turnaround time** | Total time from customer deposit to delivered goods (includes lead time + your QC + delivery) |

### WHAT YOU NEED TO UNDERSTAND

The single most common beginner mistake in this list of terms: **confusing markup and margin.** They are not the same number, and mixing them up quietly destroys your profit. Here's the difference, worked through:

- Your cost (blank shirt + embroidery) = **R100**.
- You want a **50% markup**: sell price = R100 + (50% of R100) = **R150**.
- Check the margin on that R150 sale: gross profit = R150 − R100 = R50. Margin = R50 ÷ R150 = **33%**, not 50%.

If you instead *think* you're getting a 50% margin and price for that: sell price needed = R100 ÷ (1 − 0.50) = **R200**. That's a very different number from R150. Mixing these up means you could be pricing an entire order almost 25% too cheap without ever noticing — and at volume, that gap is the difference between a business that pays you a salary and one that quietly loses money on every order. From now on, when this course says "margin," it always means gross profit ÷ selling price. When it says "markup," it always means gross profit ÷ cost. We'll build a calculator in Module 6 so you never have to do this math by hand — but you need to understand it before you trust a tool to do it for you.

### EXERCISES

Do these on paper or in a notes app — no calculator shortcuts, work the numbers yourself first, then you can check with a calculator.

1. A blank workwear shirt + embroidery costs you **R120** landed (i.e. including everything to get it embroidered and in your hands). You want a **60% markup**. What's your sell price? What's the resulting margin %?
2. A customer wants to pay exactly **R250** per shirt. Your landed cost is **R120**. What margin % are you actually getting at that price? Is that markup or margin, and what's the difference?
3. You get an order for 60 shirts at R250 each. Total order value = R15,000. At a 50% deposit, how much do you collect before you order anything from your supplier? If your total COGS for the whole order is R7,200, what's your total gross profit, and what's your margin %?
4. True or false, and explain why in one sentence: "If I raise my markup from 50% to 60%, my margin also goes up by exactly 10 percentage points."

(No answer key given here on purpose — bring me your answers and reasoning next session and I'll tell you exactly what's right, what's off, and why, before we move on.)

### BUSINESS IMPLEMENTATION

**[ME]** — real tasks for your actual business, not a simulation:

1. **Brainstorm 5-8 possible business names.** Keep them short, easy to say over the phone, and credible for a B2B buyer (a security-company ops manager, not a consumer). Avoid names that only make sense in English if you plan to expand regionally later. Write them in `business/decisions-log.md` under a new dated entry — I'll help you narrow this down properly in Module 7 (Branding), so this is a first draft, not a final decision.
2. **Decide your home city/region for initial outreach** — the roadmap recommends security + cleaning companies as your starting niche; you'll need a specific geographic area to make that concrete. Record it in the decisions log.
3. **Start your prospect list** (`business/prospect-list.md`) — spend 15-20 minutes finding real local security and cleaning companies using Google Maps, PSIRA's registered-provider list, and local directories, per the instructions already in that file. Target at least 10-15 rows today; the full 50 is a Module 2 target, not today's.

### CLAUDE CODE / AI BUILDING

**What we're building today:** your business workspace — already done for you in this session, so you can see exactly what "Claude Code builds it" looks like in practice.

**What I built:**
- `/business/README.md` — explains what this folder is and how it's used going forward.
- `/business/decisions-log.md` — a running, dated record of every real decision (name candidates go here today).
- `/business/prospect-list.md` — your real target-customer tracker, with instructions and a starter table.
- Empty folders (`pricing/`, `suppliers/`, `customers/`, `marketing/`, `finance/`, `website/`, `crm/`) that later modules will fill with real tools.

**The exact prompt you'd give Claude Code to reproduce this yourself on a future project** (this is the reusable pattern — save it):
```
Set up a business workspace for a new company. Create:
- /business/README.md explaining the folder's purpose
- /business/decisions-log.md as a dated decision log, with a template
  entry format (Decision / Reasoning / Date)
- /business/prospect-list.md as a target-customer tracker with columns:
  company name, industry, contact info, estimated size, notes, status
Keep everything as plain markdown files, no code, no dependencies.
```

**How to test it:** open `business/decisions-log.md` and `business/prospect-list.md` right now and confirm you understand every column and section — if anything is unclear, tell me and I'll fix the file, which is exactly how you'll handle every future Claude Code output in this course: read it, test it against what you actually need, report back what's wrong.

### TODAY'S DELIVERABLES

- [ ] You can explain, in your own words, the 7-step money flow from deposit to profit.
- [ ] You can state the difference between markup and margin without looking it up.
- [ ] Exercises 1-4 attempted (answers ready to report next session).
- [ ] 5-8 business name candidates written in `business/decisions-log.md`.
- [ ] Home city/region for outreach recorded in `business/decisions-log.md`.
- [ ] At least 10-15 real prospects added to `business/prospect-list.md`.

### END-OF-DAY CHECK

Answer these to yourself before closing today's session — if any answer is "no" or "not sure," flag it when you report back:

1. Could I explain to a friend, in 60 seconds, how this business makes money without owning a factory?
2. Do I know why collecting a deposit before ordering from a supplier matters?
3. Do I know the difference between a 50% markup and a 50% margin, and could I show it with numbers?
4. Do I have a real prospect list started, with real company names in it — not a placeholder?

### NEXT DAY

**Day 2 (Module 1, Lesson 2)** depends on today's exercises and prospect list: we'll go deeper on outsourcing business models (the exact variant you'll run vs. the alternatives), walk through your exercise answers, and start validating real demand using the prospect list you started today. Bring: your exercise answers, your name candidates, and your prospect list so far.

---

### DAY 2 — Business Model Variants & Your Exercise Answers

**Module 1: Understanding the Outsourcing Business — Lesson 2**

### TODAY'S OBJECTIVE

Confirm, with real comparisons, that the deposit-first reseller model is the right one to run — not just because the roadmap says so, but because you understand what each alternative would cost you. Then lock in yesterday's math with full worked answers, and extend into MOQs and lead times with a real numeric example.

### WHAT YOU NEED TO LEARN

**1. The model you're running, versus the realistic alternatives.** There isn't one "right" way to run an outsourced uniform business — there are trade-offs. Here's the honest comparison:

| Model | How it works | Pros | Cons | Verdict |
|---|---|---|---|---|
| **Deposit-first reseller (yours)** | Take 50% deposit, order from supplier with that cash, inspect before delivery, collect balance on delivery | Your cash is never at risk for production cost; you control quality before it reaches the customer; low capital to start; scales without owning equipment | You depend on suppliers' lead times; margin is lower than owning your own production | **Recommended — this is what the rest of this course builds** |
| **Pure dropship, no QC** | Customer orders, you forward the order straight to a supplier who ships directly to the customer, you never see or inspect the goods | Fastest to set up, zero handling effort | One bad batch (wrong size, sloppy embroidery, a torn seam) reaches the customer with your name on it and no chance for you to catch it first — in B2B, one bad delivery can end a corporate account permanently, and word travels between owners in the same industry | Rejected for this business — too risky for B2B relationships you're trying to build for the long term |
| **Holding inventory upfront** | Buy blank garments in bulk ahead of demand, brand them once you have a confirmed order, or even pre-brand generic stock | Faster turnaround once you have stock on hand; can look more "established" | Ties up your own capital in stock that might not sell in that exact size run or style; storage becomes a real cost and problem; you're carrying the very risk the deposit-first model exists to avoid | Rejected for now — revisit only once you have proven, predictable repeat-order volume in specific sizes (later module, once real data exists) |
| **Buying your own embroidery machine day one** | Skip the decorator, do the branding yourself | No decorator markup eating your margin; full control over turnaround | Real capital outlay (machine, training, maintenance) before you've sold a single order; a beginner mistake spending on equipment before proving demand; a skill you don't have yet, learned on customer orders that must be right first time | Rejected for now — this is a legitimate move once volume justifies it (later module), never a Day 1 decision |

The pattern across all three rejected alternatives: each one reintroduces a risk the deposit-first model exists specifically to remove — either cash risk (you fund production before being paid), quality risk (nobody but the end customer inspects the goods), or capital risk (money tied up in equipment or stock before demand is proven). Every business model decision in this course gets tested against the same question: **does this put my own money or reputation at risk before the customer has committed theirs?**

**2. MOQs and lead times, worked example.** Your decorator (the person/company that embroiders your logos) has an MOQ of 20 units per design — below that, their setup cost per garment is too high for them to bother, or they charge a steep small-order fee to cover it. Suppose a prospect wants only 12 golf shirts. You have two real options: (a) tell them the practical minimum is 20 and offer to help them get there (e.g. suggesting a few spares for turnover, which most security/cleaning companies actually want anyway), or (b) accept the order at a higher per-unit price that absorbs the decorator's small-order fee. Neither is "wrong" — it depends on the relationship and whether this could become a repeat account. What's wrong is not knowing your MOQ and promising a price that doesn't cover the real cost.

Lead time is different from MOQ — it's about time, not quantity. If your blank-garment wholesaler takes 4 business days to deliver stock to your decorator, your decorator takes 5 business days to embroider it, you need 1 day to personally inspect it, and delivery to the customer takes 2 days, your **minimum realistic turnaround is 4 + 5 + 1 + 2 = 12 business days.** Never quote a customer your fastest possible time — always add a buffer (a supplier running one day late, a public holiday, your own schedule) before you promise a delivery date. This becomes second nature once you've done it a few times; for now, always add it consciously.

### WHAT YOU NEED TO UNDERSTAND

**Day 1 exercise answer key — full worked solutions.**

**Exercise 1:** Cost = R120, markup = 60%.
Sell price = R120 × 1.60 = **R192**.
Margin = (R192 − R120) ÷ R192 = R72 ÷ R192 = **37.5%**.
(Notice the pattern from Day 1: a 60% markup does not produce a 60% margin — it produces a lower number, because margin is measured against the bigger figure, the sell price.)

**Exercise 2:** Customer pays R250, cost = R120.
Margin = (R250 − R120) ÷ R250 = R130 ÷ R250 = **52%**.
This is a margin, because it's expressed as a % of the selling price (R250), not the cost. If you calculated it as a markup instead, it would be R130 ÷ R120 = **108.3%** — a completely different-looking number for the exact same deal. This is exactly why the terms must never be mixed up: someone could tell you "I'm getting 52% on this deal" and someone else could tell you "I'm getting 108% on this deal" and they could be describing the identical sale.

**Exercise 3:** 60 shirts × R250 = **R15,000** total order value.
Deposit at 50% = R15,000 × 0.50 = **R7,500** — collected before you place a single supplier order.
Total COGS = R7,200.
Gross profit = R15,000 − R7,200 = **R7,800**.
Margin = R7,800 ÷ R15,000 = **52%**.

**Exercise 4:** **False.** A markup increase from 50% to 60% does not raise margin by 10 percentage points. Worked proof, using a R100 cost in both cases:
- At 50% markup: sell price = R150. Margin = R50 ÷ R150 = 33.3%.
- At 60% markup: sell price = R160. Margin = R60 ÷ R160 = 37.5%.
- The margin only moved from 33.3% to 37.5% — a gain of **4.2 percentage points**, not 10. Markup and margin move together, but never at the same rate, because margin's denominator (sell price) keeps changing as markup changes. This is exactly why you should never estimate margin in your head from a markup number — always calculate it, or let the Module 6 calculator do it.

### EXERCISES

1. Your decorator's MOQ is 20 units per design. A prospect wants exactly 12 branded golf shirts, and it's their first order with you — no track record yet of them becoming a repeat account. Decide what you'd do and write 2-3 sentences of reasoning. (Open-ended — there's no single correct answer here. A strong answer names the trade-off explicitly: taking the small order at a fair small-order rate protects the relationship and might turn into a repeat account, while insisting on 20 protects your margin discipline; a strong answer picks one and explains why, rather than avoiding the decision.)

2. Your supplier chain looks like this: blank garment sourcing = 4 business days, embroidery = 5 business days, your own QC = 1 day, delivery = 2 days. Calculate the minimum realistic turnaround time. Then decide how much buffer you'd add before quoting a customer a delivery date, and state your final quoted number.

**Check your work:**

- Question 2: Minimum turnaround = 4 + 5 + 1 + 2 = **12 business days**. A reasonable buffer is roughly 25-30%, or a flat 3-4 extra days, to absorb a late supplier delivery, a public holiday, or your own schedule slipping — giving a quoted turnaround of around **15-16 business days (about 3 calendar weeks)**. There's no single "correct" buffer number, but the principle is fixed: never promise your fastest-possible time, and always round up, never down, when you're not sure.

### BUSINESS IMPLEMENTATION

**[ME]**

1. Mark your own Day 1 exercise answers against the answer key above. Where you got something wrong, write one sentence in `business/decisions-log.md` about what specifically confused you — this becomes useful later when you're explaining pricing to a future employee.
2. Add a dated entry to `business/decisions-log.md` confirming, in your own words, which business model you're running and why — even though the roadmap already recommends it, writing your own reasoning means you actually understand it, not just agree with it.
3. Continue `business/prospect-list.md` — add at least 10 more real companies today (running total 25+). Module 2 needs volume to validate demand against, so this list is not busywork.

### TODAY'S DELIVERABLES

- [ ] Day 1 exercises marked against the answer key, with any confusion noted.
- [ ] Business model decision logged in `business/decisions-log.md` in your own words.
- [ ] Exercise 1 (MOQ judgment call) and Exercise 2 (lead time calculation) completed.
- [ ] Prospect list at 25+ real companies.

### END-OF-DAY CHECK

1. Can I explain, without looking, why pure dropshipping is riskier for this business than the deposit-first model?
2. Do I understand why a 10-point markup increase doesn't mean a 10-point margin increase?
3. Do I know the difference between an MOQ problem and a lead time problem?
4. Is my prospect list real, growing, and usable for outreach — not placeholder rows?

### NEXT DAY

**Day 3** depends on nothing new from today specifically — bring your general understanding of the money flow and model, because we're going deep on the mistakes that sink businesses like this one, using realistic scenarios.

---

### DAY 3 — Risks & Beginner Mistakes, In Depth

**Module 1: Understanding the Outsourcing Business — Lesson 3**

### TODAY'S OBJECTIVE

Move from knowing the list of risks and mistakes (roadmap sections 7-8) to actually recognizing them when they show up in real conversations — because they rarely announce themselves as "a mistake," they show up as a reasonable-sounding request from a customer or a shortcut that feels harmless in the moment.

### WHAT YOU NEED TO LEARN

Every mistake below follows the same shape: a real-world moment creates social or time pressure to skip a boring process step, and skipping it is what actually causes the damage — not the moment itself.

**Scenario A — "Just start, I'll pay you after."** A prospect you like says: "We urgently need 15 jackets by Friday, no time for the paperwork, just get going and I'll sort payment once it's done." This is the deposit risk showing up in real life. If you say yes, you're funding their order out of your own pocket, and if the job changes, the deadline slips, or they simply don't pay, you carry all of the loss. **The prevention:** the deposit rule has no "just this once" exception — a fast-tracked order can still be confirmed and deposited in five minutes over WhatsApp (a short message stating quantity, price, and delivery date, with proof of a deposit payment) even under time pressure. The first time you skip it "because it was urgent," it quietly becomes the new normal for that customer, and possibly for the next one who hears you did it.

**Scenario B — the size dispute with no size chart.** You deliver 60 shirts. The customer calls: "Half of these run too small — we need them redone." Without a documented, agreed size chart that the customer confirmed before you ordered, this is now your word against theirs, and in a dispute like that, you're the one who eats the cost of getting it right. **The prevention:** a written size chart (S/M/L/XL/XXL with the actual measurements for the garment you're using) that the customer explicitly confirms — even a simple "please confirm these sizes are correct" WhatsApp message with their reply counts — before you place the supplier order. It costs you two minutes. It's the difference between "here's what you signed off on" and an argument you can't win.

**Scenario C — the supplier who lets you down with no backup.** Your decorator tells you, two days before a big delivery to a corporate account, that they're two weeks behind. You have no backup decorator lined up. Now you're either late to a customer who's counting on you, or scrambling to find and vet a new supplier under pressure — the worst time to be doing that. **The prevention:** always have a second, vetted decorator and a second blank-garment wholesaler you could call on short notice, even if you never use them. You don't need to split your orders between them day to day — you need to know they exist and roughly what they charge, so a crisis doesn't become a scramble. (Module 4 covers this properly.)

**Scenario D — underpricing to win the first deal.** You're excited about your first real prospect and offer a discount "just to get the foot in the door" without recalculating what that does to your margin. You win the deal — then discover the discounted price barely covers your real costs, and the customer now expects that price on every reorder, because you never told them it was a one-time special. **The prevention:** any discount is a conscious, calculated decision made using your pricing tool (Module 6), not a panic reaction to a nervous moment in a sales conversation — and if you do offer an introductory discount, you say so explicitly, in writing, so the customer knows the standard rate going forward.

**Scenario E — no follow-up, and a lead goes cold.** A prospect responds enthusiastically on WhatsApp, you mean to follow up in two days, life happens, and three weeks later you remember — by which point they've gone with someone else, or a repeat customer's reorder window (driven by staff turnover) has quietly passed without you noticing. **The prevention:** even before the CRM gets built in Module 11, a simple spreadsheet column for "next follow-up date" on every lead, checked daily, closes this gap. The system doesn't need to be sophisticated to work — it needs to exist and get checked.

### WHAT YOU NEED TO UNDERSTAND

Notice the common thread: none of these five mistakes require bad luck, a dishonest customer, or a bad supplier to hurt you. Each one only needs you to skip a boring, two-minute process step under pressure, once. The businesses that survive aren't the ones that never face pressure — they're the ones that keep doing the boring step anyway, especially when it feels awkward (asking a friend's referral for a deposit, insisting on size sign-off from a busy operations manager who "doesn't have time"). Every SOP (standard operating procedure — a written, repeatable step you follow the same way every time) this course builds exists to make the disciplined choice the easy, default choice, not something you have to remember to do under pressure.

### EXERCISES

1. Using Scenario A above: what exactly would you say to that customer, in writing, that still gets them their urgent order while still protecting your deposit rule? Draft the actual message. (Open-ended. A strong answer is short, friendly, doesn't lecture the customer, and still clearly states quantity, price, and "50% deposit to confirm" before anything is ordered.)

2. Using Scenario C: your primary decorator is now two weeks behind on an order due to a corporate customer this Friday. You have no backup decorator yet. What do you do in the next 24 hours, and what do you change permanently after this? (Open-ended. A strong answer separates the immediate fix — communicate proactively with the customer before they find out from the delay itself, and look for emergency capacity — from the permanent fix — qualifying a backup decorator this month, not "eventually.")

3. You deliver 15 shirts at R250 each (landed cost R130 each) and the customer disputes the sizing, with no signed-off size chart to point to. You agree to redo the whole order at your own cost to save the relationship. What was your gross profit on the original sale, and what's your actual profit or loss once you've eaten the cost of the redo?

**Check your work:**

- Original sale: revenue = 15 × R250 = R3,750. COGS = 15 × R130 = R1,950. Gross profit on the original sale = R3,750 − R1,950 = **R1,800** (a 48% margin — looked healthy).
- The redo means paying for the garments and embroidery a second time: an extra R1,950 in COGS, with no extra revenue collected.
- Total COGS across both rounds = R1,950 + R1,950 = R3,900. Revenue is still R3,750.
- Final result: R3,750 − R3,900 = **a R150 loss** on an order that looked like a solid R1,800 profit before the dispute. One missing size-chart sign-off turned a profitable order into a loss — this is exactly why Scenario B's two-minute prevention step matters more than it looks like it does.

### BUSINESS IMPLEMENTATION

**[ME]**

1. Draft a one-page size chart for the garment type you expect to sell most (e.g. golf shirts or overalls) — standard sizes (S-XXL) with chest/length measurements. You don't need exact supplier measurements yet (Module 4-5 will refine this against real supplier spec sheets) — a first draft is enough to understand the practice. Note it in `business/decisions-log.md` as a task started, to be finalized once you have a real supplier's size guide.
2. Write a short note in `business/decisions-log.md` naming which of the five scenarios above feels like the one you'd personally be most tempted to skip under pressure, and why — self-awareness here is what actually prevents it happening for real.

### TODAY'S DELIVERABLES

- [ ] Exercises 1-3 completed, including the redo-cost calculation.
- [ ] First-draft size chart started.
- [ ] Self-awareness note logged in `business/decisions-log.md`.

### END-OF-DAY CHECK

1. Can I name all five scenarios and, for each, the specific two-minute practice that prevents it?
2. Do I understand how a single missing size-chart sign-off turned a profitable order into a loss?
3. Have I honestly identified which mistake I'm personally most likely to make under pressure?

### NEXT DAY

**Day 4** builds directly on today's cost discipline: we'll walk one complete real order all the way from quote to profit banked, with full arithmetic, then take a first look at how individual order profit rolls up into whole-business profit.

---

### DAY 4 — Full Unit Economics of One Real Order

**Module 1: Understanding the Outsourcing Business — Lesson 4**

### TODAY'S OBJECTIVE

Walk one complete, realistic order all the way from quote to profit banked, with every number verified — so the money flow from Day 1 stops being an abstract diagram and becomes a calculation you could run on any real order from Module 2 onward. Then take a first, light look at how gross profit at the single-order level relates to net profit at the whole-business level.

### WHAT YOU NEED TO LEARN

**One full order, worked end to end.** A security company wants 60 branded golf shirts.

**Step 1 — Quote.** You price the order at R280 per shirt.
Order value = 60 × R280 = **R16,800**.

**Step 2 — Deposit collected.** 50% deposit = R16,800 × 0.50 = **R8,400**, collected before you order anything.

**Step 3 — Costs.** Your landed cost per shirt (blank garment R95 + embroidery R35) = **R130 per unit**.
Total product COGS = 60 × R130 = **R7,800**.
Delivery for this order (flat, not per-unit) = **R400**.
Total order costs = R7,800 + R400 = **R8,200**.

**Step 4 — Cash-flow check.** Your R8,400 deposit comfortably covers your R8,200 in total order costs, with R200 left over before the customer has even paid the balance — this is the deposit-first model doing exactly what it's designed to do. You were never at risk of funding this order yourself.

**Step 5 — Delivery and balance.** You inspect, deliver, and collect the remaining balance: R16,800 − R8,400 = **R8,400**.

**Step 6 — Profit.** Gross profit = Revenue − Total costs = R16,800 − R8,200 = **R8,600**.
Margin = R8,600 ÷ R16,800 = **51.2%**.
Markup (for comparison) = R8,600 ÷ R8,200 = **104.9%**.

That single order put R8,600 in gross profit in the business, and at no point did your own money fund production — the customer's deposit did.

**A first look at gross vs. net profit at the business level.** So far every calculation has been about *one order*. But the business as a whole also has costs that don't belong to any single order — things like mobile data, transport between suppliers, software subscriptions, and eventually an accountant's fee. These are called **overheads**. Suppose in one month you complete four orders similar in profile to the one above, with combined revenue of R67,200 and combined COGS + delivery of R32,800:

- **Business-level gross profit** = R67,200 − R32,800 = **R34,400** (simply the sum of each order's own gross profit).
- If that month's overheads (data, transport, a bookkeeping subscription) came to R5,000:
- **Net profit** = R34,400 − R5,000 = **R29,400**.

Gross profit tells you whether your *orders* are priced correctly. Net profit tells you whether the *business as a whole* is actually profitable once everything it costs to run it, not just to fulfil individual orders, is accounted for. Right now, one order at a time, you only need to think about gross profit per order — Module 15 (Finance) builds a full tracker for the business-level view once you have real, ongoing revenue to track.

### WHAT YOU NEED TO UNDERSTAND

Notice that the deposit (R8,400) and the total order cost (R8,200) are two different numbers that happen to be close in this example — that's not a coincidence you should expect every time. A 50% deposit will only reliably cover your costs when your margin is roughly 50% or better; at a much thinner margin, a 50% deposit could actually fall short of what you need to pay your supplier, and you'd need to either raise your margin or reconsider the deposit percentage on that particular deal. This is exactly the kind of check the Module 6 pricing calculator will run automatically — for now, you should be able to see, by eye, that the deposit needs to cover the cost.

### EXERCISES

1. A cleaning company orders 40 branded overalls at R320 each. Your landed cost per overall is R180. Delivery is a flat R350. Calculate: order value, deposit collected (50%), total COGS, total order costs, gross profit, and margin %.
2. Using your answer to Exercise 1: does the deposit collected comfortably cover the total order costs? By how much (or how short)?

**Check your work:**

- Order value = 40 × R320 = **R12,800**.
- Deposit (50%) = **R6,400**.
- Total product COGS = 40 × R180 = **R7,200**.
- Total order costs = R7,200 + R350 = **R7,550**.
- Gross profit = R12,800 − R7,550 = **R5,250**.
- Margin = R5,250 ÷ R12,800 = **41%**.
- Deposit check: R6,400 deposit vs. R7,550 total costs — the deposit is actually **R1,150 short** of covering the full order cost. This is a realistic warning sign: at this margin, you'd need to either hold back on paying your decorator until the balance lands, negotiate supplier payment terms, or raise the price/deposit percentage — never quietly cover the shortfall from your own pocket without noticing you're doing it.

### BUSINESS IMPLEMENTATION

**[ME]**

1. Pick one realistic order size and price for your actual planned garment/niche (use placeholder numbers if you don't have real supplier costs yet — Module 4 will replace them with real ones) and run the full six-step calculation yourself, on paper, without looking at the worked example above.
2. Note in `business/decisions-log.md`: at what rough margin level would a 50% deposit stop reliably covering your order costs? (You don't need a precise answer yet — just show you understand the relationship.)

### TODAY'S DELIVERABLES

- [ ] Exercises 1-2 completed and checked.
- [ ] Your own worked example completed independently.
- [ ] Deposit-vs-cost relationship noted in `business/decisions-log.md`.

### END-OF-DAY CHECK

1. Could I run all six steps (quote → deposit → costs → cash-flow check → balance → profit) on a new order without help?
2. Do I understand why a thin margin can make a 50% deposit insufficient to cover costs?
3. Can I explain, in one sentence, the difference between gross profit on one order and net profit for the business?

### NEXT DAY

**Day 5** is Module 1's capstone: we consolidate your business name shortlist, write a one-sentence elevator pitch, review the whole module with a short quiz, and bridge into Module 2 (Market Research), where your prospect list gets put to real use.

---

### DAY 5 — Module 1 Capstone: Name, Pitch & Review

**Module 1: Understanding the Outsourcing Business — Lesson 5**

### TODAY'S OBJECTIVE

Close out Module 1 with two concrete outputs — a shortlisted business name and a one-sentence elevator pitch — and confirm, with a short review quiz, that the core concepts (money flow, margin vs. markup, MOQ, lead time, the five beginner mistakes) are solid before Module 2 builds on top of them.

### WHAT YOU NEED TO LEARN

**1. Naming criteria for a B2B buyer.** The person deciding whether to trust you with 60 uniforms for their staff is a security-company owner or operations manager, not a consumer browsing a shop — so the bar is different from a catchy consumer brand name:

- **Easy to say and spell over the phone and in WhatsApp** — this is genuinely how most of your early deals will start.
- **Sounds credible for B2B work** — avoid anything that reads as a hobby or a personal nickname; avoid overpromising words that invite scrutiny you can't back yet (e.g. claiming "national" or "premium" before you've delivered a single order).
- **Works in English at minimum** — even if you expand regionally later, a name that's awkward or means something unintended in another local language is a real risk to check for, not just English.
- **Not already heavily used** by an existing local supplier in the same space — a quick Google/Facebook search of your shortlist avoids obvious confusion later.

This is a first-pass working name, not a final trademarked brand — Module 7 (Branding) goes deeper into positioning, logo, and a proper check before anything is printed or registered. Don't over-invest time here.

**2. The elevator pitch.** One sentence, said out loud in under 10 seconds, that answers three things: **who you serve, what problem you solve, and what you actually deliver.** A working structure: *"I supply [branded uniforms/workwear] to [security and cleaning companies] in [your region], handling [sizing, quality, and delivery] so they never have to chase a printer themselves."* You'll refine this in Module 7, but having a working version now means you're never caught fumbling an answer to "so what do you do?" from Day 6 onward, when Module 2 has you talking to real prospects.

### WHAT YOU NEED TO UNDERSTAND

A shortlist, not a final decision, is today's job. Picking 2-3 names you'd actually be comfortable using on a real quote to a real prospect next week is enough — final branding decisions (Module 7) benefit from having gone through actual sales conversations first, which is exactly what Module 2 starts.

### EXERCISES

**1. Narrow your name list.** Take your 5-8 candidates from Day 1. Score each one against the criteria above (say-ability, credibility, no unintended meaning, not already in use locally) and narrow to a shortlist of 2-3. Write the shortlist and your reasoning for eliminating the others into `business/decisions-log.md`. (Open-ended. A strong answer shows the criteria were actually applied — not just "these are my favourites" — and briefly states why each survivor made the cut.)

**2. Write your elevator pitch.** Using the structure above, write your actual one-sentence pitch. Say it out loud three times until it doesn't sound rehearsed. (Open-ended. A strong pitch is specific — names the actual niche and region — rather than generic enough to describe any uniform supplier anywhere.)

**3. Module 1 review quiz.**

a. Define gross margin and markup in one sentence each, and state which one uses the selling price as its denominator.
b. Your landed cost is R210 and you apply a 65% markup. What's your sell price, and what margin does that produce?
c. True or false: a 50% deposit fully removes all cash-flow risk from the business.
d. Name the two types of specialists you outsource production to, and what each one provides.
e. What single two-minute practice prevents most size-related disputes?
f. In one sentence, what's the difference between gross profit on one order and net profit for the whole business?

**Check your work:**

a. Margin = gross profit ÷ selling price. Markup = gross profit ÷ cost. **Margin** uses selling price as its denominator.
b. Sell price = R210 × 1.65 = **R346.50** (round to R347 in practice). Margin = (R346.50 − R210) ÷ R346.50 = R136.50 ÷ R346.50 = **39.4%**.
c. **False** — a deposit removes the risk of funding *production* for that order out of your own pocket. It does not remove overhead costs, the risk of the balance not being paid, refunds, or business-level cash-flow risk overall.
d. A **blank-garment wholesaler** (supplies the plain, unbranded items) and a **decorator** (embroiders or prints the branding onto them).
e. A written, customer-confirmed **size chart**, signed off before you place the supplier order.
f. **Gross profit** is revenue minus COGS for one order; **net profit** is the sum of gross profit across all orders, minus the business's overheads (data, transport, subscriptions, professional fees, etc.).

### BUSINESS IMPLEMENTATION

**[ME]**

1. Finalize your 2-3 name shortlist in `business/decisions-log.md`, with the scoring/reasoning from Exercise 1.
2. Write your elevator pitch into `business/decisions-log.md` as a dated entry.
3. Check your prospect list total in `business/prospect-list.md` against the Module 2 target of 50 — note how many more you'll need and when you plan to add them, since Module 2 starts putting this list to real use.

### TODAY'S DELIVERABLES

- [ ] 2-3 name shortlist logged with reasoning.
- [ ] Elevator pitch written and said out loud until it's natural.
- [ ] Review quiz (a-f) completed and checked.
- [ ] Prospect list total checked against the Module 2 target.

### END-OF-DAY CHECK

1. Could I say my elevator pitch to a stranger right now without reading it?
2. Do I have a name shortlist I'd actually be comfortable putting on a real quote next week?
3. Did I get all six review quiz questions right without help? If not, which one, and why?

### NEXT DAY

**Module 2 (Day 6)** starts market research for real: you'll use your actual prospect list to have short, low-pressure validation conversations with real security and cleaning company contacts — not a pitch, a conversation to confirm the problem you think exists actually exists. Bring your prospect list and your elevator pitch.
