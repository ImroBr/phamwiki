# Hazard Analysis Methods for Automotive Safety Assessment

[Home](README.md) · [Foundations](foundations.md) · [FMEA](FMEA.md) · [FTA](FTA.md) · [ETA](ETA.md) · [STPA](STPA.md) · [Sources](sources.md)

**Revision:** 13 October 2026 draft. Independent technical review pending. Source-status checks are dated 6 October 2026; see [maintenance and limitations](review-guidance.md#maintenance-and-release).

This Wiki introduces methods that can support the examination of automotive safety analyses. Its main focus is the reasoning, assumptions and evidence behind an analysis, rather than the selection of a particular method name.

Process Hazard Analysis is a process-safety assessment activity that may use techniques such as FMEA, FTA, HAZOP and What-if analysis. It is therefore not treated here as a separate technique that excludes those methods. For an example of this terminology, OSHA 1910.119(e)(2) lists several techniques that may be used in a Process Hazard Analysis. That US provision is cited to clarify terminology, not as a regulatory basis for European vehicle type approval. [B01](references.md#b01)

The methods covered here also have applications outside industrial process safety. Their applicability depends on the system, the analysis question and the decision that the results must support.

## Purpose and status

**Status:** educational reference under technical revision. The content is intended to help readers understand and question safety analyses; it is not an RDW approval procedure or a substitute for the applicable regulations and standards. The technical-review status of each page is stated separately.

This project supports readers, including automotive inspectors and auditors, in understanding and questioning OEM safety analyses. It is maintained by Imro Brammerloo. The repository name remains phamwiki.

## Start here

1. Read [terminology and scope](foundations.md).
2. Read the [automotive assessment context](automotive-context.md).
3. Compare the [questions answered by each method](method-comparison.md).
4. Explore [FMEA](FMEA.md), [FTA](FTA.md), [ETA](ETA.md) and [STPA](STPA.md), alongside the [shared automotive example](automotive-example.md).
5. Apply the [review questions and evidence guidance](review-guidance.md).

Publication versions are recorded in the [standards register](standards-register.md). [Sources](sources.md) separates methodological references from research awaiting review. [Related methods](related-methods.md) introduces possible extensions.

The [implementation record](audit-implementation.md) maps the correction guide to this draft. Authors can use the [method-page template](PHA_template.md).

## Analysis and its limits

Hazard analysis identifies hazardous system conditions and examines how they could arise or lead to harm. Depending on its purpose, it may produce qualitative findings, causal models, constraints, failure-effect descriptions or quantitative estimates. Not every hazard-analysis method requires a numerical likelihood estimate.

Risk analysis develops an understanding of risk; risk evaluation compares the results with stated decision criteria. Risk treatment selects and implements measures to change the risk. An analysis supports risk reduction, but the analysis alone does not implement or verify a safety measure. [B16](references.md#b16)

## Regulatory context

**Reading the regulatory requirement.** For Regulation (EU) 2022/1426, the method examples appear in Annex III, Part 2, point 3.5.5.2(b). Read this together with the concept-level assessment, validation/verification review and coverage provisions in points 3.5.5.2–3.5.5.4. The analysis must support a defensible safety argument, not merely demonstrate that a named technique was used. This Wiki uses the consolidation dated 24 March 2026 for that discussion. [B03](references.md#b03)

For UN Regulation No. 157, the historical extract used here is from Annex 4, point 3.4.4 of the original version. It is not presented as a complete statement of the amendment set applicable to every current approval. [B02](references.md#b02)

ALKS means **Automated Lane Keeping Systems**. ADS means **Automated Driving System**.

ETA is included because it complements FTA: FTA examines combinations of conditions leading to a selected top event, while ETA examines possible developments following an initiating event. This complementarity is useful, but using the two methods together does not by itself demonstrate regulatory compliance. An assessment must establish that the chosen analyses actually cover the required reasoning from hazards to design and from design to possible hazards, including relevant functions, interactions, operating conditions and safety measures. Method labels do not establish that coverage. [B02](references.md#b02), [B03](references.md#b03)
