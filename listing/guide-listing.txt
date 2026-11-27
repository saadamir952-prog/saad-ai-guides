# One Raw Clip to a Finished Listing Reel — The Free Shot-Plan Setup

**Free guide · Keyword: LISTING · Saad AI**

## The cost — read this first

Claude Code needs a paid Claude plan or API credits. Everything else in
this setup is free: ffmpeg, a local Whisper model for word timings, and
Python with Pillow. Remotion is optional, only if you want animated
panels instead of still graphics.

## The idea in one sentence

Nobody opens a timeline: you write a shot plan where every shot is
anchored to the spoken phrase that triggers it, and code renders the
edit from that plan — cuts, number fills, a chart behind you, and a
measure graphic all land on your words.

## What you need

- One raw talking clip (your own take — this edits a take, it does not
  invent one)
- A computer with a shell, ffmpeg + ffprobe, Python 3, Pillow
- A local Whisper for word timestamps (runs on your CPU, free)
- Claude Code to write and run the edit code

## The setup, step by step

**1. Make the project folder.** One folder per video, with subfolders
for the raw clip, the audio, the graphics, and the export. Keep every
file the edit produces inside it — the shot plan is only useful if the
whole run can be repeated.

**2. Transcribe the raw take.** Run Whisper on the raw clip to get word
timings. Read the transcript against the take: mark the retakes,
blinks-and-restart moments, and dead air you want gone. Whisper's
timings are close, not perfect — check the names and numbers first.

**3. Cut first, decorate later.** Cut the retakes and pauses from the
take with ffmpeg, using the transcript marks. Short crossfades on the
joins keep the voice smooth. This tightened take is the spine of the
edit; everything else is timed against it.

**4. Transcribe the tightened take to `words.json`.** Run Whisper again
on the cut take and save one row per word: the word, its start, its
end. These timings — not hand-typed timestamps — drive every graphic
from here on.

**5. Write the shot plan.** One row per shot:
`{layout, anchor_phrase, content}`. The `anchor_phrase` is matched
against `words.json`, so the shot starts when those words are said.
Example rows from a listing-style edit:

- `{layout: "finished-frame", anchor_phrase: "four bedrooms", content: "big 4 fills in on the word Four"}`
- `{layout: "chart-behind", anchor_phrase: "a chart rises", content: "two bars rise behind the speaker — only numbers actually spoken"}`
- `{layout: "measure", anchor_phrase: "twelve-meter pool", content: "measure line draws across the pool visual"}`
- `{layout: "prompt-window", anchor_phrase: "shot plan", content: "the shot-plan rows appear, matched to the voice"}`

Only put numbers in the chart that the speaker actually says. No
invented stats, no fake prices.

**6. Render the edit from the plan, by code.** Your render code reads
the shot plan, looks up each anchor phrase in `words.json`, and places
the graphic on that word: number fills highlight on their spoken word,
the chart rises behind the speaker, the measure line draws while the
pool is named. Because the edit is rendered from the plan, nobody
opened a timeline — change a row, re-render, done.

**7. Captions last, on the final audio.** Caption text comes from your
script; caption timing comes from Whisper on the finished audio, so
the words land with the voice the viewer actually hears. Highlight the
current word; keep chunks short enough to read at speed.

**8. Check the export before you post.** Watch the whole video once
with sound and once muted. Confirm: no silent gaps, every number
appears on its word, the chart carries only spoken numbers, and the
measure graphic lands while the pool is named.

## The honest catch

This will not save a boring take. The cuts, fills, and graphics are
timed to your words — your words still have to land. A weak script
with perfect timing is still a weak video.

This guide is free. If you want the full editor system behind these
videos, the Complete Editor Pack ($39, one-time) is linked in my bio.

Saad AI (@saad.aig) · Keyword: LISTING
