# Claude

Documentation checked 13 November 2026. Installation has not been tested for v0.1.0.

## Claude app

1. Stage the runtime files in a folder named `local-seo-audit/`, containing `SKILL.md` and `references/`. The folder name must match the `name` field in `SKILL.md`.
2. ZIP the folder itself so every entry starts with `local-seo-audit/`. From the parent folder, run `zip -r local-seo-audit.zip local-seo-audit/`, then `unzip -l local-seo-audit.zip` to confirm the layout.
3. Turn on code execution and file creation. On individual plans this is in **Settings**, then **Capabilities**. On Team and Enterprise plans an owner enables it, with skills, in organisation settings.
4. Open **Customize**, then **Skills**. Select **+**, then **Create skill**, then **Upload a skill**, and choose the ZIP.

Availability depends on your plan and organisation settings. The description is under 200 characters, which fits the stricter of the two limits Anthropic currently publishes: 200 characters in the Help Center article and 1,024 in the Claude documentation.

[Anthropic Help Center: Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude) · [How to create custom skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) · [Claude docs: Create custom skills](https://claude.com/docs/skills/how-to)

## Claude Code

Copy the runtime folder to `.claude/skills/local-seo-audit/` for a project or `~/.claude/skills/local-seo-audit/` for your user account. Keep `SKILL.md` and `references/` together. Type `/local-seo-audit` with the evidence pack attached or described, or ask for a local SEO audit and let Claude load the skill from its description.

[Claude Code documentation: Extend Claude with skills](https://code.claude.com/docs/en/skills)
