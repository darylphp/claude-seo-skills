# Decline Output

Synthetic case. A dog grooming salon reports: "Our website leads are down about 40% since September. Which Google update hit us? We need a new strategy." Supplied: an Analytics key event export for June to October 2026 showing fewer `booking_request` events from September, a note that the site moved to a new theme on 12 Sep 2026, and a note that a cookie consent banner was added on 15 Sep 2026. No Search Console access, no booking-system records and no list of changed URLs.

Sections 4 to 9 are shortened here to show the routing.

## 1. Strategy conclusion and status

- Status: Diagnose before prioritising
- The drop is recorded in Analytics events, not in bookings, and two site changes landed in the same fortnight. A consent banner can change what Analytics records, and a theme change can affect pages, forms and tracking. A Google update is one possible explanation among several, and timing alone does not show which one applies [S14]. Rewriting the strategy before the cause is narrowed down would risk fixing the wrong thing.
- Provisional priorities that do not depend on the cause: test the booking form end to end on the new theme, and compare booking-system requests with the Analytics events for the same months, timezone and pages. Any tracking change waits for a confirmed finding.
- Recommended urgent handoff: none yet. If a booking form test fails, recommend it for immediate diagnosis and repair.

Approval state: Proposed

This pack does not itself grant implementation authority.

## 2. Business and scope record

Dog grooming salon, name and market not supplied. Outcome: booking requests. Confirmation needed: the salon's identity, location and the booking system used.

## 3. Access and evidence coverage

Mode: supplied exports only. Analytics key events, Observed finding as exported, period June to October 2026, property timezone not supplied. Not inspected: Search Console, the booking system, the live site, the consent setup and the theme migration's URL changes.

## 4. Dated baseline

Recorded events fell from September (Analytics). Bookings: `Not available`. Search exposure: `Not available`.

| Competing explanation | Evidence for | Check that would separate it |
| --- | --- | --- |
| Consent banner reduced recorded events | Banner added 15 Sep | Compare booking-system requests with events for June to October |
| Theme change broke a form or page | Theme moved 12 Sep | Test the booking form; compare old and new page URLs and responses |
| Search exposure fell | None yet | Search Console clicks and impressions for the same periods, by page |
| Seasonality | None yet | The same months in 2025, if records exist |
| Algorithmic update | None yet | Only after the checks above, with dated Search Console evidence |

## 5. Competitor context

Deferred until the diagnosis narrows the cause.

## 6. Opportunity register

Deferred until the diagnosis narrows the cause.

## 7. Priorities and trade-offs

Deferred until the diagnosis narrows the cause.

## 8. Staged plan

Deferred until the diagnosis narrows the cause.

## 9. Handoffs

```text
Task and opportunity ID: Diagnose the September decline (O1)
Recommended handoff to: technical diagnosis
Bounded question: did bookings fall, or only recorded events, and did the 12 Sep theme change alter pages, forms or URLs?
Existing authorisation, approval and work state: none supplied; Recommended
Acceptance check: a dated finding for each explanation in section 4, with confidence
```

## 10. Open items and review

Search Console access, booking-system records for June to October 2026 and a list of URLs changed by the theme move. The strategy resumes once diagnosis reports.
