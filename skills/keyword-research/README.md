# Keyword Research Skill

Turn the keyword, Search Console and customer data you supply into task-based query families for one business, market and research question. The skill returns a 9-section research pack: scope and sources, coverage, a family map with intent, result evidence, decision criteria, candidates worth checking, exclusions and a handoff for page planning.

## Start here

1. Supply the business scope (real offers, audience, market, language, goal, inclusions and exclusions) and the data you have: Search Console exports, keyword tool exports, customer questions and any dated result observations. See [scope and modes](references/scope-and-modes.md) and the [synthetic input](examples/ready-input.md).
2. Ask the skill to research that question. Example request: "Use the Keyword Research Skill on the attached data. Label every source and keep URL decisions for planning."
3. Review the families, the evidence behind each and the open checks before planning any pages.

The status line tells you how far the research can go. Ready and provisionally ready families can move to planning, with any restrictions stated. Return statuses name the missing scope or evidence.

## What it does not do

- Invent search volumes, difficulty, CPC, trends, traffic or result observations.
- Treat tool estimates, Search Console rows, customer language and model suggestions as the same kind of evidence.
- Choose URLs, slugs, page builds, consolidations or build order.
- Write briefs, copy, density targets or keyword lists for insertion.
- Promise rankings, traffic or conversions.

## Package layout

- [SKILL.md](SKILL.md) and `references/` are the shared runtime files.
- `examples/` contains a synthetic ready case and a scope-return example.
- [Acceptance tests](tests/acceptance-tests.md) define behaviour and package checks.
- [Claude setup](platforms/claude.md) covers installation.
- [Changelog](CHANGELOG.md) tracks revisions.

Keep the runtime folder named `keyword-research` when staging it for installation. Copy `SKILL.md` and `references/` together, preserving relative paths. The package uses Markdown only and has no scripts or service dependencies.

## Workflow provenance

The method follows the Keyword, Query Family and Intent Research Playbook v1.1, sections 1 to 12, and stops at the handoff to query-to-URL planning. The runtime carries the applicable rules in its own references. Google guidance is paraphrased with source IDs and check dates in the [source register](references/source-register.md), including two Search Console features added after the playbook's last review.
