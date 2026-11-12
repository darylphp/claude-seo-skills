# Local SEO Audit Skill

Audit one business location's local search presence from the evidence you supply: its Google Business Profile, the website page the profile links to, the reviews process and local measurement. The skill returns a 10-section report with evidence-labelled findings, a priority for each, the smallest justified action and a check that shows whether the action worked.

## Start here

1. Supply one location's business record (approved facts, business model, objective, access and permissions) and the evidence you have. See [input requirements](references/input-requirements.md) and the [synthetic input](examples/ready-input.md).
2. Ask the skill to audit that location. Example request: "Use the Local SEO Audit Skill to audit the attached location. Label the evidence and keep approval separate."
3. Review the findings. An authorised person approves specific actions before anyone edits the profile, the website or the review process.

The status line tells you what happened. Ready means the findings are ready for review. Escalate means a suspension, duplicate, ownership dispute or similar incident comes first. Blocked names the missing business fact or evidence.

## What it does not do

- Sign in to, change or create Google Business Profiles, websites or other accounts.
- Contact customers, or request or reply to reviews.
- Promise rankings, map positions, call volumes or timelines.
- Write publishable page copy, a finished profile description, review replies or final structured data code.
- Research keywords or decide whether new pages should exist. It hands those to the right workflow.

## Package layout

- [SKILL.md](SKILL.md) and `references/` are the shared runtime files.
- `examples/` contains a synthetic ready case and blocked and incident outputs.
- [Acceptance tests](tests/acceptance-tests.md) define behaviour and package checks.
- [Claude setup](platforms/claude.md) covers installation.
- [Changelog](CHANGELOG.md) tracks revisions.

Keep the runtime folder named `local-seo-audit` when staging it for installation. Copy `SKILL.md` and `references/` together, preserving relative paths. The package uses Markdown only and has no scripts or service dependencies.

## Workflow provenance

The method follows the Local SEO and GBP Operating Playbook v1.2, sections 1 to 13 and 15. Measurement definitions align with the SEO Measurement, Reporting and Refresh Playbook v1.1, and structured data work is handed to the Schema Markup Implementation and Validation Playbook v1.3. The runtime carries the applicable rules in its own references. Google guidance is paraphrased with source IDs and check dates in the [source register](references/source-register.md).
