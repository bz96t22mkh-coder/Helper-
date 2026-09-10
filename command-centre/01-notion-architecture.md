# The Notion Build — Exact Architecture

Written for a Notion beginner. Build in the order given — later databases relate to earlier ones, so building out of order means re-doing relation fields.

Notion vocabulary used below: a **database** is a table (you can view it as Table/Board/Calendar/etc.); a **property** is a column; a **relation** links a row to a row in another database; a **rollup** pulls a value from a related row (e.g. "show me the Pillar's name on this Task"); a **formula** computes a value from other properties.

---

## 1. PAGE HIERARCHY

Create one parent page called **🧭 Command Centre**. Everything else is a sub-page or an inline database inside it.

```
🧭 Command Centre                         (parent page)
├── 🏠 TODAY                              (page — your morning landing view, built from linked database views)
├── 🎯 Vision & Goals                     (page, contains the Goals database)
├── ⭐ Pillars                            (database — the 8 life areas)
├── 📈 Phases                             (database — related to Pillars)
├── 🎓 Courses                            (database — related to Pillars)
├── 📖 Curriculum Items                   (database — related to Courses; modules/lessons/exercises)
├── 🗂️ Projects                           (database — related to Pillars/Phases/Goals)
├── ✅ Tasks                              (database — the daily engine; related to everything above)
├── 🔁 Habit Tracker                      (database)
├── 💹 Trading
│   ├── Trade Journal                     (database)
│   ├── Backtest Log                      (database)
│   └── Strategies                        (database)
├── 🎥 YouTube Pipeline                   (database)
├── 📚 Reading Log                        (database)
├── 💰 Finance Tracker                    (database)
├── 🧳 Travel
│   ├── Trips                             (database)
│   └── Trip Activities                   (database — related to Trips)
├── 📝 Reviews                            (database — Daily/Weekly/Monthly/90-Day/Yearly)
└── ⏱️ Weekly Time Summary                (database — Planned vs Actual)
```

18 databases total (Goals, Pillars, Phases, Courses, Curriculum Items, Projects, Tasks, Habit Tracker, Trade Journal, Backtest Log, Strategies, YouTube Pipeline, Reading Log, Finance Tracker, Trips, Trip Activities, Reviews, Weekly Time Summary), organized into 19 numbered sections below (some sections cover more than one database, e.g. §11 covers all 3 Trading databases). That's the whole system — nothing else gets created later without a specific reason.

---

## 2. DATABASE 1 — ⭐ Pillars

Your 8 life areas. Built once, edited rarely (only when priorities change, e.g. Crypto unlocking).

| Property | Type | Notes |
|---|---|---|
| Name | Title | "Day Trading", "Outsourcing (Workwear)", "YouTube", "AI Automation Agency", "Crypto Trading", "Personal Development", "Reading", "Fitness" |
| Priority | Select | Options: `⭐ Major Priority`, `🔵 Important`, `⚪ Routine`, `🔒 Locked` |
| Current Allocation | Number (or text) | Hours/day, e.g. `5` for Trading |
| Current Phase | Relation → Phases | Set to the one Phase row currently `Active` for this pillar |
| Status | Select | `Active`, `Locked` |
| Description | Text | One line — what this pillar is for |

**Starting rows and Priority values — use `csv-imports/pillars.csv` to load these directly:**

| Name | Priority | Allocation | Status |
|---|---|---|---|
| Day Trading | ⭐ Major Priority | 5 hrs/day, 5 days/week | Active |
| Outsourcing (Workwear) | ⭐ Major Priority | 2 hrs/day, 5 days/week | Active |
| YouTube | ⭐ Major Priority | 1 hr/day, 5 days/week (course phase) | Active |
| AI Automation Agency | 🔒 Locked | 0 | Locked |
| Crypto Trading | 🔒 Locked | 0 | Locked |
| Personal Development | 🔵 Important | 1 hr/day, 5 days/week | Active |
| Reading | ⚪ Routine | 30 min/day | Active |
| Fitness | ⚪ Routine | ~50 min/day | Active |

