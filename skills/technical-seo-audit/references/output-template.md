# Audit Report Template

Use these 10 numbered headings in this order with one exact status from SKILL.md. For a blocked report, explain the gap in section 1, keep confirmed facts in section 2, and mark sections that depend on the missing input as `Deferred`. Keep raw rows and long exports in a referenced appendix, not in the narrative.

## 1. Status and conclusion

The exact status, then the direct conclusion in two or three sentences: what is wrong, what matters most, and what should happen first. Name the site, the scope, the audit date and evidence cut-off, the evidence basis (public output, supplied exports, account screenshots, logs) and the main limitation. Then, on its own line:

`Implementation approval: Awaiting approval`

Replace it only when an approval for the exact actions was supplied, naming the approver, role, date and the action IDs it covers. Existing authorisation that covers an action belongs with that action in section 8. Follow with: `This report does not itself grant implementation authority.`

## 2. Case record

The site and the URLs, templates or sections in scope; the CMS, builder and hosting where known; the objective and customer action; the symptom with its first observed date, period and magnitude; the intended state of each affected URL group; the change history; who owns, implements and approves. List missing facts.

## 3. Evidence and access

| ID | Source | What it showed | Date | Collection conditions | Label | Limits |
| --- | --- | --- | --- | --- | --- | --- |

Then the checks that were needed but are `Not verified` or `Not checked`, and why.

## 4. Measurement check

The properties, filters, search type, country, device, timezone and comparison periods used. Each measure kept separate, with absolute and percentage change. Any measurement defect or gap, and which conclusions it limits. Write `Not available` where data does not exist.

## 5. Urgent defects

Each urgent defect with its evidence, owner, containment within existing authority, what not to do, and the production acceptance check. If there are none, write `None found in the inspected evidence` and say what the inspection covered.

## 6. Findings

| ID | Area | URL, template or pattern | Observed | Intended | Evidence label and confidence in the defect | Producer |
| --- | --- | --- | --- | --- | --- | --- |

Include verified tool warnings and their outcome. Mark sampled findings with the sample size and how it was chosen.

## 7. Explanations for the symptom

| Explanation | Evidence for | Evidence against | Confidence in the cause | Share of the change it could explain | Next check |
| --- | --- | --- | --- | --- | --- |

Write `Not applicable` when the case has no decline or symptom to explain. Never name a cause from timing alone.

## 8. Prioritised actions

| ID | Finding | Priority | Smallest action | Producer and owner | Authority (existing or needed) | Dependencies and recovery | Production acceptance check | Work state | Outcome measure and review trigger |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Order by priority, then by customer impact. List no-action decisions separately, each with its reason.

## 9. Developer handoffs

For each Urgent and High action:

```text
Action ID and URL, template or pattern:
Reproducible problem and current output:
Intended output and affected scope:
Producer to change (or how to find it):
Approved or authorised change, and restrictions:
Cases that must pass:
Cases that must stay unaffected:
Recovery method:
Who verifies production, and how:
```

## 10. Open items and routes

Each unknown with the evidence that would resolve it and who can supply it. Handoffs to other workflows, with what each needs. The state of every action: proposed, approved, implemented, technically verified, reprocessed or outcome reviewed. Proposed is the default.
