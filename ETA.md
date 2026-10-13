# Event Tree Analysis (ETA)

[Home](README.md) · [Foundations](foundations.md) · [FMEA](FMEA.md) · [FTA](FTA.md) · [ETA](ETA.md) · [STPA](STPA.md) · [Sources](sources.md)

**Revision:** 13 October 2026 draft. Independent technical review pending. Source-status checks are dated 6 October 2026; see [maintenance and limitations](review-guidance.md#maintenance-and-release).

Event Tree Analysis (ETA) examines developments following a defined initiating event. It represents response alternatives and their terminal states. Qualitative use can expose missing responses; quantitative use requires justified conditional probabilities or frequencies.

FTA and ETA can be used together. A fault tree may model causes of an initiating event, or it may quantify failure of a protection function represented by an ETA branch. A bow-tie representation also connects causes and consequences around a selected central event, often emphasizing prevention and mitigation barriers. It should not automatically be treated as a quantitative FTA–ETA model: event definitions, dependencies and probability assumptions must still be established.

## Inputs, outputs and scope

Define the initiating event, configuration, operating conditions, response sequence and physical end states. Outputs are a partition of modeled paths, their meanings, and any justified conditional probabilities or outcome frequencies. An Automated Driving System (ADS) example is linked below.

## Method steps

### 1. Define the initiating event

State exactly what has already happened and what remains to be analyzed. Starting after successful obstacle detection excludes missed detection; an encounter-based study must model detection explicitly.

### 2. Identify responses and end states

Specify the protection functions and other conditions that affect development. Define success, degraded performance and failure against explicit requirements. Do not assume an unspecified backup can act after the only brake command path fails.

### 3. Order and branch the model

Arrange stages so that the sequence and conditional dependencies are clear. Where protections act in a temporal sequence, show that sequence unless another ordering is explicitly justified. An alternative logical ordering may be mathematically possible, but it must preserve the appropriate conditional probabilities and must not imply a physically impossible response. Explain any ordering that a reader could otherwise mistake for chronology.

At each branching point, the alternatives must represent a mutually exclusive and collectively exhaustive partition of the possibilities considered at that point. Their conditional probabilities must sum to one. Apply this check separately to each node; do not add probabilities from unrelated nodes merely because they are drawn in the same column.

### 4. Assign justified conditional probabilities

For each probability, record the event definition, conditioning events, reference period or demand, source data, estimation method and uncertainty. Check whether the data represent the analyzed population and operating conditions. Manufacturer data, operational observations, justified expert elicitation and validated models can support estimates, but their limitations must be stated. A standard may specify a method or requirement without supplying the numerical probability needed here.

AI/ML-based estimation requires the same evidential scrutiny: representative data, independent validation, a defined target quantity and an account of uncertainty or distribution shift. The use of an algorithm is not itself evidence that an estimate is valid.

The following path probabilities are conditional on the initiating event having occurred. The initiating event therefore does not appear as a separate numerical factor in these conditional calculations. This is a restriction of the calculation’s scope, not a claim that the initiating event happens in every journey or that external uncertainty has disappeared. To estimate outcome frequency in operation, an applicable initiating-event frequency is also needed.

### 5. Calculate and interpret the paths

**Calculate and interpret outcomes.** Multiply the conditional branch probabilities along each path and identify the physical end state represented by that path. Combine mutually exclusive paths only where they represent the same outcome of interest. If the initiating event has frequency fIE, the corresponding path frequency is fIE × P(path given IE), using consistent operating conditions.

Assess consequences separately. Failure to stop within a specified distance does not automatically mean collision, and collision does not automatically establish a particular injury severity. Any risk conclusion needs the relevant consequences, exposure and decision criteria in addition to the tree probabilities.

## Worked example

Read the [common vehicle scope](automotive-example.md#scope-and-assumptions) and [conditional event tree](automotive-example.md#conditional-event-tree). That page contains the maintained Mermaid source and selectable outcome table.

The initiating event is an obstacle encounter. Detection is modeled; a failed stage terminates its path because no independent fallback has been specified. The diagram and numbers replace the old inconsistent screenshot sequence as one coordinated example.

## Modeling choices and limitations

A binary success/failure model can hide partial performance or different failure states. ETA can represent more than two alternatives at a node where needed—for example, full, degraded and absent braking—provided their meanings and conditional probabilities form a valid partition. Greater detail increases the modeling and data burden.

A fully expanded binary tree with n successive branching stages can have up to $2^n$ terminal paths. A new binary stage doubles only the paths to which it applies; early termination or irrelevant stages can produce fewer outcomes. Use the detail needed to answer the analysis question rather than an arbitrary fixed maximum number of barriers.

Do not rank different outcomes only by counting failed barriers. For a specified event set, adding another required failure cannot increase the probability of that intersection. However, different paths can involve different failure probabilities and dependencies. Compare their conditional probability models and consequences, not merely the number of barriers shown.

## Assessor review

Use the [assessor checklist and acceptance guidance](review-guidance.md). Record open assumptions, owners and evidence; completing this tutorial does not establish conformity with a standard.

## Used terminology

| Term | Description |
|---|---|
| Initiating event | The event or condition on which the event-tree analysis is based. It need not itself be an accident. |
| Branch | One alternative at a branching point, with meaning and probability conditional on the preceding path. |
| Mutually exclusive | Alternatives that cannot occur together within the defined event model; their intersections are empty. |
| Collectively exhaustive | Alternatives whose union covers the defined possibilities at that branching point. Numerical normalization alone does not demonstrate this coverage. |
| Path | A connected sequence of alternatives from the initiating event to a terminal outcome. |
| End state | The specified condition represented at the end of a path; its consequences may require further analysis. |
| Branching point | The point at which alternatives are distinguished. A separate node symbol is optional. |

## Method references and history

[IEC 62502:2010 — Analysis techniques for dependability — Event tree analysis (ETA)](https://webstore.iec.ch/en/publication/7131) provides a dedicated reference for ETA. This Wiki’s tutorial is explanatory; it does not reproduce the complete standard or demonstrate conformity with every provision. [B11](references.md#b11)

**Modeling choices:** an event tree can use binary or multi-state alternatives and can be analyzed qualitatively or quantitatively. More detailed or time-dependent extensions require their own modeling assumptions and references; they are not implied by this introductory example.
Event-tree methods have a longstanding role in probabilistic safety analysis, particularly in nuclear safety. The US Nuclear Regulatory Commission’s Reactor Safety Study, WASH-1400/NUREG-75/014 (1975), is a historical reference linked below. Historical accounts of earlier development should be read separately from the current method guidance.

Historical source: [NRC Reactor Safety Study, WASH-1400/NUREG-75/014 (1975)](https://www.nrc.gov/docs/ML0706/ML070610293.pdf).
