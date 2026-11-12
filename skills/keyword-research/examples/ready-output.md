# Ready Output

Synthetic output for [ready-input.md](ready-input.md). Fictional business, metrics and observations.

## 1. Research conclusion and readiness

- Status: Provisionally ready
- Homeowners in this data are working through five tasks: what a swap costs, how a heat pump compares with gas or electric, finding an Adelaide installer, whether the unit will be too noisy, and rebate eligibility. Cost and comparison (F01, F02) are ready for planning. Installation (F03) and noise (F04) are provisionally ready pending one result observation each, plus manufacturer specifications for F04. Rebates (F05) return for evidence because no current official program source was supplied.
- Main limit: Search Console chart totals were not supplied, so the share of search traffic these rows represent is not known.

Page and URL decisions: Deferred to planning

## 2. Scope, mode and sources

- Question: which customer tasks around heat pump hot water should planning consider next, and what supports each.
- Mode: existing-site opportunities.
- Business: Tallowood Heat Pumps, supply and installation of heat pump hot water systems from two brands, replacing gas or electric storage units, Adelaide metropolitan area only (BS-03).
- Out of scope: repairs, pool heaters, solar panels, solar hot water and rebate applications.
- Market: Australia, Australian English, mobile and desktop.
- Sources: S1 Search Console (observed first-party), S2 Keyword Planner (sourced estimate), S3 sales inbox questions (observed first-party), S4 two result observations (observed public). Settings as recorded in the input.

## 3. Dataset coverage

| Source | Processed | Notes |
| --- | --- | --- |
| S1 | 12 of 12 rows. 153 clicks and 5,445 impressions across the rows. | Anonymised and truncated queries are not in the rows. Share of total traffic: Not available, because chart totals were not supplied. |
| S2 | 9 of 9 rows | Ranges kept as ranges and not summed. P08 shows no estimate, recorded as Not available. |
| S3 | 5 question types, 37 messages | Small sample from one inbox over three months |
| S4 | 2 observations | Rank tracker set to Adelaide, desktop, one date |

Identical strings in S1 and S2, such as G03 and P01, are kept as separate source records.

## 4. Family map

| Family ID | Name | Representative queries and row IDs | Reader task and next action | Stage and intent | Constraints | Evidence status and confidence |
| --- | --- | --- | --- | --- | --- | --- |
| F01 | Swap cost and price drivers | heat pump hot water cost (G03, P01), heat pump hot water price (G04, P02), heat pump hot water cost adelaide (G12), C01 | Work out what a swap will cost and why, then request a quote | Evaluate. Commercial, with a local secondary need from G12. | No published prices. Approved drivers only (PD-1). | First-party, estimate and observed (O1). High for the task, Medium for the local boundary. |
| F02 | Heat pump compared with gas or electric | heat pump vs gas hot water (G05, P03) | Decide whether a heat pump suits them better than gas or electric | Understand and evaluate. Informational with commercial follow-on. | Running cost claims need sourced figures | First-party, estimate and observed (O2). High. |
| F03 | Adelaide installer and installation | heat pump hot water adelaide (G01, P04), heat pump hot water installation adelaide (G02), heat pump hot water installer near me (G11), C04 | Find an installer that covers their area and book a quote | Act. Transactional and local. | Adelaide metropolitan area only | First-party and estimate. No direct observation. Medium. |
| F04 | Noise and placement | heat pump hot water noise (G06, P06), C02 | Check whether the unit will be too loud where it would go | Evaluate. Informational. | Model-specific noise and clearance facts needed | First-party and estimate. No observation. Medium. |
| F05 | Rebates and eligibility | heat pump rebate sa (G10), heat pump hot water rebate (P05), C03 | Find out whether they qualify for a rebate | Understand. Informational, time-sensitive and financial. | The business does not handle rebate applications | First-party and estimate. No official source. Low for any factual answer. |
| F06 | Brand | tallowood heat pumps (G07) | Reach the business directly | Navigational | None | First-party. Existing awareness, not a new opportunity. |

## 5. Result evidence and open boundaries

- **O1, heat pump hot water cost adelaide, 4 Nov 2026, Adelaide setting, desktop, rank tracker:** local results plus mostly installer service pages with price-driver sections, and two cost guides. This supports F01 as an evaluate-and-quote task, and shows a local need sitting inside the cost task.
- **O2, heat pump vs gas hot water, same method:** comparison guides and no local results. This supports F02 as a non-local comparison task, separate from F01 and F03.
- **No observation:** F03, F04 and F05. Validation plan: observe "heat pump hot water installation adelaide" for F03 and "heat pump hot water noise" for F04 with the same method, and check mobile for F03 because the local need is likely to show there.
- **Open boundary F01 and F03:** O1 mixes cost information with local results. Whether cost belongs on an installation page, its own page or both is a planning decision.
- **Open item P07, best heat pump hot water system:** this looks like an independent review or comparison task. The business sells two brands and has no independent testing, so planning needs a disclosure and scope decision before any use. Not observed.

