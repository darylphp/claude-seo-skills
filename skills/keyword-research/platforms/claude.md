# Claude

Documentation checked 13 November 2026. Installation has not been tested for v0.1.0.

## Claude app

1. Stage the runtime files in a folder named `keyword-research/`, containing `SKILL.md` and `references/`. The folder name must match the `name` field in `SKILL.md`.
2. ZIP the folder itself so every entry starts with `keyword-research/`. From the parent folder, run `zip -r keyword-research.zip keyword-research/`, then `unzip -l keyword-research.zip` to confirm the layout.
3. Turn on code execution and file creation. On individual plans this is in **Settings**, then **Capabilities**. On Team and Enterprise plans an owner enables it, with skills, in organisation settings.
4. Open **Customize**, then **Skills**. Select **+**, then **Create skill**, then **Upload a skill**, and choose the ZIP.

Availability depends on your plan and organisation settings. The description is under 200 characters, which fits the stricter of the two limits Anthropic currently publishes: 200 characters in the Help Center article and 1,024 in the Claude documentation.

Code execution also lets Claude count and deduplicate larger exports with a script rather than estimating. Check the reported coverage either way.

[Anthropic Help Center: Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude) · [How to create custom skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) · [Claude docs: Create custom skills](https://claude.com/docs/skills/how-to)

## Claude Code

Copy the runtime folder to `.claude/skills/keyword-research/` for a project or `~/.claude/skills/keyword-research/` for your user account. Keep `SKILL.md` and `references/` together. Type `/keyword-research` with the scope and data files, or ask for keyword research and let Claude load the skill from its description.

[Claude Code documentation: Extend Claude with skills](https://code.claude.com/docs/en/skills)
