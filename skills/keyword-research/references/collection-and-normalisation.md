# Collection and Normalisation

IDs in brackets refer to the [source register](source-register.md).

## 1. Use the available evidence first

Work through the sources in this order and stop asking for more when a smaller set answers the question.

1. Approved business information, offer and inventory boundaries, and known customer tasks.
2. Relevant Search Console queries and page signals, with the export settings.
3. Site search, sales and support questions, CRM notes and real objections, where authorised.
4. Named keyword-tool exports for the correct market.
5. Dated search results, suggestions, related questions and public terminology.
6. Authoritative entity, product or technical sources for factual concepts and attributes.
7. Inferred additions, clearly marked as awaiting validation.

Identical wording in two datasets does not make their metrics interchangeable. Keep both source records.

## 2. Expansion lenses

| Lens | Investigate | Guardrail |
| --- | --- | --- |
| Offer or category | What is actually sold, provided or supported | Do not invent adjacent services or inventory |
| Problem or outcome | The situation that prompts the search | A plausible problem stays a candidate until supported |
| Comparison or choice | Alternatives, suitability, exclusions and trade-offs | Do not invent testing or differences |
| Cost or terms | Price drivers, eligibility, delivery, guarantees | Do not infer the business's terms from competitors |
| Process or use | Installation, implementation, maintenance, compatibility, troubleshooting | Keep buyer needs apart from support needs |
| Audience | Role, expertise, business type, constraints | A new modifier does not automatically mean a new task |
| Geography or urgency | Real coverage, availability, time-sensitive needs | No automatic town permutations |
| Evidence | What proof a responsible decision needs | A claim without proof is a research gap |

Explore meaningful combinations only. Do not generate every modifier, product and town permutation. Stop when new sources mostly add existing variants, unsupported terms or out-of-scope tasks.

**Google guidance [K01, K07]:** readers use different words for the same thing, and Google's language systems can relate a page to queries it does not repeat word for word. Creating content for every variation, including AI fan-out queries, mainly to manipulate rankings breaches the scaled content abuse policy. Breadth in research supports understanding. It is not a list of phrases to insert or pages to make.

## 3. Normalise without losing meaning

Keep the original query and source row unchanged, and work on a separate normalised form. Fix case, spacing and punctuation. Correct spelling only when the meaning is clear, and record the correction.

Do not collapse a modifier that can change geography, urgency, product class, brand, audience, regulation, compatibility, the expected result or the next action. Singular and plural forms and close synonyms can share a family when the task aligns. Check for exceptions.

### Raw record

```text
Row ID / original query / normalised working query
Evidence status / source ID / file or URL / period or date
Country or region / language / device / filters
Provider-labelled metrics and units / missing-value status
Observed existing URL signal, if any
Provisional family ID / secondary tags
Ambiguity, exclusion or normalisation note
```

A query can support more than one interpretation. Use a secondary tag or an ambiguity note rather than copying its metrics into several families without saying so.
