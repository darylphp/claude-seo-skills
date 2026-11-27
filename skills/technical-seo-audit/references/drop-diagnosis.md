# Drop Diagnosis

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. Everything else is operating method.

## 1. Sequence

1. **Confirm the measure.** Clicks, impressions, average position, sessions, enquiries or sales? Record the onset, whether the change is sustained, and its size in absolute and percentage terms.
2. **Separate the scope.** Site-wide, template, section, single page, country, device, search type or query group. Keep at least one unaffected comparator.
3. **Check the operational history.** Releases, CMS, plugin or theme updates, server or CDN changes, URL changes, tracking or consent changes, stock, prices, campaigns. Reproduce any apparent regression.
4. **Check official context.** The Search Status Dashboard lists confirmed ranking updates and incidents with their dates [D25]. Record those dates as context, not as proof of a cause for this site.
5. **List the competing explanations** and give each the evidence for it, the evidence against it, and the next check that would separate it from the others.
6. **Choose the response.** Repair an evidenced fault, investigate with a named check, improve a failing task, or monitor for a bounded period with a trigger. Do not bulk rewrite, delete or deindex pages because of timing.

**Google guidance [D01]:** the main causes of a drop in organic Search traffic are algorithmic updates, technical issues, security issues, spam issues, seasonality and changing interests, and site moves and migrations. Small position changes can happen at any time and may recover without action, and Google advises against radical changes to pages that already perform well.

## 2. Patterns worth separating

These are possible explanations, not diagnoses.

| Observation | Possible explanations | Next useful check |
| --- | --- | --- |
| One section falls, the rest is stable | A template or section-level control, a change to those pages, a demand shift for that offer | Compare that section's URLs before and after; inspect a failing URL and a comparator |
| Clicks down, comparable impressions broadly stable | Query mix, position, result layout, title or snippet appeal | Stable query and page groups; dated result observations |
| Impressions and clicks both down | Demand, exposure or position, indexing, changed scope | Trends, indexing state of the affected pages, deployment history |
| Average position improves while clicks fall | A changed query mix or lost broad exposure | A comparable query group rather than the overall average |
| Sessions down, Search Console clicks steady | Tracking, consent, attribution or landing-path changes | Tag and consent releases; landing-page paths |
| Enquiries down, qualified traffic steady | A broken path, an offer or capacity change, seasonality, event definitions | The real customer journey and business records |
| One rank tracker shows a fall | Location, device, query or collection differences, or real movement | Repeat comparable observations and corroborating data |

## 3. Google updates

**Google guidance [D02, D35]:** confirm on the Search Status Dashboard that an update has finished, wait at least a full week after it completes, then compare that week with a week before the rollout started. Small drops generally do not call for drastic action; large, sustained drops warrant a deeper review of the site and the most affected pages. Changes can take days to months to show, and there is no guarantee that changes will have a noticeable effect.

**Operating rule:** the waiting period never applies to an outage or a clear defect. Fix those now. An update that coincides with a drop stays a candidate explanation, and its share of the drop stays `Not established` unless the evidence separates it from the other candidates.

## 4. Manual actions, security issues and allegations

**Google guidance [D22]:** a manual action follows a human reviewer's finding and is shown in the Manual actions report. An empty report does not show that no algorithmic or policy issue exists.

**Operating rule:** record the Manual actions and Security issues reports as `Not checked` when no evidence of them is supplied. A vendor's "penalty" label, a "toxic backlinks" email or a forum thread is not evidence of an action. Do not call every decline a penalty, every AI-assisted page spam, or every third-party page site reputation abuse; apply the relevant current policy to the actual pages [D27].

## 5. Release regressions

For a drop after a release, compare the same URLs before and after: status, indexability, canonical, main content, internal links, structured data and the customer path. Identify the change set and the producer of each regression.

Make any rollback or restore conditional on a diagnosis, a suitable backup or recovery point, a compatibility check and existing authority. A scoped repair of the responsible producer is often less risky than a full rollback. Before any database restore, protect orders, enquiries and other data created since the release.

## 6. What the explanation section must say

- Each explanation as supported, unsupported or untested, with confidence and the evidence for and against it.
- What share of the change each one could explain, or `Not established`.
- The next check, who can run it, and what result would change the conclusion.
