# Ready Output

Expected output for the synthetic [ready input](ready-input.md). Every business, person, URL and figure is fictional.

## 1. Status and decision summary

**Ready for review: Architecture plan**

Larkspur Tile & Stone needs one new page, not 30: shower repairs are a real, separate customer task with 27 enquiries in 13 weeks and no page that serves them. The two bathroom renovation pages serve the same task and should become one, keeping the Geelong page's two project photos. The cost guide stays separate but needs links in and out. The agency's 30 suburb pages, `/services/` restructure and 40 question posts are not recommended.

Site `https://larkspurtiling.example/`, scope: service, cost and suburb pages and the proposals in E7. Site or section mode. Plan date 27 Nov 2026, evidence cut-off 25 Nov 2026. Main limitation: built from the supplied crawl and exports; the live site and Search Console's URL Inspection were not checked.

Decisions: 1 Consolidate, 1 Differentiate, 1 Create (conditional), 1 Research first, 2 Keep, 3 Reject.

`Implementation approval: Awaiting approval`

This plan does not itself grant implementation authority.

## 2. Scope and sources

- **Site and scope:** `https://larkspurtiling.example/`, WordPress with a page builder. Bathroom, shower repair, cost and suburb pages, and the three E7 proposals. Laundry, tiling and project pages are out of scope except as link sources.
- **Business:** renovations, tiling, waterproofing and shower repairs in Geelong, the Bellarine and the Surf Coast. No tile sales to the public.
- **Objective:** quote requests and calls; more shower repair work from May to August.
- **People:** Priya Nair approves. Tom Becker implements. CP-3 covers bug fixes, not new pages, redirects, menus or content.

| ID | Source | What it showed | Date | Coverage and settings | Label | Limits |
| --- | --- | --- | --- | --- | --- | --- |
| E1 | Crawl export | 97 pages, two near-duplicate bathroom pages, 14 suburb pages, no shower repair page | 24 Nov 2026 | Sitemap and home seeds, rendering on, smartphone | Supplied | Pages not linked or listed would be missed; similarity is the crawler's estimate |
| E2 | Search Console export | Clicks and impressions by page and query-page row | 25 Nov 2026 | Web, Australia, 13 weeks, top 1,000 rows | Supplied | Row limit; no URL Inspection; no daily rows beyond the summary |
| E3 | Enquiry log | 48 renovation and 27 shower repair enquiries | 25 Nov 2026 | Same 13 weeks | Owner statement | Source of each phone call not recorded |
| E4 | GA4 lead events | Form events by landing page | 25 Nov 2026 | Organic Search, Australia/Melbourne | Supplied | Phone calls not tracked |
| E5 | Backlink export | 2 linking domains to the Geelong page | 24 Nov 2026 | Tool's index | Third-party estimate | Not every link; no value implied |
| E6 | KR-07 research pack | Families F1 to F5 and list U1 | 20 Nov 2026 | Result observations 19 Nov | Supplied | F4 and F5 provisional; U1 unvalidated |
| E7 | Agency proposal | Three proposals | 12 Sep 2026 | | Supplied | Proposals, not evidence of need |
| E8 | Shower repair assets | 6 permitted photos, warranty W-2, process notes | 25 Nov 2026 | | Owner statement | Price range not yet confirmed in writing |
| E9 | Navigation | Main menu and footer links | 24 Nov 2026 | From E1 | Supplied | |

`Not verified`: Google's selected canonical for the two bathroom pages (no URL Inspection supplied); the live pages (not opened for this plan); 12-month performance for the `/areas/` pages.

## 3. URL inventory

