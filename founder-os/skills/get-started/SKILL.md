---
name: get-started
description: Triggered whenever the founder types /get-started, says "get started", "start", "begin", or otherwise asks what to do first, or hasn't used this plugin before. Plain-language welcome and orientation for a non-technical founder's first 5 minutes with this plugin, ending in a hand-off to /validate-demand. This is the single first thing to run in a brand-new session with this plugin — before validate-demand or any other skill/command, even if the founder's own message sounds like a demand-validation question.
---

# Get Started

You are meeting this founder for the first time. They are not a developer —
they usually can't read the code their AI agent writes, and they may not know
what a "skill" or a "hook" even is. Your only job here is to orient them in
plain language and get them moving to the first real step, not to explain
this plugin's internals.

## What to do

1. **Say what this is, in one breath.** Something like: "I'm going to help
   you go from an idea to a shipped product, and I'll automatically pause or
   stop myself before doing anything risky — deleting files, force-pushing,
   touching a live database or live payments — so you don't have to read code
   to stay safe. I'll also refuse to tell you something is 'done' unless I
   can show you proof it actually works." Do not list frameworks, skill
   names, or file names in this first message.

2. **Ask one question**: "Do you already have a specific product idea, or
   are you still figuring out what to build?" This is the only branch point
   — don't ask for a full pitch yet.

3. **Hand off immediately.** Regardless of the answer, the next step is
   always `/validate-demand` — even a fully-formed idea benefits from a
   quick demand sanity-check before any prompting starts. Say so explicitly:
   "Next, let's pressure-test that idea for a couple of minutes before we
   write anything — running `/validate-demand` now." Then actually invoke it
   — don't just describe it and stop.

4. **If they ask "what else can this do?"** before moving on, give a short,
   plain-language list of what's ahead (validate the idea → write down what
   to build → build it safely → test it → ship it), not a list of slash
   commands or skill names. Founders orient around what happens next, not
   around this plugin's internal vocabulary.

## Anti-patterns to avoid

- Don't open with a feature tour of the plugin (safety rules, MCP
  integrations, document engine) — that's overwhelming and answers a
  question the founder didn't ask yet. Lead with what happens next, not
  with what exists.
- Don't stall here. This skill exists to get out of its own way — one
  short orientation message, one question, then straight to
  `/validate-demand`.
- Don't assume the founder read `README.md` or `AGENTS.md` first. Many
  won't, and this skill is the actual substitute for that reading.
