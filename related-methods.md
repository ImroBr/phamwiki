# Related methods and concepts

[Home](README.md) · [Foundations](foundations.md) · [FMEA](FMEA.md) · [FTA](FTA.md) · [ETA](ETA.md) · [STPA](STPA.md) · [Sources](sources.md)

**Revision:** 13 October 2026 draft. Independent technical review pending. Source-status checks are dated 6 October 2026; see [maintenance and limitations](review-guidance.md#maintenance-and-release).

| Group | Possible additions | Purpose |
|---|---|---|
| Prospective analysis methods | Preliminary Hazard Analysis; HAZOP; What-if analysis | Identify hazardous conditions or deviations and their consequences. |
| Barrier and dependence analysis | Bow-tie analysis; LOPA where appropriate; common-cause/dependent-failure analysis | Examine protection measures, their limitations and dependence. |
| Reliability modeling | Reliability Block Diagrams | Model how item success or failure affects a specified function. |
| Incident learning and problem solving | CAST; RCA; Kepner–Tregoe methods | Investigate events or structure problem-solving; distinguish this from prospective hazard analysis. |
| Classification and allocation concepts | ASIL; SIL | Describe integrity-related classifications in their respective frameworks; these are not standalone hazard-analysis methods. |

These topics are related but serve different purposes. Inclusion here does not imply that they are interchangeable or equally applicable to every automotive system. There is no universal numerical conversion between an FMEA RPN, an ASIL and a SIL.

## Introductory descriptions

| Topic | Description |
|---|---|
| Preliminary Hazard Analysis | An early, scope-bounded examination of hazards, potential consequences and candidate controls while the system definition is developing. Record uncertainty and carry significant findings into later analysis rather than treating the early list as complete. |
| HAZOP | A structured examination of deviations from intended operation, commonly using guide words and defined parameters/functions. Explain the chosen application and how deviations, causes, consequences and safeguards are recorded; do not assume a process-plant worksheet transfers unchanged to software or vehicle control. |
| Bow-tie/barrier analysis | A representation connecting threats, a selected central event, consequences and preventive/mitigating barriers. Define each barrier’s function, owner, effectiveness conditions and dependence. The drawing alone is not quantitative risk assessment. |
| Common-cause/dependent-failure analysis | Examination of conditions that can defeat several elements or protections together. Shared environment, energy, communication, design, software and maintenance may matter. Use the findings to revise independence and redundancy assumptions. |
| Human factors and interface analysis | Examination of responsibilities, information, workload, timing and interactions that influence safe behavior. Avoid treating “human error” as a sufficient causal explanation or assuming a person can always detect and recover from automation failures. |
| LOPA | A scenario-based approach that evaluates credited protection layers under a defined procedure. Independence, effectiveness and applicability of the layers require justification. Explain why the approach suits the application before using process-industry assumptions in a vehicle analysis. |
| SIL | A safety-integrity classification within its applicable functional-safety framework. It is not a hazard-identification technique and is not numerically interchangeable with an ASIL or an RPN. |
| RBD | A reliability representation of how item success supports a specified function. State assumptions about independence, repair and operating conditions before drawing conclusions from series/parallel blocks. |
| RCA and CAST | Related incident-learning approaches. Define the particular procedure and evidence base. Avoid ending the explanation at a convenient single “root cause” if interacting technical, organizational or operational conditions remain relevant. |
| Kepner–Tregoe methods | Structured problem-solving and decision-support methods. If included, explain the specific technique and purpose; do not label the entire family a substitute for a vehicle hazard analysis. |

These are introductions, not full procedures. Further chapters need primary method references, assumptions and worked examples.
