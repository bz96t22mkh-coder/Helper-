# Module 6 — Software Deep Dive

> **In short:** This is where you learn the real editing tools — cutting, keyframes, zooms, audio, color, and exporting. Go slowly. These skills are used in almost every video you'll edit.

Module 2 got you through one simple edit. This module builds real skill with the tools you'll use every day. Go through this in order. Each part builds on the last.

## The Edit page vs. the Cut page

DaVinci Resolve has two editing screens:
- **Cut page:** simple and fast. Good for quick trims.
- **Edit page:** full control. Multiple tracks, exact keyframes, detailed settings. **This is where you'll do almost all real comedic editing.** Use this one from here on.

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

Right-click a track header → **Add Track** to build this out. Keep the same layout every project, so you always know "memes go on V3" without having to think about it.

## Cutting and trimming

- **Blade tool (press B):** click a clip to split it at that point.
- **Trimming:** hover over a clip's edge until the cursor changes, then drag. This changes the clip's length without moving other clips — but it can leave a gap (see ripple edits below).
- **JKL playback:** press **L** to play forward, **K** to pause, **J** to play backward. Tap again to change speed. This is the fastest way to scan through footage looking for a moment. Learn this early — it saves hours.

## Ripple edits

A **ripple edit** trims a clip *and* automatically pulls everything after it forward, closing the gap. A normal trim leaves a black gap. A ripple edit doesn't.

- **Ripple Delete** (press Shift+Delete, or right-click → Ripple Delete): removes the clip and closes the gap.
- **Ripple trim:** with Trim Edit mode on, dragging a clip's edge also shifts everything after it.

**Why this matters:** almost all of your "remove the boring part" work (Module 16) is ripple edits. If you delete something without rippling, you leave an empty gap or silence — just as bad as the boring part was.

## Audio basics

- Drag audio (music, sound effects, voice) onto its own track, same as video.
- **Volume:** select the clip → Inspector (top-right) → Audio tab → adjust Volume. Or drag the small line right on the clip in the timeline.
- **Fades:** hover near the top corner of a clip until a fade handle appears, then drag inward. Use this on music so it doesn't start or stop suddenly (Module 12 explains exactly when).

## Layers, images, and moving things around

- A clip on a **higher video track shows on top of** lower tracks. This is how facecams, memes, and text sit over the gameplay.
- Select a clip → Inspector → **Transform** panel: change **Zoom** (size), **Pan/Tilt** (position), and **Rotation**. This is how you position a facecam in a corner, or resize a meme.
- You can also drag the handles directly on the preview window — often faster than typing exact numbers.

## Adding text

- Go to **Effects Library → Titles → Text+** (this gives you more control than the basic Text option). Drag it onto a track above your footage.
- In the Inspector, set the font (from your Module 4/5 library), size, color, and position. Add an outline or drop shadow — this keeps white or bold text readable over busy gameplay.

## Keyframes — the skill behind zooms and movement

A **keyframe** saves a value (like size or position) at one specific moment in time. Set two keyframes at two different times, and the software automatically fills in the movement between them. That's how a still image becomes a zoom, or a meme slides onto screen.

**Try this now, as a practice drill:**
1. Select a clip. Open Inspector → Transform.
2. Move the playhead to where you want the zoom to *start*. Click the small keyframe icon next to **Zoom**. This locks in the current value (like 1.0).
3. Move the playhead forward a few frames. Change the Zoom value (like 1.15). A new keyframe is added automatically.
4. Play it back. The image now smoothly scales up between those two points.

This exact trick — two keyframes, a value change between them — is the whole basis for Module 9's comedic zooms. Practice this before moving on.

## Changing speed

Right-click a clip → **Change Clip Speed** (or use the Inspector's speed control). A few ways this channel uses it:
- **Speed ramps** (a gradual speed-up) build energy heading into a big moment.
- **Fast-forwarding** through slow, repeated gameplay (Module 13), instead of cutting it out completely.

## Basic effects and color

You don't need to become a professional colorist. What you actually need:
- **Color page (basic use):** select a clip, go to the Color page, and use the color wheels to fix footage that's too dark. Use the Contrast and Saturation sliders to make it feel punchier. Gaming and reaction content usually looks better with a little more saturation and contrast than raw, flat footage.
- **Effects Library → Effects/OpenFX** (on the Edit page): drag a basic blur or glow onto a clip like a transition. Good for freeze-frame emphasis (Module 9).

## Balancing audio

Covered in more depth in Modules 10–12. The basic rule: the creator's **voice stays the loudest and clearest**. Game audio comes second. Music and sound effects support — they never compete. Watch the audio meters at the top of the screen. Keep voice levels safely below the red "clipping" zone, with music noticeably quieter underneath.

## Adding transitions

Covered in more depth in Module 7. To add one: drag it from **Effects Library → Transitions** onto the point where two clips meet. Drag its edges to change how long it lasts.

## Export settings

On the **Deliver** page:
- **Format:** MP4. **Codec:** H.264 works well and is widely supported.
- **Resolution:** match your project — usually 1080p, or 4K if your source footage is 4K.
- **Frame rate:** match your source footage exactly. Don't drop 60fps gameplay down to 30fps — you'll lose the smoothness that matters for gaming content.
- **Bitrate:** just use the built-in **YouTube preset**. It's already set up correctly.
- Always export to `04_Exports/Drafts/` first. Watch the actual exported file — not just the timeline preview — before sending it to anyone. Then move the approved final version into `04_Exports/Final/`.

## Do this before Module 7

On a throwaway clip: build a 3-track timeline (footage, one image, one text element). Ripple-delete a section cleanly. Add a keyframed zoom on the image. Add a small color boost. Export it. If all of that goes smoothly without you needing to look up a button, you're ready for the creative modules.

Move to [Module 7: YouTube Editing Principles](07-youtube-editing-principles.md).
