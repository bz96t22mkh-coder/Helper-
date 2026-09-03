# Module 6 — Pricing

**Days 28–33 of ~120.**

**A note on accuracy:** every worked pricing, markup, and margin calculation in this module has been independently recomputed before being written down. Where a number is rounded for real-world pricing (e.g. to a clean rand amount), the exact unrounded figure is shown first so you can verify the arithmetic yourself. If you ever spot a number here that doesn't check out, treat that as a real bug to flag — this module exists specifically so you never have to trust pricing math you haven't verified.

This module takes your Module 5 product catalogue and puts real, correct numbers on it: a full cost breakdown, bulk pricing tiers built properly on markup vs. margin, deposits and corporate pricing, and a Claude Code-built pricing calculator you'll use for every real quote from here on.

---

### DAY 28 — Full COGS Breakdown for a Real Order

**Module 6: Pricing — Lesson 1**

### TODAY'S OBJECTIVE

Build a complete, itemized cost breakdown for a real order — every cost component, not just "garment + embroidery" — so your pricing from Day 29 onward is built on a number that reflects your actual full cost, not an underestimate.

### WHAT YOU NEED TO LEARN

**Every real cost component of an order**, using a worked example (40 branded overalls, a realistic order for a cleaning company client):

| Cost component | Per-unit cost | Notes |
|---|---|---|
| Blank garment | R145 | From your Module 4 wholesaler |
| Embroidery/branding | R40 | From your Module 4 decorator |
| Packaging (poly bag, size label) | R5 | Module 5, Day 26 |
| **Per-unit landed cost** | **R190** | R145 + R40 + R5 |

| Order-level cost | Amount | Notes |
|---|---|---|
| Product COGS (40 units × R190) | **R7,600** | |
| Delivery (flat, not per-unit) | **R350** | Doesn't scale per-unit the same way — a flat trip cost regardless of exact quantity within a normal range |
| **Total order COGS** | **R7,950** | R7,600 + R350 |

Use your own real supplier quotes and Module 5 packaging decisions to build this same table for your actual product — the R145/R40/R5 figures above are a worked example, not a number to copy.

**Why "landed cost" includes everything, not just the garment.** A common beginner mistake is pricing off just the blank garment cost and treating embroidery, packaging, and delivery as afterthoughts to "figure out later" — this quietly erodes margin, because every one of those costs is real money leaving the business on every single order, whether or not you remembered to price for it.

### WHAT YOU NEED TO UNDERSTAND

