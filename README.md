# CK Skills Pack

Agent skills for Comfort Keepers social content. Install with the open [skills](https://skills.sh) CLI (`npx skills add`) and use them in Claude Code, Cursor, Codex, and other compatible agents.

This pack currently ships one skill:

- **ck-social-content-calendar** — a monthly Facebook and Instagram content calendar for one Comfort Keepers office, with weekly themes, captions, CTAs, and static / carousel / reel copy in plain language for readers aged 60 to 80.

## Install

After this repo is on GitHub:

```bash
npx skills add cecvic-wigoh/ck-skills-pack
```

Install only this skill:

```bash
npx skills add cecvic-wigoh/ck-skills-pack --skill ck-social-content-calendar
```

List what's in the pack without installing:

```bash
npx skills add cecvic-wigoh/ck-skills-pack --list
```

From a local clone:

```bash
npx skills add ./ck-skills-pack --skill ck-social-content-calendar
```

Add `-g` to install globally, or `-a claude-code` (or `cursor`, `codex`, and so on) to target a specific agent. Use `-y` to skip prompts.


## What it does

For one office and one month, the skill:

1. Confirms the office from the public Comfort Keepers locator (address, phone, services).
2. Plans weekly themes around real moments in that month.
3. Assigns a format to each post (static, carousel or reel).
4. Writes on-creative copy, a caption, and one CTA with the office phone number written out.
5. Makes a few sample creatives, labeled as AI stand-ins until real, consented photos are used.
6. Lists anything that still needs to be confirmed with the office.

It drafts only. It never posts, schedules or spends.

## How to use it

Once installed, ask your agent something like:

- `Build a December content calendar for CK Lexington, KY`
- `/ck-social-content-calendar CK Greensboro, January`
- `Write January Facebook and Instagram posts for Comfort Keepers of Lexington`

Tell it the office (city and state) and the month. Optionally say who the reader is (the senior, default, or the adult child) and how many posts per week (default is three: Tuesday, Thursday, Saturday).

Deliverables are saved under `./<office-slug>/` in the current project:

- `<month-year>-content-calendar.md` — the full calendar
- `<month-year>-content-calendar.html` — optional HTML page
- `posts.json` — structured post data
- `creative/` — sample visuals
- `brand/` — reused or newly built brand notes

The agent will also read the bundled copy guide and format rules before writing:

- `skills/ck-social-content-calendar/references/ck-copy-guide.md`
- `skills/ck-social-content-calendar/references/formats-and-creative.md`

## Repository layout

```text
ck-skills-pack/
├── LICENSE
├── README.md
└── skills/
    └── ck-social-content-calendar/
        ├── SKILL.md
        └── references/
            ├── ck-copy-guide.md
            └── formats-and-creative.md
```

This follows the [skills.sh](https://skills.sh) / [Agent Skills](https://agentskills.io/specification) discovery path: `skills/<name>/SKILL.md`, with `name` in kebab-case matching the folder.

## License

MIT © AiMT / Wigoh
