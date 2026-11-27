# Scope and Intake

## 1. Pick the route

Start from the symptom, not from a full checklist. A routine question does not need a complete site audit.

| Symptom or request | First checks | What the route produces |
| --- | --- | --- |
| Site down, hacked, redirecting unexpectedly, or main content missing | Availability, security evidence, recent deployments | The urgent route with an owner |
| Drop after a release, redesign, plugin or theme update, or URL change | What changed in templates, URLs, directives and tracking; the affected scope; measurement | A reproducible regression, or competing explanations with the next check |
| An important URL is missing from Search | Intended state, inspection evidence, access, canonical, content | Fix, investigate, improve, defer or confirm an intended exclusion |
| Clicks, impressions or positions declining | Comparable reporting, page and query groups, demand, technical changes | Explanations ranked by evidence, and the next check |
| Search traffic steady but enquiries or sales falling | Tracking and the real enquiry or purchase path | A measurement or path finding, or a handoff for commercial causes |
| An audit tool reports many issues | A verified sample, intended behaviour, business impact | Defects, supported improvements and no-action items |
| A release check before or after launch | The approved release record and the production output | Acceptance results and exceptions |

## 2. Outside this skill

Hand these on and say what the handoff needs. Equivalent records from the user's own process work in place of the named workflows.

- **Planning a domain move, URL restructure or consolidation map.** The release team owns the plan. This audit can check a release against an approved plan, but it does not write the URL mapping or the migration runbook.
- **Choosing which URL should serve a task, or whether two pages should merge.** Page or site architecture planning. Shared queries alone do not justify a merge.
- **Rich result or structured data changes.** A schema workflow, after this audit has found every producer of the markup.
- **Business Profile or Maps changes.** The Local SEO Audit Skill (`skills/local-seo-audit/`) or an equivalent local audit.
- **Mentions or citations in AI features.** Separate AI visibility work with its own evidence.
- **Content quality, intent fit and claims.** Content workflows. The audit can record that a technically sound page still underperforms, without rewriting it.
- **Measurement setup and outcome review.** Measurement workflows. The audit records measurement defects that limit its own conclusions.
- **Setting SEO priorities for the business.** The SEO Strategy Skill (`skills/seo-strategy/`) or an equivalent strategy record, when the findings change what should come first.

## 3. Minimum case record

| Field | Minimum usable detail |
| --- | --- |
| Site and scope | Host and protocol; the exact URLs, templates or sections in scope; the CMS, page builder and hosting where known |
| Objective | The customer action and business outcome that matter, and the market |
| Symptom | What changed, the first observed date, magnitude and scope, and who reported it and how |
| Intended state | For each URL group: public and indexed, redirected, excluded, private or retired, and who decided |
| Evidence and access | What can be inspected (exports, crawls, page source, headers, logs, account screenshots), with dates, and what is missing |
| Change history | Releases, CMS, plugin or theme updates, content, URL, server, CDN, consent or tracking changes, campaigns and seasonality in the period |
| Authority | Who owns the site and accounts, who implements, and any standing authorisation with its scope |

Ask for an exact export, URL or confirmation rather than every account by default. Never ask for or keep passwords, API keys, verification codes or customer personal data. If any are supplied, leave them out of the report and recommend storing them in an approved restricted location.

A domain on its own, a keyword, or "my SEO is broken" is not yet a case. A crawl export with no question attached is evidence without a case: ask what decision it should support, or audit it for blocking defects only and say so in section 1.

## 4. Return paths

- **Blocked: Define the case** when the site, the scope or the problem cannot be identified, when several sites are in scope and none is selected, or when the intended state of the affected URLs is unknown and only the owner can decide it. Name the missing fact and who can supply it.
- **Blocked: Supply audit evidence** when the case is clear but nothing can be inspected: no exports, no page source or headers, no screenshots, and no ability or permission to open public pages. Name the smallest evidence set that would let the audit start, such as the affected URLs, their response headers and source HTML, a Performance export for two comparable periods, and the release notes for the period.
- If both apply, report the case gap first and list the evidence needed for the next pass.
- **Escalate first: Urgent defect** takes precedence over both blocked statuses when the supplied evidence already shows an urgent defect. Report it, then name what is missing for the rest of the audit.
- One report per site. For several sites, ask the user to pick one, or audit them one at a time with separate records.
- Missing private reports do not block an audit of public output. Mark the conclusions that depend on them as provisional.