Note: the priority stars are semantic, not a fixed Notion feature — the `Priority` Select property above **is** the star system. When AI Agency or Crypto unlocks, you just change its Priority value from `🔒 Locked` to `⭐ Major Priority` and Status to `Active` — every dashboard view that filters on Priority updates automatically.

---

## 3. DATABASE 2 — 📈 Phases

Every pillar's phase ladder lives here as individual rows, in order. This is what makes "stable phase = stable schedule" mechanical instead of something you have to remember.

| Property | Type | Notes |
|---|---|---|
| Name | Title | e.g. "Trading — Phase 1: Course Completion" |
| Pillar | Relation → Pillars | |
| Order | Number | 1, 2, 3... within that pillar, so phases sort correctly |
| Status | Select | `Not Started`, `Active`, `Ready for Review`, `Completed` |
| Definition of Done | Text | What "complete" objectively means for this phase (see phase maps in `03-goals-and-phases.md`) |
| Allocation While Active | Text | e.g. "5 hrs/day" — this is what the schedule reads |
| Complete Phase | Button property | See §9 below — one click sets Status→Completed here and Status→Active on the next Order row for the same Pillar |
| Next Phase | Relation → Phases (self-relation) | Point to the next row in the ladder |

**Views:**
- **By Pillar** — Board view grouped by Pillar, sorted by Order. This is your at-a-glance phase map.
- **Active Only** — Table view, filter `Status = Active`. This is what feeds the Today dashboard.

Load all 54 real phase rows (Trading's 22, Outsourcing's 8, YouTube's 4 worlds, Personal Development's 20 sections) from `csv-imports/phases.csv` — see `03-goals-and-phases.md` for the full detail behind each. AI Agency and Crypto get their phase ladders built the same way once/if they're unlocked.

---

## 4. DATABASE 3 — 🎓 Courses

One row per course (not per lesson).

| Property | Type | Notes |
|---|---|---|
| Name | Title | "Personal Development Mastery Course", "Day Trading Course", "Outsourcing Course", "YouTube Course" |
| Pillar | Relation → Pillars | |
| Content Status | Select | `✅ Available`, `⏳ Needs Content` — flags which courses are still missing source material |
| Total Modules/Sections | Number | 20 (PD), 58 sections (Trading), 21 (Outsourcing), 24 (YouTube) |
| Est. Completion (realistic) | Text | See `03-goals-and-phases.md` for each — e.g. Outsourcing's own stated "120 days at 2 hrs/day" |
| Progress % | Rollup | From Curriculum Items: `Percent` of related items where Status = Completed |
| Source | Text/URL | Where the course content lives |

Create all 4 rows now, all Content Status = ✅ Available: Personal Development (20 sections, `course/00-master-curriculum.md`), Day Trading Course (58 sections across 22 phases), Outsourcing Course (21 modules, "120 days at 2 hrs/day" per the course itself), YouTube Course (24 modules across 4 worlds, estimated 10–14 weeks at 1 hr/day — see `03-goals-and-phases.md` §4).

---

## 5. DATABASE 4 — 📖 Curriculum Items

The actual modules/lessons/exercises. This is what daily Tasks pull their content from — it's the mechanism that lets "today's exact lesson" advance automatically without you manually deciding it every morning.

| Property | Type | Notes |
|---|---|---|
| Name | Title | e.g. "Section 1, Day 1 — Active Recall Baseline" |
| Course | Relation → Courses | |
| Order | Number | Global sequence within the course — this is what "next" means |
| Module/Section | Text | e.g. "Section 1 — Meta-Learning" |
| Lesson/Day Ref | Text | e.g. "Day 1" |
| Type | Select | `Lesson`, `Exercise`, `Practical`, `Review`, `Assessment` |
| Est. Minutes | Number | |
| Status | Select | `Not Started`, `In Progress`, `Completed` |
| Milestone | Text | What finishing this item proves |

**View — "Up Next":** Table view per Course, filter `Status ≠ Completed`, sort by `Order` ascending, limit visually to top 1–3. This row is what your Tasks database (below) points to for "today's assignment" in a given pillar.