| URL | Template | Role | Primary task | State | Status, canonical and directives | Routes in | Performance (13 weeks) | Label |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `/bathroom-renovations/` | Service | Commercial | Hire a bathroom renovator | Live | 200, self-canonical, indexable | Main menu, 41 links | 612 clicks, 19 form leads | Supplied (E1, E2, E4) |
| `/bathroom-renovation-geelong/` | Service | Commercial | Same as above | Live | 200, self-canonical, indexable | Footer, 3 posts | 96 clicks, 3 form leads, 2 linking domains | Supplied, Third-party (E5) |
| `/waterproofing/` | Service | Commercial | Membrane waterproofing before tiling, for renovations and builders | Live | 200, self-canonical, indexable | Main menu | Not supplied | Supplied |
| `/blog/bathroom-renovation-cost/` | Post | Guide | Set a renovation budget | Live | 200, self-canonical, indexable | 1 link, depth 4 | 244 clicks, 5 form leads | Supplied |
| `/blog/how-to-tell-if-your-shower-is-leaking/` | Post | Guide | Diagnose a leaking shower | Live | 200, self-canonical, indexable | 2 links | 8 clicks from repair queries | Supplied |
| `/blog/choosing-bathroom-tiles/` | Post | Guide | Choose tiles for a bathroom | Live | 200, self-canonical, indexable | Not supplied | 11 clicks from comparison queries | Supplied |
| `/areas/` (14 pages) | Suburb | Location | Same as the bathroom service page, with a suburb name | Live | 200, self-canonical, indexable | Footer list only | 41 clicks combined; Torquay 19, Ocean Grove 9, Highton 6, other 11 combined 7 | Supplied |
| `/shower-repairs/` | Service | Commercial | Fix a leaking or mouldy shower without renovating | Proposed | | | | |

## 4. Task-to-URL map

| ID | Task or family | Preferred URL | Role | Nearest URL and boundary | Decision | Contribution and evidence owner | Link sources | Priority | Dependencies | Confidence (task / decision) | Next check |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| M1 | F1 Hire a bathroom renovator in Geelong | `/bathroom-renovations/` | Commercial | `/bathroom-renovation-geelong/`: no distinct task | Consolidate | Move the two project photos and captions; Priya | Main menu, home, posts | 2 | Priya's redirect approval | High / Medium | Consolidation record complete; URL Inspection of both pages |
| M2 | F2 Set a renovation budget | `/blog/bathroom-renovation-cost/` | Guide | `/bathroom-renovations/` helps choose a renovator; the guide helps plan a budget | Differentiate | Existing guide; Priya | `/bathroom-renovations/` | 1 | None | High / High | Links L1 and L2 live |
| M3 | F3 Fix a shower without renovating | `/shower-repairs/` (Proposed) | Commercial | `/waterproofing/` covers new membranes; `/bathroom-renovations/` covers full jobs | Create (conditional) | 6 permitted photos, warranty W-2, process notes, price range in writing; Priya | `/bathroom-renovations/`, `/waterproofing/`, leaking-shower post, main menu | 3 | Evidence record, brief, approval | High / High | Written price range; content steps |
| M4 | F4 Compare tile types | Not assigned | | `/blog/choosing-bathroom-tiles/` | Research first | | | 5 | KR-07 result observation | Low / Low | Observe results in Australia for the F4 queries |
| M5 | F5 Renovator searches with a suburb name | `/bathroom-renovations/` | Commercial | Same task as F1 | Keep | Service-area wording on the page; Priya | As M1 | | M1 | Medium / Medium | None beyond M1 |
| M6 | E7 item 1: 30 more suburb pages | None | | | Reject | | | | | High / High | |
| M7 | Existing 14 `/areas/` pages | Unchanged | Location | `/bathroom-renovations/` | Keep (provisional) | | Footer | 4 | 12-month URL evidence | Low / Low | 12 months of clicks, enquiries and links per URL |
| M8 | E7 item 2: move services into `/services/` | Current URLs | | | Reject | | | | | High / High | |
| M9 | E7 item 3 and U1: 40 question posts | None | | F2 and F3 pages | Reject | | | | | High / High | Validate questions as sections for F2 and F3 |

## 5. New-page gates

| Candidate | Real need | Distinct job | Existing-page test | Feasible contribution | Delivery and upkeep | Result |
| --- | --- | --- | --- | --- | --- | --- |
| `/shower-repairs/` | Pass: 27 enquiries in 13 weeks (E3), 1,350 impressions with no matching page (E2), F3 ready (E6) | Pass: fix an existing shower, not renovate it or waterproof a new one | Pass: `/bathroom-renovations/` has one sentence; adding the repair decision there would mix a small urgent job with a full renovation, and `/waterproofing/` is written for builders | Conditional: 6 of 9 photos permitted, warranty W-2 and process notes available (E8); the $300 to $900 range needs Priya's written confirmation | Pass: existing template, Priya owns it, menu slot available; menu change needs approval | Create, conditional on the written price range |
| 30 more suburb pages (E7 item 1) | Fail: F5 says the task is the same as F1 and results show main service pages | Fail: no distinct job per suburb | Fail: `/bathroom-renovations/` serves it | Fail: no suburb-specific facts or projects supplied | Not assessed | Reject (see section 6) |