## 6. Entities and decision criteria

| Family ID | Entity, attribute or criterion | Class | Why it matters | Evidence required or source | Uncertainty |
| --- | --- | --- | --- | --- | --- |
| F01 | System being replaced (gas or electric) | Required | Changes the work involved | PD-1 | None |
| F01 | Tank size | Required | Main driver of the quote | PD-1 | None |
| F01 | Electrical work | Conditional | Only when the site check finds it is needed | PD-1 | Frequency unknown |
| F01 | Removal of the old unit | Useful | A cost readers may not expect | PD-1 | None |
| F01 | Published price ranges | Exclude | No prices are approved | Owner approval | Not available |
| F02 | Running cost compared with gas and electric | Required | Central to the decision | A dated official or tariff-based source, not supplied | High until sourced |
| F02 | Suitability conditions such as space and climate | Required | Decides whether a heat pump fits | Manufacturer or official source, not supplied | High until sourced |
| F04 | Noise level by model | Required | Answers the C02 concern directly | Brand A and Brand B specifications, not supplied | High until sourced |
| F04 | Placement clearances | Required | Affects where the unit can go | Manufacturer installation manuals, not supplied | High until sourced |
| F05 | Program eligibility rules | Required | Readers need current rules | Current official program pages, not supplied | Time-sensitive |

## 7. Specific-task and gap candidates

- **Install duration (C04, 5 messages):** a supported customer question with no tool volume (Not available). Keep it under F03.
- **Energy use (P08):** no estimate shown in S2, so Not available. Credible as part of F02. Needs sourced specifications before use.
- **Best system (P07):** see section 5. Candidate only.
- **Competitor gaps:** Not assessed. No competitor pages were inspected.

## 8. Exclusions, missing evidence and corrections

- **Excluded:** repairs (G08, C05), pool heaters (G09) and solar hot water (P09), because BS-03 rules them out.
- **Missing evidence:** current official rebate program pages (F05); Brand A and Brand B noise and clearance specifications (F04); a sourced running-cost comparison (F02); Search Console chart totals for coverage; result observations for F03 and F04.
- **Corrections:** none needed in the supplied data.

## 9. Planning handoff

```text
Family ID, name and representative queries: F01 Swap cost and price drivers. G03, G04, G12, P01, P02, C01
Reader task, outcome, intent and next action: Work out likely cost and drivers, then request a quote. Commercial, local secondary.
Meaningful variants, urgency and constraints: "cost" and "price" share the task. "adelaide" adds a local need.
Observed result types and supporting URLs: O1, installer service pages with price drivers, cost guides, local results.
Candidate role(s), for the planning decision only: A cost section on an installation page, or a standalone cost guide.
Source-labelled metrics and limits: S1 clicks and impressions per row. S2 ranges 1K to 10K for P01 and P02, close variants, not summed.
Decision criteria and entities: Section 6, F01 rows.
Observed existing URL signals: Not available. S1 was exported without the page dimension.
Evidence and useful contribution expected: Approved price drivers (PD-1) explained plainly, with no published prices.
Ambiguity, exclusions and restrictions: The F01 and F03 boundary is open. No prices without owner approval.
Confidence and next check: High for the task. Check the page dimension in Search Console.
```

```text
Family ID, name and representative queries: F02 Heat pump compared with gas or electric. G05, P03
Reader task, outcome, intent and next action: Decide which system type suits them. Informational, commercial follow-on.
Meaningful variants, urgency and constraints: "vs electric" is likely the same task. Not observed.
Observed result types and supporting URLs: O2, comparison guides, no local results.
Candidate role(s), for the planning decision only: A comparison guide.
Source-labelled metrics and limits: S1 per row. S2 range 100 to 1K for P03.
Decision criteria and entities: Section 6, F02 rows.
Observed existing URL signals: Not available.
Evidence and useful contribution expected: A sourced running-cost comparison and suitability conditions.
Ambiguity, exclusions and restrictions: No running-cost claims without a dated source.
Confidence and next check: High. Obtain the sourced comparison.
```

- **F03 and F04:** provisionally ready, with the same fields as above. Both need a result observation first, and F04 also needs manufacturer specifications.
- **F05:** not handed off. It returns for evidence.
- **F06:** brand family, recorded for context only.

Restrictions for all families: no URL, slug or build-order decisions here, no suburb permutations, and no ranking or traffic forecasts. Raw rows, source records and the exclusion log are in the input file and sections 3 and 8.
