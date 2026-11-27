# Architecture Plan Template

Use these 10 numbered headings in this order with one exact status from SKILL.md. For a blocked or research-first plan, explain the gap in section 1, keep confirmed facts in section 2, and mark sections that depend on the missing input as `Deferred`. In single-page mode, keep all 10 headings, mark sections that do not apply as `Not applicable`, and put the decision card in section 5 or section 7. Keep raw rows and long exports in a referenced appendix, not in the narrative.

## 1. Status and decision summary

The exact status, then the direct conclusion in two or three sentences: which tasks get which URLs, what changes first, and what is not worth doing. Name the site, the scope, the mode, the plan date and evidence cut-off, and the main limitation. Give a count of decisions by type. Then, on its own line:

`Implementation approval: Awaiting approval`

Replace it only when an approval for the exact actions was supplied, naming the approver, role, date and the action IDs it covers. Existing authorisation that covers an action belongs with that action in section 9. Follow with: `This plan does not itself grant implementation authority.`

## 2. Scope and sources

The site and the section in scope; the business, priority offers and exclusions; the objective and customer action; audience, market and language; the CMS and template constraints; who owns, implements and approves. Then:

| ID | Source | What it showed | Date | Coverage and settings | Label | Limits |
| --- | --- | --- | --- | --- | --- | --- |

Then the checks that were needed but are `Not verified`, and why. List missing facts.

## 3. URL inventory

| URL | Template | Role | Primary task | State | Status, canonical and directives | Routes in | Performance (period) | Label |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

Only the URLs relevant to the scope. Write "No existing pages (stated by owner)" for a new site.

## 4. Task-to-URL map

| ID | Task or family | Preferred URL (existing or proposed) | Role | Nearest URL and boundary | Decision | Contribution and evidence owner | Link sources | Priority | Dependencies | Confidence (task / decision) | Next check |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

One decision per row. Name the research family IDs. Mark a proposed URL as `Proposed`.

## 5. New-page gates

For each Create candidate, and each candidate that failed:

| Candidate | Real need | Distinct job | Existing-page test | Feasible contribution | Delivery and upkeep | Result |
| --- | --- | --- | --- | --- | --- | --- |

Each cell gives pass, conditional or fail with its evidence ID. Name what a conditional pass is waiting for, and who supplies it. Write `Not applicable` if no new page is proposed.

## 6. Page sets

For each templated set proposed or under review: the set gate record (purpose and boundaries, template utility, member evidence, discovery and search scope, delivery and policy review), the sample reviewed and its limits, and the result: pass, revise or defer. Keep proposals for new members apart from decisions about existing members. Write `Not applicable` if there is no set.

## 7. Overlap and consolidation

For each overlap hypothesis: the pages, the comparison, the evidence for and against substitutability, and the decision. For each Consolidate decision, the full consolidation record. Write `None identified in the inspected evidence` and say what the check covered if there is none.

## 8. Internal links and navigation

| ID | Source URL | Destination URL | Placement | Anchor and context | Reader benefit | Template reach | Dependency | Owner | Work state |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Then any navigation change, with the menu, label and position.

## 9. Build order, approvals and handoffs

The ordered queue with one reason per item, or the optional score with its factor reasons. For each action: the existing authorisation or the approval needed, dependencies, the recovery method for a shared change, the production acceptance check and the work state. Then the handoff block:

```text
To the content steps (per Create or Improve): URL; role; task and family IDs; audience and market; boundary and nearest URL; owned and excluded topics; contribution and evidence owner; link routes in and out; decision status
To the technical work: redirect and reference maps; canonical, indexing and crawl control decisions; release and production checks
To keyword research: the bounded question for each Research first item
To schema review or local SEO: the page and the question
```

## 10. Open items, measurement and review

Unknowns and who can resolve them. What evidence would change a decision. The baseline per URL and task, the outcome measures, the review trigger, and the confidence in each outcome. No ranking, traffic, indexing or timing promise.
