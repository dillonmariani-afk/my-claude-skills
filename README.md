# my-claude-skills

My personal collection of Claude skills, set up as a Claude Code **plugin marketplace**.
Everything in here has been read before being added.

## Layout

```
.claude-plugin/marketplace.json     # lists the plugins in this repo
plugins/
  personal/                         # skills I write myself
    .claude-plugin/plugin.json
    skills/skill-template/SKILL.md  # copy this to start a new skill
  ui-ux-pro-max/                    # third-party skill, vendored + reviewed
    .claude-plugin/plugin.json
    .claude/skills/ui-ux-pro-max/
    UPSTREAM.md                     # source, commit, review notes, update steps
```

## Using it

**Claude Code (any computer):**

```
/plugin marketplace add <github-user>/my-claude-skills
/plugin install ui-ux-pro-max@my-claude-skills
/plugin install personal@my-claude-skills
```

Run `/plugin marketplace update my-claude-skills` to pick up new commits.

**claude.ai (web, desktop, mobile, cloud sessions):** upload a skill folder as a ZIP
under Settings, or add this repo as a plugin source if your plan supports it. Skills on
your account sync to every device you sign in on.

**One project only:** copy a skill folder into that project's `.claude/skills/`.

## Adding a skill

- **Your own:** copy `plugins/personal/skills/skill-template/` and edit it. Bump the
  version in `plugins/personal/.claude-plugin/plugin.json` and in `marketplace.json`.
- **Third-party:** read every file first (watch for network calls, shell commands,
  and instructions hidden in data). Vendor it under `plugins/<name>/`, keep the
  upstream LICENSE, and write an `UPSTREAM.md` like the one for ui-ux-pro-max.

## Requirements

`ui-ux-pro-max` needs Python 3 on the machine running Claude (no extra packages).