## 6. Page sets

**Proposed set: 30 more `/areas/` pages (E7 item 1).** Purpose and boundaries: fail, the task is F1 with a place name, and separate destinations would not help readers more than the service page. Template utility: fail, 11 of the existing members differ mainly in the suburb name (E1). Member evidence: fail, no suburb-specific projects, prices or facts were supplied for the 30 suburbs. Discovery: footer list only. Policy review: the pattern matches Google's doorway example of pages targeted at specific cities that funnel users to one page [G4]. Result: **Reject.** Service-area settings belong in a local SEO review of the Business Profile.

**Existing set: 14 `/areas/` pages.** The failed proposal says nothing about these. Do not noindex, delete or redirect them on that basis. Three (Torquay, Ocean Grove, Highton) carry real project summaries and earn 34 of the 41 clicks. The other 11 earn 7 clicks combined, but 13 weeks is too short to judge. Result: **Keep, provisionally.** Next check: 12 months of clicks, enquiries and linking domains per URL, then a separate decision with a consolidation record for any page that would merge.

## 7. Overlap and consolidation

**`/bathroom-renovations/` and `/bathroom-renovation-geelong/`.** For substitutability: same task, audience and offer; both shown for the same two queries, the Geelong page on 23 of 91 days (E2); 82% similar (E1). Against: none found. The Geelong page's distinct assets are two project photos and two linking domains. Decision: **Consolidate** into `/bathroom-renovations/`, which has the menu position, more internal links and more enquiries.

```text
Source and destination URLs: /bathroom-renovation-geelong/ to /bathroom-renovations/
Substitutability evidence: same task, audience and offer (E1, E6 F1); query-page rows for the same queries (E2)
Useful differences and how each is kept: Belmont ensuite and Newtown family bathroom photos and captions move to the destination's project section
Comparable performance by URL: 13 weeks to 23 Nov 2026: 612 and 96 clicks; 19 and 3 form leads (E2, E4)
Links, enquiry paths and conversion dependencies: footer link, 3 blog posts, trades directory listing, tile supplier feature (E5); both pages use /get-a-quote/
Content and assets to move, with permissions: two photos already published by Larkspur; confirm customer permission still applies
Redirect and reference map: 301 from the source to the destination; update the 3 blog posts (L3); remove the footer link (L4); remove the source from the sitemap
Approvals needed: Priya, in writing (CP-3 does not cover redirects)
Backup and recovery: export the source page before the change; restore it from the export if the redirect causes problems
Production acceptance check: source returns one 301 hop to the destination with a 200; photos visible on the destination; no internal links to the source remain; sitemap lists only the destination
Outcome measure and review trigger: F1 clicks and quote requests for both URLs combined against this 13-week baseline, 12 weeks after the change, labelled as a comparison of periods
```

Redirect rules are a draft for Tom's review. Implementation and production checks belong to the technical work.

**`/bathroom-renovations/` and `/blog/bathroom-renovation-cost/`.** They share the word "renovation" but not the task: one helps choose a renovator, the other helps set a budget. Decision: **Differentiate.** No canonical between them, because they are not duplicates [G5].

## 8. Internal links and navigation

