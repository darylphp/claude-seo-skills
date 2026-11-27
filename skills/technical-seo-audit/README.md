# Technical SEO Audit Skill

Find what blocks crawling, indexing, rendering or the customer path on one site, and weigh the competing explanations for a drop. The skill returns a 10-section report: the status and conclusion, the case record, the evidence and access, a measurement check, urgent defects, findings with their producers, explanations for the symptom, prioritised actions with production acceptance checks, developer handoffs, and open items.

## Start here

1. Describe the case: the site, the pages or templates that matter, the symptom and when it started, the intended state of the affected pages, recent changes, and who owns, implements and approves. See [scope and intake](references/scope-and-intake.md) and the [synthetic input](examples/ready-input.md).
2. Supply what you have: a Search Console Performance export for two comparable periods, URL Inspection or Page indexing screenshots, a crawl export with its settings, page source and response headers, release notes, robots.txt and sitemap URLs, and any analytics or enquiry records.
3. Ask for an audit. Example request: "Use the Technical SEO Audit Skill on the attached exports. Our service pages dropped after the 28 October release. Label every source and keep implementation approval separate."
4. Review the conclusion, the findings and the open items before approving any change.

The status line says what happens next. **Escalate first: Urgent defect** means the site or its main customer path is unavailable or unsafe, and the report leads with the owner and containment. **Ready for review: Technical audit** means the findings are ready for a person to review. **Blocked: Define the case** and **Blocked: Supply audit evidence** name what is missing.

## What it does not do

- Change sites, settings, redirects or Search Console, request indexing, or contact anyone.
- Name a Google update, a plugin or theme update or a release as the cause of a drop from timing alone.
- Treat a crawler warning, a vendor score or a third-party email as a defect before it is verified.
- Recommend noindex to choose a canonical, redirects of every missing URL to the home page, disavow from a "toxic" score, instant indexing plugins, or crawler-only content.
- Describe a fix as live, verified or recognised by Google without evidence.
- Write a migration plan or URL mapping. It can check a release against an approved plan.
- Promise rankings, traffic, indexing or timing.

## Package layout

- [SKILL.md](SKILL.md) and `references/` are the runtime files, intended for both Claude and ChatGPT. Compatibility is not verified until platform tests are recorded.
- `examples/` contains a synthetic ready case with its output, a blocked case and an urgent case.
- [Acceptance tests](tests/acceptance-tests.md) define behaviour and package checks.
- [Claude setup](platforms/claude.md) and [ChatGPT setup](platforms/chatgpt.md) cover installation.
- [Changelog](CHANGELOG.md) tracks revisions.

## Status

Unreleased draft. Package checks have passed. No behaviour case has been run, and the skill has not been installed or invoked on any platform. The [acceptance tests](tests/acceptance-tests.md) record each state separately.

## Installation

Keep the runtime folder named `technical-seo-audit` when staging it for installation. Copy `SKILL.md` and `references/` together, preserving relative paths. The package uses Markdown only and has no scripts or service dependencies.

## Where it fits

The skill works on its own. It suits a "diagnose before prioritising" handoff from the SEO Strategy Skill (`skills/seo-strategy/`), and it hands Business Profile issues to the Local SEO Audit Skill (`skills/local-seo-audit/`). Each of those is under review in its own pull request. Equivalent records from your own process work in their place.

## Workflow provenance

The method follows the SEO Diagnosis and Technical Decision Playbook v1.2, sections 1 to 9, 11 and 12. Section 10, the launch and migration runbook, is used only for release checks against an approved plan. Google guidance is paraphrased with source IDs and check dates in the [source register](references/source-register.md), which keeps the playbook's IDs and records the differences from it.
