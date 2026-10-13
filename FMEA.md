# Failure Mode and Effects Analysis (FMEA)

[Home](README.md) · [Foundations](foundations.md) · [FMEA](FMEA.md) · [FTA](FTA.md) · [ETA](ETA.md) · [STPA](STPA.md) · [Sources](sources.md)

**Revision:** 13 October 2026 draft. Independent technical review pending. Source-status checks are dated 6 October 2026; see [maintenance and limitations](review-guidance.md#maintenance-and-release).

Failure Mode and Effects Analysis (FMEA) systematically examines how specified functions, items or process steps can fail and what effects those failures can have. It commonly reasons from individual failure modes toward their local and higher-level effects. Causes, existing controls and proposed actions are recorded at an appropriate level of detail.

FMEA can be used during development and maintained as the system or process changes. Its results support decisions about prevention, detection and mitigation. The analysis is bounded by its scope, assumptions and the knowledge available; it does not guarantee identification of every possible failure or hazardous interaction. [B05](references.md#b05)

## Inputs, outputs and variant

**Choose the FMEA variant first.** DFMEA examines the design, PFMEA examines a manufacturing or assembly process, and supplemental FMEA-MSR examines diagnostic monitoring and system response during operation. The controls and rating criteria must match the chosen variant. Development tests intended to reveal a design weakness before release are not the same control as a runtime diagnostic intended to detect a fault in service. [B06](references.md#b06), [B07](references.md#b07)

The linked worked example is a qualitative function-level FMEA used to teach failure-mode/effect reasoning and action planning. It is not presented as a completed AIAG & VDA DFMEA, PFMEA or FMEA-MSR. Runtime measures are identified as design provisions; tests of those measures are identified separately as verification activities.

Start with functions and requirements, the architecture or process sequence, configuration, operating conditions and a multidisciplinary team. Outputs are traceable failure-mode/effect records, current provisions, open actions and verification evidence.

## Method steps

### 1. Define scope and assemble the team

Select the function/item/process boundary, lifecycle stage and variant. Record assumptions, operating modes and configuration. Include design, operation, verification and relevant domain expertise.

### 2. Identify functions and failure modes

For each function, describe the ways its required behavior could be absent or incorrect. Useful prompts include: no output, unintended output, output too high or too low, incorrect value or direction, intermittent output, output too early or too late, and output maintained too long or stopped too soon. These prompts are not an exhaustive or mutually exclusive classification.

Express the mode at the selected analysis level. For “provide a timely obstacle track”, “track provided too late” is a functional failure mode; a defective sensor may be one possible cause. A component can meet its own specification while its interaction with the wider system remains inadequate.

### 3. Trace effects and assess severity

Identify the relevant failure effects before assigning severity. Evaluate the consequences at the level required by the selected FMEA procedure, including the vehicle-level or user effect where applicable. Apply a defined severity table consistently and identify its source and version.

For example, “the vehicle does not achieve the required deceleration” is an effect on a function. The severity assessment also needs the operating situation and potential consequence, such as collision with a pedestrian or failure to complete a maneuver without injury. The component name or repair cost alone does not establish the safety severity.

This Wiki does not provide a replacement automotive severity scale. Where no justified scale and effect description are available, record the consequence and leave the numerical classification unassigned rather than inventing a rating.

Severity is linked to a stated consequence, not assigned automatically to a subsystem. A perception failure, a late decision and inadequate brake force may all contribute to failure to stop before a pedestrian. If the relevant consequence and classification conditions are the same, a different component origin does not by itself justify a different severity rating. Different ratings require different documented effects or assessment conditions.

### 4. Identify causes and baseline controls

Record the prevention and detection controls that already apply to the analyzed configuration, together with their evidence and limitations. Establish the baseline assessment using those controls. Record additional or modified controls as proposed actions in separate fields; do not credit them in the baseline merely because they are planned. Identify the configuration and date to which each assessment applies.

Describe mechanisms or conditions at the selected level, and distinguish local effects from causes. Use other analyses where combinations or interactions need separate examination.

### 5. Evaluate priorities under the selected procedure

**Occurrence:** rate the occurrence of the specified cause or failure mechanism according to the selected procedure and the effectiveness of applicable prevention controls. State the reference conditions and evidence. A rating is a category from that procedure; it is not automatically a probability and its highest value does not literally mean inevitability.

**Detection:** rate the capability of the applicable detection controls to identify the specified cause or failure mode at the point defined by the selected procedure. State what is detected, by which control and before which release or consequence. Lower numerical ratings do not establish perfect detection.

**RPN:** where the selected procedure uses RPN, calculate S × O × D. It is a prioritization index formed from ordinal ratings, not a calibrated measure of expected harm. Equal RPNs can represent materially different combinations of severity, occurrence and detection. Review serious consequences explicitly rather than relying on one RPN threshold.

### 6. Assign actions and verify effectiveness

Record the action, its owner, target completion date and the evidence needed to demonstrate effectiveness. Keep predicted improvements separate from ratings supported by completed verification. Reassess occurrence only when the prevention or failure-mechanism evidence justifies the change, and detection only when the relevant detection capability has demonstrably changed. Severity normally remains tied to the failure effect unless the design change alters that effect.

In this educational example the proposed actions have not been implemented or tested. Residual ratings are therefore not assigned, and the action status is “Proposed—effectiveness not demonstrated”.

## Worked example and download

Read the [common scope](automotive-example.md#scope-and-assumptions) and [qualitative FMEA](automotive-example.md#qualitative-function-level-fmea).

This example assumes driverless operation within a restricted operating area. No human driver is credited with immediate collision avoidance. Obstacle response, braking and hold-at-rest behavior are responsibilities of the vehicle system. A remote supervisor may authorize a later restart but is not credited as a time-critical fallback in this scenario.

[Download the blank template and matching worked example](example_files/fmea-qualitative.xlsx). The two sheets use the same fields as the maintained example. The earlier XLS and screenshot sequence have been retired; historical versions remain in Git history.

The example uses neutral presentation and explicit action/evidence status. It assigns no S/O/D, RPN or AP to the vehicle rows. **Reading the colors:** any color applied to S, O, D or RPN is a display aid only. It does not indicate that the residual safety risk is acceptable. Serious potential consequences require explicit review under the applicable criteria even when the RPN is low. Action closure requires evidence and a recorded decision; a changed score alone is not sufficient.

## FMECA and automotive guidance

Some analyses supplement FMEA with an explicit criticality assessment; these are commonly described as FMECA. The selected procedure determines how criticality is evaluated—for example, through a severity-based ranking or a defined quantitative model. FMECA is not generally obtained by multiplying an RPN by an additional criticality rating. Record the chosen procedure and explain how its results support action priorities. [B05](references.md#b05)

The harmonized AIAG & VDA FMEA Handbook was introduced in 2019. It provides a seven-step approach: planning and preparation, structure analysis, function analysis, failure analysis, risk analysis, optimization and results documentation. Its Action Priority approach replaces reliance on RPN for prioritizing actions within that handbook’s procedure. This does not mean that RPN has disappeared from every FMEA procedure. Identify the applicable handbook edition, printing, errata and customer requirements when describing an actual analysis. [B06](references.md#b06), [B08](references.md#b08)

**Supplemental FMEA for Monitoring and System Response (FMEA-MSR):** an automotive approach addressing diagnostic monitoring and the system response during operation. It complements design FMEA and uses its own evaluation procedure; do not construct an FMEA-MSR merely by inserting runtime diagnostics into an ordinary S/O/D worksheet. [B06](references.md#b06), [B07](references.md#b07)

**Research-specific extensions:** some publications use labels such as AFMEA for a particular extension. Such a label should be accompanied by the cited authors’ definition and procedure. This Wiki does not treat an unexplained acronym as a universally standardized variant.

## Strengths and limitations

A structured record makes individual failure effects and actions reviewable and can be maintained as the design changes. FMEA can examine interfaces, software, human actions and timing-related failure modes when these are explicitly included in the scope. A conventional single-failure FMEA may nevertheless miss hazardous combinations, feedback-related behavior or interactions that are not readily represented as individual failure modes. Complementary system-level or combination analyses may therefore be needed. Timing is not automatically modeled by a worksheet; deadlines, durations and operating sequences must be stated when they affect the failure effect. [B05](references.md#b05)

Ordinal S/O/D multiplication does not preserve equal intervals or a calibrated harm scale. Prioritization must not hide serious effects or unresolved dependencies.

## Assessor review

Use the [assessor checklist and acceptance guidance](review-guidance.md). Record open assumptions, owners and evidence; completing this tutorial does not establish conformity with a standard.

## Used terminology

| Term | Description |
|---|---|
| Failure | Loss of the ability to perform a specified required function. State the function and conditions concerned. |
| Fault | A condition or defect that can contribute to failure. Distinguish the condition from the event or behavior being analyzed. |
| Failure mode | The manner in which an item or function fails, such as absent, incorrect or late output. |
| Cause | A condition, mechanism or circumstance contributing to a specified failure mode at the selected analysis level. |
| Failure effect | A consequence of a failure mode, described at the local, next-higher or end-system level as appropriate. |
| Local effect | Consequence at the level of the analyzed item or function. |
| Next-higher-level effect | Consequence at the containing assembly, subsystem or next analysis level. |
| End effect | Consequence at the highest system or user level selected for the analysis. |
| Single point of failure | An item whose failure alone defeats a specified function or objective. Identify that function; the entire vehicle need not stop operating. |
| Action Priority | A prioritization classification determined using the selected procedure’s criteria; it is not itself a residual-risk acceptance decision. |

**Criticality assessment:** an evaluation of the importance of a failure mode using stated criteria, which include the severity of its consequences and may include other measures. A criticality rank, a numerical criticality measure and an RPN are not automatically equivalent. Any formula must identify its variables, units, reference period and assumptions. An expected number of failures is not itself a probability. [B05](references.md#b05)

## References and history

FMEA and FMECA have a long history in reliability and safety engineering. This page distinguishes historical references from the procedure selected for present use. MIL-STD-1629A is a historical FMECA reference; contemporary references used here include IEC 60812 and automotive-specific guidance. [B05](references.md#b05), [B19](references.md#b19)

Use [IEC 60812, AIAG & VDA and SAE J1739 entries](standards-register.md) with their edition, scope and status. These sources do not all prescribe the same procedure.
