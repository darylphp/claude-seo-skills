# Site Architecture Skill

Decide which URL should serve each customer task on one site or section, before any brief is written. The skill returns a 10-section plan: the status and decision summary, the scope and sources, the URL inventory, a task-to-URL map, the gates for each new page, page-set reviews, overlap and consolidation records, internal links and navigation, the build order with approvals and handoffs, and open items with measurement.

Each task gets one decision: Keep, Improve, Differentiate, Consolidate, Create, Research first, Defer or Reject.

## Start here

1. Describe the case: the site and the section to plan, the offers, the market, the customer action that matters, and who owns, implements and approves changes. See [scope and modes](references/scope-and-modes.md) and the [synthetic input](examples/ready-input.md).
2. Supply what you have: keyword research or a list of customer tasks, a crawl or CMS export of the section, a Search Console page and query export, an enquiry log, and any proposals you want checked.
3. Ask for a plan. Example request: "Use the Site Architecture Skill on the attached research and crawl. Tell us which pages we should have, which to merge and which links to add. Keep approval separate."
4. Review the decisions, the gates and the open items before approving any page, redirect or menu change.

The status line says what happens next. **Ready for review: Architecture plan** means the decisions are ready for a person to review. **Research first: Task unclear** names the research question to answer first. **Blocked: Define the scope** and **Blocked: Supply the inventory** name what is missing.

## What it does not do

- Create, move, redirect, noindex or delete pages, or change menus.
- Plan a URL for every keyword, synonym, suburb or AI fan-out question.
- Treat shared queries or a "cannibalisation" warning as proof that pages should merge.
- Use a canonical tag to combine different topics, or noindex to choose between pages.
- Change stable URLs or build folder "silos" to make a structure look tidy.
- Write page copy, briefs, redirect rules or schema. It hands these on with what they need.
- Promise rankings, traffic, indexing or timing.

## Package layout

- [SKILL.md](SKILL.md) and `references/` are the runtime files, intended for both Claude and ChatGPT. Compatibility is not verified until platform tests are recorded.
- `examples/` contains a synthetic ready case with its output, a blocked case and a single-page research-first case.
- [Acceptance tests](tests/acceptance-tests.md) define behaviour and package checks.
- [Claude setup](platforms/claude.md) and [ChatGPT setup](platforms/chatgpt.md) cover installation.
- [Changelog](CHANGELOG.md) tracks revisions.

## Status

Unreleased draft. Package checks have passed. No behaviour case has been run, and the skill has not been installed or invoked on any platform. The [acceptance tests](tests/acceptance-tests.md) record each state separately.

## Installation

Keep the runtime folder named `site-architecture` when staging it for installation. Copy `SKILL.md` and `references/` together, preserving relative paths. The package uses Markdown only and has no scripts or service dependencies.

## Where it fits

The skill works on its own. It takes the planning handoff from the Keyword Research Skill (`skills/keyword-research/`) and a strategy pack from the SEO Strategy Skill (`skills/seo-strategy/`), and its page records give the SEO Content Brief Skill (`skills/seo-content-brief/`) the URL, page role and page decision it asks for. Redirects and crawl controls go to the Technical SEO Audit Skill (`skills/technical-seo-audit/`) or the developer, and service-area questions to the Local SEO Audit Skill (`skills/local-seo-audit/`). Each of those is under review in its own pull request. Equivalent records from your own process work in their place.

## Workflow provenance

The method follows the Patent-Informed Cluster Build Framework v3.2 (File 02), sections 2 to 8: page gates, the set gate, query-to-URL mapping, overlap and consolidation, architecture and internal links, prioritisation, and publication and learning. It covers the playbook stages "A4 Query-to-URL, Cluster and Roadmap Planning" (site or section mode) and "B1 Page Opportunity and Intent Validator" (single-page mode). The framework's patent research is not used. Google guidance is paraphrased with source IDs and check dates in the [source register](references/source-register.md), which keeps File 02's IDs and records the differences from it.
