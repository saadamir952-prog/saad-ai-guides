# Claude Can Hear Its Own Edit — The Earshot Setup

**Free guide · Keyword: LISTEN · Saad AI**

## The cost — read this first

Earshot itself is **free and open-source (MIT)** and runs on your own
computer's CPU. The one paid part is **Claude Code, which needs a paid
Claude plan**. You also need Python 3.10 or newer and ffmpeg. The
listening models (about 1.1 GB) download once on first use; after that
it works offline.

## The idea in one sentence

Claude can cut your video, but it cannot hear it — Earshot gives it
ears, so it describes a sound in words, scores it against the sound you
asked for, and grades your whole video's audio with fixes listed worst
first.

## The proof (from the video, run for real)

On our own sound file (`sound-04.wav`, a classic telephone ring):

- **describe** → Ringtone 0.83 · Telephone bell ringing 0.53 ·
  "a phone ringing" (z +2.4)
- **match** "a classic telephone ringing" → **strong (z +3.8, ranked
  #1 of 322 descriptions)**; the wrong description "rain on a window"
  → **no match (z −0.2)**
- **critique** on our last posted video → **needs work, 19/23 metrics
  in range**, fixes listed worst first

## Setup (copy-paste)

Mac / Linux terminal (Windows: same commands in PowerShell, use
`python -m pip` if `pip` is not found):

```
pip install torch --index-url https://download.pytorch.org/whl/cpu
pip install "earshot[listen,mcp] @ git+https://github.com/Leonxlnx/earshot"
earshot doctor --fetch
claude mcp add earshot --scope user -e EARSHOT_THREADS=3 -- earshot mcp
```

The first line is optional — it installs the smaller CPU build of
torch. `earshot doctor --fetch` downloads the listening models now
instead of on first use. The last line connects Earshot to Claude Code
as an MCP server, so Claude can call it directly.

## The 3 commands from the video

**1. Describe — what does this sound actually sound like?**

```
earshot describe sound.wav
```

You get plain-language tags with scores, AudioSet labels, and
measurements (loudness, brightness, attack/decay). Use it when a file
name tells you nothing.

**2. Match — is this the sound I asked for?**

```
earshot match sound.wav "a classic telephone ringing"
```

You get a verdict — strong, plausible, weak, or no match — with a
z-score. Write the sound you want in plain words (source + material +
action, e.g. "a deep thocky mechanical keyboard press"), and add
`--alts` with realistic alternatives to sharpen the choice.

**3. Critique — grade the whole video's sound**

```
earshot critique video.mp4
```

You get a scorecard against seven professional launch films: each
metric ok / low / high, a verdict (launch-grade / close / needs work /
not launch-grade), and timestamped fixes, worst first. Fix the
critical rows, re-render, run it again.

Two more checks worth knowing: `earshot find` locates the best moment
inside a long recording, and `earshot realness` flags whether a sound
reads as a real recording or code-synthesized. Together with the three
above, those are the five checks from the video.

## The honest limits

- It cannot judge **taste, emotion, or speech content** — it hears
  that there is speech, not what is said.
- **Busy mixes blur it**: tags inside dense material are hints, not
  facts. Describe a stem or a short segment when you can.
- Very short sounds (under ~0.5 s) read weakly; judge the exact trim
  you will use.
- It compares against launch-film references — a "fix" that fights
  your format (for example, our videos use no music on purpose) is
  yours to overrule. **Listen once yourself** before you post.

## One line on the pack

This guide is free. If you want the full editor system behind these
videos, the Complete Editor Pack ($39, one-time) is linked in my bio.

— Saad AI (@saad.aig)
