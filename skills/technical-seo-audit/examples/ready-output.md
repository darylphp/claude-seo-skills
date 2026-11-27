# Ready Output

Synthetic example produced from the [ready input](ready-input.md). It shows the method, not a real site, account or result.

## 1. Status and conclusion

**Ready for review: Technical audit**

All nine service pages have carried a noindex directive since the 28 October template release, and Google has excluded at least the shopfront signs page from its index because of it. The `/services/` group accounts for 424 of the 442 lost clicks while the blog, home and industry pages held steady, so this defect is the leading explanation for most of the drop. A Google update is not supported by the supplied evidence, but it is not ruled out. First action: Ridgeline Web removes the unintended noindex at its producer, then production is verified.

Site: `https://kestrelsigns.example/`. Scope: the whole site, with the decline in `/services/` as the case. Audit date 27 Nov 2026, evidence cut-off 26 Nov 2026. Evidence basis: supplied Search Console, GA4, crawl and business records and account screenshots (E1 to E11). No page was fetched in this audit. Main limitation: the crawl and inspection results are supplied, not re-run, and no daily or year-on-year data was supplied.

Implementation approval: Awaiting approval

This report does not itself grant implementation authority.

## 2. Case record

- **Site:** WordPress with a page builder, an SEO plugin and a redirect plugin, on managed hosting with a CDN. About 140 published URLs.
- **Objective:** quote requests through `/request-a-quote/` and phone calls from businesses in the Hunter region.
- **Symptom:** Search clicks fell from 1,184 to 742 (down 442, 37%) between 30 Sep to 27 Oct and 29 Oct to 25 Nov 2026. First noticed by Mia Torres in November.
- **Intended state:** service, industry and blog pages indexed. `/thank-you/` and `/?s=` excluded. `/tag/` archives undecided.
- **Change history:** RN-11 on 28 Oct 2026 (theme and SEO plugin updates, new "Service page v2" template on all 9 service pages). The 2024 move from `/signage/` to `/services/`. No other content, URL, tracking or consent changes reported in the period.
- **Ownership and authority:** Mia Torres (Search Console Full user, GA4 viewer, WordPress Editor). Ridgeline Web, Sam Okafor (administrator). MA-2 covers template and plugin bug fixes; URL, redirect, content and feature changes need Mia's written approval.
- **Missing facts:** whether `/tag/` archives should be indexed.

## 3. Evidence and access

| ID | Source | What it showed | Date | Collection conditions | Label | Limits |
| --- | --- | --- | --- | --- | --- | --- |
| E1 | Performance export | Clicks and impressions by page group for two 4-week periods | 26 Nov 2026 | Web search, Australia, all devices | Supplied | No daily data, query rows or year-on-year comparison |
| E2 | RN-11 | Theme, SEO plugin and template changes on 28 Oct | 28 Oct 2026 | Developer's note | Supplied | Settings changed by the updates not listed |
| E3 | Crawl export | Noindex on 9 service pages; redirect chains; sitemap entries; two 404s; warnings | 26 Nov 2026 | Sitemap and home seeds, rendering on, smartphone agent, robots.txt respected | Supplied | Only URLs reachable from the seeds; crawler is not Google |
| E4 | URL Inspection, one URL | Indexed result excluded by noindex, last crawl 12 Nov; live test finds noindex | 25 Nov 2026 | `/services/shopfront-signs/` only | Supplied | Other 8 service URLs not inspected |
| E5 | Page indexing report | "Excluded by 'noindex' tag" rose from 6 to 15 after 3 Nov | 25 Nov 2026 | Screenshot | Supplied | Example list partial (5 service URLs shown) |
| E6 | Developer email | Attributes the drop to an early November update | 24 Nov 2026 | Opinion, no source | Supplied | No dates or source for the update |
| E7 | GA4 summary | Organic sessions to `/services/` and `generate_lead` events | 26 Nov 2026 | Organic Search, Australia/Sydney timezone | Supplied | Event definition not inspected |
| E8 | Quote log | Web form and phone quotes | 26 Nov 2026 | Owner's records | Supplied | Manual log |
| E9 | robots.txt | Blocks `/wp-admin/` and `/?s=` only; sitemap declared | 26 Nov 2026 | Fetched by Mia | Supplied | None noted |
| E10 | PageSpeed Insights | Lab LCP 4.1 s on the mobile home page; no field data | 26 Nov 2026 | One run, mobile | Supplied | One lab run |
| E11 | Note about backlinks | Third-party email claims 300 toxic backlinks | 26 Nov 2026 | Unsolicited email | Supplied | Not evidence of an action |

