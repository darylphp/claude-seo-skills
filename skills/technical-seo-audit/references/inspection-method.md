# Inspection Method

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. Everything else is operating method.

## 1. Inspect one URL

Record each step with the tool, device, user state (logged out, uncached, consent given or not) and date.

1. **Requested URL.** Use the URL exactly as it is linked, listed in the sitemap or reported.
2. **Redirect hops.** Record each status code and `Location`. **Google guidance [D06]:** Google's crawlers follow up to 10 redirect hops by default. Chains still slow visitors and add requests, so shorten them where practical.
3. **Final response.** Status code and headers, including `X-Robots-Tag`, any `Link` canonical header, content type and caching.
4. **Source HTML.** Title, meta robots, canonical, hreflang, main content, links and structured data as served before scripts run.
5. **Rendered output.** The same items after JavaScript runs, and any difference from the source.
6. **Mobile and other states.** The mobile view, and logged-out, uncached or consent-dependent states where they matter.
7. **The customer path.** The form, booking or checkout destination the page exists for. Do not submit a real lead or order unless the owner authorised a test.

Record anything that blocked the inspection, such as a firewall, a geo rule or a login, as a limit, not as a finding about Google.

## 2. Sample with a reason

- Inspect a failing example, a healthy comparator from the same template, and each template variant involved.
- Widen the sample when a shared template, plugin, server rule or CDN rule is implicated, or when the change is high risk.
- Record how the sample was chosen. Never extend a spot check into a claim about every URL.

## 3. Crawl for a defined question

1. Define the host, the scope, the seeds (sitemaps, navigation, a URL list), whether rendering is needed, the user agent and the question the crawl answers.
2. Set request limits that suit the site. Avoid an unnecessary full crawl of a fragile site.
3. Record inclusions, exclusions, robots handling, authentication, rendering mode and any limits.
4. Collect the response, directive, canonical, title, heading, link and sitemap evidence the question needs.
5. Inspect real examples, including healthy comparators and exceptions, before grouping anything as a template defect.
6. Keep the configuration with the export so that later crawls compare like with like. Export the evidence a decision needs, not every warning.

A crawler is not Google. Do not report a crawl as complete when exclusions, limits, blocked resources or partial seeds constrain it.

## 4. Find the producer before changing output

| Output or problem | Where to look |
| --- | --- |
| Robots and indexing directives | The CMS visibility setting, page or template settings, the SEO plugin, HTTP headers, server or CDN rules, leftover staging configuration |
| Canonical, title, meta description, structured data | The SEO plugin, theme, page builder template, custom code, tag manager, or more than one of these at once |
| Redirects and status codes | A redirect plugin, server configuration, CDN rules, CMS routes, page state (draft, private or trashed) |
| Missing content or links | Page builder templates, widget display conditions, scripts, API responses, cache variants |
| Broken enquiry path | The link or form action, popup trigger, validation, external booking domain, notification delivery, tracking |

Do not assume a site uses any particular component. Check the deployed HTML and headers rather than treating a setting screen as proof. Avoid adding a plugin to control a field that an existing maintained system already controls. When two producers emit the same element, record both and recommend one owner for it.

## 5. Staging, caching and production

- Keep a recoverable baseline before a shared change: a configuration export, a content backup or the previous template.
- Staging results do not certify production. Check production after deployment, including cache and CDN variants.
- Check that staging-only controls (a site-wide noindex, a password, a `Disallow: /`) have not reached production, and that a public staging copy is not open to indexing. **Google guidance [D07]:** robots.txt is not a mechanism for keeping a page out of Google, so it is not privacy protection for staging. Use authentication.
