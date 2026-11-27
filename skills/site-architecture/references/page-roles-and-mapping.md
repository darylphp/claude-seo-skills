# Page Roles and Mapping

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. Everything else is operating method.

## 1. Mapping procedure

1. **Group by task.** Work from the reader's task, expected page type, audience, locale and offer. Keep mixed intent and uncertainty visible rather than forcing every query into one bucket.
2. **Compare with existing pages.** Use the inventory and any dated result observations from the research. Competitor coverage informs the investigation. It does not dictate what this site needs.
3. **Assign a preferred URL for planning.** Add secondary tasks that fit naturally on the same page. The assignment does not claim exclusive ownership of a query, or that Google must rank that URL.
4. **Prefer the smallest form that completes the task.** A section, table, tool or improved explanation inside an existing page is often enough. A new entity, synonym, question or location does not need a new URL by itself.
5. **Create a URL only when the gates pass.** A distinct user decision, function or meaningful market requirement must justify it. Document its boundary and the useful next step.

**Google guidance [G7]:** creating separate content for every variation of how people might search, including fan-out queries, primarily to manipulate rankings or generative AI responses violates Google's spam policies. Google also describes this as ineffective long term, because a high quantity of pages does not make a site higher quality or more relevant. Its systems can understand several topics on one page, and there is no requirement to break content into small pieces.

**Google guidance [G1]:** Google's ranking systems work mainly at page level, and site-wide signals and classifiers also contribute. Good site-wide signals do not mean all of a site's content will rank well. This gives no basis for a cluster bonus or a required number of pages per topic.

## 2. Decisions

Give each task, URL or candidate exactly one decision.

| Decision | Use when | What it hands on |
| --- | --- | --- |
| Keep | The existing URL already serves the task, or the evidence is too thin to justify change | Nothing, or a provisional keep with the next check |
| Improve | The right URL exists but does not yet complete the task | An improvement scope for the content steps |
| Differentiate | Two related pages serve different tasks but their boundary is blurred | Boundary statements and cross-links for each page |
| Consolidate | Pages are materially substitutable and one destination can keep their useful content and functions | A consolidation record, and the technical work to the developer |
| Create | A new URL passed all five gates, or passed with named conditions | The page record for the content steps |
| Research first | The task, intent or business fit is unclear | A bounded research question |
| Defer | The task is real but not worth doing now: low fit, missing evidence or no capacity | The reason and the trigger for review |
| Reject | The proposal fails a gate on purpose or policy grounds, such as a doorway pattern or pages made for each keyword variation | The reason, and the useful alternative if one exists |

"Retire" an existing page (remove it with no replacement) is not a mapping decision. Record the URL evidence and hand the retirement treatment to the technical work.

## 3. Page roles

Give each URL one primary role and a boundary against its nearest neighbour.

| Role | Primary job and boundary |
| --- | --- |
| Commercial or service | Help a real buyer assess an offer and enquire, book or buy. Use verified scope, terms and proof. Never invent a service or a local presence |
| Category or collection | Help shoppers browse and narrow a meaningful product set. Keep category choice apart from an individual product decision |
| Product or feature | Explain the specific product, capability or integration and its fit. Do not copy one sales claim across many URLs |
| Guide or comparison | Resolve an information need or a real choice with clear explanation, evidence and fair criteria. Split only when the reader's task warrants it |
| Proof or utility | A genuine case study, method, example, calculator, dataset or tool. Embed it in another page when that is more useful |
| Hub or index | Orient visitors across distinct resources. A simple index or a menu route is often enough |
| Location or market | Serve a real presence, a real service area with distinct facts, or a language or regional version that readers need. Never a swapped place name |

## 4. Naming a new URL

**Google guidance [G13]:** use readable words rather than long ID numbers where possible, separate words with hyphens rather than underscores, and trim unnecessary parameters. Overly complex URLs, especially those with many parameters or ones that create infinite spaces such as calendars, sorting and filtering, can cause crawling problems.

**Google guidance [G14]:** organising a site logically can help people and search engines understand how pages relate, but search engines will likely understand pages as they are now, so there is no need to reorganise a site for that alone. Keywords in the domain or URL path alone have hardly any effect on ranking beyond appearing in breadcrumbs. Choosing between subdomains and subdirectories is a business decision. On sites with more than a few thousand URLs, grouping similar topics into directories can help Google learn how often each directory changes.

Operating rules:

- Name the URL for the task in the words readers use, short enough to read aloud.
- Use a folder when it groups a real section the site will maintain, not to create a "silo" signal.
- Do not change a stable URL to fit a new naming scheme. A change needs a reason a reader or the business would recognise, plus redirects, link updates and checks that the technical work owns.

## 5. Language and regional versions

**Google guidance [G10, G16]:** Google recommends a separate URL for each language version, without switching language by cookie, browser setting or IP on one URL. It works out a page's language from its visible content, not from the URL or code attributes. Hreflang tells Google about localised variations of the same content, and each version must list itself and every other version, with pages pointing to each other.

Create a regional or language version only when readers in that market need something different: a translation, different offers, prices, availability or legal terms. A copy with only the country changed is a candidate for the doorway check in the page gates. Implementation of hreflang goes to the technical work.

## 6. URL map fields

Each row of the URL map records:

`Task or family ID | Evidence source | Existing or proposed URL | Primary task | Role | Audience and locale | Nearest overlapping URL and boundary | Decision | Contribution and evidence owner | Link sources | Priority | Dependencies | Confidence | Next check`

A row with a missing field keeps the field and writes what is missing.
