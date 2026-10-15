---
name: skill-template
description: Template to copy when writing a new skill. Replace this description with what the skill does AND when Claude should use it (the trigger), e.g. "Formats weekly status reports in our team style. Use when the user asks for a status update, weekly report, or standup summary."
---

# Skill Template

Copy this folder to `plugins/personal/skills/<your-skill-name>/`, rename `name` above to
match the folder, and rewrite the description. The description is what Claude reads to
decide whether to load the skill, so make the trigger specific.

## Instructions

Write the steps Claude should follow, in plain language:

1. What to gather or check first.
2. How to do the work (conventions, format, tone).
3. What a finished result looks like.

## Optional extras

- `references/*.md`: longer material Claude reads only when needed. Link to it from here.
- `scripts/`: helper scripts. Reference them as
  `${CLAUDE_PLUGIN_ROOT}/skills/<your-skill-name>/scripts/<file>`.
