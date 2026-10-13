# Automotive assessment context

[Home](README.md) · [Foundations](foundations.md) · [FMEA](FMEA.md) · [FTA](FTA.md) · [ETA](ETA.md) · [STPA](STPA.md) · [Sources](sources.md)

**Revision:** 13 October 2026 draft. Independent technical review pending. Source-status checks are dated 6 October 2026; see [maintenance and limitations](review-guidance.md#maintenance-and-release).

Hazard Analysis and Risk Assessment (HARA) in the ISO 26262 concept phase begins from the defined item and its intended behavior and context. It examines hazardous events associated with malfunctioning behavior. The classification considers severity, exposure to the relevant operational situation and controllability, using the prescribed criteria to determine the appropriate classification and derive safety goals. [B17](references.md#b17)

Exposure is not the probability that a component fails. Controllability is not the same quantity as an FMEA detection rating. An ASIL is not obtained by multiplying FMEA S, O and D scores, and there is no universal conversion from RPN to ASIL.

Detailed FMEA, FTA and other analyses can inform and support the safety concept, but a populated worksheet does not replace the HARA. Conversely, a HARA classification does not itself demonstrate that the implemented design satisfies the resulting safety requirements.

**Illustrative relationship:** an omission of braking when approaching a pedestrian must be considered in an operational situation, with its potential harm and the ability of the people involved to avoid it. For the driverless example, a human driver is not available to supply an assumed corrective intervention. The example intentionally does not assign S/E/C classes or an ASIL without the required situation analysis and classification basis.

A review should establish the item boundary, operational situations, malfunction descriptions, hazardous-event definitions, classification rationale, safety goals and traceability into subsequent requirements. Detailed application requires the applicable ISO 26262 procedure; this introductory explanation does not reproduce its classification tables.

## Complementary disciplines

| Discipline/topic | Question it helps answer | Reference starting point | Boundary to preserve |
|---|---|---|---|
| Functional safety | How can malfunctioning E/E behavior create harm, and how is the associated safety lifecycle addressed? | ISO 26262 series. | Not a complete account of every nominal-performance insufficiency. |
| SOTIF | How can functional insufficiencies make intended behavior hazardous? | ISO 21448:2022. | Do not relabel cybersecurity threats or all E/E faults as SOTIF. |
| Cybersecurity engineering | How can malicious actions compromise vehicle assets/functions, with what damage scenarios and treatment? | ISO/SAE 21434:2021; applicable UN R155 requirements. | Attack feasibility is not a constant random-hardware failure rate. |
| ODD and scenario-based evaluation | Under which conditions is operation intended, and what cases support evaluation within and at those boundaries? | ISO 34503:2023 and the ISO 34501/34502/34504/34505 family. | A scenario catalog does not by itself establish adequate coverage or safe performance. |
| AI safety | What safety concerns arise from the use, limitations and lifecycle of AI elements? | ISO/PAS 8800:2024. | Identify this publication as a PAS; do not substitute it for the complete system safety argument. |
| Safety argument | Why do the requirements, analyses, tests and operational evidence support a stated safety claim? | Applicable assessment framework and explicit claim–argument–evidence links. | Presence of a document is not proof of the claim it is intended to support. |

A single issue may need coordinated treatment across disciplines. For example, an incorrect obstacle track can arise from a malfunction, a perception limitation or an attack. The similar output symptom does not make those causes, evidence needs or assessment procedures interchangeable. The reference list is a map of relevant material, not a universal list of mandatory documents. [B18](references.md#b18), [B21](references.md#b21), [B22](references.md#b22), [B23](references.md#b23), [B24](references.md#b24)

## Cybersecurity and safety interfaces

Suppose an attacker can alter a communication path and replay an old path-clear message. The safety analysis asks how accepting that message could affect the controller’s process model, braking action, stopping margin and potential harm. The cybersecurity analysis asks which asset/property is compromised, what attack path and prerequisites allow it, how feasible that attack is, and which security measures address it.

Candidate safety measures include information-validity handling and a defined response to missing or inconsistent data. Candidate security measures include source authentication, integrity protection and protection against replay, where appropriate to the interface and architecture. Each measure has limits: an authenticated message can still contain incorrect source data, and freshness information must itself be handled reliably. Neither analysis substitutes for the other.

An EV–EVSE application can use the same reasoning structure for an incorrect or stale limit or status message, but must identify the actual signal, responsible controllers, trust boundaries and safe physical response. The relevant charging-standard edition and implementation determine those details; this generic example does not assert that a particular protocol message or cryptographic feature exists.

## Regulations and applicability

**Reading the regulatory requirement.** For Regulation (EU) 2022/1426, the method examples appear in Annex III, Part 2, point 3.5.5.2(b). Read this together with the concept-level assessment, validation/verification review and coverage provisions in points 3.5.5.2–3.5.5.4. The analysis must support a defensible safety argument, not merely demonstrate that a named technique was used. This Wiki uses the consolidation dated 24 March 2026 for that discussion. [B03](references.md#b03)

For UN Regulation No. 157, the historical extract used here is from Annex 4, point 3.4.4 of the original version. It is not presented as a complete statement of the amendment set applicable to every current approval. [B02](references.md#b02)

See the [standards register](standards-register.md) for the publication boundary used in this revision.