| ID | Source URL | Destination URL | Placement | Anchor and context | Reader benefit | Template reach | Dependency | Owner | Work state |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| L1 | `/bathroom-renovations/` | `/blog/bathroom-renovation-cost/` | Pricing paragraph | "what a bathroom renovation costs in Geelong", in a sentence about planning a budget before the quote | Budget help before asking for a quote | One page | None | Tom, after Priya's approval | Proposed |
| L2 | `/blog/bathroom-renovation-cost/` | `/bathroom-renovations/` and `/get-a-quote/` | Closing section | "our bathroom renovation service" and "book an on-site quote" | Next step after budgeting | One page | None | Tom | Proposed |
| L3 | 3 blog posts | `/bathroom-renovations/` | Existing link positions | Existing anchors kept if descriptive | No redirect hop | 3 posts | M1 | Tom | Proposed |
| L4 | Site footer | Remove "Geelong bathrooms" | Footer | | Removes a duplicate route | Every page | M1 | Tom | Proposed |
| L5 | `/bathroom-renovations/` | `/shower-repairs/` | Replaces "We also fix leaking showers." | "shower repairs and regrouting", in a sentence for people who need a fix, not a renovation | Reaches repair callers who land on the renovation page | One page | M3 live | Tom | Proposed |
| L6 | `/waterproofing/` | `/shower-repairs/` | After the scope paragraph | "repairs to existing leaking showers" | Separates builders' work from home repairs | One page | M3 live | Tom | Proposed |
| L7 | `/blog/how-to-tell-if-your-shower-is-leaking/` | `/shower-repairs/` | Final section | "get a leaking shower assessed" | Next step after diagnosis | One page | M3 live | Tom | Proposed |

Navigation change N1: add "Shower Repairs" to the main menu after "Bathroom Renovations", once M3 is live. Needs Priya's approval.

The `/services/` restructure (M8) is not recommended. Google generally works out a site's structure from the links between pages, not its URLs [G9], and keywords in the URL path alone have hardly any ranking effect [G14]. Moving every service URL would add redirects and risk without a supported benefit.

## 9. Build order, approvals and handoffs

1. **L1 and L2.** Small, no dependencies, and they connect the page with the most impressions to the service page. Approval: Priya (content change). Check: links visible and resolving with a 200 on the production pages.
2. **M1 consolidation, with L3 and L4.** Approval: Priya, in writing. Recovery: export of the source page. Check: section 7 acceptance check.
3. **M3 `/shower-repairs/`, then L5 to L7 and N1.** Evidence first: the written price range and the six permitted photos. Then the brief, drafting, QA and publication, each approved by Priya. Check: page returns 200, self-canonical, indexable, linked from the three sources and the menu. Aim to publish before May if the evidence and approvals allow; no timing promise is made.
4. **M4 research question.** For the consultant.
5. **M7 evidence for the `/areas/` pages.** Then a separate decision.

All items are `Proposed`. CP-3 covers none of them.

```text
To the content steps (M3): /shower-repairs/ (Proposed); commercial service page; task: fix a leaking or mouldy shower without renovating (F3); Geelong, Bellarine and Surf Coast homeowners; boundary: not full renovations (/bathroom-renovations/) or new membranes (/waterproofing/); owned topics: regrouting, resealing, leak repair, warranty, process; excluded: renovation pricing, tile sales; contribution: 6 permitted photos, warranty W-2, process notes, written price range; links in: L5, L6, L7, N1; link out: /get-a-quote/; decision status: Create, conditional, awaiting approval
To the content steps (M2): no brief needed; links L1 and L2 only
To the technical work (M1): redirect and reference map in section 7; production acceptance check
To keyword research: M4: do Australian searchers comparing porcelain and ceramic tiles want a tile shop or renovation planning, and which U1 questions match F2 or F3 tasks?
To local SEO: service-area settings in the Business Profile for the suburbs in E7 item 1
```

## 10. Open items, measurement and review

- **Open:** the written price range (Priya); Google's selected canonical for the two bathroom pages (URL Inspection in Search Console); 12-month `/areas/` evidence; F4 result observation.
- **Would change a decision:** if URL Inspection shows the Geelong page as Google's choice for both, keep the consolidation but recheck the destination's content against the source before the redirect. If the 11 thin suburb pages show enquiries over 12 months, revisit M7.
- **Baseline (13 weeks to 23 Nov 2026):** F1 612 and 96 clicks; 48 renovation quote requests; 27 shower repair enquiries (21 phone); F3 1,350 impressions, 22 clicks; cost guide 244 clicks.
- **Outcome measures:** F1 clicks and renovation quote requests across both URLs; shower repair enquiries by source; impressions and clicks for F3 queries on `/shower-repairs/`.
- **Review trigger:** 12 weeks after each release, and again after winter. Prior-year data was not supplied, so a seasonal comparison is `Not available`.
- **Confidence in outcomes:** Low until released and measured. No ranking, traffic, indexing or timing promise.
