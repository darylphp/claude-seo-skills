# Inventory and Evidence

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. Everything else is operating method.

## 1. Evidence labels

Give every source and every decision one label.

| Label | Meaning |
| --- | --- |
| Observed | Opened, fetched or rendered during this plan. Record the URL or file, the date, the tool and its settings, and what it showed. |
| Supplied | Provided by the user and not independently checked: a crawl, an export, a research pack, a screenshot or a note. Record who supplied it and when. |
| Owner statement | A business fact stated by the owner or an authorised person, such as an offer, a price range, a capacity limit or a permission. Record who said it and when. |
| Third-party estimate | A keyword tool volume, a backlink count, a crawler similarity score or a vendor metric. Keep the provider, settings, market and date. |
| Inference | A conclusion drawn from labelled premises. Name the premises and keep the uncertainty. |
| Not verified | The check was needed but no evidence was available. Never report it as passed. |

Write `Not available` for data that does not exist. Never write zero for a value that was not measured.

## 2. Inventory only the scope

Combine the available crawl, sitemap, CMS export, navigation and performance records for the section in scope. Record each source's date and coverage. Do not crawl or audit the whole site when the question concerns one section.

| Record | Minimum useful detail |
| --- | --- |
| Identity and role | URL, template, existing or proposed state, audience and locale, offer, primary task, meaningful next step |
| Discovery and status | Observed status and final URL, crawl access, robots directives, declared canonical, internal routes in. Record Google's selected canonical or indexing state only if a Search Console inspection was supplied |
| Content and evidence | Visible purpose, nearest competing URLs, distinct contribution, available proof and its permissions, factual gaps |
| Performance and risk | Query-to-page data, search exposure, enquiries or sales, relevant external links, comparable period, limits, commercial dependencies, owner |

## 3. What each source can and cannot show

| Source | Can show | Cannot show |
| --- | --- | --- |
| Crawl export | URLs reachable from its seeds under its settings, titles, headings, canonicals, directives, internal links and a similarity estimate | URLs it was not seeded with or could not reach, Google's processing, whether two pages serve the same task |
| XML sitemap | The URLs the site lists for discovery | Live URLs left out of it, or whether listed URLs are indexed. A sitemap is a hint, not a guarantee [G17] |
| CMS export | Published, draft and private items, templates and slugs | What a visitor or crawler actually receives |
| Search Console Performance export | Clicks, impressions and average position by page and query, under its filters and row limits | Sessions, enquiries, a rank every searcher sees, or the queries it withholds |
| Analytics | Sessions and recorded events by landing page, under its configuration | Search Console clicks, or whether an enquiry reached the business |
| Enquiry or sales log | Tasks real customers brought, by source where recorded | Search demand in general |
| Keyword tool | An estimate of demand for wording in a market | Whether the business should serve the task, or how many people have it |
| Backlink tool | Links the tool has found | Every link, or how Google values any link |
| Result observation | What one search showed on one date, market, device and setting | What every searcher sees, or why a page ranks |

A crawler's near-duplicate score is a lead for the overlap check, not proof that two pages serve one task. A crawl-depth figure is a diagnostic, not a Google threshold.

**Google guidance [G9]:** Google can use the number of links it needs to follow to reach a page, and the number of links to a page, to infer that page's relative importance within the site. It generally does not look at URL structure to work out a site's structure, and analyses the links between pages instead.

## 4. Confidence

Record three confidences separately, as High, Medium or Low with a reason:

- **The task:** how sure the plan is that real readers have this task and that this business can serve it.
- **The decision:** how sure the plan is that the chosen URL action fits the evidence.
- **The outcome:** what the action is expected to change. This is usually Low before release and is never a ranking or traffic promise.

High demand does not raise confidence in a decision that failed a gate.

## 5. Measurement for page decisions

Keep impressions, clicks, sessions, recorded events, received enquiries and sales as separate measures. Compare like periods and record the timezone, filters and row limits. When two URLs share queries, record which URL Search Console attributed each row to and on which dates, rather than adding their figures into one total. Combined figures for a proposed merge are a scenario, not an observed result.
