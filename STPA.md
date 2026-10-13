# System-Theoretic Process Analysis (STPA)

[Home](README.md) · [Foundations](foundations.md) · [FMEA](FMEA.md) · [FTA](FTA.md) · [ETA](ETA.md) · [STPA](STPA.md) · [Sources](sources.md)

**Revision:** 13 October 2026 draft. Independent technical review pending. Source-status checks are dated 6 October 2026; see [maintenance and limitations](review-guidance.md#maintenance-and-release).

System-Theoretic Process Analysis (STPA) examines how inadequate control of a system can allow hazardous behavior. It addresses interactions, feedback, software, people and organizational responsibilities as relevant to the selected scope; component failure is not a necessary precondition for every unsafe interaction.

STPA is based on STAMP, the **System-Theoretic Accident Model and Processes**. STAMP is a model of accident causation; STPA is a prospective analysis method based on that model. [B12](references.md#b12)

## Inputs and outputs

Begin with the purpose, stakeholders, system responsibilities, relevant operating environment and design information available. Outputs include losses, hazards, system constraints, a control structure, unsafe control actions (UCAs), controller constraints and causal scenarios. Link selected measures to owners and verification evidence. [B12](references.md#b12)

## Method steps

### 1. Define purpose, losses, hazards and constraints

Define the system boundary and the purpose of the analysis. Parts outside that boundary are treated as the environment, but they are not necessarily unimportant or negligible. Environmental conditions and interactions can determine whether a system condition leads to loss. Record important external actors, disturbances and assumptions, even where the system designer cannot directly control them.

Define stakeholder losses first, then system conditions that can lead to those losses in relevant environmental conditions. State constraints on system behavior. Keep losses, hazardous conditions and failure causes distinct, and give each a stable identifier.

### 2. Model the control structure

Represent controllers, controlled processes, control actions, feedback and important external actors. For each controller, state its responsibilities and the process-model information needed to exercise control. The model is functional; it is not necessarily a wiring diagram.

Examine the complete feedback chain: a condition exists in the controlled process; sensors or other information sources observe it; information is transmitted; the controller receives and interprets it; and the controller updates its process model.

Consider missing observations, incorrect measurements, lost or delayed messages, stale values treated as current, incorrect units or coordinate frames, rejected valid information, and missing interpretation or model updates. Also consider whether the control structure provides the information needed at all. A correctly functioning sensor does not ensure that the controller receives, interprets and uses its information correctly.

### 3. Identify unsafe control actions

For each control action examine four categories: not provided when needed; provided when unsafe; provided too early, too late or in the wrong order; applied too long or stopped too soon. State the controller, action, unsafe context and linked hazard. Derive controller constraints from the identified UCAs. Do not force an example into every category if the selected losses and context do not support one.

**Providing a control action causes a hazard:** the controller provides an action in a context in which that action leads to a defined hazard. For example, it commands severe braking when no forward conflict requires it and a closely following vehicle cannot maintain separation, thereby creating a rear-collision hazard. Braking on a highway is not inherently unsafe; the context and linked hazard make this particular action unsafe.

### 4. Identify causal scenarios and measures

Explain how unsafe control or inadequate execution can arise. Include feedback/process-model issues and the control path to the physical process. A context-combination table is a prompt, not an enumeration of complete causal scenarios.

Maintain a reviewable link from losses and hazards to unsafe control actions, constraints, causal scenarios and the measures selected to address them. Identify the responsible owner and verification evidence for each measure. A context table helps organize the analysis but does not replace the causal explanation or the evidence that a measure works.

The worked example includes one complete illustrative chain from a pedestrian-injury loss to a stopping-margin hazard, a late brake command, a timing constraint, a stale-information scenario and a corresponding verification activity. Its verification is proposed, not reported as completed.

## Worked example

Read the [common scope](automotive-example.md#scope-and-assumptions) and [STPA control analysis](automotive-example.md#stpa-control-analysis). It contains consistent L/H/SC/UCA/CC/LS identifiers, the control structure, two causal scenarios and a complete illustrative verification chain.

The former aircraft and BSCU source excerpts have been replaced together. Their unrelated hazard identifiers, including the undefined H-4, are not carried into the new example. Source examples remain available through [the reading list](sources.md); they must be read with their own scope and hazard definitions.

## Strengths and limitations

STPA supports systematic examination of control, feedback and causal conditions, including software and human behavior. Its results still depend on scope, model quality, analyst knowledge and review; applying the method does not prove that every causal scenario has been found.

Building a useful control structure requires judgment about responsibilities, abstraction and boundaries. Structured guidance is available, but a diagram is not automatically complete or correct merely because it uses the expected symbols. Review the model against known responsibilities and information needs, and refine it as the analysis exposes gaps.

Effective use requires training and practice, particularly in defining useful system hazards, UCA contexts and causal scenarios. Public handbooks, papers, workshops and third-party tools are available through the MIT STAMP resources. Tool support and adoption vary by organization and application; the suitability of an analysis should be judged from its outputs rather than from popularity alone. [B13](references.md#b13)

## Related methods

**CAST — Causal Analysis based on System Theory:** a related STAMP-based method used to learn from incidents or accidents. STPA examines potential future unsafe behavior; CAST examines the circumstances and control deficiencies associated with an event that occurred. CAST is therefore presented here as a related method, rather than simply a variant of STPA. [B13](references.md#b13)

## Assessor review

Use the [assessor checklist and acceptance guidance](review-guidance.md). Record open assumptions, owners and evidence; completing this tutorial does not establish conformity with a standard.

## Used terminology

| Term | Meaning in this tutorial |
|---|---|
| Loss | An explicitly selected unacceptable stakeholder outcome. |
| Hazard | A system condition linked to loss under relevant environmental conditions. |
| Control action | An action issued by a controller to influence a controlled process. |
| UCA | A control action or omission that is unsafe in a stated context relative to a defined hazard. |
| Process model | The controller’s representation of relevant process/environment state. |
| Feedback | Information about the process or effects of control used by the controller. |
| Causal scenario | An explanation connecting circumstances, control/feedback and behavior to a hazard. |
| Safety constraint | A required restriction on system or controller behavior. |

## References and source figures

Leveson, N. G., and Thomas, J. P. (2018). *STPA Handbook*, March 2018. See printed p. 51 for the discussion of causal scenarios versus isolated causal factors. [B12](references.md#b12)

**Related source figure:** Leveson and Thomas, *STPA Handbook* (2018), Figure 2.6, printed p. 23, illustrates a basic feedback control structure. [View the source handbook](https://psas.scripts.mit.edu/home/get_file.php?name=STPA_handbook.pdf). The figure is linked here rather than reproduced.
Original simplified control-structure illustration for this Wiki’s hypothetical low-speed vehicle example. It is a functional model and does not reproduce a source figure.

The original control diagram in the shared example is newly authored for this Wiki and does not reproduce a handbook figure. Additional handbook examples should be read in their source context: Figures 2.17–2.19, printed pp. 43–49, and Appendix B Figures B.6–B.7, printed pp. 153–154. [B12](references.md#b12)
