# Module 6 — Software Deep Dive

> **In short:** This module walks through every core editing tool in DaVinci Resolve, one clear step at a time — cutting, keyframes, zooms, audio, color, transitions, and export. Go slowly, and actually do each set of steps as you read them.

Module 2 got you through one simple edit. This module builds real skill with the tools you'll use every day. Go through this in order, on real footage, doing each numbered set of steps as you reach it — not just reading them. Each part builds on the last.

## The Edit page vs. the Cut page

DaVinci Resolve has two editing screens:
- **Cut page:** simple and fast. Good for quick trims.
- **Edit page:** full control. Multiple tracks, exact keyframes, detailed settings. **This is where you'll do almost all real comedic editing.** Use this one from here on.

To get there: open your project, and click **Edit** in the row of page buttons at the very bottom of the screen (Media, Cut, **Edit**, Fusion, Color, Fairlight, Deliver).

## Understanding the timeline

The timeline is made of **tracks**. Video tracks stack on top of each other — a higher track shows on top of a lower one. Audio tracks all mix together. A typical timeline for this channel might look like:

```
V4: Text/captions
V3: Memes/reaction images
V2: Facecam
V1: Gameplay (or reaction footage)
A3: SFX
A2: Music
A1: Voice/game audio
```

**To add a track:** right-click any track header (the labeled strip on the left of the timeline, like "V1" or "A1") → **Add Track** → choose Video or Audio. Keep the same layout every project, so you always know "memes go on V3" without having to think about it.

## Cutting and trimming, step by step

**To cut a clip in two:**
1. Click on the clip in the timeline to select it.
2. Move the playhead (the tall vertical line) to the exact frame where you want the cut. Use the Left/Right arrow keys to nudge it one frame at a time.
3. Press **B** to switch to the Blade tool. Your cursor now looks like a small blade.
4. Click on the clip, right at the playhead. It's now two separate clips.
5. Press **A** to switch back to the normal Selection tool, so you don't accidentally cut something else.

**To trim a clip's length (make it shorter or longer):**
1. Move your mouse to the very left or right edge of a clip on the timeline, until the cursor changes to a trim icon (two lines with arrows).
2. Click and drag. Dragging inward makes the clip shorter. Dragging outward makes it longer (up to the length of the original footage).
3. Release the mouse. Note: a normal trim can leave an empty gap behind it — see Ripple Edits below for the version that doesn't.

**To scan through footage quickly, looking for a moment (this saves hours — learn it early):**
1. Click on the timeline or the source clip to make it active.
2. Press **L** to play forward. Press it again to go faster (2x, 4x, and so on).
3. Press **K** to pause instantly.
4. Press **J** to play backward — press it again to go faster in reverse.
5. Tap **K** and then tap **L** or **J** together to step through frame by frame, for very precise positioning.

## Ripple edits, step by step

A **ripple edit** trims or removes a clip *and* automatically pulls everything after it forward, so there's no gap left behind. A normal trim or a normal delete leaves a black gap or silence — a ripple edit closes it for you.