Not verified or not checked:

- The producer of the noindex (SEO plugin, template or theme setting): Not verified.
- Indexed state of the other eight service URLs: Not verified. E5 shows five of them as examples.
- Manual actions and Security issues reports: Not checked. No screenshot supplied.
- Search Status Dashboard for the period: Not checked. E6 names no update.
- Daily clicks and impressions, and the same periods in 2025: Not available in the supplied data.

## 4. Measurement check

Search Console data covers web search in Australia on all devices, in two complete 28-day periods that each contain four of every weekday. The release day, 28 Oct, falls between them. The export does not state Search Console's reporting timezone and GA4 uses Australia/Sydney, so daily boundaries may differ between the two.

| Measure | Before | After | Change |
| --- | --- | --- | --- |
| Clicks, whole site (E1) | 1,184 | 742 | Down 442 (37%) |
| Impressions, whole site (E1) | 41,200 | 33,900 | Down 7,300 (18%) |
| Clicks, `/services/` (E1) | 512 | 88 | Down 424 (83%) |
| Impressions, `/services/` (E1) | 14,600 | 5,100 | Down 9,500 (65%) |
| Impressions, all other pages (E1) | 26,600 | 28,800 | Up 2,200 (8%) |
| Clicks, blog, home, industries and other (E1) | 672 | 654 | Down 18 (3%) |
| Organic sessions landing on `/services/` (E7) | 640 | 131 | Down 509 (80%) |
| `generate_lead` events (E7) | 31 | 17 | Down 14 (45%) |
| Web form quotes in the owner's log (E8) | 26 | 15 | Down 11 (42%) |
| Phone quotes (E8) | 19 | 17 | Down 2 (11%) |

Search Console, GA4 and the quote log all fall together, and no tracking or consent change was reported, so a measurement artefact does not explain the drop. GA4 records more form events than the owner logs (31 against 26, then 17 against 15). The event definition was not inspected, so that gap is unexplained and neither figure is used to size the drop.

## 5. Urgent defects

None found in the inspected evidence. The quote form still produces logged requests (E8), robots.txt blocks only admin and internal search (E9), and the crawl found the main templates returning 200 (E3). The service page noindex is a section-level defect and is reported as High in sections 6 and 8.

## 6. Findings

| ID | Area | URL, template or pattern | Observed | Intended | Evidence label and confidence in the defect | Producer |
| --- | --- | --- | --- | --- | --- | --- |
| F1 | Crawl and indexing controls | All 9 `/services/` pages, template "Service page v2" | `noindex, follow` meta robots in source and rendered HTML since the 28 Oct release; Google's indexed result for the shopfront page excludes it by noindex | Indexable | Supplied (E3, E4, E5). High | Producer not identified. Candidates: the SEO plugin's robots setting for the template or post type after its update, the template's own page settings, or the theme update (E2) |
| F2 | Redirects | 3 old `/signage/` URLs; 11 links in older blog posts | Two-hop 301 chains to `/services/`; internal links point at redirecting URLs | One hop to the final URL; internal links to final URLs | Supplied (E3). High that the chains exist; low impact | Redirect plugin rules; post content |
| F3 | Sitemaps | Sitemap index | Six listed URLs redirect; a tag sitemap lists 34 `/tag/` archives whose intended state is undecided | Only final, canonical URLs meant for indexing | Supplied (E3). High for the redirecting entries; the tag entries depend on F5 | SEO plugin sitemap settings |
| F4 | Discovery and links | One 2023 blog post; the gallery page | Two internal links return 404: an old brochure PDF and `/gallery/vehicle-wraps-2022/` | Links to working, relevant pages | Supplied (E3). High | Post and page content |
| F5 | Crawl and indexing controls | 34 `/tag/` archives | Indexable; crawler flags "low content" | Undecided (CR-04) | Supplied (E3). Medium that they add little for visitors; not a defect until the owner decides | SEO plugin taxonomy settings |
| F6 | Tool warning | 41 pages | "Meta description over 155 characters" | Not applicable | Supplied (E3). Verified as a warning only [D16] | Not applicable |
| F7 | Tool warning | 30 blog posts | "Multiple H1" | Not applicable | Supplied (E3). Low; heading count alone is not a diagnosed cause, and blog traffic is stable | Theme |
| F8 | Performance | Home page | Lab LCP 4.1 s in one mobile run; no field data | Not established | Supplied (E10). Low | Producer not identified |
| F9 | Security and policy | Whole site | An unsolicited email claims toxic backlinks; Manual actions and Security issues reports not checked | Not applicable | Not verified | Not applicable |

