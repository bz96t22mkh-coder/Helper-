# DAY 1 — WHAT OUTSOURCING ACTUALLY IS & HOW THIS BUSINESS MAKES MONEY

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
