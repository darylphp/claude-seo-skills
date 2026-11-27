# Priorities and Actions

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. Everything else is operating method.

## 1. Priorities

These are operating priorities, not Google severity labels. Weigh business impact, scope, urgency, evidence, effort, dependencies, reversibility and maintenance. Never rank by issue count or tool score alone.

| Priority | Typical condition | What the report says |
| --- | --- | --- |
| Urgent | The site or its main customer path is unavailable or unsafe: an outage, a security incident, an unintended noindex, crawl block or redirect across the whole site, or a broken main enquiry, booking or purchase path | Name the owner now; contain or repair within existing authority; do not wait for a wider study |
| High | A confirmed defect on important pages or a shared template, including an unintended noindex, block or redirect on a section; wrong facts in required output | Fix before treating the affected work as complete |
| Planned | A supported improvement to discovery, rendering, efficiency or experience | Brief a bounded change with an owner and an acceptance check |
| Investigate | A material symptom with an uncertain cause, an undecided intended state, or evidence that is not yet available | Name the next discriminating check, the data needed and who decides |
| No action | Expected behaviour, negligible impact, weak evidence, or an implementation that is already adequate | Say why, and add a trigger if one would be useful |

**Audit-tool warnings.** A crawler's warning is a lead until a sample is verified and its intended behaviour and impact are known. Many warnings end as no action. For example, **Google guidance [D16]:** snippets can come from page content or the meta description, depending on the query, and Google sets no fixed character limit for descriptions, so a length warning alone is not a defect.

## 2. Urgent route

Use **Escalate first: Urgent defect** when the evidence shows a defect that meets the Urgent condition above. For each urgent defect, report:

- what is affected and the evidence for it
- the owner to contact and the authority they already hold
- the containment or repair that fits that authority, with the producer to change
- what not to do while it is fixed, such as deleting content, repeatedly toggling settings, or requesting indexing while the defect is still live
- the production acceptance check, and the cases that must stay unaffected

For a security incident, preserve the evidence securely, assign the host, developer or security owner, keep payloads and customer data out of the report, verify the clean-up and normal functionality, and use Google's review route in the Security issues or Manual actions report where it applies [D22, D36].

## 3. Smallest justified action

Choose one: fix, investigate, improve, test, monitor, defer or no action. Change the producer, not the symptom. Group related template changes into one controlled release. Avoid overlapping changes that would make the outcome impossible to read, unless a justified release requires them.

## 4. Action record

For each action, record:

- the exact URL, template or pattern, the current output and the intended output
- the producer and the owner, or `Producer not identified`
- existing authorisation that covers it, and any approval still needed
- dependencies, risks and the recovery method for a shared or risky change
- positive test cases and the cases that must stay unaffected
- the production acceptance check
- the work state the evidence supports (section 5)
- the outcome measure and a review date or trigger

## 5. Work states

| State | Evidence needed |
| --- | --- |
| Proposed | The exact change, its reason, dependencies and acceptance check are defined |
| Approved | A record of the required approval, or existing authorisation that covers it |
| Implemented | The change is applied to the intended environment |
| Technically verified | Production output meets the acceptance check, including the unaffected cases |
| Reprocessed | Later evidence, such as an indexed inspection, shows Google's updated record |
| Outcome reviewed | Suitable performance or business data was examined with its timing and attribution limits |

A CMS save is not production. A validation pass is not reprocessing, and reprocessing is not an outcome. Not every action needs every state.

**Google guidance [D04, D05]:** requesting indexing is optional, does not guarantee indexing and has a daily limit. Validating a fix in the Page indexing report rechecks the known affected URLs, typically within about two weeks, and is not required for Google to update its records.

## 6. Stop, defer or escalate when

- the next step needs permission, private data or a business decision that is not available
- a high-risk regex, server, security, legal or migration decision exceeds the available expertise or access
- further tests add nothing once the defect is verified
- the evidence does not support the explanation someone wants
- no justified improvement remains, in which case record no action

Continue useful analysis while naming the specific blocker. Missing data is not a reason to withhold every recommendation.

## 7. Never recommend

- An "instant indexing" plugin, or the Indexing API for ordinary pages [D29]
- Noindex to force a canonical choice [D09]
- Redirecting every missing URL to the home page [D17]
- Disavow from a vendor's "toxic" score alone, or as a routine task [D24]
- Crawler-only content, cloaking or sneaky redirects [D27]
- Returning 503 for robots.txt, or pausing a site with noindex or robots.txt [D30]
- Disabling consent, security, accessibility or transaction features to improve a score
- Deleting pages, mass noindexing or rewriting content because of a tool warning or the timing of a drop

## 8. Handoffs

Put developer-ready detail for each Urgent and High fix in report section 9. Hand other work to the workflow that owns it: page or architecture planning, content, structured data, local search, measurement, a migration plan, or the strategy record when the findings change what should come first. State what each handoff needs. The audit does not do that work.
