# Source and Metric Rules

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. Everything else is operating method.

## 1. Evidence status

Give every input one status and keep it on every row derived from it.

| Status | Meaning | Permitted interpretation |
| --- | --- | --- |
| Observed first-party | In supplied or authorised Search Console, sales, support, site-search or business data | Evidence within that dataset's coverage |
| Sourced estimate | A named tool reports a metric or modelled value | An estimate, with provider, settings and date |
| Observed public | A dated, directly inspected result, page or public source | An observation in its collection context |
| Inferred candidate | Suggested by a person, a model, an analogy or an unvalidated expansion | A research lead, not measured demand |
| Excluded | Out of scope, misleading, unsupported or redundant | Keep the reason so the boundary can be reproduced |

Keep the exact source, original wording, period, filters, market, language and device where they matter. Separate what a source says from your inference about it. Anonymise customer material and ask for exports, never passwords or unnecessary personal data.

## 2. What each source can and cannot show

| Source | Google guidance | Research consequence |
| --- | --- | --- |
| Search Console queries | Some rare queries are anonymised and left out of tables but kept in chart totals. Tables keep only top rows, so other queries can also be missing [K03, K14]. | The export is not all market demand. A missing query is not zero demand. Record filters and coverage. |
| Search Console metrics | Clicks, impressions, CTR and average position are different measures [K02]. Values shown as not available become zeros in downloads [K14]. | Compare compatible slices. Keep unavailable values as `Not available`, not zero. |
| Search Console query groups and branded filter | Query groups are computed with AI, can change over time and do not affect ranking [K15]. The branded filter is AI-assisted and can misidentify queries [K16]. | Use them for triage. Review family boundaries by task yourself. |
| Search Console API and bulk export | The API has row limits [K11]. The bulk export leaves anonymised query text out and marks those rows [K12, K13]. | Neither recovers every hidden query. Record the route, period, aggregation and privacy flags. |
| Keyword Planner | Keyword Planner is for researching keywords for Search ad campaigns [K05]. Average monthly searches cover a keyword and its close variants for the chosen month range, location and network. Competition shows how many advertisers showed on a keyword relative to all keywords [K04]. | Keep ranges and settings. Never treat advertiser competition as SEO difficulty or a paid forecast as organic traffic. |
| Google Trends and Autocomplete | Trends uses a sample of searches and scales interest from 0 to 100 relative to all searches in that time and place [K06]. Autocomplete does not simply show the most common queries and should not be compared with Trends [K17]. | Never convert a Trends series into search volume or treat suggestion order as demand. |
| Third-party tools | They have no access to Google's internal ranking data and cannot guarantee performance [K08]. | Label provider-specific scores. Check the tool's current definitions before using them. |

Search Console reflects the site's recorded exposure, not every query the market uses. Sales and support language shows real needs but may come from a small or biased sample. Competitor pages and suggestions are discovery leads, not proof of opportunity.

## 3. Metric integrity

- Never invent volume, difficulty, CPC, CTR, trends, traffic, leads or conversion rates.
- Write `Not available` for missing data. Write `0 reported by [source]` only when the source explicitly reports zero.
- Keep ranges as ranges. Do not turn a range into an exact number.
- Keep each provider's metrics separate. Do not average unrelated difficulty scores or mix markets or dates silently.
- Do not sum close-variant estimates into a precise family total. If you aggregate, state the unit, formula, overlap risk and coverage.
- Deduplicate repeated exports before counting.
- Do not apply a universal CTR curve or conversion rate to manufacture a forecast. A scenario needs stated, sourced assumptions and stays separate from observed data.
- CPC is advertising context. It does not prove profit, lead quality or priority.

## 4. Large datasets

Start with the smallest dataset that answers the question. If a dataset is too large to process in full, say how many rows were processed and how, and do not present a partial read as complete. For Search Console exports, keep the property, route, period, dimensions, aggregation, filters, extraction date and privacy flags with the research. Do not assign anonymised rows to invented families.
