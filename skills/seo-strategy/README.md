# SEO Strategy Skill

Set SEO priorities for one business from its real offers, market, dated baseline and constraints. The skill returns a 10-section strategy pack: the strategic choice and status, a business-fact register, evidence coverage, a dated baseline, competitor context, a ranked opportunity register, priorities and trade-offs, a staged plan, handoffs, and the open items that would change the plan.

## Start here

1. Supply the business record (identity, real offers and exclusions, capacity, audience, market and language, the outcome that matters, delivery constraints and the evidence the business holds) and whatever data you have: Search Console and Analytics exports, an enquiry or sales log, saved pages, customer questions and any dated result observations. See [scope and intake](references/scope-and-intake.md) and the [synthetic input](examples/ready-input.md).
2. Ask the skill for a strategy. Example request: "Use the SEO Strategy Skill on the attached business record and exports. Label every source and keep implementation approval separate."
3. Review the strategic choice, the opportunity register and the open items before approving any task.

The status line tells you what can happen next, judged on the leading non-urgent opportunity. **Ready for scoped research** means its customer task, suitable asset or proposed action is still materially uncertain, so a bounded research question is handed on. **Ready for implementation planning** means the evidence already settles the task, asset and action, and the scope, owner, authority, dependencies and acceptance check are established. An existing page alone doesn't settle the question either way. **Diagnose before prioritising** routes an unexplained decline or suspected defect to diagnosis first. **Return for business facts** names what is missing. An urgent repair is recommended either way.

## What it does not do

- Invent margins, capacity, credentials, locations, traffic, leads or revenue, or give a projection without sourced inputs, ranges and stated uncertainty.
- Treat tool estimates, Search Console data, Analytics events and business records as the same kind of evidence.
- Name a Google update, or a plugin update, as the cause of a problem from timing alone.
- Conclude what an Analytics event records, or change tracking, before the setup has been inspected.
- Plan location or variation pages for places the business does not serve or without a real customer task and page-specific content, or commit to a fixed publishing cadence.
- Report a handoff, repair or approval as done without evidence.
- Choose URLs, write briefs or copy, buy links, contact anyone or approve and carry out changes.
- Promise rankings, traffic or conversions.

## Package layout

- [SKILL.md](SKILL.md) and `references/` are the runtime files, intended for both Claude and ChatGPT. Compatibility is not verified until platform tests are recorded.
- `examples/` contains a synthetic ready case, a blocked-scope case and a decline that routes to diagnosis.
- [Acceptance tests](tests/acceptance-tests.md) define behaviour and package checks.
- [Claude setup](platforms/claude.md) and [ChatGPT setup](platforms/chatgpt.md) cover installation.
- [Changelog](CHANGELOG.md) tracks revisions.

## Status

Unreleased draft. The [acceptance tests](tests/acceptance-tests.md) record each state separately: documentation checked, package checks passed, installation tested, activation or invocation confirmed, behaviour tests passed, and released. A run on one platform is not a test of the other.

## Installation

Keep the runtime folder named `seo-strategy` when staging it for installation. Copy `SKILL.md` and `references/` together, preserving relative paths. The package uses Markdown only and has no scripts or service dependencies.

## Where it fits

The skill works on its own. Its handoffs suit the Keyword Research Skill (`skills/keyword-research/`) for bounded research questions, the SEO Content Brief Skill (`skills/seo-content-brief/`) once a page decision and evidence are approved, and the Local SEO Audit Skill (`skills/local-seo-audit/`) for one location's Business Profile. Each of those is under review in its own pull request. Any equivalent research, brief or audit record works in their place.

## Workflow provenance

The method follows the SEO Strategy, Business Baseline and Opportunity Playbook v1.1, sections 1 to 12, covering business intake and the strategy baseline. The runtime carries the applicable rules in its own references. Google guidance is paraphrased with source IDs and check dates in the [source register](references/source-register.md), which keeps the playbook's IDs and records two wording differences from it.
