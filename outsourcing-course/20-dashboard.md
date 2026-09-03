# Module 20 — Business Dashboard

**Days 112–115 of ~120.**
Every system you've built produces data — the CRM, the finance tracker, the fulfilment log. This module pulls it into one place so you can actually see, at a glance, whether the business is healthy, and know what to do about it when it isn't.

---

### DAY 112 — THE METRICS THAT ACTUALLY MATTER

**Module 20: Business Dashboard — Lesson 1**

### TODAY'S OBJECTIVE

Understand exactly which numbers matter for a deposit-first, reorder-driven uniform business — and why each one specifically matters here, not as a generic "business KPIs" list copied from somewhere else.

### WHAT YOU NEED TO LEARN

**1. The funnel metrics — is enough opportunity entering the business?**

- **Leads** — new prospects entering your pipeline. The floor everything else is built on: no volume of leads means every other metric is starved regardless of how good your process is.
- **Response rate** — the % of leads who reply to your first outreach. This is a message/targeting quality signal specifically, separate from volume — a healthy lead count with a weak response rate points at your outreach approach (Module 9-10), not your lead sourcing.
- **Meetings/calls booked** — leads that turn into an actual conversation. Tells you whether a reply is converting into real engagement, not just a polite "thanks, not now."
- **Quotes sent** — conversations that produce a formal quote. This isolates your discovery-call effectiveness (Module 9): plenty of meetings but few quotes usually means the conversation itself isn't landing.

**2. The conversion metrics — is the business actually closing?**

- **Orders won** — a quote that converts to a paid deposit. In this business, this is the real conversion event, not "quote sent." A quote costs you nothing until a customer commits real money — deposit paid is the moment revenue becomes real, exactly the discipline the roadmap built the whole cash-flow model around from Day 1.
- **Conversion rate** — orders won ÷ leads (or ÷ quotes, tracked separately — they answer different questions). One number that summarizes overall funnel health, useful for spotting a trend even before you dig into which specific stage is the problem.
- **Average order value (AOV)** — because your niche's order sizes genuinely vary a lot (20 guards vs. 200), AOV tells you whether you're landing bigger accounts over time or just accumulating small ones. A rising AOV with flat lead volume is still real growth.

**3. The money metrics — is it actually profitable, not just busy?**

- **Revenue** — total money in, but on its own it's a vanity number — it says nothing about whether you're making money on what you sold.
- **Gross profit / margin** — the number that actually pays you, tracked per order and in aggregate. This ties straight back to Day 1's markup-vs-margin lesson: margin is gross profit ÷ what the customer paid, and it's the number the dashboard should surface prominently, not revenue.
- **Customer acquisition cost (CAC)** — what it actually costs (ad spend, tools, and a reasonable value on your own time) to win one paying customer. Matters most once real marketing spend (Module 16) enters the picture: if CAC is higher than the profit a typical first order returns, that channel is losing you money even while it "generates leads."
- **Outstanding payments** — money owed to you and not yet collected: unpaid balances after delivery, and anything on payment terms once you extend those to trusted repeat accounts. Deposit-first protects you from funding a stranger's order, but it doesn't eliminate non-payment risk on the balance — this is where that risk becomes visible before it becomes a real problem (roadmap risk #5).

**4. The metric specific to this exact business model.**

- **Repeat-customer rate** — the % of your customers who place a second order. This is arguably the single most important number on the whole dashboard for this business specifically, because the roadmap's entire niche logic — security and cleaning companies, chosen partly for their staff turnover — was built on the assumption that most of your long-run profit comes from reorders every 6-12 months, not first orders. A low or flat repeat rate means Module 17's retention system isn't actually working, no matter how healthy the rest of the funnel looks.

### WHAT YOU NEED TO UNDERSTAND

No single metric tells you the truth alone — they only mean something in relation to each other. High leads with low response rate is a message problem. High response rate with few quotes sent is a discovery-call problem. Plenty of quotes with few orders won is a pricing or trust problem. Strong revenue with weak margin is a cost or discounting problem. Good order volume with a flat repeat rate is a retention problem, not a sales problem. Reading the dashboard well means reading it as a chain, and finding where the chain actually breaks — not staring at whichever number is biggest.

### EXERCISES

1. **Match each metric to the specific business question it answers**, in your own words, for all twelve metrics above.
2. **Diagnose this scenario:** Leads are steady and response rate is healthy. Meetings booked are healthy too. But quotes sent has dropped sharply over the last month, and orders won along with it. What's most likely broken, and which module's system would you look at first to fix it?
   **Check your work:** This pattern points at the discovery-call stage specifically — leads are engaging, but conversations aren't converting into formal quotes, so the fix starts with the Module 9 sales process (discovery-call flow, what's being asked, whether pricing expectations are being set correctly in that call) — not with lead generation (Module 10), which is clearly still working fine upstream.
