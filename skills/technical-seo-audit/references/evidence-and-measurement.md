# Evidence and Measurement

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. Everything else is operating method.

## 1. Evidence labels

Give every source and every finding one label.

| Label | Meaning |
| --- | --- |
| Observed | Opened, fetched or rendered in this audit. Record the URL or file, the date, the tool and its settings, and what it showed. |
| Supplied | Provided by the user and not independently checked: an export, crawl, screenshot, log extract or note. Record who supplied it and when. |
| Inference | A conclusion drawn from labelled premises. Name the premises and keep the uncertainty. |
| Not verified | The check was needed but no evidence was available. Never report it as passed. |

Account screenshots and exports stay **Supplied** with their property, report, mode (indexed result or live test), filters and date. A crawler export stays **Supplied** with its configuration.

## 2. What each source can and cannot show

| Source | Can show | Cannot show |
| --- | --- | --- |
| Browser or public fetch | Status, redirects, headers, source HTML and rendered page for that request, device and user state | Search Console state, Google's selected canonical, manual actions, server history, real conversions, or what Google's own fetch received |
| Crawler export | Patterns across the crawled set under its settings | URLs it was not seeded with or could not reach, Google's processing, a complete inventory unless the seeds were complete |
| URL Inspection, indexed result | What Google recorded at its last crawl, including the Google-selected canonical | Whether today's deployment works |
| URL Inspection, live test | Whether Google can fetch the page now and whether indexing is allowed | Canonical selection, duplicate handling, sitemap and referring-page presence, manual actions, or a guarantee of indexing [D04] |
| Page indexing report | Reasons and example URLs for groups of pages | The root cause behind each status, or a complete URL list |
| Performance report | Clicks, impressions, CTR and average position under the stated filters [D03] | Sessions, leads, or a fixed rank seen by every searcher |
| Analytics | Sessions and events recorded under its configuration | Search Console clicks, or whether a submission reached the business |
| Server or CDN logs | Requests received during the retained period | Requests blocked before logging, or anything outside retention |
| Lab performance test | One run under stated device, network and cache conditions | What real users experience |
| Field performance data | Real-user experience for a page or a group of pages | The cause of a problem on one page, or its effect on rankings |

**Google guidance [D04]:** the indexed result reflects Google's known version of the page, and the live test checks the current page. The live test cannot predict whether the tested version would be chosen as canonical, does not check sitemaps or referring pages, does not take manual actions into account, and a valid result is not a guarantee of indexing. Requesting indexing does not guarantee it, and requests have a daily limit.

**Google guidance [D05]:** the aim is to get the canonical version of every important page indexed. Duplicate and alternate pages are expected to stay out, so full coverage is not the goal. "Crawled, currently not indexed" is common and not always a problem.

**Google guidance [D28]:** a request can be verified as Google's through a reverse DNS lookup followed by a forward lookup, or by matching the IP against Google's published ranges. The user-agent string is not identity proof.

## 3. Confidence

Give separate confidence for the defect, the cause and the proposed action when they differ.

- **High**: direct evidence for the affected URLs and a clear applicable rule.
- **Medium**: good evidence with a gap, or an operating method applied to clear facts.
- **Low**: indirect evidence, a single sample or an untested assumption.

For example, an unintended noindex observed in a shared template supports high confidence in the defect and the repair, while the share of a traffic loss it explains can stay `Not established`.

Timing alone does not show cause. A decline after a Google update, a plugin or theme update or a release is a lead to check. The same claim repeated across tools, forums or vendors is not corroboration.

## 4. Measurement checks

Run these before explaining any movement.

1. Confirm the property, host and protocol, search type, filters, country, device and timezone of each source, and keep the settings with the export.
2. Use complete comparison periods of equal length and state why they were chosen. **Google guidance [D01]:** a recent period can be compared with the previous period or the same period a year earlier, and search types (web, image, video, news) should be checked separately.
3. Report absolute and percentage change together. Small counts produce large percentages.
4. Segment by search type, page group, query group, country and device where the data allows, and keep an unaffected comparator. Do not present a filtered or incomplete query subset as all demand.
5. Keep impressions, clicks, sessions, recorded events, stored submissions, received enquiries, qualified leads and sales separate. A gap between two of them is investigated (definitions, counting, consent, attribution, coverage) before either source is called wrong.
6. Keep missing values as `Not available`. **Google guidance [D03]:** exports can show unavailable values as zeros, and totals can differ between chart and table because of aggregation.
7. Do not submit a real lead, order or payment to test a path without the owner's authorisation, and record whether a test proved a click, a stored submission or actual receipt.

If measurement is broken, repair or qualify it before interpreting the history. Genuine visible defects can be reported in parallel.

## 5. Rule sources

Keep two kinds of rule apart in every finding.

- **Google guidance**: a paraphrase of a current Google page, cited by its ID.
- **Operating method**: a working practice from this skill, such as a priority, a sampling rule or an acceptance check. It is not a Google requirement or a ranking factor.

If a source and a user instruction conflict, follow the supported rule and state the conflict.

## 6. Claims to avoid

- Ranking, traffic, indexing, recovery or timing promises.
- A named cause supported only by timing.
- That a fix is live, verified or recognised by Google when the evidence shows only that it was proposed, approved or saved in a CMS.
- That a page is indexed, excluded or canonical from a third-party tool alone.
- First-hand experience, tests or results attributed to anyone without supporting evidence.