**To ripple-delete a section (the main tool you'll use to cut boring parts, Module 16):**
1. Click the clip or section you want to remove, to select it.
2. Press **Shift+Delete** — or right-click the clip and choose **Ripple Delete**.
3. Everything after it slides forward automatically to close the gap. (Plain **Delete**, without Shift, leaves an empty black gap — avoid that unless you actually want one.)

**To ripple-trim a clip's edge (shortens it and closes the gap in one move):**
1. Near the top-left of the Edit page toolbar, find the trim mode buttons and switch to **Trim Edit** mode (sometimes shown as a small icon that looks like two clip edges).
2. Drag a clip's edge the same way you would for a normal trim.
3. Everything after that clip shifts to follow it automatically — no gap left behind.

**Why this matters:** almost all of your "remove the boring part" work (Module 16) is ripple edits. If you delete something without rippling, you leave an empty gap or silence — just as bad as the boring part was.

## Audio basics, step by step

**To add music or a sound effect:**
1. Drag the audio file from the Media Pool onto an empty audio track (or a new one — right-click a track header → Add Track → Audio) below your video.
2. Trim it the same way you trim video — drag its edges, or use the Blade tool to cut it to length.

**To change a clip's volume:**
1. Click the audio clip to select it.
2. Open the **Inspector** panel (top-right of the screen) and click the **Audio** tab.
3. Drag the **Volume** slider up or down. You'll see the number change in decibels (dB).
4. Alternative: there's also a thin horizontal line running across the clip itself, right on the timeline. Drag that line up or down for a quick volume change without opening the Inspector.

**To fade audio in or out (so music doesn't start or stop suddenly — Module 12 explains exactly when to use this):**
1. Hover your mouse near the top-left or top-right corner of the audio clip on the timeline. A small round fade handle appears.
2. Click and drag that handle inward, toward the middle of the clip. A smooth fade line appears.
3. Do the same on the other corner if you want a fade at both ends.

## Layers, images, and moving things around, step by step

A clip on a **higher video track shows on top of** lower tracks. This is how facecams, memes, and text sit over the gameplay.

**To position or resize an image, meme, or facecam:**
1. Click the clip to select it.
2. Open the **Inspector** panel → **Transform** section.
3. Change **Zoom** to make it bigger or smaller.
4. Change **Pan** (left/right) and **Tilt** (up/down) to move it around the frame.
5. Faster alternative: with the clip selected, look at the preview window (top of the screen) — small square handles appear around the image. Drag them directly with your mouse to resize and reposition, instead of typing exact numbers.

## Adding text, step by step

1. Open the **Effects Library** (top-left of the Edit page).
2. Click **Titles**, and find **Text+** (this gives you more control than the plain "Text" option — use Text+).
3. Drag it onto a track above your footage, at the point where you want it to appear. Trim its length the same way you trim any clip.
4. Double-click the text clip on the timeline, then open the **Inspector** panel.
5. Type your words into the text box in the Inspector.
6. Set the font (pick one from your Module 4/5 library), size, and color.
7. Turn on an outline or drop shadow in the same panel — this keeps white or bold text readable over busy gameplay footage.

## Keyframes — the skill behind zooms and movement

A **keyframe** saves a value (like size or position) at one specific moment in time. Set two keyframes at two different times, and the software automatically fills in the movement between them. That's how a still image becomes a zoom, or a meme slides onto screen.

**Try this now, as a practice drill:**
1. Select a clip. Open Inspector → Transform.
2. Move the playhead to where you want the zoom to *start*. Click the small keyframe icon (it looks like a stopwatch or a diamond) next to **Zoom**. This locks in the current value (like 1.0).
3. Move the playhead forward a few frames. Change the Zoom value (like 1.15). A new keyframe is added automatically.
4. Play it back. The image now smoothly scales up between those two points.

This exact trick — two keyframes, a value change between them — is the whole basis for Module 9's comedic zooms. Practice this before moving on.

## Changing speed, step by step

1. Right-click the clip on the timeline.
2. Choose **Change Clip Speed**.
3. Type a percentage — over 100% speeds the clip up, under 100% slows it down.
4. Click OK, and check how it looks and sounds. If the pitch of any voice or music sounds strange, most speed tools have a "preserve pitch" option nearby — turn it on.

A few ways this channel uses it:
- **Speed ramps** (a gradual speed-up, done with keyframes on the speed value instead of one flat number) build energy heading into a big moment.
- **Fast-forwarding** through slow, repeated gameplay (Module 13), instead of cutting it out completely.

## Basic color, step by step

You don't need to become a professional colorist. Gaming and reaction content usually looks better with a little more punch than raw, flat footage.

1. Click the clip you want to adjust, then click the **Color** page at the bottom of the screen.
2. You'll see three circular **color wheels** (Lift, Gamma, Gain) — these control shadows, midtones, and highlights. If footage looks too dark, drag the middle of the Gamma wheel up slightly.
3. Below the wheels, find the **Contrast** and **Saturation** sliders. Nudge both up a little for a punchier look — small moves go a long way. Don't overdo it.
4. Click back to the **Edit** page when you're done — your changes are already applied to that clip.

**For a quick glow or blur effect** (useful for freeze-frame emphasis, Module 9): open the **Effects Library** on the Edit page, find **Effects** (or **OpenFX**), and drag one — like Blur or Glow — directly onto a clip, the same way you'd drag on a transition.

## Balancing audio, step by step

The basic rule: the creator's **voice stays the loudest and clearest**. Game audio comes second. Music and sound effects support — they never compete. (Modules 10–12 go deeper on the creative side of this.)

1. Look at the **audio meters** — thin vertical bars, usually near the top-right of the screen, that light up as the video plays.
2. Play your video and watch the meters during the loudest moment of dialogue. It should stay comfortably below the red zone at the top (that red zone means clipping — distorted, damaged sound).
3. Select your music or SFX clips and lower their **Volume** in the Inspector (as covered above) until they sit clearly under the voice — you should always be able to understand every word without straining.

## Adding transitions, step by step

1. Open the **Effects Library** → **Transitions**.
2. Drag one — start with a simple **Cross Dissolve** — directly onto the point where two clips meet on the timeline. A small icon appears there.
3. Drag the edges of that icon to make the transition longer or shorter.

Use transitions rarely in this style — Module 7 explains why hard cuts, not transitions, are the usual choice for fast-paced comedic editing.

## Export settings, step by step

1. Click the **Deliver** page at the bottom of the screen.
2. In the presets list (usually on the right), choose **YouTube** and then **1080p** (or **4K**, if your footage is 4K).
3. Under **Filename**, type your file's name, following your Module 1 naming pattern.
4. Under **Location**, click Browse and choose your project's `04_Exports/Drafts/` folder.
5. Click **Add to Render Queue** (bottom-right).
6. In the Render Queue panel, click **Start Render**.
7. When it finishes, open the exported file itself and watch it — don't just trust the timeline preview — before sending it to anyone. Once it's approved, move it into `04_Exports/Final/`.

## If playback is choppy (especially on an older graphics card, like a GTX 1070)

A GTX 1070 (or similar) handles this software fine — but it's an older card, and 4K footage or many effects stacked on one moment can make playback stutter while you're editing. Your export quality is never affected by this — it only affects how smooth things look while you work. Two easy fixes:

**Lower the playback resolution (fastest fix, try this first):**
1. In the top-right corner of the video preview window, click the small resolution dropdown (it might say "Full Res").
2. Change it to **Half Res** or **Quarter Res**.
3. Playback gets much smoother. Your export still renders at full quality — this setting only changes what you see while editing.

**Turn on Optimized Media (helps with heavily-compressed footage, like H.265/HEVC):**
1. Go to the **Media Pool**, right-click the clip (or clips) that are stuttering.
2. Choose **Generate Optimized Media**.
3. Wait for it to process — this creates an easier-to-play version of that footage just for editing. Your original file, and your final export, stay full quality.

## Do this before Module 7

On a throwaway clip: build a 3-track timeline (footage, one image, one text element). Ripple-delete a section cleanly. Add a keyframed zoom on the image. Add a small color boost. Export it. If all of that goes smoothly without you needing to look up a button, you're ready for the creative modules.

Move to [Module 7: YouTube Editing Principles](07-youtube-editing-principles.md).
