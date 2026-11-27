# Claude

Documentation checked 27 November 2026. For v0.1.0, installation has not been tested and invocation has not been confirmed in the Claude app or Claude Code. No behaviour case has been run.

## Claude app

1. Stage the runtime files in a folder named `site-architecture/`, containing `SKILL.md` and `references/`. The folder name must match the `name` field in `SKILL.md`.
2. ZIP the folder itself so every entry starts with `site-architecture/`. From the parent folder, run `zip -r site-architecture.zip site-architecture/`, then `unzip -l site-architecture.zip` to confirm the layout.
3. Turn on code execution. Anthropic's help page lists skills on Free, Pro, Max, Ultra, Team and Enterprise plans, with code execution enabled. On Team and Enterprise plans an owner may need to enable skills in organisation settings.
4. Upload the ZIP and turn the skill on under **Customize**, then **Skills**.

The description is within the 200-character limit on Anthropic's help page, and the `name` is within its 64-character limit.

Code execution also lets Claude group and count larger crawl or Search Console exports with a script rather than estimating. Check the coverage the plan states either way.

[Anthropic Help Center: How to create custom skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) · [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude)

## Claude Code

Copy the runtime folder to `.claude/skills/site-architecture/` for a project or `~/.claude/skills/site-architecture/` for your user account. Keep `SKILL.md` and `references/` together. Type `/site-architecture` with the case details and evidence files, or ask which pages a site needs and let Claude load the skill from its description. The Claude Code documentation was last checked on 13 November 2026 for the Keyword Research Skill and was not reopened here.

[Claude Code documentation: Extend Claude with skills](https://code.claude.com/docs/en/skills)
