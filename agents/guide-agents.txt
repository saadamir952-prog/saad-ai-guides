# Seventy-Two Agents. One Install.

**Free guide · Keyword: AGENTS · Saad AI**

## The cost — read this first

ECC itself is **free and open-source (MIT)** — the plugin, the 72
agents, the 328 skills, all of it. **Claude Code needs a paid Claude
plan** — that is the one paid part, and you already need it to run the
plugin.

**Do not confuse this with paid extras.** The ECC GitHub App offers
paid tiers for private repos (from $19/seat/month) — you do not need
it for the install in this guide. And never pay anyone for ECC itself:
if someone is selling you this plugin, it is not the official project.

## The idea in one sentence

One Claude does everything — plans, writes, reviews, fixes — and hopes
the output is decent. This setup splits the work: one agent per job,
all installed as one plugin.

## The proof

Everything Claude Code (ECC) is a free, open-source plugin for Claude
Code: 72 specialized agents, 328 skills, and 99 slash commands,
installed as one plugin. **We counted every number ourselves** in a
direct clone of the official repo on 24 Nov 2026 — 72 agent files, 328
skill folders, 99 command files. The repo passed 300,000 stars
(309,027 on 23 Nov 2026).

The setup in the video comes from @vektor.fm's reel (23 Nov 2026).
Every number in this guide was verified by us in the repo itself —
nothing here is copied on trust.

## The 2 install commands (copy-paste)

**Path A — inside Claude Code (no terminal needed).** Open Claude Code
and run these two commands, one after the other:

```
/plugin marketplace add https://github.com/affaan-m/ECC
/plugin install ecc@ecc
```

That installs the whole plugin: all 72 agents, 328 skills, and 99
commands. Verify it worked:

```
/plugin list
```

You should see `ecc@ecc` enabled.

**Path B — the guided setup (the README's recommended path).** If you
prefer a wizard that handles updates, scope, and hook settings, run
this in your terminal instead. Prerequisites: Node.js 18 or newer,
Git, and Claude Code 2.1 or newer.

```
npx ecc-universal@2.2.3 setup
```

For a typical personal setup, choose **Global user**, choose
**Standard** hooks, and confirm. Then start a new Claude Code session
and run `/plugin list` to verify `ecc@ecc` is enabled.

**Pick ONE path.** Both install the same `ecc@ecc` plugin. Do not stack
them — installing ECC twice into the same setup can duplicate skills,
commands, and hooks.

## Which agents to switch on first

The README's own advice: **start with the workflow you need, not the
full catalog.** Seventy-two agents is a team, not a to-do list. These
six cover the work most people do first:

1. **planner — plan the feature first.** `/ecc:plan "describe the
   feature"` — planner writes the implementation blueprint before any
   code exists. Always first.
2. **tdd-guide — write code tests-first.** The `tdd-workflow` skill —
   write the failing test, then the code that passes it. Same skill
   for fixing bugs: reproduce it with a failing test first.
3. **code-reviewer — review what you just wrote.** `/code-review` — a
   fresh-context review of new code, before it ships.
4. **build-error-resolver — fix the failing build.** `/build-fix` —
   one agent whose only job is build errors.
5. **security-reviewer — check for holes.** `/security-scan` — reads
   every line for vulnerabilities before production.
6. **e2e-runner — test the real user flow.** The `e2e-testing` skill —
   end-to-end tests on the critical path, not just unit tests.

Two more worth knowing on day one: **architect** (design the system
architecture, alongside `/ecc:plan`) and **go-reviewer**
(`/go-review`, if you write Go). The other 64 agents are specialists
by language and domain — call them when the work calls for them.

## It learns the way you code

One command reads your git history and writes the way you code into
skills the agents reuse:

```
/skill-create
```

Run it after the install, once you have some history in the repo. It
turns your own patterns — how you structure code, how you test, how
you name things — into skills ECC applies next time. That is the part
most people skip, and the part that makes the agents feel like yours
instead of generic.

## The official repo

Install only from the official project:

https://github.com/affaan-m/ECC

The official channels are the GitHub repo, the npm packages
`ecc-universal` and `ecc-agentshield`, the GitHub App, the plugin slug
`ecc@ecc`, and https://ecc.tools. The project's own warning, from its
README: *third-party re-uploads and unofficial mirrors are not
maintained or reviewed by the project and may contain malware.* If the
install source is not one of the official channels above, do not run
it.

## The catch

Seventy-two agents is a lot — and that is the trap. If you try to use
all of them on day one, you will spend the day configuring instead of
building. Start with the six above, one workflow at a time. The agents
are only as good as the plan: skip the planner and the rest of the
team builds the wrong thing faster. And remember the install rule: one
path, once — never stack two installs into the same setup.

## What it costs, in full

- ECC plugin — 72 agents, 328 skills, 99 commands (MIT, open-source): $0
- Guided setup (`npx ecc-universal`): $0
- Claude Code: needs a paid Claude plan (the one paid part)
- ECC GitHub App, paid tiers for private repos (from $19/seat/month): optional — NOT needed for this install
- Anyone selling you ECC itself: not the official project — do not pay

---

**Next step:** this guide is the free version — the install commands
and the first agents to switch on. Turning Claude into a finished,
watchable edit every time — cutting, captioning, sound design, and
rendering, all inside Claude — is a separate skill.

That is what the **Complete Editor Pack** teaches: "How to Turn Your
Claude Into a Professional Editor" — the full skill, a setup guide, a
walkthrough video, 15 sound effects, 3 ready workflows, and free
updates. $39, one-time payment, on Gumroad:
https://saadai.gumroad.com/l/complete-editor-pack

Just want the skill on its own? The starter version is $20, one-time:
https://saadai.gumroad.com/l/claude-video-editor

If this guide showed you how to turn one Claude into a team of
specialists, the pack is the next step: it shows you how to finish the
whole edit.
