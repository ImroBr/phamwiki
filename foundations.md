# Foundations: scope and terminology

[Home](README.md) · [Foundations](foundations.md) · [FMEA](FMEA.md) · [FTA](FTA.md) · [ETA](ETA.md) · [STPA](STPA.md) · [Sources](sources.md)

**Revision:** 13 October 2026 draft. Independent technical review pending. Source-status checks are dated 6 October 2026; see [maintenance and limitations](review-guidance.md#maintenance-and-release).

**The abbreviation PHA has more than one meaning.** In process safety it commonly means Process Hazard Analysis. In system-safety work it can also mean Preliminary Hazard Analysis: an early examination of hazards, possible consequences and candidate controls, undertaken while the design is still developing. This Wiki spells out the intended meaning wherever the abbreviation would be ambiguous.

Hazard analysis identifies hazardous system conditions and examines how they could arise or lead to harm. Depending on its purpose, it may produce qualitative findings, causal models, constraints, failure-effect descriptions or quantitative estimates. Not every hazard-analysis method requires a numerical likelihood estimate.

Risk analysis develops an understanding of risk; risk evaluation compares the results with stated decision criteria. Risk treatment selects and implements measures to change the risk. An analysis supports risk reduction, but the analysis alone does not implement or verify a safety measure. [B16](references.md#b16)

The concerns included in an analysis depend on its purpose. An automotive safety assessment may focus on harm to people, while a broader organizational or STPA study may also consider unacceptable losses involving property, mission, privacy or reputation. These concerns should be recorded separately where they require different acceptance criteria. A loss included in one framework is not automatically a safety hazard or approval requirement in another. State which definition and scope are used before comparing results.

## Terms and framework boundaries

The descriptions below explain how this Wiki uses terms. They are paraphrases for navigation, not replacement normative definitions. Identify the governing framework when performing an actual analysis, particularly where the same word has different scope.

| Term | Explanatory description and boundary |
|---|---|
| Harm | Injury or damage to the interests protected by the selected framework. In a particular automotive functional-safety assessment, use that framework’s specific scope rather than assuming every business loss is included. |
| Loss in STPA | An outcome stakeholders judge unacceptable, such as injury, property damage or mission loss. State the selected losses explicitly. |
| Hazard | A condition with the potential to contribute to harm; use the selected framework’s definition. In STPA, relate a hazardous system condition to losses and relevant environmental conditions. |
| Hazardous event in automotive HARA | A hazard considered together with an operational situation; it is not merely the name of a failed component. |
| Fault / failure / failure mode | Distinguish a contributing condition or defect, loss of required function, and the manner of that functional failure. See the method-specific glossary. |
| Risk | The possibility and consequences of adverse outcomes, characterized using the chosen framework. An RPN or AP classification is not automatically a calibrated risk measure. |
| Safety goal in ISO 26262 context | A high-level safety requirement resulting from HARA; its classification and derivation follow the applicable procedure. |
| Safety constraint in STPA | A required restriction on system/controller behavior to prevent the identified hazardous behavior. |
| Residual risk | Risk remaining after the measures actually credited in the assessment. Planned but unverified measures must be distinguished from demonstrated measures. |
| Verification / validation | Here, verification asks whether specified requirements are met; validation asks whether the system or measure is suitable for its intended use in the relevant context. Record the exact claim and evidence rather than relying on either label alone. |
