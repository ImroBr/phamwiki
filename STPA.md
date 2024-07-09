_Draft_

# System-Theoretic Process Analysis

## Introduction 
System-Theoretic Process Analysis (STPA) is fairly recent hazard analysis technique. This technique is generally used in larger, complex systems. What differentiates the STPA method from other traditional hazard analysis techniques is the emphasis on (abstract) intended functionality of subsystems from the top down, rather than a regression into the smallest subsystems or components of a system. Another differentiating approach of STPA is the conclusion that unsafe interactions between system components could occur, when none of those individual system components may have failed.

## History
STPA is a analysis technique developed by [Nancy Leveson](http://sunnyday.mit.edu/bio-serious.html) and [John P. Thomas](http://web.mit.edu/jthomas4/www/index.htm). It is founded upon _System-Theoretic Accident Model and Process_ (STAMP), which is in turn based on Systems Theory.

## Underlying systems
Underpinning STPA are other theoretical frameworks, which are described below.

### STAMP - System-Theoretic Accident and Processes
STAMP is an accident causality model based on Systems Theory. It expands beyond the traditional model of causality to include more complex processes and unsafe interaction among system components. STAMP focuses on understanding and managing the control structures and safety constraints necessary to prevent accidents in complex systems.

### Systems Theory 
Systems Theory is an interdisciplinary framework that studies the complex interactions and behaviors of systems as wholes rather than just the sum of their parts. It emphasizes the importance of relationships, feedback loops, and the dynamic behavior of systems over time. Systems Theory is applied to a wide range of fields, including biology, engineering, and social sciences, to understand how components of a system interact to produce emergent properties and behaviors that cannot be understood by examining the components in isolation.

## Variations
**CAST** - Causal Analysis based on Sytems Theory (CAST) is a retroactive analysis method that examines an accident/incident that has occurred and 
identifies the causal factors that were involved. It is another analysis method based on STAMP. [p12-13] 

## Application
Fields in which the STPA is applied:
* Aerospace (Such as NASA and in aviation)
* Automotive (In the context of _Autonomous Driving Systems_ (ADS) and _Advanced Driver-Assistence Systems_ (ADAS)
* Healthcare <sup>[[2]](#references)</sup>
* Nuclear Energy <sup>[[3]](#references)</sup>
* Railroading <sup>[[4]](#references)</sup>
* Military Defense <sup>[[5]](#references)</sup>
* Chemical and Process Industries 


## Method steps
The STPA method steps are defined in 4 parts, described below.

### 1. Scope
The first step defines the purpose of the analysis. What is the system boundary that is being described that seperates all relevant subsystems (the _system_) from the outside/ negligible parts (the _environment_)? This part consists of four steps:
1. Identify [losses](#used-terminology)
   * Encapsulation of relevant stakeholders, and their stake in the system
   * What type of losses? (human life, reputation, privacy, security, etc)
   * Translate each relevant goal or value into a list of losses: `L-<number>: Loss (of) <critical objective>` \
     Such as: `L-1: Loss of life or injury to people`
   
   Some tips to prevent common mistaks when identifying losses:
   1. Losses can include any loss that is unacceptable to any stakeholder
   2. Losses should not reference individual components or specific causes like “human error” and “brake failure”
   3. Losses may involve aspects of the environment that are not directly controlled by the system designer
   4. Document any special considerations or assumptions made, such as losses that are explicitly excluded
2. Identify [system-level hazards](#used-terminology):

   Once the system and system boundary is identified, the next step is to define the system-level hazards by identifying system states or conditions that will lead to a loss in worst-case environmental conditions. 
   * Translate each system-level hazard into a list using the follosing general notation: `<Hazard specification> = <System> & <Unsafe Condition> & <Link to Losses>`
     Such as: `H-1 = Aircraft violate minimum separation standards in flight [L-1, L-2, L-4, L-5]`
	 
    In general, a hazard can lead to one or more losses and each hazard should be traced to the resulting losses. This traceability is typically documented in brackets after the hazard description. The example above shows the traceability to the loss(es) previously constructed.
	
    There are three basic criteria for defining system-level hazards:
    1. Hazards are _system_ states or conditions (not component-level causes or environmental states)
    2. Hazards _will_ lead to a loss in some worst-case environment
    3. Hazards must describe states or conditions to be prevented
	
	See [Common mistakes when identifying system-level hazards](#common-mistakes-when-identifying-system-level-hazards) for help when identifying system-level hazards.
3. Identify [system-level Constraints](#used-references)
   Once the system-level hazards are identified, it is straightforward to identify system-level constraints that must be enforced: simply invert the condition. \
   Translate the system-level constraints using the general notation: `<System-level Constraint> = <System> & <Condition to Enforce> & <Link to Hazards>`
   
   An example in the correct syntax and the respective inversion:
   ```
   H-1: Aircraft violate minimum separation standards [L-1, L-2, L-4, L-5]
   SC-1: Aircraft must satisfy minimum separation standards from other aircraft and objects [H-1]
   
   H-2: Aircraft airframe integrity is lost [L-1, L-2, L-4, L-5]
   SC-2: Aircraft airframe integrity must be maintained under worst-case conditions [H-2]
   ```
   
4. Refine hazards (Optional)

### 2. Control Structure
* Capturing functional relationships and interactions\
Factoring in (global) functional relationships and establishing points of control with downward arrows (control actions), and points of feedback with upward arrows.


| Generic control loop |
| - |
| ![STPA Generic Control Loop](images/stpa_handbook_figure2.6_page23_noreference.png) |


| - |
| - |
| ![STPA Generic Control Loop](images/stpa_handbook_figure2.6_page23_noreference.png) |


| ![STPA Generic Control Loop](images/stpa_handbook_figure2.6_page23_noreference.png) |
| - |
| | Generic control loop |



### 3. Identify Unsafe Control Actions (UCA)s
In the flow of control actions and feedback, what unsafe control actions can occur?

There are broadly 4 possible categorizations of unsafe control actions that can lead to a hazard or loss:
[introduction to stpa video, ~13:00](https://youtu.be/2W-iqnPbhyc?t=776)
1. **Command not provided causes hazard** \
 A control action that **should** have been provided but isn't, such as not sending a brake command when a collision is imminent; 
2. **Command providing causes hazard** \
 A control action that has been provided, but **in a scenario wherein such action is unsafe**, such as sending a brake command when on a highway;
3. **Command provided too early, too late, out of order** \
 A control action that has been provided in a correct situation, but **offset in its timing**, such as sending a brake command seconds later than is warranted;
4. **Stopped too soon, applied too long** \
 A control action that has been provided in a correct situation and timing, but **too long or short in duration**

Any ACU action that can be derived will generally fall in the above 4 categries.

Once unsafe control actions are identified, high-level safety constraints and controller functional safety requirements can be derived. 

The following high-level safety constraints can be created:
* **Controller X shall not allow A**
* **Controller X shall enforce B**
* ...

For  each of the 4 stated ACU's above, the following respective constraints van be constructed:
1. **`Controller X` shall provide `Command Y` when `D`**\
 `Controller X` = The responsible controller\
 `Command Y` = Output\
  `D` = situation that needs to be responded to. Additionally, awareness of `D` should be done through feedback.
2. **`Controller X` shall not provide `Command Y` when `E`**
3. **`Controller X` shall provide `Command Y` within `F` seconds of `G`**
4. **`Controller X` shall stop providing `Command Y` within `H` seconds of `J`**

### 4. Identify Loss Scenario
<img align="right" src="images/stpa_handbook_figure2.17_page43_noreference.png"> 
Two types of loss scenarios are to be considered, also illustrated in corresponding figure<sup>[[1]](#see-also), page 43</sup>:  
 
a. Why would unsafe Control Action(s) occur? 

b. Why would control action(s) be improperly executed or not executed?

<br clear="right"/>

1. Identifying scenarios that lead to Unsafe Control Actions
   Identification of loss scenarios can be considered as an inverse to identifying the unsafe control actions, askying _why_ a unsafe control action would occur. Some of these that may lead to UCAs may include:
   * Failures related to physical controller 
     * Physical failure of controller itself
	 * Power failure
	 * Etc
   * Inadequite control algorithm
     * Flawed implementation of specified control algorithm
   * Unsafe control input
   * Inadequate process model

Some example scenarios may include:
* Controller incorrectly believes X because ...
* Controller control algorithm does not enforce Y because ...
* Incorrect feedback Z received because ...
* Sensor failure causes ...
* Etc. ...

Note that in this step, physical components such as actuators or sensors are included, if they are relevant to the initial [losses](#1.scope)

## Example(s)
_Theoretical example_ \
* _Example of historical factual application_


## Pros and cons
Advantages of STPA over other hazard analysis: <sup>[[1]](#see-also), page 4</sup>
* Very complex systems can be analyzed.
* STPA can be utilized early in concept Analysis.
* STPA includes software and human operators in analysis to ensure all potential causal factors in Losses.
* STPA provides documentation of system functionality, which may be missing in other hazard analyses in the context of large and complex systems
* Easy integration into the system engineering process and model-based system engineering.
* Rationale and intent of design safety requirements are made clear by applying the STPA methodology, which makes it easier understandable for laymen or designers after a long hiatus.

Disadvantages of STPA:
* Lesser known analysis technique; few online resources.
  * Lesser software tools available.
  * Less widely accepted/ mandated by industry standards and regulations.
* More abstract in nature compared to conventional Hazard Analysis;
  * Higher degree of familiarity required of participating engineers (which may required more time and resources comparitively).
  * Harder to interpret by stakeholders.
* May be unnecessarily complex for smaller/simpler projects.
* May be less suited when a narrow, component-focused analysis is needed.


## _Things to avoid_

### Common mistakes when identifying system-level hazards
From the [STPA Handbook](#see-also) (page 19):
> _A common mistake in defining hazards is to confuse hazards with causes of hazards. For example, “brake failure”, “brake failure not annunciated”, “operator is distracted”, “engine failure”, and “hydraulic leak” are not system-level hazards but potential causes of hazards. To avoid this mistake, make sure the identified hazards do not refer to individual components of the system, like brakes, engines, hydraulic lines, etc. Instead, the hazards should refer to the overall system and system states. 

> **Too many hazards containing unnecessary detail** \
Like losses, there are no hard limits on the number of system-level hazards to include. As a rule of thumb, if you have more than about seven to ten system-level hazards, consider grouping or combining hazards to create a more manageable list. You may be including unnecessary detail and making the list unmanageable, difficult to review, and harder to identify things that are missing. Instead, begin with a more abstract and manageable set of system-level hazards and refine them into sub-hazards later if needed (as explained in the section on refining hazards below). \

> **Ambiguous or recursive wording** \
The system-level hazards define exactly what “unsafe” means at the system level. A common mistake is to use the word “unsafe” in the hazards themselves. Doing so creates a recursive definition and does not add information or value to the analysis. For example, it might be tempting to write “H-1: Aircraft experiences unsafe flight [L-1]”. It can be tempting because it certainly sounds dangerous—an unsafe flight by definition must be hazardous, right? The problem is that it is too vague and does not help specify the actual condition that is unsafe. Some have fallen into the same trap with statements like “H-1: Aircraft experiences an unsafe state [L-1]”, only to struggle with the rest of the analysis and miss important cases. A simple solution is to avoid using the word “unsafe” in the hazard itself and instead specify exactly what is meant by “unsafe”—what system states or conditions would make it unsafe? For example, an aircraft that is uncontrolled or that is too close to other aircraft would be unsafe. As you will see, specifying actual conditions like this is extremely useful during later STPA steps.

> **Confusing hazards with failures** \
Professionals who are experienced in other hazard analysis methods sometimes fall into the trap of writing STPA hazards describing potential deviations from specified technical functions or describing physical component failures. You may be familiar with traditional techniques that begin by searching for a set of deviations, faults, or functional failures in the technical system. To identify a broader set of causes in STPA, we cannot assume that the defined and specified functions are safe and correct, that human operators will perform as expected, that automated behaviors will not induce human error or confusion, that off-nominal cases will not occur, or that the technical design, specification, and requirements are correct. For example, the hazard “Controlled flight of aircraft into terrain” can be included in STPA while it may be omitted by efforts to examine only purely technical functional failures. Hazard identification in STPA is about system states and conditions that are inherently unsafe—regardless of the cause. In fact, the system hazards should be specified at a high-enough level that does not distinguish between causes related to technical failures, design errors, flawed requirements, or human procedures and interactions._

> **What should I look for when reviewing hazards?** \
Tips to prevent common mistakes when identifying hazards:
> * Hazards should not refer to individual components of the system
> * All hazards should refer to the overall system and system state
> * Hazards should refer to factors that can be controlled or managed by the system designers and operators
> * All hazards should describe system-level conditions to be prevented
> * The number of hazards should be relatively small, usually no more than 7 to 10
> * Hazards should not include ambiguous or recursive words like “unsafe”, “unintended”, “accidental”, etc.

## Used terminology

| Term | Definition |
| - | - |
| Constraints | Conditions or behaviors that need to be satisfied to prevent hazards (and ultimately prevent losses) <sup>[[1]](#see-also), page 20</sup> |
| Control Action | A directive issued by a controller to another subsystem |
| Control Structure | A hierarchical control structure is a system model that is composed of feedback control loops. An effective control structure will enforce constraints on the behavior of the overall system. |
| Controller | Part of a system (subsystem) that enforces constraints on the bahavior of a system. <sup>[[1]](#see-also), page 11</sup> |
| Controlled Process | The controlled process is any process that is controlled, such as a physical process or another controller. <sup>[[1]](#see-also), page 22</sup> |
| Controller Constraint | Specifies the controller behaviors that need to be satisfied to prevent UCAs.<sup>[[1]](#see-also), page 41</sup> |
| Environment | Part of the scenario outside the operational system boundary, of which there is little to no direct influence by the operator or designer <sup>[[1]](#see-also), page 17</sup> |
| Hazards | System state or set of conditions that, together with a particular set of worst-case environmental conditions, will lead to a loss. |
| Losses | One or more undesired, safety-critical outcomes to stakeholder(s). It may include a loss of human life or human injury, property damage, environmental pollution, loss of mission, loss of reputation, loss or leak of sensitive information, or any other unacceptable loss. <sup>[[1]](#see-also), page 16</sup> |
| Loss scenario | Describes the causal factors that can lead to the unsafe control actions and to hazards. <sup>[[1]](#see-also), page 42</sup> |
| Process Model | The Controllers represented internal beliefs for decisionmaking. Process Models may self-update based on feedback through observation of a controlled process.<sup>[[1]](#see-also), page 23</sup> |
| System | Set of components that function together as a whole to achieve a desired goal. A system can contain subsystems, or itself be a subsystem. |
| System Boundary | The transition between internal parts of a system that the designer or analyst has control over, as opposed to the (outside) environment of the system |
| Unsafe Control Action (UCA) | A control action that, in a particular context and worst-case environment, will lead to a hazard. |

## See also
A [video introduction to STPA](https://www.youtube.com/watch?v=2W-iqnPbhyc).

For a more thorough description of the System-Theoretic Process Analysis method including examples and use-cases, see the
* [STPA Handbook](http://psas.scripts.mit.edu/home/get_file.php?name=STPA_handbook.pdf)

## References
2. Antoine, Blandine (2013), [Systems Theoretic Hazard Analysis (STPA) applied to the risk review of complex systems: an example from the medical device industry](https://dspace.mit.edu/handle/1721.1/79424)
3. Torok, Ray; Geddes, Bruce (March 26-28, 2013), [Systems Theoretic Process Analysis (STPA) - Applied to a Nuclear Power Plant Control System](file:///C:/Users/BRAMMERL/Downloads/02_EPRI_MIT_STAMP_Mar2013.pdf)
4. Dunsford, Ross; Chatzimichailidou, Mikela (January 14<sup>th</sup> 2020), [Introducing a system theoretic framework for safety in the rail sector: supplementing CSM-RA with STPA](https://doi.org/10.1080/09617353.2019.1709289) p. 59-82
5. Homey, David Craig; B,S, Aeronautical Engineering, United States Air Force Academy (2015), [SYSTEMS-THEORETIC PROCESS ANALYSIS AND SAFETY-GUIDED
DESIGN OF MILITARY SYSTEMS](https://apps.dtic.mil/sti/trecms/pdf/AD1109554.pdf)

