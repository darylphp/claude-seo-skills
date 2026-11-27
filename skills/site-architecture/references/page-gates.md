# Page Gates

IDs in brackets refer to the [source register](source-register.md). Text marked **Google guidance** paraphrases that source. The gates, sampling and release controls are operating methods, not Google ranking or eligibility requirements.

## 1. Five gates for a new page

Run every Create candidate through all five. Record pass, conditional pass or fail for each, with the evidence and its label.

| Gate | Pass evidence | If it fails |
| --- | --- | --- |
| 1. Real need | A supported customer task and business relevance, from enquiries, Search Console rows, result observations or research marked ready. Inferred demand is labelled as inference | Research first, with a bounded question |
| 2. Distinct job | A one-sentence purpose and a boundary against the nearest URLs. Shared subject matter is allowed. Redundant pages need investigating | Improve or Differentiate the nearest page |
| 3. Existing-page test | The closest existing page is named, with the reason a restrained improvement, a section or a link cannot serve the task | Improve or Keep the existing page |
| 4. Feasible contribution | The actual evidence, experience, utility, analysis or decision help the page will offer, with its availability, permission and a way to verify it before drafting | Conditional pass with the missing item named, or Defer |
| 5. Delivery and upkeep | A workable CMS route, a discovery route, the intended search status, an owner and the capacity to maintain it, and the relevant policy risk assessed | Defer until an owner or route exists |

A conditional pass names exactly what is missing and who supplies it. A planned case study or a future expert quote is not current evidence.

Missing evidence never justifies inventing it. A failed creation gate is not an instruction to noindex, delete or redirect an existing page. Assess those actions separately with URL evidence.

**Google guidance [G2]:** Google offers self-assessment questions about people-first content, including whether a site has a primary purpose or focus, whether content gives original information, research or analysis, whether a reader leaves having learned enough to reach their goal, and whether content is being produced on many topics in the hope that some of it performs well. The gates apply these questions proportionately. They do not require every ordinary service page to contain a proprietary study.

## 2. The set gate for templated pages

Apply it to any proposed set of location, service-area, category, directory or data-driven pages that share a template. Keep the five gates for each member, and inspect the whole pattern and its data.

| Gate | Required evidence |
| --- | --- |
| Purpose and boundaries | The audience task, business need, URL pattern and proposed members. Existing URLs compared and exclusions recorded. Why separate destinations help readers rather than one page |
| Template utility | Useful browsing, decision help, records or functions beyond swapping a town, product or keyword. The right role for the set. No invented presence, products or stock |
| Member evidence | Verified data and critical facts for each URL, their provenance, how missing facts are handled, and an upkeep owner. A sound template cannot make up for unsupported member facts |
| Discovery and search scope | Which members are meant for indexing and how readers reach them. Duplication and facets assessed separately, with technical controls handed to the technical work [G12] |
| Delivery and policy review | Doorway and scaled-content patterns assessed across the set, CMS constraints, maintenance and recovery. No compulsory word counts or invented uniqueness percentages |

**Google guidance [G4]:** doorway abuse is when sites or pages are created to rank for specific, similar search queries and lead users to intermediate pages that are less useful than the final destination. Google's examples include pages targeted at specific regions or cities that funnel users to one page, and substantially similar pages that are closer to search results than a clearly defined, browseable hierarchy. Scaled content abuse is when many pages are generated primarily to manipulate rankings rather than help users, no matter how they are created [G4, G8].

A shared template or a large URL count alone does not establish either policy problem. Assess purpose, usefulness and the policy examples. Passing the set gate is not a policy clearance.

## 3. Sample, release and review before expanding a set

- Review representative members, including edge cases and members with sparse data or no inventory. Record how the sample was chosen, its size and what was not reviewed. A sample pass does not verify every member.
- Use a staged release when the risk justifies it. Set the scope, production acceptance, business outcome, stop criteria and review trigger before release. Google prescribes no batch size in the sources reviewed.
- Expand only after reviewing implementation, reader value, outcomes and upkeep. Repair or defer weak proposed members.
- Assess removing, redirecting or excluding existing members separately, with URL evidence and a recovery plan.

## 4. Faceted and filtered pages

**Google guidance [G12, G18]:** faceted navigation can create very large numbers of URLs that crawlers must fetch before they can tell whether they are useful, which slows discovery of new pages. If filtered URLs are not needed in Search, Google describes preventing their crawling. If some are needed, it describes consistent parameters, a stable filter order and a 404 for combinations with no results. Its pagination guide recommends crawlable links between paginated pages, a unique URL for each page, and keeping sorted and filtered variations out of the index.

The architecture decision is which filtered views have a distinct task, real search demand and useful inventory, so they deserve an indexable URL in the plan. Everything else is a browsing control. The crawl and indexing controls themselves go to the technical work.

## 5. Single-page decision card

```text
Scope and evidence: site and section; audience and locale; objective; task or family IDs; exact URLs; source dates; what was inspected; unknowns
Decision and boundary: Keep / Improve / Differentiate / Consolidate / Create / Research first / Defer / Reject; why; nearest competing URL; alternative considered; confidence
Gates: real need; distinct job; existing-page test; feasible contribution; delivery and upkeep (pass, conditional or fail, with evidence)
Contribution: useful outcome; verified evidence or asset; permissions; missing facts; owner
Architecture: preferred URL; navigation and context; link sources; onward routes; intended canonical and search status
Delivery and review: dependencies; priority reason; implementer; approval status; production checks; baseline; review trigger; recovery plan where material
```

These are templates, not observed findings.
