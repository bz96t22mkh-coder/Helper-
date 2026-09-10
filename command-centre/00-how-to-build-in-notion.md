# How To Actually Build This In Notion

Two ways to get this into your Notion account. Read §0 to pick, then follow the path.

## 0. Pick a path

| | Manual build (below) | Notion connector |
|---|---|---|
| What it is | You click through Notion yourself, following exact steps | You connect your Notion account to Claude, and Claude creates the pages/databases for you via the Notion API |
| Works right now, in this conversation? | Yes | **No** — this conversation is a coding session wired to your GitHub repo, not a general claude.ai chat. It can't reach your Notion account even if you connect it. |
| How to use it | Follow §1–§6 below | Go to claude.ai → Settings → Connectors → find **Notion** → Connect → authorize it to access your workspace/pages. Then open a **new, regular Claude chat** (not this one) and say "build my life command centre from this spec" and point it at this repo's `command-centre/` folder. It can then create pages, databases, and content directly. |

**My recommendation: do the manual build.** It's the same total effort either way (the connector still needs you to review/approve everything it creates, and mistakes are harder to fix after the fact than to avoid by building it yourself once, carefully). The manual path also means you actually understand where everything lives, which matters for a system you're going to run your life through daily. Budget **2–3 hours**, one sitting if possible.

---

## 1. Create the workspace

1. Go to notion.so, sign in (or create a free account).
2. Sidebar → **+ New page** → name it **🧭 Command Centre**. Leave it empty for now — this is your parent page, everything else nests under it.

## 2. Build each database using CSV import (fastest way to get rows in)

I've pre-built the row data for you as CSV files in `command-centre/csv-imports/` in this repo, now from your **real course files**:
- `pillars.csv` → 8 rows (Trading, Outsourcing, YouTube, Personal Development, Reading, Fitness active; AI Agency and Crypto locked)
- `phases.csv` → 54 rows: Trading's real 22-phase ladder, Outsourcing's real 8-phase ladder, YouTube's real 4-world ladder, and all 20 Personal Development sections
- `curriculum-items-trading.csv` → 58 rows, one per real section of the Trading course, with real minutes
- `curriculum-items-outsourcing.csv` → 21 rows, one per real module, with the course's own day ranges
- `curriculum-items-youtube.csv` → 24 rows, one per real module, with priority tiers
- `curriculum-items-personal-development.csv` → the real Section 1, Day 1–6 content
- `goals.csv` → your Life Vision + 5 real starter 90-Day goals + 6 hobby/lifestyle 1-Year goals (hiking, cooking, social life, travel, tennis, and piano as a deliberately Future one)

**To import each one:**
1. Open your **Command Centre** page.
2. Type `/` → choose **Import**.
3. Select **CSV** as the source, choose the file from your computer (download it from this repo first — open the file on GitHub, click "Raw," save it, or clone the repo).
4. Notion creates a new full-page database named after the file, with one column per CSV header and one row per line. Rename the page to match the names in `01-notion-architecture.md` (e.g. rename to "⭐ Pillars", "📈 Phases", "🎯 Goals"). For the four Curriculum Items CSVs, import all four into the **same** "📖 Curriculum Items" database — Notion's CSV import has a "Merge with existing database" option when you import into a page that already holds one; use it so all your courses' items end up in one database, distinguished by their `Course` column.

Do this 7 times — once per CSV. That gets ~110 rows of real data into Notion in about 20–25 minutes total, instead of typing them by hand.

## 3. Fix property types after each import

CSV import makes every column plain **Text**. You need to change some to their real type, per the exact spec in `01-notion-architecture.md`. For each database, click the column header → **Edit property** → change **Type**:

- **Pillars:** `Priority` → Select (it'll auto-create the 4 options from your existing text values). `Status` → Select.
- **Phases:** `Status` → Select (options: Not Started, Active, Ready for Review, Completed). `Order` → Number.
- **Curriculum Items:** `Order` → Number. `Est. Minutes` → Number. `Type` → Select. `Status` → Select.
- **Goals:** `Level` → Select. `Status` → Select. `Target Date` → Date.

## 4. Add the databases that don't need pre-loaded rows

These start empty — create them directly (Command Centre page → `/table` → **Table - Full page**, name it, then add properties one by one via the **+** at the right end of the column headers): **Courses**, **Projects**, **Tasks**, **Habit Tracker**, **Trade Journal**, **Backtest Log**, **Strategies**, **YouTube Pipeline**, **Reading Log**, **Finance Tracker**, **Trips**, **Trip Activities**, **Reviews**, **Weekly Time Summary**. Full property lists for every one of these are in `01-notion-architecture.md` §2–§17 — go column by column, typing the property name then picking its Type from the dropdown. **Trips/Trip Activities** (§15) is where your future trips and their planned activities live — start empty and add a row each time you're thinking about a trip, no need to front-load anything.

For **Courses**, add these 4 rows by hand (only 4, faster than a CSV, all ✅ Available now): Personal Development Mastery Course, Day Trading Course, Outsourcing Course, YouTube Course.

## 5. Wire up relations, rollups, formulas, and the button

This is the part CSV import can't do — do it once per database, it only takes a few minutes each since you already have the rows:

1. **Relations:** on each database, add a property → Type **Relation** → pick the target database. Then open each row and link it (e.g. on every Phases row, click into `Pillar` and pick the matching Pillar — with only ~30 rows this is quick).
2. **Rollups:** add property → Type **Rollup** → pick the Relation to go through → pick which property of the related page to show → pick the calculation (Sum/Percent/Count as specified per-database in `01-notion-architecture.md`).
3. **Formulas:** add property → Type **Formula** → paste the exact formula text given in `01-notion-architecture.md` (e.g. Tasks' `Variance` formula, the Priority-icon formula) into the formula editor.
4. **The Complete Phase button** (on Phases): add property → Type **Button** → **Edit** → add action **Edit page** (this page) → set `Status` = Completed → add a second action **Edit related page's property**, follow `Next Phase` → set `Status` = Active. Full spec in `01-notion-architecture.md` §9.

## 6. Build the views and the Today dashboard

For each database, click **+ Add a view** at the top to create the Table/Board views listed in `01-notion-architecture.md` (e.g. Tasks → "Today" view: Filter → `Date` → `is` → `Today`; Group by → `Pillar`; Sort → `Priority`; Trips → "Upcoming" view: Filter → `Start Date` → `is on or after` → `Today`, sorted ascending). Then build the **TODAY** page last (§18 of that file) by going to your Command Centre page, typing `/` → **Linked view of database** → picking Tasks' "Today" view, and repeating for Phases' "Active Only" view and today's Habit Tracker row.

---

## Status: all 4 active courses now have real content loaded

Trading, Outsourcing, YouTube, and Personal Development all have real phases/modules/sections loaded into the CSVs above — no more placeholders. AI Automation Agency and Crypto stay locked/future (see `03-goals-and-phases.md` §6–7); when you're ready to revisit either, send the course content the same way and it gets the same treatment.
