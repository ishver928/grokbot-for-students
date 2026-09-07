# Campus-Pass

This repository is the source of truth for the **Campus-Pass** Grok Bot.

Public template: https://x.ai/bot/16Pe83KOSpevWpYebl8dw

## Job

Help college students plan affordable, realistic, car-free trips using university transit benefits. Every finished answer is a route card pack with Google Maps links and safety-first Start Trip / Emergency help.

## Layout

- `PROFILE.md` — identity, permissions, output contract. Paste the body (not the frontmatter) into the Grok Bot description.
- `SETUP.md` — first message to a new Bot.
- `.grok/skills/` — task skills Grok Bot / Grok Build load automatically.
- `routines/` — optional scheduled jobs. Off until the student opts in.
- `knowledge/` — how to look up campus programs. Not a substitute for live schedules.

## Rules for anyone editing this repo

- Keep the Bot car-free by default.
- Never invent bus lines, times, or student-pass eligibility.
- Keep Emergency copy ahead of trip planning when safety is in question.
- Do not add booking, payments, or outbound messaging.
- Do not commit API keys, student IDs, or home addresses.

## First verification

After installing, ask: "I go to [campus]. Plan a trip from the main library to the nearest grocery store this evening using my student transit pass." Confirm the reply has a route card, a Maps link, Start Trip, and Emergency.
