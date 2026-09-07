# Campus-Pass

Grok Bot source for **Campus-Pass** — a car-free trip planner for college students.

This repo is built to match the published bot template:

**https://x.ai/bot/16Pe83KOSpevWpYebl8dw**

Name, job, and accent (`#1084FE`, hex) come from that template. Skills, route-card format, and safety rules live here so you can version them on GitHub, clone them onto the Bot's computer, and keep the Bot consistent after you reinstall it.

## What the Bot does

Helps college students plan affordable, realistic car-free trips using university transit benefits, with accessible route cards, Google Maps navigation links, and safety-first Start Trip / Emergency help.

It will:

- Look up campus shuttles and student U-Pass-style benefits
- Build one cheap-on-time option and one faster backup
- Return phone-readable route cards with Maps links
- Recheck live directions when you say **Start Trip**
- Lead with **911 / campus police / safe-ride** when you say **Emergency** or you are not safe

It will not book tickets, pay fares, or message people for you.

## Install in Grok Bot

1. Create a GitHub repository from this project (or push this tree to GitHub).
2. Download [Grok Bot](https://x.ai/grok-bot) if you do not have it.
3. **New chat → Create new agent.**
4. Name it `Campus-Pass`. Title: `Car-free campus trip planner`.
5. Paste `SETUP.md` as the first message, or tell the Bot to clone this GitHub repo and follow `SETUP.md`.
6. Connect **Browser** (and use Google Maps in that browser).
7. Enable the five skills under `.grok/skills/`.
8. Send the first task: campus, origin, destination.

You can also add the existing public copy with **Add to Grok Bot** on the [template page](https://x.ai/bot/16Pe83KOSpevWpYebl8dw), then point that Bot at this repo so it picks up the skills.

### Fast path: paste SETUP

Copy the contents of [`SETUP.md`](SETUP.md) into a new Bot. It will read [`PROFILE.md`](PROFILE.md) and load the skills.

## Skills

| Skill | When it runs |
| --- | --- |
| [plan-car-free-trip](.grok/skills/plan-car-free-trip/SKILL.md) | Any "how do I get there without a car" request |
| [university-transit-benefits](.grok/skills/university-transit-benefits/SKILL.md) | Before quoting a fare |
| [accessible-route-card](.grok/skills/accessible-route-card/SKILL.md) | Formatting the answer |
| [start-trip](.grok/skills/start-trip/SKILL.md) | "I'm leaving now" |
| [emergency-help](.grok/skills/emergency-help/SKILL.md) | Danger, night, missed last bus, 911 |

Optional weekday commute: [`routines/weekday-campus-commute.md`](routines/weekday-campus-commute.md).

## Grok Build / local clone

```bash
git clone <this-repo-url>
cd campus-pass
```

Grok loads `AGENTS.md` and `.grok/skills/` from the repo root. The plugin package is `.grok-plugin/`.

## First task

Ask: you attend [campus]. Plan a trip from [origin] to [destination] at [time] using your student transit pass.

You should get a route card, a Maps link, Start Trip, and Emergency. Times and eligibility must come from live official pages, not from the example file.

## License

MIT. Campus-Pass is a third-party Grok Bot configuration, not a product of SpaceXAI.
