# Claude Edits Inside Your Timeline — The VN MCP Setup

**Free guide · Keyword: MCP · Saad AI**

## The cost — read this first

**Claude Code needs a paid Claude plan or API credits.** That is the
one paid part. VN itself is a free download with a free tier, and VN
Pro is optional for this setup. Before you post with it, check on your
own free VN install that the Auto Edit MCP toggle is available without
VN Pro — if it is gated on your version, the setup is not free on
your machine.

## The idea in one sentence

Most AI editors hand you a finished file you can't touch; VN's Auto
Edit MCP server lets Claude Code build the edit **on VN's timeline**,
so after the AI pass you can still trim a clip, fix a caption word, or
balance the audio by hand.

## What you need

- VN Video Editor on **macOS or Windows** (the Auto Edit flow is
  desktop; keep VN open while the agent is connected). The VN tutorial
  shows VN 1.7.0+ on Mac / 0.6.4+ on Windows — re-check the current
  version requirement in the app.
- Claude Code (paid Claude plan or API credits).
- Your own clips.

## The 4 steps

**Step 1 — Turn the switch on.** Download and open VN, go to
**Auto Edit**, and toggle on **MCP Server**. Keep VN open while your
agent is connected.

**Step 2 — Copy the setup prompt.** In the VN app (Auto Edit →
Config), copy the setup prompt/configuration for Claude Code.

**Step 3 — Connect.** Start a new Claude Code chat, paste the setup
prompt, and confirm VN is connected.

**Step 4 — Ask in plain words.** Type what you want, for example the
official example prompt: *"Turn today's clips into a 30-second travel
vlog."* Claude builds the edit on the timeline.

## After the AI pass — the part that matters

The timeline stays yours. Trim and rearrange clips, refine captions,
adjust audio, or ask the agent for another pass. It will not nail
every caption word — click the caption and fix the word yourself;
that hand fix is faster than explaining it.

## Troubleshooting

- **Agent cannot connect:** keep VN open with MCP Server enabled in
  Auto Edit → Config, copy the current configuration again, then
  restart the agent or start a new session.
- **It is not fully offline:** VN runs a local MCP server, but your
  connected agent may still need internet access.
- **No separate CLI install:** the Auto Edit flow connects through MCP
  directly; no separate CLI installation is needed for this flow.

## The honest limits

Claude builds the timeline; you keep the final fix. Captions can miss
words, and pacing choices are still yours to judge. Setup page:
https://vlognow.me/mcp

This guide is free. If you want the full editor system behind these
videos, the Complete Editor Pack ($39, one-time) is linked in my bio.
