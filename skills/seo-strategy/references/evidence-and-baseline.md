# Evidence and Baseline

Evidence labels, registers and baseline steps are operating methods. Google statements carry source IDs from the [source register](source-register.md).

## Business-fact and assumption register

Keep business-specific information in the pack, not in the skill. For each material item record:

- The fact or assumption, with its exact scope and wording.
- Status: **Approved fact**, **Supplied, unconfirmed**, **Published statement**, **Supported interpretation** or **Unknown**.
- Source or evidence owner, and the date or validity period.
- Permitted use, confidentiality and any publication restriction.
- The decision it affects and the confirmation still needed.

A website statement confirms what the site publishes, not that the claim is true. A public address does not establish Business Profile eligibility. A testimonial does not establish a general performance claim. When new information conflicts with an earlier approval, keep both, ask the responsible owner to resolve it, and continue the work that does not depend on it.

## Access is not authority

Record what can be seen separately from what may be changed.

| Asset | Record |
| --- | --- |
| Search Console, Analytics, Business Profile and exports | The exact property or profile, role or export, date, coverage and limits |
| CMS, theme, plugins and hosting | The environment, implementer, staging or backup, and restrictions |
| Measurement and commercial systems | The event or report owner, the lead or sales source and the approved data-sharing scope |
| Content and business facts | Who can supply proof, approve claims and approve the exact revision |
| Delivery actions | Existing authority for edits, redirects, tracking, plugins, profile changes and publishing, and what needs further approval |

Do not request passwords, recovery codes or customer data that is not needed. Use invitations, restricted records or redacted exports. Strategy approval is not approval for every implementation, and existing authorisation for routine work still stands.

## Evidence modes

| Mode | What can be assessed | What stays limited |
| --- | --- | --- |
| Public only | Visible pages, the customer journey, public listing details and dated search or competitor observations | Private performance, account status, actual leads, tracking configuration and Google's indexing or canonical choices |
| Public plus supplied exports | The above, plus the metrics and settings in the dated files | Missing dimensions, stale coverage, unknown configuration and any claim about the live account state |
| Authorised account evidence | Inspected properties, reports and settings, plus business records | Tracking errors, missing history, attribution limits, incomplete records and uninspected areas |

More access does not make every conclusion certain. A screenshot shows the view it captured, not the full history or configuration.

## Evidence labels

Give every source and statement one label, and keep the owner or provider, the exact asset, the collection date, period, timezone, filters and unit.

1. **Verified source statement**: what current primary documentation explicitly says, with its source ID.
2. **Observed finding**: what inspected site, account or business evidence shows.
3. **Sourced estimate**: a named tool's estimate, with its settings and date.
4. **Supported interpretation**: a conclusion tied to named observations.
5. **Recommendation**: a proposed choice, with its reasoning and uncertainty.
6. **Unknown**: what has not been established, and the next useful check.

A confident repair recommendation does not prove that the defect caused all lost traffic.

## Build the smallest useful baseline

| Area | Inspect or obtain when relevant | Record and route |
| --- | --- | --- |
| Business delivery | Current offers, capacity or stock, geographic scope, enquiry handling, known changes | Whether the business can meet the demand; unresolved commercial facts |
| Search exposure | Search Console clicks, impressions, CTR and position, sliced by page, query, country, device and search type | Exact filters, period and limits [S01, S02]; detailed query work goes to keyword research |
| Site acquisition and behaviour | Analytics source and medium, landing pages, meaningful journey events | The report definitions inspected and any configuration gaps |
| Customer outcomes | Enquiries, qualified leads, bookings, sales or another agreed outcome | The business source and its quality definition; missing attribution |
| Site and URL system | Relevant pages, their roles, discovery, indexability observations, templates and major technical risks | URL and page decisions go to page planning; defects go to technical diagnosis |
| Content and evidence | Intent fit, offer clarity, useful contribution, proof assets, factual gaps and upkeep | Whether accurate, useful content is feasible; evidence and briefing go to the content workflow |
| Local presence | Real locations or service coverage, Business Profile destinations and profile data | A location-level local audit |
| Structured data and AI features | Existing markup and its producer, or a specific AI feature question | A schema or AI-visibility check only when there is a reason |
| Reputation and links | Verified credentials, genuine reviews, recognition, important links and known incidents | A specific opportunity or risk question, never an invented authority score |

