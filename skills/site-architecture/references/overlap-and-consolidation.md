# Overlap and Consolidation

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. Everything else is operating method.

## 1. Overlap is a hypothesis

Use "cannibalisation" as a hypothesis about unhelpful overlap. Shared queries, ranking URLs that change between dates, or one low-performing page do not by themselves show harm. Related pages can serve different tasks, and both can be useful.

## 2. Compare before choosing a destination

Compare the pages on each of these, over comparable periods, and record missing data:

- primary task, intent and page type
- audience, locale and offer or inventory
- useful content and assets, such as photos, data, tools or answers found nowhere else
- conversion paths and the enquiries or sales each page starts
- query-to-URL history, with the dates each URL was shown
- relevant external links
- technical state: status, canonical, directives and internal routes
- operational dependencies, such as campaigns, print material or menu positions

Do not choose the destination on traffic, word count or a tool score alone.

## 3. Decide

| Observed situation | Decision to evaluate |
| --- | --- |
| Same topic, different task | Keep both and Differentiate: state each boundary and add contextual cross-links where they help the reader |
| Materially substitutable pages | Consolidate when one destination can keep the useful content and business functions, supported by URL-level evidence and a controlled plan |
| Technical duplicates (the same content at several URLs) | Canonicalisation or redirects chosen by the technical work. Never use a canonical tag to combine distinct topics |
| Local or language variants | Keep justified market functions. Investigate near-duplicate doorway patterns without assuming every local or translated page is redundant [G4, G10] |
| Insufficient evidence | Keep provisionally, name the next check that would separate the explanations, and record lower confidence. Do not invent conversions, link value or a cause |

**Google guidance [G5]:** canonical tags are for duplicate or very similar pages. A redirect and a `rel="canonical"` are both strong signals, and Google may still choose its own canonical. Google does not recommend noindex to stop a page being chosen as canonical within one site, because noindex blocks the page from Search entirely, and robots.txt should not be used for canonicalisation. Linking consistently to the preferred URL helps.

**Google guidance [G14]:** content available under several URLs is inefficient but does not lead to a manual action.

## 4. Before any merge or redirect

Complete this record. A proposed redirect without it stays `Research first` or `Keep`.

```text
Source and destination URLs:
Substitutability evidence (task, audience, offer, query history):
Useful differences and how each is kept on the destination:
Comparable performance by URL, with periods and limits:
Links, enquiry paths and conversion dependencies:
Content and assets to move, with permissions:
Redirect and reference map (internal links, menus, sitemap, canonicals, hreflang and structured data references where present):
Approvals needed and who gives them:
Backup and recovery:
Production acceptance check:
Outcome measure and review trigger:
```

**Google guidance [G6, G15]:** for a permanent move, Google recommends a server-side permanent redirect where possible, and 301 and 308 both mean a page has moved permanently. Its site move guide says to keep redirects for as long as possible, generally at least a year, to update internal links and sitemaps to the new URLs, to give new URLs self-referencing canonicals, and not to redirect many old URLs to one irrelevant destination such as the home page.

Operating rules:

- A useful destination must exist before the redirect goes live.
- Reject blind bulk redirects to the home page or a broad category. If no relevant replacement exists, hand the retirement treatment to the technical work.
- A rollback plan is a safeguard. It is not a reason to use a temporary redirect for a move meant to be permanent.
- Writing, implementing and checking the redirect belongs to the technical work. The plan records the decision, the map and the acceptance check.

## 5. After a consolidation

Track the source and destination separately from technical completion. Record when the redirect was implemented, when it was checked in production and when Google's reports first reflect it. Compare the destination's combined query set against the baseline of both URLs, labelled as a comparison of two periods, not as proof that the merge caused any change.
