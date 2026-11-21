Edit my video: cut silences, add captions, export vertical.

# The Exact Prompt — TIME video

Free from Saad AI (@saad.aig). The first line above is the exact prompt
from the video, verbatim — copy it, paste it into Claude Code, and let
it run. The rest of this file explains how to adapt it.

Full guide: https://saadamir952-prog.github.io/saad-ai-guides/minutes/

---

## What the line does

One line, three jobs:

1. **Cut silences** — every dead gap in the voiceover is detected and
   cut. (Measured: 7.2 s on the run in the video.)
2. **Add captions** — word-by-word captions, timed to the speech.
   (Measured: 5.2 s.)
3. **Export vertical** — the final export, mastered sound, 1080×1920.
   (Measured: 19.5 s including the encode.)

Total: 32.1 seconds. The same edit by hand took three hours.

## How to adapt it

Add ONE detail at a time — the more specific the line, the closer the
first draft lands:

- **Length:** `Edit my video: cut silences, add captions, export
  vertical. Keep it under 30 seconds.`
- **Caption style:** `Edit my video: cut silences, add captions,
  export vertical. Word-by-word captions, bold, bottom third.`
- **Platform:** `Edit my video: cut silences, add captions, export
  vertical 1080x1920 for Reels.`
- **Keep a pause:** `Edit my video: cut silences, add captions,
  export vertical. Keep the pause before the last line — it's
  the beat.`

## What it does NOT do

- **It does not pick your takes.** Watch your clips once, keep the
  ones you want, drop the rest — before you type the line.
- **It does not grade colour.** If your footage needs a look, grade
  it yourself first. The edit will be clean; the colour will be
  whatever your camera gave you.
- **It does not write your script.** The prompt edits what you shot.
  The idea, the hook, the words — those are yours.

## If the first draft is off

Don't re-type the whole line. Tell Claude what to fix in one more
line, e.g.:

- `Make the captions bigger.`
- `Cut the last 2 seconds.`
- `The voice is too quiet — raise it.`

Then re-export. The loop is fast because the run is seconds.

## The full pipeline

This prompt is the free DIY version. If you want the whole pipeline
packaged — transcribe, cut the silences, pick the best takes,
animated captions, SFX, and a mastered export — the Claude Video
Editor skill does it in one command. $20, one-time payment:
https://saadai.gumroad.com/l/claude-video-editor
