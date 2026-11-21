# Claude

Documentation checked 20 November 2026. For v0.1.0, installation has not been tested and invocation has not been confirmed in the Claude app or Claude Code. Behaviour runs recorded in the acceptance tests supplied the files to Claude directly; they are not installation or invocation tests.

## Claude app

1. Stage the runtime files in a folder named `seo-strategy/`, containing `SKILL.md` and `references/`. The folder name must match the `name` field in `SKILL.md`.
2. ZIP the folder itself so every entry starts with `seo-strategy/`. From the parent folder, run `zip -r seo-strategy.zip seo-strategy/`, then `unzip -l seo-strategy.zip` to confirm the layout.
3. Turn on code execution. Anthropic's help page lists custom skills for Free, Pro, Max, Ultra, Team and Enterprise plans, with code execution enabled. On Team and Enterprise plans an owner may need to enable skills in organisation settings.
4. Open **Customize**, then **Skills**, and upload the ZIP.

The description is 195 characters, inside the 200-character limit on Anthropic's help page. The `name` is within its 64-character limit.

Code execution also lets Claude total and compare larger exports with a script rather than estimating. Check the coverage the pack reports either way.

[Anthropic Help Center: How to create custom skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) · [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude)

## Claude Code

Copy the runtime folder to `.claude/skills/seo-strategy/` for a project or `~/.claude/skills/seo-strategy/` for your user account. Keep `SKILL.md` and `references/` together. Type `/seo-strategy` with the business details and data files, or ask for an SEO strategy and let Claude load the skill from its description. The Claude Code documentation was last checked on 13 November 2026 for the Keyword Research Skill and was not reopened here.

[Claude Code documentation: Extend Claude with skills](https://code.claude.com/docs/en/skills)
