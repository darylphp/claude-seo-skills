# Priorities and Sequencing

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. Everything else is operating method.

## 1. Short reasoned queue first

For a small backlog, a short queue with one reason per item is enough. Tie-break with evidence strength, business urgency, dependencies and the cost of being wrong.

## 2. Optional comparison score

Use only for work that passed its gates. It is a project comparison tool, not a Google formula, a ranking probability or a forecast.

| Factor | Weight | 1 to 5 score |
| --- | --- | --- |
| Business or conversion value | 20 | 1 = limited contribution; 5 = strong, justified relevance |
| User need and task fit | 20 | 1 = weak fit; 5 = clear, supported task |
| Useful contribution and evidence | 20 | 1 = limited feasible value; 5 = strong feasible contribution |
| Existing-page opportunity | 15 | 1 = little supported benefit; 5 = clear improvement opportunity |
| Discovery and architecture value | 10 | 1 = little benefit; 5 = a clear useful route or defect to address |
| Relevant trust and proof | 10 | 1 = limited support; 5 = strong, verified support |
| Delivery ease and low upkeep | 5 | 1 = difficult or costly; 5 = easy and maintainable |

Total = sum of (weight × score ÷ 5), from 20 to 100 when all seven factors are scored. Higher means higher internal priority. An unknown factor stays unscored: leave the total unscored or show a labelled scenario. Keep a one-line reason per factor, and record confidence separately. High demand cannot override a failed gate.

## 3. Sequence by dependencies

| Stage | Work and acceptance |
| --- | --- |
| 1. Confirm the problem | Scope, baseline and access. Send confirmed blockers, such as a broken enquiry path or a noindexed section, to the technical work first. Do not make every planning task wait for an exhaustive audit |
| 2. Choose the page action | Existing pages and overlap evaluated. Consolidate only when justified |
| 3. Secure the contribution | Facts, original assets, expert input, permissions and decision help confirmed and passed to the content steps before drafting |
| 4. Produce the scoped work | Improve the chosen page or build the highest-value missing page. Copy, metadata, media and links reviewed. Structured data routed to schema review |
| 5. Release and verify | The approved revision implemented, production checked and the change recorded. Technical verification comes before any outcome is interpreted |
| 6. Learn before expanding | Reader and business results, upkeep and uncertainty reviewed. Then expand, improve, keep, investigate or stop |

**Google guidance [G8]:** content made with generative AI, including titles, descriptions, structured data and image alt text, should be fact-checked and reviewed manually before publishing. Keep each review tied to the exact revision.

## 4. Work states

| State | Evidence needed |
| --- | --- |
| Proposed | Named action, reason and scope. Preparing the plan does not authorise any live change |
| Approved | Who approved which action IDs, and when. Existing authorisation that covers the action is recorded with it |
| Implemented | A recorded release, its owner and the exact URLs or templates affected. A CMS save is not proof of the production output |
| Technically verified | Production status, intended access, indexability and canonical, rendered content and links, the redirect map where relevant, and a working enquiry or purchase path |
| Outcome reviewed | A comparable period, the observed result, other explanations considered, confidence, and the keep, improve, investigate or recover decision |

Report a state only when the input shows it. "The developer did it yesterday" is implemented according to the owner, not technically verified.

## 5. Measure the decision

Before release, record the baseline for each affected URL and task: search exposure and query mix by URL and family, country, device and period; enquiries or sales; and production and upkeep cost. Keep unavailable data explicit. Do not add overlapping family figures into a precise total.

**Google guidance [G11]:** traffic drops have several possible causes, including algorithmic updates, technical issues, seasonality, changing interests and reporting problems. Google suggests comparing a period with a similar earlier period, and recommends against radical changes to pages that are already performing well.

Annotate each release. Examine demand, seasonality, measurement changes, competitors, search result layout and technical changes before attributing a result to the architecture change. Choose a review window that suits the data volume. No universal waiting period proves success or failure.
