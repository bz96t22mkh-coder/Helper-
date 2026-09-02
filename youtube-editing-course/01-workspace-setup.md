# Module 1 — Workspace Setup

> **In short:** Before you edit anything, set up your computer, your storage, and a folder system. This stops you from losing files or wasting time searching for them later.

## 1. What computer do you need?

You don't need an expensive computer to start. You need a computer that can handle gaming footage plus a webcam overlay without freezing up.

Rough beginner targets:

| Part | Minimum (it works) | Comfortable |
|---|---|---|
| CPU (processor) | 6-core, made in the last ~4 years | 8-core or more |
| RAM (memory) | 16GB | 32GB |
| GPU (graphics card) | Any with 4GB+ of its own memory | A strong gaming-level GPU |
| Storage | 1TB, with a separate drive just for footage | 2TB+ fast SSD |
| Screen | One monitor works | Two monitors — one for editing, one for browsing |

**Why this matters:** if your computer is slow, playback will lag while you're trying to find the funny moment. That makes it hard to feel the comedy timing. If your computer is slower, edit at a lower preview quality (Module 6 shows you how) instead of fighting full-quality playback.

### Is a GTX 1070 good enough?

If your GPU is a GTX 1070 (or a similar card from around the same time — a GTX 1080, or an RTX 2060/2070): **yes, it's good enough to start.** Here's why:

- It has 8GB of its own memory. That's above the minimum DaVinci Resolve needs, and enough for 1080p editing without trouble.
- It supports the graphics processing DaVinci Resolve relies on (called CUDA, if you ever see that word in a settings menu).

A couple of things to know, since it's an older card (it came out in 2016):

- It doesn't have some of the newest hardware tricks that brand-new graphics cards have. So if your footage is 4K, or recorded in a newer, heavily-compressed format (you'll sometimes see this called "H.265" or "HEVC"), playback might stutter, especially once you stack several memes, zooms, and effects on the same moment.
- If that happens, don't assume something is broken. It's just your GPU working hard. Module 6 shows you two easy settings — **Optimized Media** and a lower **timeline playback resolution** — that fix this in a couple of clicks. You still export in full quality at the end. You're just previewing at a lower quality while you work.

In short: edit your videos, and if playback ever gets choppy, turn to Module 6's "if playback is choppy" section before worrying that your computer isn't good enough. For this channel's kind of content, it is.

## 2. How much storage do you need?

Raw gaming footage takes up a lot of space.

- 1080p60 gameplay: about 8–15GB per hour.
- 1440p or 4K footage: 2–4 times that.
- A facecam records as a second file on top of that.

**Simple rule:** plan for at least 3x the raw footage size per project. That leaves room for cache files and exports. If you record 3 videos a week at 30GB each, that's about 90GB a week — a 1TB drive fills up in a couple of months.

**A simple two-drive setup, once you're doing this regularly:**
- **Working drive** (fast SSD): the footage and project you're editing right now.
- **Archive drive** (a cheaper external drive, or cloud storage): finished projects, moved off your working drive once the video is published.

## 3. Set up your folders

Use the exact same folder layout every single time. That way, you never have to think about where something is.

```
YouTube-Channel/
├── 00-ASSETS-LIBRARY/              ← shared across ALL videos (see Module 5)
│   ├── Music/
│   ├── SFX/
│   ├── Memes-Images/
│   ├── Memes-GIFs/
│   ├── Overlays/
│   ├── Fonts/
│   └── Stock-Footage/
│
├── 01-Projects/
│   ├── 2026-09-03_GameName_Ep12/
│   │   ├── 01_Raw_Footage/
│   │   │   ├── Gameplay/
│   │   │   ├── Facecam/
│   │   │   └── Mic_Audio/          ← if recorded separately
│   │   ├── 02_Project_Files/       ← your editing software's project file
│   │   ├── 03_Assets_Used/         ← memes/SFX used in this video
│   │   ├── 04_Exports/
│   │   │   ├── Drafts/
│   │   │   └── Final/
│   │   └── 05_Notes/               ← Editor Brief, script, notes (Modules 18–19)
│   └── 2026-09-10_GameName_Ep13/
│       └── ...
│
└── 02-Archive/                     ← finished, published projects go here
```

Every project folder should look exactly the same. On project #40, you'll already know exactly where everything is.

## 4. Name your files clearly

A bad file name — like `final2_REAL_use_this_one.mp4` — costs you time every time you look at it. It's also how the wrong file accidentally gets uploaded.

**Use this pattern:** `YYYY-MM-DD_Project_Description_vXX.ext`

Examples:
- `2026-09-03_MinecraftEp12_RawGameplay.mp4`
- `2026-09-03_MinecraftEp12_Facecam.mp4`
- `2026-09-06_MinecraftEp12_Draft_v1.mp4`
- `2026-09-08_MinecraftEp12_Draft_v2_AfterFeedback.mp4`
- `2026-09-09_MinecraftEp12_FINAL_v3.mp4`

Simple rules:
- Put the date first, so files sort in order automatically.
- Never just call something "final." Always add a version number: `v1`, `v2`, `FINAL_v3`. A second "final" export becomes `FINAL_v4`.
- Avoid spaces in file names. Use underscores or hyphens instead.
- Never rename the original raw footage files. Rename copies and exports instead.

## 5. Where things go

- **Raw footage** goes in that episode's `01_Raw_Footage/` folder. Never mix footage from different episodes. Never edit the original file directly — always work from a copy or reference it, and keep the original untouched.
- **Music and sound effects** live in the shared `00-ASSETS-LIBRARY/` folder, sorted by type and mood (Module 5 shows the full layout). When you use one in a project, copy it into that project's `03_Assets_Used/` folder — don't move the original out of the library.
- **Memes and reaction images** also live in the shared library (Modules 4–5). Never save a meme straight into a project folder without knowing where it came from — you need to know its source to check if it's legal to use (Module 3).
- **Project files** go in `02_Project_Files/`. Keep autosave turned on.

## 6. Back up your work

A lost project means a lost video. Follow this simple version of the **3-2-1 rule**:

- Keep **at least 2 copies** of anything you can't easily redo — raw footage, finished exports, project files.
- Keep **1 copy somewhere else** — an external drive, or cloud storage like Google Drive or Dropbox.
- **Back up after every recording session.** Raw footage is the hardest thing to replace — if it's gone, it's gone.
- **Back up after big milestones too** — when the rough cut is done, and when the final version is approved.

For now, a simple habit works: plug in an external drive and copy that week's `01-Projects/` folder onto it. You can automate this later once the channel grows.

## Do this before Module 2

1. Create your `00-ASSETS-LIBRARY/`, `01-Projects/`, and `02-Archive/` folders.
2. Create one test project folder, using the layout above.
3. Set up a backup destination — even just a plugged-in external drive is enough for now.

Then move to [Module 2: Software Selection & First Edit](02-software-selection.md).
