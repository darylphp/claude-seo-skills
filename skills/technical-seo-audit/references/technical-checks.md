# Technical Checks

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. **Check**, **Accept when** and **Avoid** are operating method.

Use an area only when the symptom or the evidence calls for it. Each finding still needs an evidence label, a confidence, a producer and an acceptance check.

## 1. Availability and status codes

**Google guidance [D06]:** content returned with a 2xx status may be indexed, but that is not guaranteed. A 2xx page that looks like an error or is empty can be reported as a soft 404. For 404, 410 and other 4xx codes except 429, Google stops using the URLs over time and removes indexed ones. 5xx and 429 responses slow crawling, and URLs that keep returning errors can be dropped.

**Google guidance [D30]:** for a temporary closure, keep the site online with reduced functionality. Disabling the whole site is not recommended; if unavoidable for a day or two, return an informational 503 page, and for longer closures serve an indexable placeholder home page with a 200 status. Do not return 503 for robots.txt, and do not pause a site with noindex, 403, 404 or 410 responses or robots.txt rules, because those remove URLs from Search.

**Check:** reproduce the response; check normal routes and deliberate error routes; for intermittent failures, capture times, locations and logs and give the host or developer a reproducible case.

**Decide:** an important page returning an error is restored and verified. A retired URL with no useful replacement can return 404 or 410 on purpose. Moved content with a relevant replacement goes to area 4. An error page returning 200 gets the right status or its real content back.

**Avoid:** treating requests for URLs that never existed, such as security probes, as lost landing pages.

## 2. Crawl and indexing controls

**Google guidance [D07, D08]:** robots.txt manages crawling and is not a way to keep a page out of Google. A blocked URL can still be indexed without its content if other pages link to it. To keep a page out, use noindex or password protection. Noindex works as a meta tag or an `X-Robots-Tag` header, but only if the page is not blocked by robots.txt, because Google has to crawl it to see the rule. Google does not support noindex in robots.txt.

**Google guidance [D11]:** when Google finds noindex in the original HTML it may skip rendering, so removing noindex with JavaScript may not work.

**Check:** confirm the intended state, then inspect robots.txt rules, meta robots in source and rendered HTML, and `X-Robots-Tag` on the final response. Find the producer, measure the affected scope, correct only unintended controls, and verify the deployed output.

**Accept when:** pages meant to be indexed carry no blocking directive in source, rendered output or headers, and deliberate exclusions are unchanged.

**Avoid:** removing intentional exclusions (internal search, account, cart, thank-you or staging pages) to raise indexed counts; using robots.txt or noindex as a security control; blocking crawling of a URL whose noindex still needs to be seen.

## 3. Canonicals and duplicate URLs

**Google guidance [D09]:** redirects and `rel="canonical"` are strong canonicalisation signals and sitemap inclusion is a weak one. Google can still choose a different canonical. Do not use robots.txt for canonicalisation, and avoid noindex as a way to choose a canonical within one site, because it removes the page from Search. Keep signals consistent, use a self-referencing canonical on the canonical page, use absolute URLs, and link internally to the canonical URL.

**Google guidance [D11]:** a canonical set by JavaScript should match the original HTML, and only one canonical should remain after rendering.

**Check:** the page's role and its genuinely equivalent variants; the declared canonical against the Google-selected canonical from an indexed inspection; redirects, sitemaps, internal links and hreflang that point elsewhere.

**Accept when:** the intended URL, its content and its signals agree. Record Google's selected canonical as `Not verified` until indexed evidence shows it.

**Avoid:** canonicalising unrelated pages because they share a topic; claiming that a declared canonical forces Google's choice.

## 4. Redirects

**Google guidance [D10]:** permanent redirects (301, 308) tell Google to show the target, and temporary redirects (302, 303, 307) keep the source in results. Server-side permanent redirects are preferred. Meta refresh and JavaScript redirects are fallbacks for when server-side redirects are not possible.

**Google guidance [D17]:** after a site move, keep redirects for as long as possible, generally at least a year, redirect old URLs straight to their final destination, and avoid sending many pages to an irrelevant single URL such as the home page.

**Google guidance [D32]:** for A/B tests that use separate URLs, point variants to the original with a canonical and use temporary redirects, never cloak, and remove test URLs and scripts when the test ends.

**Check:** each source and destination pair, chains, loops, parameters, letter case and trailing-slash variants, and broad pattern rules. Include a URL that a rule must not match.

**Accept when:** each source reaches its approved, relevant destination, in one hop where practical; the destination returns 200 with its intended index state; business functions still work; the previous rule set is kept for recovery.

**Avoid:** redirecting every missing URL to the home page; a temporary redirect for a permanent move or a permanent one for a test; removing redirects soon after a move.

## 5. Rendering and JavaScript

**Google guidance [D11]:** Google processes JavaScript sites in three phases: crawling, rendering and indexing. It will not render JavaScript from blocked files or on blocked pages. Rendering may be skipped for non-200 responses and for pages with noindex in the original HTML. In single-page apps that cannot return a real 404, Google describes redirecting to a URL that returns 404, or adding noindex to the error view with JavaScript.

**Check:** compare source and rendered main content, links, metadata and structured data; blocked resources; delayed data or API errors; mobile and logged-out states. Trace the smallest defect to the template, script, API or security layer.

**Avoid:** assuming JavaScript content is invisible, or that everything a browser renders is indexed; prescribing a framework rebuild before the need is shown; serving crawler-only content, which is cloaking [D27].