A public-only baseline must mark unavailable history explicitly. A new site starts with intended outcomes, technical readiness and a record that performance history is unavailable. Never manufacture an earlier performance period.

## Keep measures distinct

- Search Console measures search performance and Analytics measures interaction with the site. Clicks and sessions are different measures and will not match. Implementation, cookies or tracking, timezone, attribution, canonical URLs, traffic breakdowns, non-HTML pages and bot traffic can all contribute to the difference [S03].
- Search Console's default timezone is Pacific Time, while an Analytics property may use another [S03]. Record the time basis of each report and compare matching dates, countries, devices and search types.
- Search Console omits anonymised queries to protect privacy and keeps only the most important rows, so an absent query is not zero demand. Most page data is assigned to the canonical URL, and branded or non-branded classification can be wrong [S02]. Check canonical attribution before calling a page invisible, and record how brand groups were defined.
- Google Trends is sampled, normalised relative interest, not absolute search volume [S05]. Use it as context only.
- Keep Google organic distinct from all organic sources, all traffic or all channels when the distinction matters. An aggregate position or engagement rate is not a strategy result. Look at the important page and task segments.

## Outcomes

Analytics key events measure actions that are particularly important to the business. Conversions are created from events for advertising measurement and bidding [S04]. Name the report and definition actually used.

Record the real-world action, its event or report, the counting method, the channel scope and the quality checks. Keep these levels apart:

- Interaction, such as a click on a phone link or a form button.
- Recorded event, such as an Analytics key event. It shows what the tracking counted, not what happened next.
- Successful form submission: the form processed the entry and stored it where the form keeps entries.
- Notification delivery: the email or message reached its destination.
- Received enquiry: the business has it in its own records.
- Qualified lead or completed booking, confirmed by the business.
- Completed sale and verified revenue, where they apply.

A call-button click is not a connected call. An Analytics event does not by itself prove that a form was submitted, that a message was delivered, or that the enquiry was unique or useful. Do not claim a query produced a specific lead by joining aggregate Search Console and Analytics data. If attribution or lead quality is unavailable, say so and use a labelled provisional measure.

## When sources disagree

A gap between recorded events and business records is an observation to investigate, not a diagnosis. Do not conclude what an event records, or that its trigger is faulty, until its setup has been inspected. Before recommending any change, check:

- The event's definition, trigger and counting method.
- Duplicate firing, repeated or invalid submissions, and test submissions.
- Consent, filtering and reporting differences between the two sources.
- Form processing, stored entries, notification delivery and how the business records enquiries.
- Whether the two figures cover the same period, timezone, forms, pages and channels.

Record each possible cause as confirmed, ruled out or untested. Make any tracking or form configuration change conditional on a confirmed finding, with a test showing the change records what it should, and restore an earlier configuration only after checking it is suitable. Do not expect Analytics and business records to match exactly, because consent, deduplication and recording rules differ. Agree a tolerance and an explanation instead. Keep names, email addresses and phone numbers out of Analytics.

Business Profile performance includes activity from both organic results and Google Ads [S07]. Keep each metric's scope and do not report every profile interaction as unpaid SEO or a completed outcome.

## Periods and confounders

Choose a baseline period that suits the decision, the available history, seasonality and the sales cycle. A recent view and a longer comparison can both be useful. There is no single correct duration. Annotate migrations, outages, offer or stock changes, tracking or consent changes, releases, campaigns and relevant search incidents. An annotation is context, not evidence of cause.
