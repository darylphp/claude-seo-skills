# Urgent Output

Synthetic example. The business, people, URLs, records and observations are fictional.

**Input summary.** Hana Lee owns Fernhill Nursery, an online plant shop at `https://fernhill-nursery.example/`. A redesigned site went live on 24 Nov 2026 with the same URLs, built by Brightline Dev. On 26 Nov she wrote: "No web orders since the new site launched. Should we roll the whole thing back?" She supplied:

- **U-E1** (26 Nov 2026): terminal output from Brightline Dev for the home page and `/plants/monstera-deliciosa/`, both `HTTP/2 200` with the header `x-robots-tag: noindex, nofollow`.
- **U-E2** (26 Nov 2026): the live robots.txt, which contains `User-agent: *` and `Disallow: /`.
- **U-E3** (26 Nov 2026): a screen recording showing the checkout button posting to `https://staging.fernhill-nursery.example/checkout/`, which returns 401.
- **U-E4** (26 Nov 2026): shop records showing 0 web orders from 24 to 26 Nov, against 9 to 17 a day in the previous 4 weeks.
- **U-E5**: Brightline Dev's agreement lets it fix launch defects without separate approval. Hana approves anything else.

## 1. Status and conclusion

**Escalate first: Urgent defect**

The new site went live with staging controls in place. Every inspected page sends a noindex header, robots.txt blocks all crawling, and checkout posts to the protected staging host, so no customer can complete an order. Both defects need fixing now at their producers. A full rollback is not needed to fix them and carries its own risk, so it should only be considered if the targeted fix fails.

Site: `https://fernhill-nursery.example/`. Audit date 27 Nov 2026, evidence cut-off 26 Nov 2026. Evidence basis: supplied terminal output, robots.txt, a screen recording and shop records. No page was fetched in this audit. Main limitation: only two URLs' headers were supplied, and Search Console data for the days since launch was not supplied.

Implementation approval: Awaiting approval

This report does not itself grant implementation authority.

## 2. Case record

- **Site:** online plant shop, redesigned on the same URLs, live since 24 Nov 2026. CMS and hosting: not supplied.
- **Objective:** web orders.
- **Symptom:** no web orders since launch (U-E4).
- **Intended state:** product, category and information pages public and indexed; checkout on the production host.
- **Change history:** the redesign launch on 24 Nov 2026.
- **Ownership and authority:** Hana Lee owns the site. Brightline Dev implements and may fix launch defects under its agreement (U-E5).

## 3. Evidence and access

| ID | Source | What it showed | Date | Collection conditions | Label | Limits |
| --- | --- | --- | --- | --- | --- | --- |
| U-E1 | Response headers | `x-robots-tag: noindex, nofollow` on two pages returning 200 | 26 Nov 2026 | Developer's terminal | Supplied | Two URLs only |
| U-E2 | robots.txt | `Disallow: /` for all user agents | 26 Nov 2026 | Live file, as supplied | Supplied | None noted |
| U-E3 | Screen recording | Checkout posts to the staging host, which returns 401 | 26 Nov 2026 | Owner's browser | Supplied | One browser session |
| U-E4 | Shop records | 0 web orders from 24 to 26 Nov; 9 to 17 a day before | 26 Nov 2026 | Owner's records | Supplied | Three days after launch |

Not verified: headers on other templates; redirects and status codes across the old URL set; canonicals, internal links and structured data on the new templates; Search Console data since launch.

## 4. Measurement check

Web orders fell from 9 to 17 a day to 0 (U-E4). Search Console data for the days since launch was not supplied, and three days is too short to measure a Search effect. Orders are used here only to show that the purchase path is broken.

## 5. Urgent defects

- **U1. Site-wide noindex and crawl block.** The noindex header appears on both pages checked, and robots.txt blocks all crawling, so Google cannot fetch the new pages [D07]. The header has to go in the same fix, or pages would drop out of the index as soon as crawling resumes [D08]. Owner: Brightline Dev, under its launch-defect authority. Containment: replace production robots.txt with the approved production version and remove the noindex header from production responses at its producer (server, CDN or CMS setting). Do not delete or noindex anything else while fixing it, and do not request indexing until the fix is verified. Acceptance: see A1.
- **U2. Checkout posts to staging.** The purchase path fails for every customer (U-E3, U-E4). Owner: Brightline Dev. Containment: point checkout at the production endpoint and confirm payment and order notification on production with a test the owner authorises. Acceptance: see A2.

## 6. Findings

