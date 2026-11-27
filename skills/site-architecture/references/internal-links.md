# Internal Links and Navigation

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. Everything else is operating method.

## 1. Find the useful links

1. Review the navigation and the source pages in the inventory. Find important destinations with no useful route in, broken links, misleading anchors and links that pass through old redirects.
2. Match the reader's next question or decision to a destination. A cost guide may need a route to the service page and the quote form. A product category may need a selection guide. Links across sections are fine when they help.
3. Choose the smallest change: one contextual link, a sentence that introduces it, or a menu repair. Check the visible sentence and the copy around it. Add new text only when it helps the reader and is factually supported.
4. Prioritise destinations that matter to the business or are hard to reach, where the evidence supports it.

## 2. Rules for each link

| Control | Apply it this way |
| --- | --- |
| Crawlable route (Google guidance) | An `<a>` element with an `href` that resolves to the destination. Check the rendered page when JavaScript builds the menu or the links [G3] |
| Anchor and context (Google guidance) | Descriptive, reasonably concise text that makes sense on its own, in a sentence that says why the reader would follow it. Avoid generic anchors such as "click here" [G3] |
| Destination (Google guidance) | Link to the canonical URL, not to a duplicate or a redirecting URL [G5] |
| Discovery (Google guidance) | Every page you care about needs a link from at least one other page on the site. There is no ideal number of links per page [G3] |
| Navigation (operating) | Use menus, category paths, hubs and breadcrumbs where they help people find their way. A long hub or links from every page to every other page are not required |
| Quantity (operating) | No quotas, automatic all-to-all cluster blocks or repeated exact-match anchors. An accurate repeated label or a useful two-way link is not a problem in itself |
| Priority (operating) | Weigh task importance, existing routes, traffic context, how many pages a template change reaches, and effort. Crawl depth is a diagnostic, not a Google threshold |

**Google guidance [G9]:** menus and links between pages can affect how Google understands a site's structure. Google can use how many links it takes to reach a page, and how many links point to it, to infer its relative importance within the site. It generally does not look at URL structure to work out site structure. Google strongly recommends linking to every product you want indexed, using `<a href>` links rather than JavaScript events on other elements.

**Google guidance [G14]:** Google mainly finds pages through links from pages it has already crawled.

## 3. Link change record

```text
Source URL:
Destination canonical URL:
Current placement, or proposed placement:
Anchor text and the sentence around it:
Reader benefit:
Status and redirect check on the destination:
Template affected (one page, or every page using the template):
Owner and approval needed:
Work state:
Verification date and result:
```

Do not fill missing facts with plausible values.

## 4. Check the implemented route

Confirm that the link appears on the intended production page, is visible, uses the correct `href`, and reaches the intended final URL with a 200 status. Check mobile and every affected template. A crawler graph can confirm a route exists. It cannot prove that Google has crawled it, and it cannot measure a ranking gain. Do not promise an "authority transfer" from a link count.
