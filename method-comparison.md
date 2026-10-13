# Comparing analysis questions

[Home](README.md) · [Foundations](foundations.md) · [FMEA](FMEA.md) · [FTA](FTA.md) · [ETA](ETA.md) · [STPA](STPA.md) · [Sources](sources.md)

**Revision:** 13 October 2026 draft. Independent technical review pending. Source-status checks are dated 6 October 2026; see [maintenance and limitations](review-guidance.md#maintenance-and-release).

Search-engine result counts are not used here to rank methods. Counts depend on the query, date, search service and ambiguity of abbreviations; they do not measure completeness, effectiveness or suitability for a particular safety assessment.

| Method | Main question | Typical inputs | Typical outputs | Important limitation |
|---|---|---|---|---|
| [FMEA](FMEA.md) | How can the selected functions/items fail, and with what effects? | Functions, architecture or process steps and analysis boundary. | Failure modes, causes, effects, controls and actions. | Conventional single-failure analysis can miss hazardous combinations or emergent interactions. |
| [FTA](FTA.md) | Which combinations can produce the defined top event? | Top event, system model and logical relationships. | Fault tree, cut sets and conditional quantitative results where justified. | Results depend on event definitions, model coverage, dependencies and data. |
| [ETA](ETA.md) | What developments can follow the selected initiating event? | Initiating event, responses/conditions and conditional probabilities if quantified. | Paths, end states and conditional probabilities/frequencies. | Events outside the selected initiating-event/model scope are not automatically covered. |
| [STPA](STPA.md) | How can control and feedback permit hazardous system behavior? | Losses, hazards, responsibilities and control structure. | UCAs, constraints, causal scenarios and measures. | Scope, abstraction and analyst judgment affect coverage; the method alone is not quantitative risk acceptance. |

Choose and combine methods according to the questions that need answering. Record uncovered issues explicitly rather than selecting a method because it has more search results.
