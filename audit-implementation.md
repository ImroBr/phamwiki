# Correction-guide implementation record

[Home](README.md) · [Foundations](foundations.md) · [FMEA](FMEA.md) · [FTA](FTA.md) · [ETA](ETA.md) · [STPA](STPA.md) · [Sources](sources.md)

**Revision:** 13 October 2026 draft. Independent technical review pending. Source-status checks are dated 6 October 2026; see [maintenance and limitations](review-guidance.md#maintenance-and-release).

Implements the correction guide of 6 October 2026 against base commit `ad41ab01d692fdc26e521f74ce0cf39eff85a1f0`. The original guides remain review inputs outside this repository. This record maps every finding to the reader-facing implementation; it does not assert independent technical approval.

The four method pages have been reorganized around purpose, inputs/outputs, steps, examples, limitations and references. The coordinated example replaces the old mixed examples. Earlier text/assets remain recoverable through Git history.

| Finding | Matter | Implementation | Disposition |
|---|---|---|---|
| R01 | Reframe Process Hazard Analysis | [README.md](README.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| R02 | Disambiguate PHA | [README.md](README.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| R03 | Repair the regulatory inference about FTA plus ETA | [README.md](README.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| R04 | Correct ALKS | [README.md](README.md) | Correct ALKS expansion in Home and standards register. |
| R05 | Correct the FTA name | [README.md](README.md) | Use Fault Tree Analysis consistently. |
| R06 | Separate analysis, evaluation and treatment | [README.md](README.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| R07 | Distinguish broad losses from regulatory safety scope | [README.md](README.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| R08 | Repair the future-methods taxonomy | [README.md](README.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| R09 | Make regulatory citations usable | [README.md](README.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| R10 | Editorial corrections and truthful status | [README.md](README.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M01 | Replace the incorrect FMECA/RPN instruction | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M02 | Replace the criticality glossary entry | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M03 | Replace the introduction | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M04 | Replace the three-category failure-mode taxonomy | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M05 | Replace the flat-tire severity scale | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M06 | Correct occurrence, detection and RPN interpretation | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M07 | Separate analysis variants and control types | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M08 | Remove color-based acceptance implications | [FMEA.md](FMEA.md) | Remove colored RPN screenshots; explicit action/evidence state replaces acceptance colors. |
| M09 | Trace effects before comparing severities | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M10 | Make the human/fallback role explicit | [FMEA.md](FMEA.md) | Replace driver-dependent rows with driverless scope and functions. |
| M11 | Do not imply unverified residual improvement | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M12 | Separate baseline controls from actions | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M13 | Qualify limitations concerning interfaces and time | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M14 | Correct AIAG & VDA edition and AP scope | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M15 | Add FMEA-MSR and handle AFMEA | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M16 | Replace the loose glossary definitions | [FMEA.md](FMEA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| M17 | Repair the downloadable workbook mismatch | [FMEA.md](FMEA.md) | Replace older XLS with matching qualitative template/worked-example workbook. |
| M18 | Repair history, headings and links | [FMEA.md](FMEA.md) | Replace unsupported history; retire screenshots and rebuild valid headings/links. |
| T01 | Correct the starting point | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T02 | Correct the gate-probability table | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T03 | Replace the failure-frequency paragraph | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T04 | Define the exponential model correctly | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T05 | Define a top event, not automatically a hazard | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T06 | Correct intermediate-event semantics | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T07 | Correct stopping-point definitions | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T08 | Add Boolean reduction and repeated-event handling | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T09 | Replace the mixed “ten variations” list | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T10 | Replace DPMO and unrelated criticality material | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T11 | Correct redundancy and acceptance guidance | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T12 | Repair the introductory traffic-accident figure | [FTA.md](FTA.md) | Remove historical percentage image; retain source link and explanation of non-applicability. |
| T13 | Complete the A–E worked example | [FTA.md](FTA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| T14 | Clarify gate semantics and repair anchors | [FTA.md](FTA.md) | Define gates and events in linkable sections; use a newly authored labeled diagram. |
| E01 | Define what the initiating event includes | [ETA.md](ETA.md) | Encounter includes detection; new conditional tree covers all defined stages. |
| E02 | Resolve braking after a failed decision | [ETA.md](ETA.md) | Failed demand terminates path; no unspecified fallback is credited. |
| E03 | Correct the pathway-d image | [ETA.md](ETA.md) | Retire inconsistent pathway-d screenshot; replace entire diagram and table together. |
| E04 | Explain conditioning rather than IE=1 | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E05 | Separate path probability and risk | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E06 | Normalize each branching point | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E07 | Qualify the binary-model limitation | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E08 | Correct the outcome count | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E09 | Replace barrier-count ranking | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E10 | Clarify bow-tie and FTA integration | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E11 | Reconcile causal and chronological ordering | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E12 | Replace imprecise ETA glossary entries | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E13 | Repair the probability-data guidance | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E14 | Add the main ETA standard | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| E15 | Remove unfinished and overprecise history text | [ETA.md](ETA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| S01 | Correct STAMP consistently | [STPA.md](STPA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| S02 | Reclassify CAST | [STPA.md](STPA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| S03 | Correct the environment/boundary explanation | [STPA.md](STPA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| S04 | Replace the context-free highway-braking example | [STPA.md](STPA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| S05 | Correct the excessive-braking UCA category | [STPA.md](STPA.md) | Replace mixed aircraft table with correctly categorized vehicle UCAs. |
| S06 | Correct timing versus duration | [STPA.md](STPA.md) | Separate late action from early termination in new vehicle UCAs. |
| S07 | Relabel the context table and add a scenario | [STPA.md](STPA.md) | Explain context-table limits; provide causal LS-01 and LS-02. |
| S08 | Resolve undefined H-4 without inventing its meaning | [STPA.md](STPA.md) | Remove undefined H-4 excerpt; replace with complete local hazard IDs. |
| S09 | Separate source identifiers from local identifiers | [STPA.md](STPA.md) | Replace unrelated source examples with one local example; link source context separately. |
| S10 | Repair hazard-state descriptions with clear boundaries | [STPA.md](STPA.md) | New scope, losses, hazardous conditions and traceable downstream IDs. |
| S11 | Replace the confused feedback bullets | [STPA.md](STPA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| S12 | Qualify completeness and modeling claims | [STPA.md](STPA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| S13 | Replace unsupported resource-scarcity claims | [STPA.md](STPA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| S14 | Add end-to-end traceability | [STPA.md](STPA.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| S15 | Repair STPA references and typographical errors | [STPA.md](STPA.md) | Correct references and rebuild headings/links; printed p. 51 citation retained. |
| X1 | Common scope and design assumptions | [automotive-example.md](automotive-example.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| X2 | Replacement FMEA example | [automotive-example.md](automotive-example.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| X3 | Replacement ETA example and figure | [automotive-example.md](automotive-example.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| X4 | Replacement STPA worked example | [automotive-example.md](automotive-example.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| X5 | Relate the methods without claiming equivalence | [automotive-example.md](automotive-example.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| G01 | Give bibliography checkboxes an unambiguous meaning | [sources.md](sources.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| G02 | Standardize bibliography records | [sources.md](sources.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| G03 | Add critical interpretation to comparison papers | [sources.md](sources.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| G04 | Repair references that are only local filenames | [sources.md](sources.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| G05 | Replace search-hit counts with a useful method-selection table | [method-comparison.md](method-comparison.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| G06 | Expand the authoring template | [PHA_template.md](PHA_template.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| G07 | Isolate development files and fix their small errors | [development/advanced_formatting_testing.md](development/advanced_formatting_testing.md) | Move formatting experiments into development; label incomplete examples. |
| G08 | Make examples selectable and keep assets synchronized | [automotive-example.md](automotive-example.md) | Replace screenshots with selectable Markdown tables and maintained Mermaid source. |
| G09 | Repair source and reuse attribution | [references.md](references.md) | Remove former raster reproductions; use source links and original diagrams; no new license asserted. |
| G10 | Add reliable navigation and structure | [README.md](README.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| G11 | Add honest review metadata | [review-guidance.md](review-guidance.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| A01 | Shared terminology with framework boundaries | [foundations.md](foundations.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| A02 | Add an introductory automotive HARA page | [automotive-context.md](automotive-context.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| A03 | Map complementary safety disciplines | [automotive-context.md](automotive-context.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| A04 | Add an assessor-oriented checklist | [review-guidance.md](review-guidance.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| A05 | Add a method-reconciliation and acceptance section | [review-guidance.md](review-guidance.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| A06 | Supply short introductions for future methods | [related-methods.md](related-methods.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| A07 | Add a cybersecurity-to-safety interface example | [automotive-context.md](automotive-context.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| A08 | Implement the information architecture and release criteria | [README.md](README.md) | Replacement guidance applied in the linked page; shared examples and references linked where relevant. |
| U01 | EU 2022/1426 | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U02 | Method-selection clause | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U03 | UN R157 | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U04 | AIAG & VDA | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U05 | SAE J1739 | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U06 | IEC 60812 | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U07 | IEC/NEN 61025 | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U08 | IEC 31010 | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U09 | IEC 62502 | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U10 | ISO 26262 | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U11 | MIL-STD-1629A | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U12 | SAE ARP5580 | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U13 | BS 5760-5 | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U14 | STPA age/resources | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |
| U15 | Fictional action dates | [Standards register](standards-register.md) | Dated status/scope entry; unresolved applicability remains explicit. |


## Validation and remaining review

Local Markdown links and anchors, table structure, guide-ID coverage, numerical FTA/ETA examples, stopping-distance arithmetic and workbook/example alignment are checked for this draft. The workbook is visually reviewed. Independent domain review remains pending. Paid normative text, full applicability of UN R157 amendments and empirical vehicle performance are not claimed to have been verified. Reference status retains the original 6 October 2026 check boundary.

Draft pull-request review should concentrate on the revised technical explanations, scope of the shared example, publication/applicability boundaries and any useful original content that needs expansion.