## 7. Explanations for the symptom

| Explanation | Evidence for | Evidence against | Confidence in the cause | Share of the change it could explain | Next check |
| --- | --- | --- | --- | --- | --- |
| X1. Unintended noindex on the service pages from the 28 Oct release | The drop is concentrated in `/services/` (424 of 442 lost clicks; impressions down 65% there while other pages rose 8%). The noindex appears only on the new service template. Noindexed exclusions rose after 3 Nov, and the shopfront page is excluded by noindex at its 12 Nov crawl | None in the supplied evidence. Daily data was not supplied, so the timing within the period is not shown | High that it contributes | Most of the `/services/` decline is consistent with it; the exact share is Not established | Daily `/services/` clicks and impressions from 20 Oct to 25 Nov; indexed inspection of the other eight service URLs |
| X2. A Google ranking update | E6 says forums discussed an early November update | No update named or dated; non-service pages held steady or rose; an update does not add noindex tags to pages | Low as the main explanation; a minor contribution is not ruled out | Not established | Check the Search Status Dashboard for updates or incidents from 1 Oct to 25 Nov and their completion dates [D25, D35]; compare again after F1 is fixed and reprocessed |
| X3. Seasonality or lower demand | None | Mia reports October to November as usually steady; other pages' impressions rose | Low | Not established | The same two periods in 2025 from Search Console |
| X4. Measurement change | None | Search Console, GA4 and the quote log fell together; no tracking or consent change reported | Low | Not established | None needed for this case |
| X5. Competitor or result-page changes | None supplied | Would not explain a noindex exclusion | Not assessed | Not established | Dated result observations for main service queries, only if `/services/` stays down after reprocessing |

## 8. Prioritised actions