Notice the split between **per-unit costs** (things that scale directly with quantity — garment, branding, packaging) and **order-level flat costs** (things like delivery that don't scale the same way, or scale in steps rather than smoothly). This distinction matters directly for Day 29's tiered pricing: a flat cost like delivery gets proportionally cheaper per unit as order size grows, which is part of why bulk orders can genuinely support a lower per-unit price without cutting your actual margin.

### EXERCISES

1. Using your own real supplier quotes from Module 4 and packaging decision from Module 5, build your own full COGS breakdown table for your most common product, at a realistic order quantity.
2. For a 25-unit order of the same overalls example above (landed cost R190/unit, delivery flat R350), calculate: product COGS, total order COGS.

**Check your work (Question 2):**
- Product COGS = 25 × R190 = **R4,750**.
- Total order COGS = R4,750 + R350 = **R5,100**.

### BUSINESS IMPLEMENTATION

**[ME]**

1. Build your real COGS breakdown table using actual supplier numbers, and save it as the foundation for Day 29's pricing work.
2. Log it in `business/pricing/`.

### TODAY'S DELIVERABLES

- [ ] Full COGS breakdown table built from real supplier quotes.
- [ ] Exercise 2 calculation completed and checked.

### END-OF-DAY CHECK

1. Does my COGS breakdown include every real cost component, not just the garment?
2. Do I understand the difference between a per-unit cost and a flat order-level cost?
3. Is this breakdown built on real numbers from my own suppliers, not the worked example's placeholder figures?

### NEXT DAY

**Day 29** applies markup and margin properly to this cost base to build real bulk pricing tiers and MOQs — with every calculation checked.

---

### DAY 29 — Bulk Pricing Tiers, Built Correctly

**Module 6: Pricing — Lesson 2**

### TODAY'S OBJECTIVE

Build a real tiered pricing structure from your Day 28 landed cost, applying markup correctly at each tier and verifying the resulting margin — connecting Module 5's tier structure to actual numbers for the first time.

### WHAT YOU NEED TO LEARN

**Why markup should generally decrease as order quantity increases.** A smaller order costs you proportionally more to service relative to its size (a flat delivery cost and a decorator's per-design setup fee are both spread over fewer units), and a larger order represents more value and lower relative effort per unit to you — so a tiered markup that's higher for small orders and lower for bulk orders is both fair to the customer and reflects your real cost structure, not an arbitrary discount.

**A worked tiered pricing structure**, using Day 28's R190 per-unit landed cost and a decorator MOQ of 20 units per design (matching Module 4's real-world MOQ discipline):

| Tier | Quantity | Markup | Sell price (exact) | Sell price (rounded) | Margin at rounded price |
|---|---|---|---|---|---|
| 1 — below/at MOQ threshold | 1-19 | 90% | R190 × 1.90 = R361.00 | **R365** | (365−190)/365 = 175/365 = **47.9%** |
| 2 — standard | 20-49 | 70% | R190 × 1.70 = R323.00 | **R325** | (325−190)/325 = 135/325 = **41.5%** |
| 3 — bulk | 50-99 | 55% | R190 × 1.55 = R294.50 | **R295** | (295−190)/295 = 105/295 = **35.6%** |
| 4 — large bulk | 100+ | 45% | R190 × 1.45 = R275.50 | **R280** | (280−190)/280 = 90/280 = **32.1%** |

Notice: margin drops as markup drops, exactly as Module 1's markup-vs-margin math predicts — but total gross profit in rand terms still rises with volume, because you're earning that smaller margin on many more units. This is the correct, intended trade-off of bulk pricing: lower margin percentage, higher total profit.

**Why Tier 1's boundary matches your decorator's MOQ.** An order below your decorator's 20-unit MOQ genuinely costs you more proportionally (a setup fee spread over fewer units, or a small-order surcharge from your decorator) — Tier 1's higher markup exists specifically to cover that real extra cost, not to penalize small customers arbitrarily.

### WHAT YOU NEED TO UNDERSTAND

These tier boundaries and markup percentages are a worked starting structure — your actual numbers depend on your real landed cost (Day 28) and your real decorator's MOQ and setup fees (Module 4). The *method* (decreasing markup by tier, boundary aligned to your real MOQ) is what to copy; the specific percentages are a reasonable starting point to adjust once you have real supplier numbers and, eventually, real market feedback.

### EXERCISES

1. A customer orders 35 units of the overalls example above. Which tier applies? Calculate revenue, total COGS, gross profit, and margin for this specific order.
2. Build your own tiered pricing structure for your real product, using your own Day 28 landed cost and your own decorator's real MOQ as the Tier 1/Tier 2 boundary.

**Check your work (Question 1):**
- 35 units falls in **Tier 2 (20-49)** → sell price **R325/unit**.
- Revenue = 35 × R325 = **R11,375**.
- Total COGS = 35 × R190 = **R6,650**.
- Gross profit = R11,375 − R6,650 = **R4,725**.
- Margin = R4,725 ÷ R11,375 = **41.5%** — matching Tier 2's per-unit margin exactly, since no additional rounding was introduced at the order level.

### BUSINESS IMPLEMENTATION

**[ME]**

1. Build your own real tiered pricing structure using your actual landed cost and decorator MOQ, and log it in `business/pricing/`.
2. Sanity-check every tier's margin against what you'd actually be comfortable earning — if Tier 4's margin feels too thin once you see it in real numbers, that's useful information to revisit before you quote it to a real customer, not after.

### TODAY'S DELIVERABLES

- [ ] Exercise 1 calculated and checked.
- [ ] Your own real tiered pricing structure built from real numbers.

### END-OF-DAY CHECK

1. Do I understand why markup decreases while total profit still increases as order size grows?
2. Could I calculate the correct tier, revenue, COGS, profit, and margin for any real order quantity right now?
3. Is my Tier 1 boundary genuinely aligned with my real decorator's MOQ, not an arbitrary number?

### NEXT DAY

**Day 30** covers deposits, discounts, and corporate pricing structure — including what happens to your pricing when a proven repeat customer earns better terms.

---

### DAY 30 — Deposits, Discounts & Corporate Pricing

**Module 6: Pricing — Lesson 3**

### TODAY'S OBJECTIVE

Understand how discounts affect your real margin (with the arithmetic to prove it), and how corporate/repeat-account pricing and payment terms should evolve for a proven customer — without ever quietly abandoning the deposit-first discipline for a new or unproven one.

### WHAT YOU NEED TO LEARN

**1. Discounts always cost more margin than they look like they cost.** A discount is a percentage off the *sell price*, but its real impact is felt entirely out of your *profit* — because your cost stays fixed. Worked example: from Day 29's Tier 2 price of R325/unit (margin 41.5%), a 5% loyalty discount for a proven repeat customer:

- Discounted price = R325 × 0.95 = **R308.75** → round to **R309**.
- New margin = (R309 − R190) ÷ R309 = R119 ÷ R309 = **38.5%**.
- The sell price dropped by about 5%, but margin dropped from 41.5% to 38.5% — a bigger relative hit to your actual profit than the discount percentage suggests, because the discount comes entirely out of the profit portion of the price, not proportionally out of both cost and profit.

This doesn't mean discounts are wrong — a small, deliberate discount for a genuinely proven repeat account is a reasonable cost of retaining a good customer (Module 17 covers retention properly). It means every discount should be a conscious, calculated decision using this exact math, never a reflexive "sure, I can knock off a bit" in the moment.

**2. Corporate pricing and payment terms — earned, not given.** Per the roadmap's core principle: a new customer, however large or promising, still follows the standard 50% deposit rule from Module 1 — no exceptions on a first order, regardless of how established their company looks. What *can* evolve for a genuinely proven repeat account (e.g. after several completed, fully-paid orders):

- **A modest loyalty discount**, calculated properly as shown above, not guessed.
- **Extended payment terms** (e.g. 30-day invoice terms instead of deposit-then-balance) — but only for an account with a real, demonstrated payment history with you, and ideally still with some structure that protects your cash flow (e.g. a smaller deposit even under extended terms, or a credit limit tied to their payment history). Extending real credit terms to a company you don't yet have a track record with reintroduces exactly the cash-flow risk the deposit rule was built to prevent — treat any large corporate credit-terms decision as worth a second look, and get an accountant's input (**[PROFESSIONAL]**) before extending significant credit to any single account, since concentration risk (Module 1's "biggest risks" list) compounds with generous payment terms.

### WHAT YOU NEED TO UNDERSTAND

The temptation to offer better terms to a big, impressive-looking prospect is strongest exactly when you have the least track record with them — which is precisely backwards from when better terms are safe to offer. Trust and terms should move together: better terms follow a proven payment history, they don't precede it.

### EXERCISES

1. A proven repeat customer, buying at your Tier 3 bulk rate (R295/unit, from Day 29), is offered a 5% loyalty discount. Calculate the discounted price and the resulting margin.
2. A new prospect — not yet a customer — asks for 30-day payment terms on their very first order, citing that they're "a large, established company." What do you say, and why? (Open-ended — a strong answer holds the deposit-first line for a first order regardless of company size, while remaining professional and clear about the reasoning, e.g. that standard terms apply to every new account until a payment history is established.)

**Check your work (Question 1):**
- Discounted price = R295 × 0.95 = **R280.25** → round to **R280**.
- New margin = (R280 − R190) ÷ R280 = R90 ÷ R280 = **32.1%** (down from Tier 3's original 35.6%).

### BUSINESS IMPLEMENTATION

**[ME]**

1. Decide and document your own loyalty discount policy (what qualifies as "proven," what discount you'd actually offer, calculated properly) in `business/pricing/`.
2. Decide and document your own policy on when (if ever, and under what conditions) you'd extend payment terms beyond deposit-then-balance, and log it in `business/decisions-log.md` — note explicitly that this stays [PROFESSIONAL]-reviewed territory once real money is involved at scale.

### TODAY'S DELIVERABLES

- [ ] Exercise 1 calculated and checked.
- [ ] Personal loyalty discount policy documented.
- [ ] Personal payment-terms policy documented, with the deposit-first-for-new-accounts principle explicitly preserved.

### END-OF-DAY CHECK

1. Can I calculate the real margin impact of any discount, rather than guessing it feels "about right"?
2. Do I understand why better terms should follow proven trust, not precede it?
3. Have I committed, in writing, to holding the deposit-first line for new accounts regardless of how impressive they look?

### NEXT DAY

**Day 31** turns everything from Days 28-30 into a real tool — Claude Code builds your pricing calculator today, so you never have to run this math by hand for a real quote again.

---

### DAY 31 — Claude Code Builds the Pricing Calculator

**Module 6: Pricing — Lesson 4**

### TODAY'S OBJECTIVE

Get a working pricing calculator built that takes your real cost inputs and quantity, and outputs a correct, tier-appropriate quote every time — the tool that replaces manual calculation for every real quote from here on.

### WHAT YOU NEED TO LEARN

**What "working" means for this tool, before you ask for it.** Following the Claude Code Business Builder Workflow from the roadmap, define the requirement clearly first: given a per-unit landed cost, an order quantity, and your tier structure, the calculator should output the correct tier, sell price per unit, total revenue, total COGS, gross profit, margin %, and the 50% deposit amount — every time, without you doing the arithmetic by hand. It should also flag orders that fall below your Tier 1 threshold as "below standard MOQ" rather than silently pricing them, so you're always consciously aware when a small-order conversation (Module 4, Day 19's MOQ judgment call) applies.

### EXERCISES

There are no manual calculation exercises today — today's "exercise" is building and testing the real tool, done together with me below.

### BUSINESS IMPLEMENTATION

**[ME]**

1. Give me your real Day 28 landed cost(s) and Day 29 tier structure so the calculator is built around your actual numbers, not a placeholder.
2. Test the calculator (see below) against at least three of your own already-checked answers from Days 28-30, and confirm every output matches your hand-calculated numbers exactly.

### CLAUDE CODE / AI BUILDING

**What we're building today:** a pricing calculator that takes a landed cost, a tier structure, and an order quantity, and outputs a complete, correct quote.

**The exact prompt to give Claude Code:**
```
Build me a pricing calculator for a branded workwear outsourcing business.

Inputs: per-unit landed cost (garment + branding + packaging), a flat
delivery cost, my tier structure (quantity ranges and markup % per tier —
I'll give you my real numbers), and an order quantity.

For a given quantity, it should:
1. Determine the correct pricing tier (flag clearly if the quantity is
   below my Tier 1 / MOQ threshold, rather than silently pricing it)
2. Calculate sell price per unit (landed cost × (1 + tier markup)),
   rounded to a clean rand amount
3. Calculate: total revenue, total COGS (product COGS + delivery), gross
   profit, margin % (gross profit ÷ revenue), and the 50% deposit amount
4. Show its work — the exact formula used at each step, not just the
   final numbers, so I can verify it by hand

Keep it as a simple, well-commented script I can run by giving it a
quantity and getting a full breakdown back. Explain in plain language how
to actually run it, since I don't need to read the code, just use it and
verify its output.
```

**What to expect:** a working, testable tool (not a mockup) that takes an order quantity and returns a complete, correct quote breakdown, plus a plain-language explanation of how to run it.

**How to test it:** run it against Day 29's Exercise 1 (35 units, R190 landed cost) and confirm it outputs exactly R325/unit, R11,375 revenue, R6,650 COGS, R4,725 gross profit, and 41.5% margin — the numbers you already hand-verified. Then test it with a quantity below your Tier 1 threshold and confirm it flags it clearly rather than pricing it silently. If any output doesn't match your hand-checked numbers, tell me exactly what's wrong and I'll fix it — never trust a tool's output over your own verified math until it's proven itself.

### TODAY'S DELIVERABLES

- [ ] Real cost and tier data provided for the build.
- [ ] Calculator built and tested against at least three hand-verified answers from Days 28-30.
- [ ] Below-MOQ flagging confirmed working.

### END-OF-DAY CHECK

1. Does the calculator's output match my own hand-calculated numbers exactly, for every test I ran?
2. Do I understand every input and output field well enough to explain it to someone else?
3. Do I know how to actually run it for a new, real quote?

### NEXT DAY

**Day 32** stress-tests the calculator against real-world edge cases — very small orders, very large bulk orders, and changed supplier costs — before you trust it for a real customer quote.

---

### DAY 32 — Testing & Refining the Calculator

**Module 6: Pricing — Lesson 5**

### TODAY'S OBJECTIVE

Deliberately break the calculator with realistic edge cases before you rely on it for a real customer — because a pricing tool that only gets tested with "normal" inputs will eventually meet an edge case in front of a real customer instead of in a safe test.

### WHAT YOU NEED TO LEARN

**Edge case 1 — a very small order, below MOQ.** A prospect wants just 5 units. Using Day 29's R190 landed cost and Tier 1's 90% markup, the calculator should still price it (5 is below the 20-unit decorator MOQ, but Tier 1 exists to cover exactly this range with a higher markup) — at **R365/unit**, the same as any other Tier 1 order. What it must do correctly is **clearly flag** that this is a below-standard-MOQ order, prompting the same judgment call from Module 4, Day 19 (proceed at the small-order rate, or discuss reaching the decorator's real 20-unit minimum with the customer) — not silently produce a number with no flag.

**Edge case 2 — a very large bulk order with a changed supplier cost.** A corporate prospect wants 300 units. At this volume, your wholesaler may offer you a genuine volume discount on the blank garment itself — say, the blank drops from R145 to R130 per unit, while embroidery (R40) and packaging (R5) stay the same. **New landed cost = R130 + R40 + R5 = R175.** Apply Tier 4's 45% markup: R175 × 1.45 = R253.75 → round to **R254/unit**.

- Revenue = 300 × R254 = **R76,200**.
- Total COGS = 300 × R175 = **R52,500**.
- Gross profit = R76,200 − R52,500 = **R23,700**.
- Margin = R23,700 ÷ R76,200 = **31.1%**.

The critical lesson here: **the calculator only produces a correct answer if you feed it the correct, current landed cost for that specific order** — a large order that unlocks a real supplier volume discount needs its landed cost updated *before* you run the calculator, not after. A tool that calculates correctly off a stale cost input still produces a wrong quote — this is a process discipline, not a tool bug.

### WHAT YOU NEED TO UNDERSTAND

Every edge case you deliberately test now is a mistake you'll never make in front of a real customer later. The two edge cases above cover the two directions pricing can go wrong: under-flagging a small order (missing the MOQ conversation) and using a stale cost on a large order (understating or overstating a real volume discount). Get in the habit of asking "what's actually changed about my costs for this specific order?" every time an order is unusually small or unusually large, before you trust any tool's output.

### EXERCISES

1. Run your own calculator (Day 31) with a quantity below your real Tier 1/MOQ threshold and confirm it flags correctly.
2. Run it with a large bulk quantity, first using your standard landed cost, then again after manually adjusting for a hypothetical supplier volume discount — compare the two outputs and confirm you understand why they differ.
3. Recompute Edge Case 2 above by hand, independently, and confirm your numbers match.

**Check your work (Question 3):** R175 landed cost × 1.45 = R253.75 → R254/unit. 300 × R254 = R76,200 revenue. 300 × R175 = R52,500 COGS. R76,200 − R52,500 = R23,700 gross profit. R23,700 ÷ R76,200 = 31.1% margin. (Matches the worked example above exactly — if your numbers differ, recheck your arithmetic before assuming the calculator is wrong.)

### BUSINESS IMPLEMENTATION

**[ME]**

1. Complete both edge-case tests against your real calculator and report back exactly what happened — if either test doesn't behave as expected, tell me and I'll fix the tool.
2. Write a one-line personal reminder into `business/pricing/` — "always update landed cost before pricing an unusually large or small order" — as a permanent process note alongside the tool itself.

### TODAY'S DELIVERABLES

- [ ] Below-MOQ edge case tested and confirmed flagging correctly.
- [ ] Large-bulk-with-changed-cost edge case tested and hand-verified.
- [ ] Process reminder about updating landed cost logged.

### END-OF-DAY CHECK

1. Does my calculator correctly flag a below-MOQ order rather than silently pricing it?
2. Do I understand why the same calculator can produce two different correct answers for the same quantity, depending on the landed cost I feed it?
3. Am I confident enough in this tool now to actually use it on a real customer quote?

### NEXT DAY

**Day 33** is Module 6's capstone: finalizing your official rate card/price list document from everything built this module, before Module 7 moves into branding and positioning.

---

### DAY 33 — Module 6 Capstone: The Official Rate Card

**Module 6: Pricing — Lesson 6**

### TODAY'S OBJECTIVE

Finalize one official, written rate card/price list document from everything this module has built, and confirm your understanding of the whole module before Module 7 moves into branding and positioning.

### WHAT YOU NEED TO LEARN

**What the rate card should contain, pulling together Days 28-32:**
- Your product(s) and their per-unit landed cost (Day 28) — kept as an internal reference, not shown to customers.
- Your tiered pricing structure (Day 29) — quantity ranges and per-unit sell prices, the customer-facing core of this document.
- Your deposit policy (50% standard, Module 1) and loyalty/corporate terms policy (Day 30), stated clearly.
- A note on how below-MOQ small orders are handled (Day 32's Edge Case 1 logic).
- Reference to the pricing calculator (Day 31) as the tool that generates an actual quote from this rate card for any specific real order.

This becomes the document you (and eventually an employee, Module 18) work from for every quote — the rate card sets the policy, the calculator applies it to a specific order.

### WHAT YOU NEED TO UNDERSTAND

A rate card isn't meant to be permanently fixed — real supplier cost changes, real market feedback, and business growth will all justify revisiting it over time. What matters is that any future revision is a deliberate, calculated decision (using the same verified-arithmetic discipline this whole module has practiced), never a reactive, in-the-moment guess during a sales conversation.

### EXERCISES

**Module 6 review quiz:**

a. Why does markup generally decrease while total gross profit still increases as order quantity grows in a tiered structure?
b. A discount is taken as a percentage off the sell price — why does it reduce margin by more than that same percentage, proportionally?
c. Why should a new, even large-looking, prospect still follow the standard deposit-first policy on their first order?
d. Name the two edge cases tested on Day 32, and what each one protects against.
e. What's the actual relationship between the rate card and the pricing calculator?

**Check your work:**

a. Because per-unit costs that don't scale with quantity (like a flat delivery fee or a decorator's per-design setup fee) get spread over more units at higher volumes, so a lower markup still covers costs — and that lower margin percentage is earned on many more units, producing more total profit in rand terms even though the percentage is lower.
b. Because the discount comes entirely out of the profit portion of the price while the cost stays fixed — so a 5% price cut translates into a larger percentage cut to the margin itself, since margin is a smaller number than the sell price to begin with.
c. Because trust and payment terms should be earned through a real, demonstrated payment history, not granted based on how established or large a company appears — extending trust before it's earned reintroduces the exact cash-flow risk the deposit rule exists to prevent.
d. Edge Case 1 (a very small, below-MOQ order) protects against silently under-flagging orders that need a real MOQ conversation. Edge Case 2 (a very large bulk order with a supplier volume discount) protects against pricing off a stale landed cost that no longer reflects the real, current cost of that specific order.
e. The rate card sets the policy (tiers, markup, deposit and terms rules); the calculator applies that policy correctly to any specific real order quantity, producing the actual quote.

### BUSINESS IMPLEMENTATION

**[ME]**

1. Assemble the final rate card document using the structure above, pulling together your real, logged Days 28-32 outputs.
2. Save it in `business/pricing/` (e.g. `business/pricing/rate-card.md`).
3. Complete the Module 6 review quiz and check your answers.

### TODAY'S DELIVERABLES

- [ ] Final rate card document assembled and saved.
- [ ] Module 6 review quiz completed and checked.

### END-OF-DAY CHECK

1. Do I have one official rate card document I could quote a real customer from today?
2. Could I explain, with correct numbers, why my pricing works the way it does — not just what the numbers are?
3. Am I confident using the pricing calculator on a real quote, having tested it against edge cases myself?

### NEXT DAY

**Module 7 (Day 34)** moves into branding — positioning, brand identity, and your USP against the local competitors you researched in Module 2 — now that you have a real product, a real supplier chain, and real, verified pricing behind it.