## 6. Discovery, internal links and sitemaps

**Google guidance [D13]:** Google can generally crawl a link only when it is an `<a>` element with an `href`. Descriptive anchor text helps, and there is no ideal number of links on a page.

**Google guidance [D12]:** a sitemap should list the canonical URLs you want shown in results. Google uses `<lastmod>` only when it is consistently and verifiably accurate, and it should reflect the last significant change, such as to main content, structured data or links. Google ignores `<priority>` and `<changefreq>`. A sitemap is a hint, not a guarantee of crawling. Each file is limited to 50,000 URLs or 50 MB uncompressed.

**Google guidance [D29]:** the Indexing API is only for pages with JobPosting, or BroadcastEvent embedded in a VideoObject. It is not a submission route for ordinary pages.

**Check:** compare the intended URL inventory with crawl discovery, navigation and contextual links, and the sitemap. Find out why a page looks orphaned in this dataset before calling it orphaned. Inspect the sitemap generator's inclusion rules and representative output, including redirected, noindexed, non-canonical or error URLs listed in it.

**Avoid:** refreshing every `lastmod` daily; treating sitemap inclusion as proof of indexing; site-wide keyword links; "instant indexing" plugins as a general fix.

## 7. Parameters, facets and pagination

**Google guidance [D19]:** uncontrolled filter combinations create large crawl spaces. Decide which facets need to appear in Search before choosing controls. Canonicalisation is not the same as preventing crawling.

**Google guidance [D20]:** Google generally crawls URLs in `href` attributes and does not click buttons or trigger scripts that need user action, so "load more" content needs linked URLs. Link paginated pages sequentially and give each its own URL.

**Check:** for each URL pattern, its customer value, unique inventory, intended index state, how it is discovered and who owns it. Test any proposed robots rule against URLs it should and should not affect, including main products and categories.

**Avoid:** untested broad robots rules; removing useful filters or pagination wholesale; canonicalising every paginated page to page one.

## 8. International and language versions

**Google guidance [D21]:** hreflang tells Google about localised variants of a page. Localised pages count as duplicates only when the main content is untranslated. Google does not use hreflang or the `lang` attribute to detect a page's language.

**Check:** use this area only where genuine language or regional alternatives exist. Map equivalent pages, check that each target is accessible and self-canonical, and that references are reciprocal.

**Avoid:** hreflang for towns or suburbs; merging distinct markets because their pages share English text.

## 9. Performance, mobile and the customer path

**Google guidance [D14]:** Core Web Vitals are used by Google's ranking systems, but good scores do not guarantee top rankings, and chasing a perfect score for SEO alone may not be a good use of time. Page experience is broader: secure delivery, display on mobile, and avoiding intrusive interstitials. Core ranking systems generally assess pages individually, with some site-wide assessments.

**Check:** real user-facing problems first: slow or broken main functions, unstable layouts, obstructive overlays, forms or bookings that fail. Label field data and lab runs separately, and record device, network and cache for lab runs. On WordPress and page-builder sites, test scripts, forms, menus, checkout or booking and layout before and after any optimisation setting or plugin.

**Avoid:** disabling consent, security, accessibility or transaction features to improve a score; claiming a speed change caused a ranking change.

## 10. Crawl capacity, logs and bot access

**Google guidance [D18]:** crawl budget management is an advanced topic mainly for very large sites (around 1 million or more pages changing weekly), medium or larger sites (around 10,000 or more pages changing daily), or sites with many URLs in "Discovered, currently not indexed". These are rough estimates, not thresholds, and most smaller sites do not need it. Noindex does not save crawl budget, because Google still requests the page.

**Check:** use logs or infrastructure data only when the case warrants it, and record coverage, sampling and retention. For suspected firewall or CDN blocking, ask the responsible team to check verified Google requests [D28] and the responses they received.

**Avoid:** making crawl budget a priority for a small site; allowing every request that claims to be Googlebot; disabling security protection without evidence.

## 11. Security, spam and policy signals

**Google guidance [D27]:** spam policies cover cloaking, hacked content (injected code or pages, altered content, malicious redirects), sneaky redirects and malicious practices, including back-button hijacking, where a site interferes with browser navigation so users cannot go straight back. Legitimate redirects such as site moves are not spam; the test is intent to deceive. Google's back-button FAQ says site owners can keep using ad platforms and their code, and that Google acts on pages that show the behaviour. Google uses automated systems and, when needed, human review.

**Google guidance [D22, D36]:** a manual action follows a human reviewer's finding that pages do not comply with the spam policies, and can remove some or all of a site from results. The Security issues report shows Google's findings of hacking or harmful behaviour.

**Google guidance [D24]:** most sites do not need the disavow tool. It is an advanced tool for substantial artificial links tied to a manual action or a likely one, and a new upload replaces the existing list.

**Check:** the Manual actions and Security issues reports if a screenshot or export is supplied, otherwise record them as `Not checked`. Reproduce unusual redirects, injected pages or back-button behaviour and trace the responsible theme, plugin, advertising or third-party script.

**Avoid:** calling every decline a penalty; treating an empty Manual actions report as proof that no algorithmic or policy issue exists; reproducing malicious payloads or customer data in the report; answering a hack with metadata edits; recommending disavow from a vendor's "toxic" score or as a routine task. No checklist certifies a site as secure.
