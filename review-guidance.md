# Reviewing analyses and maintaining the Wiki

[Home](README.md) · [Foundations](foundations.md) · [FMEA](FMEA.md) · [FTA](FTA.md) · [ETA](ETA.md) · [STPA](STPA.md) · [Sources](sources.md)

**Revision:** 13 October 2026 draft. Independent technical review pending. Source-status checks are dated 6 October 2026; see [maintenance and limitations](review-guidance.md#maintenance-and-release).

| Review area | Question | Evidence to look for |
|---|---|---|
| Scope | Which configuration, functions, operating modes and conditions are included or excluded? | Defined boundary, version and assumptions. |
| Method suitability | Why does this method answer the required question, and what remains outside its capability? | Method/variant choice and complementary analyses. |
| Model quality | Are events, effects, contexts and causal relationships defined consistently? | Reviewable diagrams, tables and event/term definitions. |
| Dependencies | Are shared causes, timing, feedback and relevant human/external roles addressed? | Dependence analysis and explicit model assumptions. |
| Data | Do estimates represent the quantity and operating conditions being analyzed? | Sources, units, uncertainty and applicability justification. |
| Traceability | Can important findings be followed into measures and requirements? | Stable IDs and links to design provisions. |
| Verification | Has the implemented measure been tested against the claimed effect? | Configuration-specific results and acceptance criteria. |
| Residual issues | What remains unproven or unacceptable, and who owns the decision? | Open issues, action owners and recorded acceptance rationale. |
| Change control | What changes would invalidate the analysis or trigger reassessment? | Update rules for design, software, ODD and source changes. |

These are review prompts, not a replacement for an applicable legal or organizational assessment procedure. For the EU ADS context, connect them to the actual coverage and validation requirements rather than treating completion of this table as compliance. [B03](references.md#b03)

## Combining results and accepting risk

Before transferring an event or probability between methods, check that its physical meaning, boundary, operating mode, reference period and conditioning assumptions match. Record discrepancies explicitly. A failure mode may contribute to several hazards, and a hazard may arise without that failure mode.

| Record | Required content |
|---|---|
| Finding | Source method, identifier and precise statement. |
| Related findings | Linked events, hazards, UCAs or scenarios in other analyses. |
| Compatibility check | Agreement or difference in scope, conditions, timing and quantities. |
| Measure | Required design behavior or constraint and responsible owner. |
| Evidence | What demonstrates implementation and effectiveness. |
| Decision | Accepted, action required or unresolved, with basis and authority. |

Acceptance is a decision supported by evidence and the applicable criteria. It must not be inferred merely from a completed worksheet, a green cell, a low RPN or a small top-event estimate. [The shared example](automotive-example.md#reconciling-the-methods) demonstrates a coverage mismatch: restart hazards identified by FMEA/STPA are outside the stopping ETA.

## Maintenance and release

| Field | Draft status |
|---|---|
| Content version | Correction-guide implementation, 13 October 2026. |
| Independent technical review | Not yet completed. |
| Editorial review | Local link/anchor checks, table checks and example calculations performed for this draft; see the implementation record. |
| Reference-status check | 6 October 2026, publications listed in the standards and reference registers. |
| Known limitations | Paid normative clauses were not fully inspected; UN R157 applicability remains case-specific; examples use invented values and proposed verification. |
| Change triggers | Design, software, ODD, regulation/standard edition, source corrections or newly identified errors. |

A revision is ready for release when priority corrections agree across prose, tables, figures and downloads; links and references have been checked; and the scope of technical review is recorded. A commit date does not establish technical validation.

Use the [authoring template](PHA_template.md) for new method pages. Keep history after the practical explanation. Preserve stable IDs and update cross-links when headings change. Diagrams must have maintained source and adjacent readable tables where numerical results are involved.

For reused figures, record author, title, figure/page, source, exact license or permission basis, and changes made. A source citation does not itself establish reuse permission. When the reuse basis is unresolved, link to the source instead of embedding the figure.