| ID | Finding | Priority | Smallest action | Producer and owner | Authority (existing or needed) | Dependencies and recovery | Production acceptance check | Work state | Outcome measure and review trigger |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| A1 | F1 | High | Find the setting that adds noindex to the "Service page v2" template and make the 9 service pages indexable | Ridgeline Web (Sam Okafor) | Existing: MA-2 covers template and plugin bugs that break existing behaviour | Export the current SEO plugin and template settings first; change only the producing setting | On production, uncached: all 9 service URLs return 200 with no noindex in source HTML, rendered HTML or `X-Robots-Tag`; `/thank-you/` keeps its noindex; `/?s=` stays disallowed; a sample blog post is unchanged; the live test for `/services/shopfront-signs/` shows indexing allowed | Proposed | Indexed inspection of the 9 URLs, then `/services/` impressions and clicks against E1, reviewed weekly for four weeks after verification. Trigger: any service URL still excluded by noindex at an indexed inspection two weeks after verification |
| A2 | F4 | Planned | Fix the two broken links: link to the current brochure or remove the link, and point the gallery link to the live gallery page | Mia Torres | Mia's own approval (content change) | None | Both links resolve to relevant pages returning 200 | Proposed | Next crawl shows no internal 404s from these pages |
| A3 | F2 | Planned | Point the 11 old links to their final `/services/` URLs and change the 3 chained rules so each old URL goes straight to its final URL | Ridgeline Web (rules); Mia Torres (links) | Needed: Mia's written approval for the redirect change (MA-2) | Export redirect rules before the change | Each old URL returns one 301 to its final URL, which returns 200; the other 5 redirects are unchanged; the 11 links return 200 | Proposed | Next crawl shows no chains |
| A4 | F3 | Planned | Find why six redirecting URLs are listed and correct the sitemap rules; set the tag sitemap to match the F5 decision | Ridgeline Web | Needed: Mia's approval. Listing redirected URLs may be a plugin bug under MA-2, but that is not established | Note the current sitemap settings first | The sitemap lists only URLs returning 200 that are indexable and self-canonical; `lastmod` values unchanged except for real changes [D12] | Proposed | Sitemaps report and next crawl |
| A5 | F5 | Investigate | Mia decides whether tag archives help visitors find posts; route the decision to page or architecture planning. No noindex until then | Mia Torres | Not applicable | None | Not applicable | Proposed | Decision recorded |
| A6 | F9 | Investigate | Screenshot the Manual actions and Security issues reports. Take no disavow action on the strength of the email [D24] | Mia Torres | Not applicable | None | Not applicable | Proposed | Reports recorded as clear or with findings |
| A7 | X2, X3 | Investigate | Check the Search Status Dashboard for the period, and export the same periods from 2025 | Mia Torres | Not applicable | None | Not applicable | Proposed | Explanation table updated |
| A8 | F8 | Investigate | Repeat the mobile lab test with recorded settings and check the home page for real user problems (menu, quote button, layout) | Ridgeline Web | Not applicable | None | Not applicable | Proposed | Planned fix only if a real problem is confirmed |

No action:

- **F6:** Google sets no fixed description length [D16], and the warning shows no defect.
- **F7:** heading count alone is not a diagnosed cause, and blog traffic is stable. Revisit only if the theme's heading output harms accessibility or page structure.

## 9. Developer handoffs

```text
Action ID and URL, template or pattern: A1. All 9 /services/ pages using the "Service page v2" template.
Reproducible problem and current output: Source and rendered HTML contain <meta name="robots" content="noindex, follow"> (crawl 26 Nov 2026; URL Inspection 25 Nov 2026 for /services/shopfront-signs/).
Intended output and affected scope: No noindex on the 9 service pages. Nothing else changes.
Producer to change (or how to find it): Not identified. Check the SEO plugin's robots settings for the template or post type, the template's own page settings, and whether the theme 4.3 update changed either.
Approved or authorised change, and restrictions: Existing authority under MA-2 for template and plugin bug fixes. No URL, redirect or content changes in this fix.
Cases that must pass: All 9 service URLs return 200 with no noindex in source HTML, rendered HTML or X-Robots-Tag, checked uncached after the CDN clears.
Cases that must stay unaffected: /thank-you/ keeps noindex; /?s= stays disallowed in robots.txt; blog posts and industry pages keep their current robots output.
Recovery method: Exported SEO plugin and template settings from before the change.
Who verifies production, and how: Mia Torres, with a fresh crawl of /services/ and a URL Inspection live test of /services/shopfront-signs/.
```

## 10. Open items and routes

- **Producer of the noindex:** Ridgeline Web to identify while doing A1.
- **Indexed state of the other eight service URLs:** Mia to inspect after A1 is verified.
- **Daily data and the 2025 comparison:** Mia to export (A7).
- **Manual actions and Security issues:** Mia to screenshot (A6).
- **Tag archives:** owner decision, routed to page or architecture planning (A5).
- **GA4 events against the quote log:** the gap is unexplained; a measurement review can compare the event's definition with stored form entries if the figures will be used for reporting.
- **Work states:** A1 to A8 are all Proposed. None has been approved, implemented or verified.
