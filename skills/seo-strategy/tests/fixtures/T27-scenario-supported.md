# Fixture T27: scenario supported

Synthetic case. Ridgeway Joinery, its site, people, figures and dates are invented. They are not a real business or real search data.

## Request

"We want more wardrobe jobs this summer. Where should SEO focus first? Before I use the 6 booked contractor hours on the `/wardrobes/` improvement, build a bounded scenario of what it could mean for qualified wardrobe requests over the six months after release (December 2026 to May 2027), so I can decide whether it is worth doing now."

## Business record

Supplied by the owner on 18 Nov 2026. Items marked approved were approved by the owner on the date shown.

- Ridgeway Joinery, `https://ridgewayjoinery.example/`, a custom joinery workshop in Moonah, Hobart, Tasmania. The owner and two cabinetmakers.
- Offers: custom kitchens, built-in wardrobes and laundry cabinetry. Not offered: flat-pack, door-only replacements, bathroom renovations, commercial fit-outs.
- Capacity: kitchens are booked about 10 weeks ahead. Wardrobes have spare capacity for about 4 more jobs a month.
- Coverage: installs within about 40 minutes' drive of the workshop.
- Audience: homeowners renovating or building.
- Outcome: qualified quote requests, marked by the owner in the quote log.
- Delivery: WordPress with a page builder. The web contractor edits pages and has standing authority to publish a page revision once the owner has approved that exact revision.
- Approved on 15 Nov 2026: improve the existing `/wardrobes/` page by adding the approved price ranges, the design and install process, current lead times and photos of past jobs. No new URL. The contractor builds it and the owner approves the final revision before it goes live.
- Approved on 15 Nov 2026: the price-range wording for new built-in wardrobes, for publication.
- Approved on 15 Nov 2026: 14 wardrobe job photos for publication. Signed client permissions are held by the owner.
- Contractor capacity: 6 hours booked for 1 to 5 Dec 2026 (contractor's confirmation, 16 Nov 2026).
- Dependency: the wardrobe form fault was repaired by the contractor on 8 Nov 2026. On 10 Nov 2026 test submissions from the wardrobe, kitchen and contact forms were stored, their notifications arrived, and each appears in E3 (contractor's and owner's records).
- Acceptance checks agreed by the owner on 15 Nov 2026: the approved revision is live at `/wardrobes/` with the correct prices and photos on mobile and desktop; the page stays self-canonical and indexable; a test submission from the page arrives and is logged; an outcome review six weeks after release compares qualified wardrobe requests in E3 and Search Console data for `/wardrobes/` with the same weeks last year.

## Sources

| ID | Source | Period and settings |
| --- | --- | --- |
| E1 | Search Console query and page export, domain property, web search, all rows via bulk export | 1 Jul 2025 to 31 Oct 2026, exported 12 Nov 2026 |
| E3 | Owner's quote request log | 1 Aug to 31 Oct 2026 |
| E5 | Saved HTML of `/wardrobes/` | 12 Nov 2026 |
| E6 | 22 anonymised call notes about wardrobes | Aug to Oct 2026 |
| E7 | Result observations for three representative queries, desktop and mobile, location set to Hobart, manual check by the user | 12 Nov 2026 |

## Figures as supplied

- E1: every wardrobe-related query in the full export is about new built-in or walk-in wardrobes ("built in wardrobes hobart", "custom wardrobes hobart", "walk in wardrobe cost hobart"). There are no door-only or repair queries. Together: 2,140 impressions and 38 clicks, mostly attributed to the home page. The `/wardrobes/` page row: 610 impressions, 9 clicks.
- E3: 31 quote requests, 22 qualified. Wardrobe requests: 7, all for new wardrobes.
- E5: `/wardrobes/` has about 120 words and no photos, prices, process or lead times.
- E6: the most common questions were the price of new built-in wardrobes (9), lead times (7) and sliding compared with hinged doors (5).
- E7: for all three queries, the first results were local joinery or wardrobe businesses' service pages with project photos, price guidance and a description of the process.

## Scenario inputs

All values are synthetic and supplied for this case. Labels show where each came from.

| ID | Input | Values | Source and label |
| --- | --- | --- | --- |
| I1 | Google organic landing sessions on `/wardrobes/`, same months last year | Dec 2025: 110, Jan 2026: 125, Feb 2026: 118, Mar 2026: 102, Apr 2026: 94, May 2026: 88 | Analytics export, session source google / organic, landing page `/wardrobes/`, property timezone Australia/Hobart. Observed. Landing page and source dimensions checked by the contractor on 10 Nov 2026 |
| I1b | The same sessions, recent months and a year earlier | Jun to Oct 2026: 92, 101, 95, 104, 98. Jun to Oct 2025: 90, 99, 97, 101, 95 | Same export. Observed |
| I2 | Qualified wardrobe enquiries from those sessions | Nov 2025 to Jul 2026: 26 qualified enquiries from 870 landing sessions. Monthly rates ranged from 2.0% to 4.1% | Stored form entries record landing page and source; matched to E3 qualified flags by the owner and contractor on 10 Nov 2026. Observed |
| I3 | Comparable page: `/laundries/` was improved on 3 Mar 2026 with the same kind of changes (approved price ranges, process, lead times, photos) | Google organic landing sessions. Before, Dec 2025 to Feb 2026: 41, 46, 52. After, Apr to Jun 2026: 58, 66, 71. A year earlier, Dec 2024 to Feb 2025: 44, 47, 50, and Apr to Jun 2025: 45, 49, 52. March is excluded as the release month. Qualified laundry enquiries: 3 before, 6 after | Same export and log. Observed. One page, one release, small enquiry counts |
| I4 | Quote and job conversion | Every qualified enquiry receives a quote (approved process). 2025 wardrobe quotes: 40, jobs won: 11 | Owner's job book, 1 Jan to 31 Dec 2025. Observed |
| I5 | Wardrobe job values | 11 jobs in 2025, from A$2,800 to A$9,500, median A$5,200 | Owner's job book. Observed. Revenue, not margin. The owner declines to share margin |
| I6 | Cost of the change | Contractor: 6 hours at A$95 an hour, A$570. Owner time: about 5 hours, not costed | Contractor quote, 16 Nov 2026. Supplied |
| I7 | Release timing | Planned release 5 Dec 2026 | Contractor booking. Supplied |