| ID | Area | URL, template or pattern | Observed | Intended | Evidence label and confidence in the defect | Producer |
| --- | --- | --- | --- | --- | --- | --- |
| F1 | Crawl and indexing controls | Whole site (2 URLs inspected) | Noindex header; `Disallow: /` | Indexable, crawlable | Supplied (U-E1, U-E2). High | Producer not identified. Likely staging configuration carried into production |
| F2 | Customer path | Checkout | Posts to staging, which returns 401 | Production checkout | Supplied (U-E3, U-E4). High | Producer not identified. Checkout endpoint configuration |

Other redesign checks are Deferred until U1 and U2 are verified.

## 7. Explanations for the symptom

| Explanation | Evidence for | Evidence against | Confidence in the cause | Share of the change it could explain | Next check |
| --- | --- | --- | --- | --- | --- |
| X1. Broken checkout | Checkout posts to a host that refuses it; orders stopped at launch | None | High | All of the web order loss is consistent with it; exact share Not established | Order flow after A2 |
| X2. Lost Search traffic from the noindex and crawl block | The controls are present | Too soon after launch to see a Search effect; no Search Console data supplied | Not established | Not established | Performance and Page indexing data from 24 Nov, once available |

## 8. Prioritised actions

| ID | Finding | Priority | Smallest action | Producer and owner | Authority (existing or needed) | Dependencies and recovery | Production acceptance check | Work state | Outcome measure and review trigger |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| A1 | F1 | Urgent | Restore production robots.txt and remove the noindex header at its producer | Brightline Dev | Existing: launch-defect agreement (U-E5) | Keep the current files for reference; change only the staging controls | robots.txt no longer contains `Disallow: /` and matches the approved production rules; home, a category, a product and an information page return 200 without noindex in headers or HTML, checked uncached; checkout, account and cart keep any intended exclusions | Proposed | Page indexing and Performance reports from 24 Nov, reviewed weekly until indexed coverage of key pages is confirmed |
| A2 | F2 | Urgent | Point checkout at the production endpoint | Brightline Dev | Existing: launch-defect agreement (U-E5). A real-payment test needs Hana's authorisation | Confirm payment and order notification settings on production | An owner-authorised test order completes on production, the order reaches the shop records and the notification arrives | Proposed | Daily web orders against the previous 4 weeks |
| A3 | Deferred checks | Planned | After A1 and A2 are verified, compare old and new templates on status, redirects, canonicals, internal links and structured data | Brightline Dev with Hana Lee | Needed: Hana's approval for any change beyond launch defects | None | Not applicable until scoped | Proposed | Not applicable |

A full rollback is not recommended now. If the targeted fixes fail, consider it only after a diagnosis, with a backup or recovery point, a compatibility check, Hana's authority, and protection for any orders or customer records created since launch.

## 9. Developer handoffs

```text
Action ID and URL, template or pattern: A1. Whole production site.
Reproducible problem and current output: x-robots-tag: noindex, nofollow on 200 responses (home, /plants/monstera-deliciosa/); robots.txt Disallow: / for all user agents.
Intended output and affected scope: No noindex on public pages; production robots.txt rules.
Producer to change (or how to find it): Not identified. Check server, CDN and CMS settings carried over from staging.
Approved or authorised change, and restrictions: Launch-defect agreement. No content or URL changes.
Cases that must pass: Home, a category, a product and an information page return 200 with no noindex, uncached.
Cases that must stay unaffected: Intended exclusions on checkout, account and cart. Staging stays behind authentication.
Recovery method: Current production files kept for reference.
Who verifies production, and how: Hana Lee, with a header check and a URL Inspection live test of the home page.

Action ID and URL, template or pattern: A2. Checkout.
Reproducible problem and current output: Checkout posts to https://staging.fernhill-nursery.example/checkout/, which returns 401.
Intended output and affected scope: Checkout on the production host.
Producer to change (or how to find it): Checkout endpoint configuration.
Approved or authorised change, and restrictions: Launch-defect agreement. A real-payment test needs Hana's authorisation.
Cases that must pass: An authorised test order completes and reaches the shop records; the notification arrives.
Cases that must stay unaffected: Payment provider settings other than the endpoint; staging authentication.
Recovery method: Previous endpoint setting noted before the change.
Who verifies production, and how: Hana Lee, with the authorised test order.
```

## 10. Open items and routes

- Producers of the noindex header and the staging checkout setting: Brightline Dev.
- Headers on other templates, and the redirect and template comparison: after A1 and A2 (A3).
- Search Console data since launch: Hana Lee, once available.
- Work states: A1 to A3 are Proposed. Nothing is reported as fixed.
