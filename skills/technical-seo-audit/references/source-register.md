# Source Register

The rules in this skill paraphrase the Google pages below. "Rechecked 27 Nov 2026" means the page text was reviewed on that date (Asia/Singapore) for the passages this skill uses. "Search-result text" means the passage was confirmed from the page's indexed text in search results on that date, without opening the page. Entries marked "carried forward" keep the playbook's earlier check and were not reopened for v0.1.0. None of these checks inspected an account, a website or a business. Recheck the relevant page before a consequential decision, and review the whole register at least quarterly.

IDs D01 to D32 match the source IDs in the SEO Diagnosis and Technical Decision Playbook v1.2, so each rule can be traced back. D35 and D36 are additions for this skill.

| ID | Source | Used for | Displayed update | Check |
| --- | --- | --- | --- | --- |
| D01 | [Debugging drops in Google Search traffic](https://developers.google.com/search/docs/monitor-debug/debugging-search-traffic-drops) | Main causes of drops, comparison periods, separate search types, small fluctuations, no radical changes to pages performing well | 10 Dec 2025 | Rechecked 27 Nov 2026 |
| D02 | [Google Search's core updates](https://developers.google.com/search/docs/appearance/core-updates) | Confirm completion, wait a full week, small versus large drops, no guarantee of effect | 10 Dec 2025 | Rechecked 27 Nov 2026 |
| D03 | [Performance report overview](https://support.google.com/webmasters/answer/7576553) | Metric definitions, aggregation, exports showing unavailable values as zeros | Not established | 18 Oct 2026, carried forward |
| D04 | [URL Inspection tool](https://support.google.com/webmasters/answer/9012289) | Indexed result versus live test, live test limits, request indexing limits | Not established | Rechecked 27 Nov 2026 |
| D05 | [Page indexing report](https://support.google.com/webmasters/answer/7440203) | Canonical version of important pages, duplicates excluded, no full-coverage target, validation scope and timing | Not established | Rechecked 27 Nov 2026 |
| D06 | [How HTTP status codes affect Google's crawlers](https://developers.google.com/crawling/docs/troubleshooting/http-status-codes) | 2xx not a guarantee, soft 404s, 4xx and 5xx handling, 10 redirect hops | 4 Feb 2026 | Rechecked 27 Nov 2026 |
| D07 | [Introduction to robots.txt](https://developers.google.com/search/docs/crawling-indexing/robots/intro) | Crawl control, not a way to keep pages out of Google | 10 Dec 2025 | Rechecked 27 Nov 2026 |
| D08 | [Block Search indexing with noindex](https://developers.google.com/search/docs/crawling-indexing/block-indexing) | Meta tag or header, must not be blocked by robots.txt, no robots.txt noindex | 10 Dec 2025 | Rechecked 27 Nov 2026 |
| D09 | [How to specify a canonical URL](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls) | Signal strength, Google's own choice, no robots.txt or noindex for canonicalisation, consistent signals | 10 Jul 2026 | Rechecked 27 Nov 2026 |
| D10 | [Redirects and Google Search](https://developers.google.com/search/docs/crawling-indexing/301-redirects) | Permanent and temporary types, server-side preference | 16 Nov 2026 | Rechecked 27 Nov 2026. Displayed update is later than the playbook's check; the passages used here are consistent with the playbook rule |
| D11 | [Understand the JavaScript SEO basics](https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics) | Three phases, blocked resources, noindex and non-200 rendering, JavaScript canonicals, single-page app soft 404s | 4 Mar 2026 | Rechecked 27 Nov 2026 |
| D12 | [Build and submit a sitemap](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap) | Canonical URLs, accurate lastmod, ignored priority and changefreq, a hint only, size limits | 8 Jul 2026 | Rechecked 27 Nov 2026 |
| D13 | [Link best practices for Google](https://developers.google.com/search/docs/crawling-indexing/links-crawlable) | Crawlable `<a href>` links, anchor text, no ideal link count | 10 Dec 2025 | Rechecked 27 Nov 2026 |
| D14 | [Understanding page experience](https://developers.google.com/search/docs/appearance/page-experience) | Core Web Vitals in ranking systems, no guarantee, perfect scores, wider page experience, page-level assessment | 22 Sep 2026 | Rechecked 27 Nov 2026 |
| D16 | [Control your snippets](https://developers.google.com/search/docs/appearance/snippet) | Snippet sources, no fixed description length | Not established | 18 Oct 2026, carried forward |
| D17 | [How to move a site](https://developers.google.com/search/docs/crawling-indexing/site-move-with-url-changes) | Keep redirects at least a year, redirect to final destinations, no mass redirects to an irrelevant URL | 20 Aug 2026 | Rechecked 27 Nov 2026 |
| D18 | [Optimize your crawl budget](https://developers.google.com/crawling/docs/crawl-budget) | Who the guide is for, rough estimates, noindex does not save crawl budget | 22 Jul 2026 | Rechecked 27 Nov 2026 |
| D19 | [Managing crawling of faceted navigation URLs](https://developers.google.com/crawling/docs/faceted-navigation) | Crawl spaces, deciding which facets need Search, canonical versus crawl prevention | Not established | 18 Oct 2026, carried forward |
| D20 | [Pagination and incremental page loading](https://developers.google.com/search/docs/specialty/ecommerce/pagination-and-incremental-page-loading) | `href` crawling, no button clicks, sequential links | Not established | Search-result text 27 Nov 2026. Canonical guidance carried forward from 18 Oct 2026 |
| D21 | [Tell Google about localized versions of your page](https://developers.google.com/search/docs/specialty/international/localized-versions) | Hreflang purpose, untranslated duplicates, language detection | Not established | Search-result text 27 Nov 2026. Reciprocal references carried forward from 18 Oct 2026 |
| D22 | [Manual actions report](https://support.google.com/webmasters/answer/9044175) | Human review, some or all of a site affected, review route | Not established | Search-result text 27 Nov 2026 |
| D24 | [Disavow links to your site](https://support.google.com/webmasters/answer/2648487) | Most sites do not need it, limited use, list replacement | Not established | 18 Oct 2026, carried forward |
| D25 | [Google Search Status Dashboard](https://status.search.google.com/) | Confirmed ranking updates and incidents with dates | Not applicable | 18 Oct 2026, carried forward |
| D27 | [Spam policies for Google web search](https://developers.google.com/search/docs/essentials/spam-policies) | Cloaking, hacked content, sneaky redirects, malicious practices and the back-button FAQ, enforcement | 23 Nov 2026 | Rechecked 27 Nov 2026 |
| D28 | [Verify requests from Google crawlers and fetchers](https://developers.google.com/crawling/docs/crawlers-fetchers/verify-google-requests) | Reverse and forward DNS, published IP ranges | 23 Nov 2026 | Rechecked 27 Nov 2026 |
| D29 | [Using the Indexing API](https://developers.google.com/search/apis/indexing-api/v3/using-api) | Only JobPosting or BroadcastEvent in VideoObject pages | Not established | Search-result text 27 Nov 2026 |
| D30 | [Temporarily pause or disable a website](https://developers.google.com/search/docs/crawling-indexing/pause-online-business) | Reduced functionality, short 503 use, placeholder home page, robots.txt access | 10 Dec 2025 | Rechecked 27 Nov 2026 |
| D32 | [Website testing and Google Search](https://developers.google.com/search/docs/crawling-indexing/website-testing) | Test variants, temporary redirects, no cloaking, clean-up | 10 Dec 2025 | 19 Oct 2026, carried forward |
| D35 | [How to stay informed on Google Search ranking updates](https://developers.google.com/search/docs/ranking/stay-informed) | Wait for completion plus at least a week of data | 24 Nov 2026 | Opened 27 Nov 2026 |
| D36 | [Security issues report](https://support.google.com/webmasters/answer/9044101) | Google's findings of hacking or harmful behaviour, warnings in results | Not established | Search-result text 27 Nov 2026 |

## Differences from the playbook

- **D06:** the playbook does not mention the default of 10 redirect hops. The skill adds it from the current page.
- **D27:** Google added a back-button hijacking FAQ on 23 Nov 2026, after the playbook's check. It says site owners can keep using ad code and that Google acts on pages that show the behaviour. The playbook's own caution, that ordinary use of browser-history features is not by itself a demonstrated violation, stays an operating method because the page does not address it.
- **D30:** the current page adds that a longer closure should use an indexable placeholder home page with a 200 status. The playbook summarised only the short 503 case.
- **D35:** a new page published after the playbook. It repeats the core-update advice to wait for completion and at least a week of data.
- **D23:** the playbook's "Prevent abuse on your site" page is not used by this skill. D36 covers the report the audit reads.

When a page changes, record the ID, the section, the check date, what changed and which reference file it affects. Update the reference file first, then this register.
