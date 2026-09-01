# Module 1 — Workspace Setup

Before you edit a single frame, you need a system: a computer that can handle the work, enough storage, and a folder structure that means you never lose a file or waste ten minutes hunting for "that one sound effect." This module builds that foundation.

## 1. Computer specifications

You don't need a $4,000 workstation to start. You need a machine that won't choke on 1080p/1440p gaming footage with a webcam overlay. Rough beginner-friendly targets:

| Component | Minimum (workable) | Comfortable |
|---|---|---|
| CPU | 6-core modern (Ryzen 5 / Intel i5, last ~4 years) | 8-core+ (Ryzen 7/9, Intel i7/i9) |
| RAM | 16GB | 32GB |
| GPU | Any dedicated GPU with 4GB+ VRAM (GTX 1650 / RX 6600 class) | RTX 3060/4060 class or better — DaVinci Resolve leans heavily on GPU for effects and color |
| Storage | 1TB total, with a separate drive/partition for footage | 2TB+ NVMe SSD as your working (scratch) drive |
| Display | One monitor works | Two monitors — one for the timeline/preview, one for browser (memes, references, communication with the creator) |

**Why this matters practically:** gaming footage plus a facecam plus effects layers is genuinely demanding to scrub through in real time. Underpowered hardware doesn't just mean slower exports — it means laggy playback while you're trying to *find the funny moment*, which kills your ability to feel the comedic timing. If you're stuck on weaker hardware for now, edit at a lower "proxy" preview resolution (covered in Module 6) rather than fighting full-res playback.

## 2. Storage requirements

Raw gaming/reaction footage is large. A rough budget:

- 1080p60 gameplay recording: roughly 8–15GB per hour, depending on codec/bitrate.
- 1440p/4K footage: 2–4x that.
- Add a facecam layer, and you're recording two files at once.

**Rule of thumb:** budget for at least 3x the raw footage size per project, to leave room for the project's cache/render files and export(s). If you record 3 videos a week at ~30GB of raw footage each, that's ~90GB/week just in source footage — a 1TB drive fills up in a couple of months. Plan for an external HDD/SSD (or NAS) as an archive drive, separate from your fast working drive.

**Two-drive setup (recommended once you're doing this regularly):**
- **Working drive** (SSD, ideally NVMe): current project's footage, project files, cache. Fast, because the software reads/writes here constantly.
- **Archive drive** (HDD is fine, or cloud/NAS backup): finished projects and their footage, moved off the working drive once a video is published, kept in case of future re-edits or copyright disputes.

## 3. Folder structure

Consistency matters more than the "perfect" structure. Use the same skeleton for every project so you (or the creator) can find anything without asking. A structure that works well for a Gaming + Reaction channel:

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
│   │   ├── 02_Project_Files/       ← .drp / .prproj etc., autosaves
│   │   ├── 03_Assets_Used/         ← video-specific memes/SFX pulled in from the library, kept for reference
│   │   ├── 04_Exports/
│   │   │   ├── Drafts/
│   │   │   └── Final/
│   │   └── 05_Notes/               ← the Editor Brief, timestamps, script/plan (Module 18–19)
│   └── 2026-09-10_GameName_Ep13/
│       └── ...
│
└── 02-Archive/                     ← finished, published projects moved here
```

Keep every project folder named and shaped identically. When you open project #40, you already know exactly where the raw footage and the final export live, without thinking.

## 4. Naming files properly

Bad names (`final2_REAL_use_this_one.mp4`, `IMG_4821.mov`) cost you time every single time you touch the project later, and they're how the wrong version accidentally gets uploaded. Use a consistent, sortable pattern:

**Format:** `YYYY-MM-DD_Project_Description_vXX.ext`

Examples:
- `2026-09-03_MinecraftEp12_RawGameplay.mp4`
- `2026-09-03_MinecraftEp12_Facecam.mp4`
- `2026-09-06_MinecraftEp12_Draft_v1.mp4`
- `2026-09-08_MinecraftEp12_Draft_v2_AfterFeedback.mp4`
- `2026-09-09_MinecraftEp12_FINAL_v3.mp4`

Rules:
- Date first (`YYYY-MM-DD`) so files sort chronologically by default.
- Never call anything just "final" — always version it (`v1`, `v2`, `FINAL_v3`). If a second "final" export happens, it's `FINAL_v4`, not a second file called `FINAL`.
- No spaces if you can avoid it (use underscores or hyphens) — spaces sometimes cause problems when files are shared through certain upload tools or command-line processes.
- Keep the raw footage filenames the recording software gives you (don't rename source files — you risk breaking the link between the project file and the media). Rename copies/exports instead.

## 5. Organizing raw footage, music, sound effects, and memes

- **Raw footage** lives in that episode's `01_Raw_Footage/` folder, never mixed with other episodes, and never edited/trimmed in place — always work from the original, uncut file.
- **Music and SFX** live in the shared `00-ASSETS-LIBRARY/`, organized by category (Module 5 covers the exact structure — e.g., music by mood, SFX by emotion: "shock," "fail," "victory"). When you use a track in a specific project, don't move it — copy or reference it into that project's `03_Assets_Used/` folder so the library stays intact for the next video.
- **Memes/reaction images/GIFs** also live in the shared library, organized by the emotion or moment they fit (Module 4–5 cover exactly how). Never save a meme straight from a random search result into a project folder and forget where it came from — you need to know the source to check its license (Module 3).
- **Project files** (the actual `.drp`, `.prproj`, or CapCut project) go in `02_Project_Files/`, and most editing software auto-saves/versions there too — don't disable autosave.

## 6. Backing up projects

A lost project is a lost video and lost trust. Follow the **3-2-1 rule**, simplified for a small channel:

- **At least 2 copies** of anything irreplaceable (raw footage, finished exports, project files) — the working copy on your fast drive, plus one backup.
- **One of those copies off your main machine** — an external drive, a NAS, or cloud storage (Google Drive, Dropbox, Backblaze, etc.).
- **Back up after every recording session** (raw footage is the least replaceable thing you own — if the creator's gameplay session is gone, it's gone) and **after every major edit milestone** (rough cut done, final approved).

Practically, for a beginner: an external hard drive you copy the week's `01-Projects/` folder onto is enough. Automate it later with backup software or a cloud-sync folder once the channel is generating enough footage that manual copying gets tedious.

## Do this before Module 2

1. Create your `00-ASSETS-LIBRARY/`, `01-Projects/`, and `02-Archive/` top-level folders.
2. Create one project folder for a test video using the structure above.
3. Set up (or confirm you have) a backup destination — even just an external drive plugged in and ready.

Then move to [Module 2: Software Selection & First Edit](02-software-selection.md).