Load real items for all 4 courses from the CSVs: `curriculum-items-personal-development.csv` (6 rows, Section 1), `curriculum-items-trading.csv` (58 rows, all 22 phases' sections), `curriculum-items-outsourcing.csv` (21 rows, all modules with day ranges), `curriculum-items-youtube.csv` (24 rows, all modules with priority tiers). Import all four into this one database (Notion's CSV import offers "Merge with existing database" — use it) so every course's items live together, distinguished by the `Course` column.

All 4 active courses now have real items loaded via the CSVs above — nothing left empty. If AI Agency or Crypto unlock later, they get their own Curriculum Items the same way once course content exists for them.

---

## 6. DATABASE 5 — 🗂️ Projects

Every business, channel, or non-course goal becomes a project row.

| Property | Type | Notes |
|---|---|---|
| Name | Title | |
| Pillar | Relation → Pillars | |
| Phase | Relation → Phases | |
| Goal | Relation → Goals (see §7) | |
| Status | Select | `Not Started`, `Active`, `Blocked`, `Completed` |
| Priority | Select | `⭐`, `🔵`, `⚪` (mirror the Pillar's, or override per-project) |
| Deadline | Date | |
| Next Action | Text | One line — always kept current, this is the anti-procrastination field from brief section 29 |
| Milestone | Text | |
| Progress | Rollup or Number | % complete, manual or rolled up from linked Tasks |

Starter rows: "Outsourcing — First Customer", "YouTube — Channel Launch", "Trading — Funded Evaluation" (created but Status = Not Started until unlocked by phase progression). Add "AI Agency — First Client" back once that pillar unlocks.

---

## 7. Vision & Goals page — 🎯 Goals database

One database, self-relating, holds the entire ladder from your brief section 21/22.

| Property | Type | Notes |
|---|---|---|
| Name | Title | |
| Level | Select | `Life Vision`, `5-Year`, `3-Year`, `1-Year`, `90-Day`, `Monthly`, `Weekly` |
| Parent Goal | Relation → Goals (self) | Links a Weekly goal up to its Monthly goal, up to its 90-Day goal, etc. |
| Pillar | Relation → Pillars | |
| Status | Select | `Active`, `Achieved`, `Dropped`, `Superseded`, `Future` (goals you've deliberately deferred, like Piano — tracked but not yet competing for time; see `03-goals-and-phases.md` §9) |
| Target Date | Date | |
| Success Criteria | Text | Objective, checkable |

**View — "90-Day Focus":** filter `Level = 90-Day AND Status = Active`. Per brief section 22, keep this view to a small handful of rows — if you have more than ~5 active 90-Day goals, that's a signal you're over-committing, not a signal to build a bigger dashboard.

---

## 8. DATABASE 6 — ✅ Tasks (the daily engine)

Every dashboard view you open each morning is a filtered view of this one database.

| Property | Type | Notes |
|---|---|---|
| Name | Title | |
| Date | Date | |
| Pillar | Relation → Pillars | |
| Curriculum Item | Relation → Curriculum Items | Optional — only for course-learning tasks |
| Project | Relation → Projects | Optional — for execution-phase tasks |
| Priority | Rollup | Pull `Priority` from the related Pillar — this is what makes ⭐ show up automatically, you never set it by hand per task |
| Status | Select | `Not Started`, `In Progress`, `Completed`, `Carried Over` |
| Planned Minutes | Number | |
| Actual Minutes | Number | Filled in at end of day |
| Variance | Formula | `prop("Actual Minutes") - prop("Planned Minutes")` |
| Notes | Text | |

**Formula for Priority icon directly on the Task (alternative to rollup, if you want the emoji inline):**
```
if(prop("Pillar Priority") == "⭐ Major Priority", "⭐", if(prop("Pillar Priority") == "🔵 Important", "🔵", "⚪"))
```
(Requires a rollup property `Pillar Priority` pulling the Pillars' Priority select first, then this formula reads that rollup.)

**Views:**
- **Today** — filter `Date = Today`, group by `Pillar`, sort by `Priority` (⭐ first). **This is your morning dashboard.**
- **This Week** — filter `Date is within next 7 days`, grouped by Pillar.
- **Carried Over** — filter `Status = Carried Over` — surfaces what keeps slipping, feeds your Weekly Review.

---

## 9. THE "COMPLETE PHASE" BUTTON

Notion has a native **Button** property type. On the **Phases** database, add:

- Property `Complete Phase`, type **Button**.
- Configure it with two actions, in order:
  1. **Edit property** → set `Status` = `Completed` (on this row).
  2. **Edit related page's property** → follow the `Next Phase` relation → set that page's `Status` = `Active`.

That's the entire "I confirm completion → next phase activates" mechanism from brief section 7, done with zero automation tooling — one click, native Notion.

Practical effect: when you finish the Trading course phase and click **Complete Phase** on "Trading — Phase 1", the "Trading — Phase 2: Backtesting" row automatically flips to Active. Nothing else changes automatically — and that's deliberate. Your **Pillars** row for Trading still shows "5 hrs/day" until *you* edit it, because time-reallocation is a judgment call (per brief section 7/8), not something a button should silently decide. Treat that edit as part of your phase-transition ritual: click Complete Phase → open the new Phase row → read its "Allocation While Active" field → manually update the Pillar's Current Allocation to match → done. Takes 30 seconds, and it's the one moment your schedule is *allowed* to change.

---

## 10. 🔁 Habit Tracker

One row per day, checkboxes across. Keep it to the habits your brief actually names — do not expand this list.

| Property | Type |
|---|---|
| Date | Title/Date |
| Woke at 5 AM | Checkbox |
| Slept on time | Checkbox |
| Gym | Checkbox |
| Trading block done | Checkbox |
| Outsourcing block done | Checkbox |
| YouTube course block done | Checkbox |
| Reading done | Checkbox |
| Personal Dev done | Checkbox |
| Steps target hit | Checkbox |
| Journaled | Checkbox |
| Content published (if scheduled) | Checkbox |

That's 11 — matches your brief's list, no invented habits. **View:** Calendar or Table, one row auto-created per day (use "Create new database automation: new page daily" or just duplicate yesterday's row each morning — takes 5 seconds).

---

## 11. 💹 Trading — three databases

**Trade Journal:** Date, Instrument, Setup (Select, matches your Strategies names), Direction, Entry, Stop, Target, R:R (Formula from Entry/Stop/Target), Result (Select: Win/Loss/BE), Screenshot (Files), Mistake Tag (Multi-select: e.g. "FOMO entry", "moved stop", "oversized"), Emotion Tag (Multi-select: "Confident", "Anxious", "Revenge", "Calm"), Notes.

**Backtest Log:** Date, Strategy (Relation → Strategies), Instrument, Setup Met? (checkbox), Outcome (Select), Chart (Files), Notes.

**Strategies:** Name, Rules (Text, long-form), Status (Select: `Testing`, `Validated`, `Live`), Backtest Win Rate (Rollup — % of related Backtest Log rows where Outcome = Win), Live Win Rate (same rollup from Trade Journal).

Weekly/Monthly Review questions for trading live inside the shared **Reviews** database (§16) — no separate database needed, that would just duplicate structure.

---

## 12. 🎥 YouTube Pipeline

| Property | Type | Notes |
|---|---|---|
| Title/Idea | Title | |
| Stage | Select | `Idea`, `Research`, `Script/Outline`, `Recorded`, `Sent to Editor`, `Editing`, `Thumbnail`, `Review`, `Revisions`, `Approved`, `Uploaded`, `Promoted` |
| Editor Deadline | Date | |
| Upload Date | Date | |
| Views / CTR / Retention / Avg View Duration / Subs Gained / Likes / Comments / Watch Time | Number (one property each) | Fill in 48h and 7-day after upload |
| Repurposed To | Multi-select | `Shorts`, `TikTok`, `Reels`, `X/Twitter`, `Reddit`, `Discord` |
| Lessons Learned | Text | |

**View — "Board by Stage":** Kanban grouped by Stage — this is your pipeline at a glance, target: never more than 2 videos in "Idea" with none "In Editing."

Platform choice (brief section 15), decided so you don't have to debate it weekly: **YouTube Shorts + TikTok + Instagram Reels** for repurposed clips (same vertical clip, three uploads, minimal extra work), **X/Twitter** for clips/highlights and community-building with other gaming/reaction creators, **Reddit** posted manually to 2–3 relevant subreddits per video where genuinely relevant (not automated, subreddits ban that). Skip Discord and Facebook until you have an audience worth hosting — a Discord with 12 members is a maintenance burden, not promotion.

---

## 13. 📚 Reading Log

| Property | Type | Notes |
|---|---|---|
| Name | Title | Book title |
| Author | Text | |
| Status | Select | `Want to Read`, `Reading`, `Completed`, `Paused`, `DNF` |
| Current Chapter/Page | Text | e.g. "Ch. 7" or "p. 142" |
| Pages / Time | Number | Total pages, or estimated hours — whichever you'd rather track |
| Key Ideas | Text | Running list as you read |
| Lessons | Text | What you're taking from it |
| Practical Application | Text | What you're actually going to do differently because of it |
| Date Completed | Date | |
| Rating | Select | `★☆☆☆☆` through `★★★★★` |

**View — "Currently Reading":** filter `Status = Reading`, should show exactly one book most of the time — this is what your 30-min daily Reading block points to.

---

## 14. 💰 Finance Tracker

Full usage detail lives in `05-finance-habits-reviews.md` §1 — this is the property spec.

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

**Views:** "By Category, this month" (Board grouped by Category, filtered to current month), "Trend" (Table sorted by Month, Sum calculation turned on at the bottom for a running total).

---

## 15. 🧳 Travel — Trips & Trip Activities

You asked for this directly: future trips, when you're going, and what you'll actually be doing. Two related databases, same pattern as Courses → Curriculum Items — one row per trip, many activity rows per trip.

### Trips

| Property | Type | Notes |
|---|---|---|
| Name | Title | e.g. "Bali — January 2027" |
| Destination | Text | |
| Status | Select | `Idea`, `Planning`, `Booked`, `In Progress`, `Completed`, `Cancelled` |
| Start Date | Date | |
| End Date | Date | |
| Duration | Formula | `dateBetween(prop("End Date"), prop("Start Date"), "days")` |
| Days Until | Formula | `dateBetween(prop("Start Date"), now(), "days")` — a live countdown |
| Companions | Text or Multi-select | Who's coming |
| Budget | Number (currency) | Planned |
| Actual Cost | Number (currency) | Filled in after booking |
| Goal | Relation → Goals | Point at your "Travel" 1-Year goal from `03-goals-and-phases.md` §9 |
| Notes | Text | |

### Trip Activities

| Property | Type | Notes |
|---|---|---|
| Name | Title | e.g. "Snorkeling at Menjangan Island" |
| Trip | Relation → Trips | |
| Date | Date | Which day of the trip |
| Category | Select | `Sightseeing`, `Food`, `Adventure`, `Culture`, `Relaxation`, `Nightlife`, `Logistics/Transport` |
| Status | Select | `Idea`, `Booked`, `Confirmed`, `Done` |
| Cost | Number (currency) | |
| Booking Link / Notes | Text or URL | |

**Views:**
- **Trips → "Upcoming"** — Table, filter `Start Date is on or after Today`, sort ascending. This answers "when am I going" at a glance, and the `Days Until` formula gives you a live countdown per trip.
- **Trips → "By Status"** — Board grouped by Status, so Idea vs. actually Booked trips don't blur together.
- **Trip Activities → "By Trip"** — Table grouped by Trip, sorted by Date, so each trip's itinerary reads top to bottom like a real day-by-day plan.

This lives under its own **🧳 Travel** page (a sub-page of Command Centre, or nested under Vision & Goals next to your Travel goal) — it does **not** need to appear on the Today dashboard. Travel isn't a daily driver like Trading or Outsourcing; it's fine for it to live one click away and only get attention when you're actually planning or about to go. If you want a light reminder anyway, add one optional line to the Today page: a linked view of Trips → "Upcoming", limited to 1 row, so your next trip's countdown is visible without cluttering the dashboard with full itinerary detail.

---

## 16. 📝 Reviews (one database, five types)

| Property | Type | Notes |
|---|---|---|
| Name | Title | e.g. "Daily Review — 2026-09-10" |
| Type | Select | `Daily`, `Weekly`, `Monthly`, `90-Day`, `Yearly` |
| Date | Date | |
| What I completed | Text | |
| What I didn't complete | Text | |
| Why | Text | |
| What I learned | Text | |
| Moves to tomorrow/next period | Text | |
| Planned vs Actual (rollup) | Rollup | From Tasks/Weekly Time Summary in the matching date range |
| Time Allocation Change? | Select | `No change`, `Proposed change` — only ticked at Monthly/90-Day/Yearly |

Use **Templates** (Notion's built-in per-database template button) so each review type opens pre-filled with its own question set exactly as your brief lists them in section 27 (Daily/Weekly/Monthly/90-Day questions) — create one template per Type, e.g. clicking "+ New" → "90-Day Review" template pre-fills the 10 questions from brief section 27 verbatim.

---

## 17. ⏱️ Weekly Time Summary

One row per week per Pillar.

| Property | Type |
|---|---|
| Week Of | Date |
| Pillar | Relation → Pillars |
| Planned Hours | Number |
| Actual Hours | Rollup | Sum of `Actual Minutes` from Tasks that week, ÷60, filtered by Pillar |
| Variance | Formula | `prop("Actual Hours") - prop("Planned Hours")` |

This feeds your Weekly/Monthly Review's "Planned vs Actual" section without you calculating anything by hand. Per brief section 26: this is diagnostic, read at reviews only — nothing here auto-changes your schedule.

---

## 18. THE TODAY DASHBOARD PAGE

This is not a database — it's a page with **linked database views** embedded, so it stays visually clean per brief section 19.

Build it in this order, top to bottom:
1. Callout block: today's date, current 90-Day Goal (linked to the Goals row).
2. Linked view of **Tasks → "Today"** view, grouped by Pillar (built in §8). This single embed *is* the "⭐ Trading / ⭐ Outsourcing / ⭐ YouTube / 🧠 PD / 📚 Reading / 💪 Gym" block your brief mockup shows — because each Task under a Pillar already carries that Pillar's name and priority icon in its group header.
3. Linked view of **Phases → "Active Only"** — a one-line reminder of which phase you're in per pillar, so you never lose the "why" behind today's tasks.
4. Linked view of **Habit Tracker**, filtered to today's row only.

Nothing else goes on this page. If a Task isn't scheduled for today, it does not appear — the filter handles "only show what genuinely needs to happen today" automatically, per brief section 19's explicit instruction.

---

## 19. STEP-BY-STEP CONSTRUCTION ORDER

1. Create the parent page **🧭 Command Centre**.
2. Create **Pillars** database, add the 8 rows from §2.
3. Create **Phases** database, relation to Pillars. Import all 54 real phase rows from `csv-imports/phases.csv` (Trading's 22, Outsourcing's 8, YouTube's 4 worlds, Personal Development's 20 sections).
4. Create **Courses** database, relation to Pillars. Add the 4 rows from §4.
5. Create **Curriculum Items** database, relation to Courses. Import all 4 CSVs (Trading 58 rows, Outsourcing 21, YouTube 24, Personal Development 6) — merge into one database as described in §5.
6. Create **Goals** database (self-relation), add your Life Vision + a first 90-Day goal per active pillar.
7. Create **Projects** database, relations to Pillars/Phases/Goals.
8. Create **Tasks** database, relations to Pillars/Curriculum Items/Projects. Add the Priority rollup/formula. Build the **Today** view.
9. Add the **Complete Phase** button property to Phases (§9).
10. Create **Habit Tracker**, add today's row.
11. Create **Trade Journal**, **Backtest Log**, **Strategies** (relate Backtest Log → Strategies).
12. Create **YouTube Pipeline**.
13. Create **Reading Log** per §13's property table.
14. Create **Finance Tracker** per §14's property table.
15. Create **Trips** and **Trip Activities** per §15 — relate Trip Activities → Trips, add the Days Until formula, build the "Upcoming" view.
16. Create **Reviews**, build the 5 templates.
17. Create **Weekly Time Summary**.
18. Build the **TODAY** page (§18) last, once every database it links to exists.

Total one-time build time: roughly 2–3 hours for someone who has never used Notion, most of it in steps 8–15 (typing property names). Steps 1–7 are the ones that matter most to get right since everything else relates back to them.
