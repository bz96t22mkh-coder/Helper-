# Financial Command Centre, Habit Tracker, Reviews

## 1. Finance Tracker — detail

Database spec is in `01-notion-architecture.md` §13; here's how to actually use it.

| Property | Type | Notes |
|---|---|---|
| Name | Title | e.g. "Outsourcing — September 2026" |
| Category | Select | `Trading`, `Outsourcing`, `YouTube`, `Personal` (add `AI Agency` back if/when it unlocks) |
| Month | Date | |
| Revenue | Number (currency) | Business categories only |
| Expenses | Number (currency) | |
| Profit | Formula | `prop("Revenue") - prop("Expenses")` |
| Payouts (Trading only) | Number (currency) | Funded-account payouts |
| Savings | Number (currency) | Personal category only |
| Personal Expenses | Number (currency) | Personal category only |
| Notes | Text | |

**Views:**
- **By Category, this month** — Board grouped by Category, filtered to current month.
- **Trend** — Table sorted by Month, one row per Category per Month, so you can see Profit trending up/down over time — this is what your Monthly and 90-Day Reviews pull from.

**Total Income / Total Profit:** don't build a separate rollup for "total" across categories inside this database — that's what the Monthly Review's own summary does (sum manually or via a linked view with a Sum footer, which Notion tables support natively — turn on the Sum calculation at the bottom of the Month view).

**Financial goals:** live in the Goals database (`01-notion-architecture.md` §7) as 90-Day/1-Year goals with `Pillar` pointed at the relevant business — e.g. "Outsourcing — $2,000 MRR" as a 90-Day goal, `Success Criteria` = "Finance Tracker shows Revenue ≥ $2,000 for one calendar month."

## 2. Habit Tracker — the exact list (do not add more)

Already specified in `01-notion-architecture.md` §10. Repeating here with the reasoning, since your brief is explicit about not letting this balloon past ~10-12 habits:

1. Woke at 5 AM
2. Slept on time
3. Gym
4. Trading block done
5. Outsourcing block done
6. YouTube course block done
7. Reading done
8. Personal Dev done
9. Steps target hit
10. Journaled
11. Content published (if scheduled that day — leave blank/N/A on non-upload days, don't count against you)

That's 11, matching your brief's own list exactly. Resist adding "meditation," "cold shower," etc. even if you start doing them — those absorb into your existing blocks (e.g. meditation is inside Personal Development's Section 18) rather than becoming their own tracked row. If AI Agency unlocks later, swap it back in for one of the routine rows rather than growing the list past 11.

## 3. Reviews — the exact question sets to put in each Notion template

Build these as **database templates** on the Reviews database (`01-notion-architecture.md` §15) so each new review pre-fills with its questions.

### Daily Review template
- What did I complete?
- What didn't I complete?
- Why?
- What did I learn?
- What moves to tomorrow?

### Weekly Review template
- Biggest win this week?
- Biggest failure/miss this week?
- Trading progress (phase, journal review, key mistake pattern)
- Outsourcing progress (which phase/module, what moved, what's stuck)
- YouTube progress (videos published vs. target, pipeline health)
- Course progress (which Curriculum Items completed)
- Personal development progress
- Fitness (gym adherence, sleep quality)
- Reading progress
- Social & hobbies — did I do something social this week? Did I do a hobby (hiking/cooking)? (see `07-life-pillars-and-social-life.md`)
- Planned vs. Actual time (pull from Weekly Time Summary)
- Next week's top 3 priorities

### Monthly Review template
- Progress toward 90-Day goals (list each, % progress)
- Course completion status (all active courses)
- Business progress (revenue, clients/customers, pipeline)
- Trading progress (phase, win rate trend, rule adherence)
- YouTube progress (subs, views trend, upload consistency)
- Personal development (sections completed, mastery levels)
- Financial progress (Finance Tracker trend)
- Schedule efficiency (recurring overruns/underruns from Weekly Time Summary)
- What should change next month?

### 90-Day Review template (your brief's exact 10 questions)
1. What changed?
2. What did I achieve?
3. What failed?
4. Why?
5. What improved?
6. What should I stop?
7. What should I start?
8. What should I continue?
9. What are my next 90-day goals?
10. How should my time allocation change?
11. Re-score your Life Wheel (`07-life-pillars-and-social-life.md`) — any pillar stuck low for 2 reviews running is your signal to actually act, not just note it again.

### Yearly Review template
- Full re-read of the Life Vision and 5-Year Goals — still accurate?
- Which 1-Year goals were achieved / missed, and why?
- Phase progress across every pillar (how many phases advanced this year)
- Financial year-in-review (Finance Tracker annual sum)
- Biggest lesson of the year
- Next year's 1-Year goals and updated 90-Day goal for Q1

This is also the only point at which it's appropriate to reconsider the *whole* schedule structure from scratch (brief section 22: "reassess priorities... do not completely rebuild the schedule unless there is a meaningful reason" — a Yearly Review is one of the few points where that meaningful reason is allowed to be "a full year has passed," everything else requires an actual phase-completion trigger).