3. **Diagnose this scenario:** Orders won and revenue both look strong this quarter, but gross margin has been quietly falling. What are the two most likely causes, and where would you check first?
   **Check your work:** Either costs are rising without prices adjusting (check actual supplier costs against what the Module 6 pricing tool assumes), or discounting is creeping in on deals to win them (check recent quotes against the pricing tool's standard output for unapproved discounts) — both are margin problems hiding behind healthy-looking revenue, exactly the trap Day 1's markup-vs-margin lesson warned about.

### BUSINESS IMPLEMENTATION

1. **[ME]** — Review your CRM (Module 11) and finance tracker (Module 15) and confirm each of the twelve metrics has real underlying data behind it — if a metric can't actually be calculated from what you're currently recording, note that now, before tomorrow's build.
2. **[ME]** — Rank the twelve by which one you'd most want to see first every week, given your business's current stage. This becomes an input to Day 115's weekly-review ritual.

### TODAY'S DELIVERABLES

- [ ] All twelve metrics explained in your own words, specific to this business.
- [ ] Two diagnostic exercises completed with reasoning.
- [ ] Confirmed which metrics your current CRM/finance data can actually support.

### END-OF-DAY CHECK

1. Can I explain why "orders won" (deposit paid), not "quotes sent," is the real conversion event in this business?
2. Do I understand why repeat-customer rate matters more here than in a typical one-off-sale business?
3. Can I read two metrics together and diagnose where in the funnel a real problem sits?

### NEXT DAY

**Day 113** builds the dashboard itself, pulling live from the CRM and finance tracker you just confirmed can support these metrics.

---

### DAY 113 — CLAUDE CODE BUILDS THE DASHBOARD

**Module 20: Business Dashboard — Lesson 2**

### TODAY'S OBJECTIVE

Get a real, working dashboard built that pulls the twelve Day 112 metrics from your actual CRM and finance tracker data — one place to look instead of digging through two systems every time you want to know how the business is doing.

### WHAT YOU NEED TO LEARN

**1. What "the dashboard" actually is, kept to the roadmap's own philosophy.** The tech stack has stayed deliberately simple this whole course — nothing more complex than the business's actual order volume requires. The dashboard follows the same rule: it's a single summary view, calculated from the same CRM and finance tracker files you already have, not a new platform or a new place to log data. You don't enter anything new into it — it reads what the CRM and finance tracker already contain and turns it into the twelve numbers from Day 112.

**2. What Claude Code needs from you to build it accurately.** The dashboard is only as good as the source data it reads — before the build, know roughly where each metric's underlying numbers actually live (which CRM fields track lead stage and dates, which finance tracker entries record revenue, COGS, and outstanding balances) so the build reads from the right places rather than guessing at your specific file structure.

### WHAT YOU NEED TO UNDERSTAND

A dashboard that has to be manually re-typed every time is a dashboard nobody keeps using past week three. The whole point of building it to pull from the CRM and finance tracker directly is that updating it becomes as simple as asking for a refresh — not a separate data-entry chore layered on top of the systems you already maintain.

### EXERCISES

1. **Before the build, sketch what you expect the dashboard's layout to look like** — which metrics grouped together, in what order. A strong answer roughly follows Day 112's three groups (funnel, conversion, money) plus the retention and outstanding-payments figures called out separately, since those are the ones you're least likely to check otherwise.

### BUSINESS IMPLEMENTATION

1. **[ME]** — Confirm your CRM and finance tracker are reasonably up to date before the build — a dashboard built against stale data will look wrong on day one for the wrong reason.
2. **[CLAUDE CODE]** — Build the dashboard.

### CLAUDE CODE / AI BUILDING

**What we're building today:** a single dashboard view, pulling from your existing CRM (`business/crm/`) and finance tracker (`business/finance/`), calculating all twelve Day 112 metrics.

**The exact prompt:**
```
Build me a business dashboard at business/finance/dashboard.md that
calculates these twelve metrics from my existing data: leads, response
rate, meetings booked, quotes sent, orders won, conversion rate, average
order value, revenue, gross profit and margin, customer acquisition cost,
repeat-customer rate, outstanding payments. Pull the underlying numbers
from business/crm/ (leads, pipeline stages, quote and order records) and
business/finance/ (revenue, COGS, outstanding balances). Group the output
into three sections: Funnel (leads through quotes sent), Conversion &
Money (orders won through margin and CAC), and Retention & Risk (repeat-
customer rate, outstanding payments). Show each metric's current number
and, where there's enough history, the trend versus the prior period.
Keep it one page, scannable in under a minute. Tell me exactly what to
run or ask for to refresh it with current numbers.
```

**What to expect:** one page, grouped exactly as described, showing real current numbers pulled from your real CRM and finance data — plus a clear, simple instruction for how you refresh it going forward (re-running the same request, or a lighter follow-up prompt, whichever fits how your CRM and tracker are actually built).

**How to test it:** manually recalculate two or three of the metrics by hand from the raw CRM/finance data and confirm they match what the dashboard shows. If any number is off, tell me exactly which metric and what you calculated instead, and I'll find where the pull went wrong.

### TODAY'S DELIVERABLES

- [ ] `business/finance/dashboard.md` built, pulling from real CRM and finance data.
- [ ] At least two metrics manually cross-checked against the raw source data.
- [ ] A clear, working method to refresh the dashboard confirmed.

### END-OF-DAY CHECK

1. Does the dashboard read from data I already maintain, rather than requiring new data entry of its own?
2. Did my manual spot-check match what the dashboard calculated?
3. Do I know exactly how to refresh it next week?

### NEXT DAY

**Day 114** puts the live dashboard to real use — reading your actual numbers and learning what a healthy vs. concerning trend looks like for each one.

---

### DAY 114 — READING THE DASHBOARD FOR REAL

**Module 20: Business Dashboard — Lesson 3**

### TODAY'S OBJECTIVE

Test the dashboard against your real accumulated data and build the judgment to tell a healthy number from a concerning one — for your business specifically, not against some invented external benchmark.

### WHAT YOU NEED TO LEARN

**1. The honest starting point: your own history is your benchmark, not an industry number.** You don't have — and shouldn't pretend to have — a reliable outside statistic for "what a good response rate looks like for a South African B2B uniform outreach campaign." No such number exists cleanly enough to be trustworthy, and treating a guessed figure as real data would be exactly the kind of fabricated precision to avoid. What you *do* have is your own trend over time, and that's genuinely more useful: is this metric improving, flat, or declining compared to your own last few weeks or months?

**2. General shape of a healthy read, for each group.**

- **Funnel metrics** — healthy looks like steady or growing volume at each stage relative to the stage above it (leads → response → meetings → quotes) without a sudden cliff at any one step. A concerning read isn't a low number in isolation — it's a stage that suddenly drops far more than the stages around it, especially if that drop wasn't there a month ago. That's your signal for exactly where in the funnel to look.
- **Conversion metrics** — healthy looks like a conversion rate and AOV that are stable or improving as you get better at qualifying leads and running discovery calls. A concerning read is a falling conversion rate even while lead volume holds steady — that's a sales-process issue, not a demand issue.
- **Money metrics** — healthy looks like margin holding at or above what your Module 6 pricing tool assumes when quotes are followed correctly. A concerning read is revenue climbing while margin quietly falls — the trap flagged on Day 112, and worth checking every single review, not just when something feels off.
- **Retention & risk** — healthy looks like a repeat-customer rate that holds up as your customer base ages past the 6-12 month reorder window, and outstanding payments that clear within your stated terms. A concerning read is outstanding payments that are growing month over month rather than being collected, or a repeat rate that stays near zero well past the point where reorders should be showing up.

**3. One bad week is data, not a crisis.** Any single metric can dip for a mundane reason — a slow week, a supplier delay, a run of tougher leads. What matters is the same discipline from Day 112's diagnostic exercises: look at the trend across several review periods, and look at metrics in relation to each other, before concluding something is actually wrong.

### WHAT YOU NEED TO UNDERSTAND

Interpreting a dashboard is a skill you build by using it repeatedly against your own real numbers, not by memorizing fixed thresholds someone else handed you. The goal of today isn't to walk away with a table of "good vs. bad" numbers — it's to walk away having actually looked at your real dashboard, compared it to what you'd expect given what you know about the last few weeks, and practiced explaining any surprises.

### EXERCISES

1. **Open your real dashboard from Day 113. For each of the three groups, write one sentence on what you see and whether it matches what you'd expect given the last month.** A strong answer engages with real numbers, not hypotheticals — if a number surprises you, say so and take a first guess at why, using the diagnostic habit from Day 112.
2. **Pick the one metric on your dashboard you trust least right now** (newest data, smallest sample, or a metric you suspect the CRM/finance data behind it is incomplete) **and say what you'd need to see over the next few weeks to trust it.** A strong answer names a concrete amount of additional data or time, not just "wait and see."

### BUSINESS IMPLEMENTATION

1. **[ME]** — Do a full real read of the dashboard today, in writing, following Exercise 1.
2. **[ME]** — Flag any metric you don't yet trust and the reason, so it isn't mistaken for a real signal too early.

### TODAY'S DELIVERABLES

- [ ] A written read of all three dashboard groups against your real numbers.
- [ ] The least-trustworthy metric identified, with a plan for when it becomes trustworthy.

### END-OF-DAY CHECK

1. Can I explain why my own historical trend is a better benchmark right now than a guessed industry number?
2. Do I know which of my metrics is currently the least reliable, and why?
3. Did I look at metrics in relation to each other rather than judging any one number alone?

### NEXT DAY

**Day 115** turns today's reading practice into a standing weekly habit — the module capstone.

---

### DAY 115 — CAPSTONE: THE DASHBOARD LIVE, AND A WEEKLY REVIEW RITUAL

**Module 20: Business Dashboard — Lesson 4**

### TODAY'S OBJECTIVE

Lock in a simple, sustainable weekly review ritual for the dashboard — when you look at it and what decision each metric should actually trigger — so measuring the business becomes a habit, not a one-off exercise from this module.

### WHAT YOU NEED TO LEARN

**1. A ritual only works if it's specific.** "Check the dashboard regularly" isn't a ritual — it's a good intention that quietly stops happening in week three. A real ritual names: the day and rough time (e.g. Monday morning, before outreach for the week starts), how long it takes (aim for under 15 minutes — if it takes longer every week, the dashboard itself needs simplifying, not your discipline), and exactly what you do with what you see.

**2. What decision each metric group should actually trigger.**

- **Funnel dropping at a specific stage** → that week's priority becomes fixing that stage specifically (more outreach volume, a message rewrite, a discovery-call adjustment) — not a vague "work harder on sales."
- **Conversion rate falling with steady leads** → review recent lost quotes for a pattern (pricing objections, timing, a competitor) before changing anything else.
- **Margin falling while revenue holds or grows** → check recent quotes against the Module 6 pricing tool's standard output for unapproved discounting, and check supplier costs haven't quietly moved.
- **CAC rising** → review which channel (Module 16) is driving it and whether that channel is still worth the spend relative to what a typical order actually returns in profit.
- **Repeat-customer rate flat or falling** → check the Module 17 reorder-reminder system is actually firing on schedule and being followed up on, not just running silently in the background unchecked.
- **Outstanding payments growing** → run the Module 14 late-payment SOP on the specific accounts involved, this week, not next.

**3. Refresh the dashboard before you review it, not after.** A stale dashboard reviewed on schedule gives you false confidence. Make "refresh" the first step of the ritual every time, using the method Day 113 confirmed.

### WHAT YOU NEED TO UNDERSTAND

The dashboard's entire value is in the loop it closes: measure → notice → act → measure again. A dashboard that gets checked but never changes a decision is just a report nobody reads twice. Today's ritual is what keeps that loop actually running once the novelty of a new tool wears off.

### EXERCISES

1. **Quiz — answer from memory, then check below:**
   - Why is "orders won" a better conversion metric to track than "quotes sent" in this business?
   - What's the honest benchmark to compare your metrics against, and why not an industry figure?
   - Name one metric and the specific action it should trigger if it looks concerning.

   **Check your work:**
   - Because a quote costs the customer nothing and commits them to nothing — a paid deposit is the real moment the sale becomes revenue, matching the business's own deposit-first cash-flow rule from Day 1.
   - Your own historical trend, because no reliable outside benchmark exists for this specific business, market, and channel mix — a guessed number would be false precision, not real data.
   - Any pairing from the list above is acceptable if the reasoning is sound (e.g. margin falling with steady revenue → check for unapproved discounting or rising supplier costs).

### BUSINESS IMPLEMENTATION

1. **[ME]** — Write your weekly review ritual as a short, real, dated commitment: day, time, duration, and the action-per-metric table above, tailored to your business's current priorities.
2. **[AUTOMATION]** — If your calendar or reminder tools support it, set a standing weekly reminder for the review slot — the ritual only works if it survives busy weeks, and a reminder outside your own memory helps that.

### TODAY'S DELIVERABLES

- [ ] Weekly review ritual written down: day, time, duration, refresh-first habit, and action-per-metric table.
- [ ] A standing reminder set for the review slot.
- [ ] Module 20 complete: metrics understood, dashboard built and cross-checked, real data read and interpreted, a ritual in place to keep using it.

### END-OF-DAY CHECK

1. Do I have a specific day and time for my weekly review, not a vague intention?
2. For each metric on my dashboard, do I know what I'd actually do differently if it looked concerning?
3. Is refreshing the dashboard the first step of my ritual, before I look at it?

### NEXT DAY

**Day 116 (Module 21: Scaling)** is the course's final stretch — you now have the measurement system to know, honestly, whether the business is ready for what Module 21 covers: a second niche, a second city, and eventually international reach.
