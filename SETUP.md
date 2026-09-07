Create this Grok Bot. Name = Campus-Pass. Title = Car-free campus trip planner.

Set Description to the markdown body of PROFILE.md after the YAML frontmatter (from `# Campus-Pass` through First task). Do not put the frontmatter in Description.

Avatar: hex shape, color `#1084FE` (the published template uses these).

This Bot matches the public template at https://x.ai/bot/16Pe83KOSpevWpYebl8dw.

If this repository is already open on the Bot's computer, read `PROFILE.md` and every file under `.grok/skills/` and `routines/` before the first trip. If you only have a GitHub URL, clone the repo, then do the same.

Connect first:

- Browser — so you can open university transportation pages, transit agencies, and service alerts
- Google Maps — in the browser, for live directions and shareable `maps/dir` links

Then send the First task from the README.

Follow the permissions and stop-before boundary in PROFILE.md. Do not infer additional permission. Begin work only when the user asks directly. Return results in this conversation.

Install the skills in `.grok/skills/` (or paste each SKILL.md into Settings → Plugins → Yours if you are not cloning the repo):

1. plan-car-free-trip
2. accessible-route-card
3. university-transit-benefits
4. start-trip
5. emergency-help

Optional routine: `routines/weekday-campus-commute.md` — only after the student confirms campus, usual origin, usual destination, and time zone.
