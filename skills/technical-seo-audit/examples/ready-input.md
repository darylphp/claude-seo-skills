# Ready Input

Synthetic fixture. The business, people, URLs, figures, records and observations are fictional and supplied for simulation only. Place names are used for realism and say nothing about real businesses there. No real plugin, theme or Google update is described.

## Request

From Mia Torres, marketing coordinator at Kestrel Signs, 26 November 2026:

"Our Google traffic has dropped a lot since the end of October. Our web developer thinks it's a Google update. Can you run a technical SEO audit and tell us what to fix first?"

## Case record CR-04

Supplied by Mia Torres on 26 November 2026.

- **Business:** Kestrel Signs, a sign maker in Newcastle, NSW. Shopfront signs, vehicle wraps, illuminated signs, safety signs and window graphics for businesses in the Hunter region.
- **Site:** `https://kestrelsigns.example/` on WordPress with a page builder, an SEO plugin and a redirect plugin, on managed hosting with a CDN. About 140 published URLs: the home page, 9 service pages under `/services/`, 6 industry pages under `/industries/`, about 85 blog posts, contact, about, gallery and `/request-a-quote/`.
- **Objective:** quote requests through the `/request-a-quote/` form and phone calls from Hunter businesses.
- **Intended state:** service, industry and blog pages public and indexed. `/thank-you/` and internal search (`/?s=`) excluded. Tag archives (`/tag/`): "We've never decided whether those should be in Google."
- **Access:** Mia is a Full user in Search Console, a viewer in GA4 and an Editor in WordPress. The developer, Sam Okafor of Ridgeline Web, has administrator access.
- **Authority:** Maintenance agreement MA-2 (1 July 2026) authorises Ridgeline Web to fix "template and plugin bugs that break existing site behaviour" without separate approval. URL, redirect, content and new-feature changes need Mia's written approval.
- **Change history:**
  - 28 Oct 2026: Ridgeline Web updated the theme and the SEO plugin and published a new page-builder template, "Service page v2", applied to all 9 `/services/` pages (release note RN-11).
  - 2024: service pages moved from `/signage/` to `/services/` with redirects.
  - No content, URL, tracking or consent changes in October or November 2026 apart from RN-11.
  - Mia says October to November is usually steady, with a dip from mid-December.

## Evidence

| ID | Source | Date | Content |
| --- | --- | --- | --- |
| E1 | Search Console Performance export, web search, Australia, all devices, 30 Sep to 27 Oct 2026 compared with 29 Oct to 25 Nov 2026, grouped by page path | 26 Nov 2026 | Total clicks 1,184 then 742; impressions 41,200 then 33,900. `/services/`: clicks 512 then 88, impressions 14,600 then 5,100. Blog: clicks 401 then 389. Home: 238 then 231. `/industries/`: 21 then 22. Other pages: 12 then 12. Daily data and query rows were not supplied. |
| E2 | Release note RN-11 from Ridgeline Web | 28 Oct 2026 | "Theme 4.2 to 4.3, SEO plugin updated, new template Service page v2 applied to /services/ pages. Tested on staging." No mention of indexing settings. |
| E3 | Crawl export supplied by Mia: sitemap index and home page as seeds, JavaScript rendering on, smartphone user agent, robots.txt respected, 2 URLs per second | 26 Nov 2026 | 152 URLs: 142 HTML pages returning 200, 8 redirects, 2 returning 404. All 9 `/services/` pages return 200 with `<meta name="robots" content="noindex, follow">` in source and rendered HTML, a self-referencing canonical and no `X-Robots-Tag` header. No other template carries noindex apart from `/thank-you/`. Three redirect chains of two 301 hops from old `/signage/` URLs to `/services/` URLs; 11 links in older blog posts still point to `/signage/` URLs. Six URLs listed in the sitemap redirect. The sitemap index includes a tag sitemap listing 34 `/tag/` archives. The 404s are an old brochure PDF linked from one 2023 post and `/gallery/vehicle-wraps-2022/` linked from the gallery page. Warnings: 41 pages with "meta description over 155 characters", 30 blog posts with "multiple H1", 34 `/tag/` archives with "low content". |
| E4 | URL Inspection screenshots for `/services/shopfront-signs/`, supplied by Mia | 25 Nov 2026 | Indexed result: "URL is not on Google", "Excluded by 'noindex' tag", last crawl 12 Nov 2026. Live test: "Indexing allowed? No: 'noindex' detected in 'robots' meta tag". |
| E5 | Page indexing report screenshot, supplied by Mia | 25 Nov 2026 | "Excluded by 'noindex' tag" rose from 6 to 15 pages after 3 Nov 2026. Examples shown include 5 `/services/` URLs. |
| E6 | Email from Sam Okafor | 24 Nov 2026 | "It's the Google update from early November, every SEO forum is talking about it. Nothing on our side changed that would affect rankings." No dates or source for the update. |
| E7 | GA4 summary, Organic Search, landing page groups, property timezone Australia/Sydney, same periods as E1 | 26 Nov 2026 | Sessions landing on `/services/`: 640 then 131. Quote form `generate_lead` events: 31 then 17. |
| E8 | Owner's quote log | 26 Nov 2026 | Web form quote requests in the same periods: 26 then 15. Phone quotes: 19 then 17. |
| E9 | robots.txt fetched by Mia | 26 Nov 2026 | `User-agent: *`, `Disallow: /wp-admin/`, `Allow: /wp-admin/admin-ajax.php`, `Disallow: /?s=`, `Sitemap: https://kestrelsigns.example/sitemap_index.xml` |
| E10 | PageSpeed Insights, mobile, home page, one run | 26 Nov 2026 | Lab LCP 4.1 s, CLS 0.02. Field data: not enough real-user data. |
| E11 | Note from Mia | 26 Nov 2026 | "Can you also make sure we're not penalised? Someone emailed us saying we have 300 toxic backlinks and need a disavow." No Manual actions or Security issues screenshot supplied. |
