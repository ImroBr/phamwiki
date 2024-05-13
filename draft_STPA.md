_Draft_

# System-Theoretic Process Analysis
_This is an early document which serves as a blueprint for adding specific Hazard Analysis Methodologies._


## Introduction 
_Abbreviation and full name._
System-Theoretic Process Analysis (SPTA) is fairly recent hazard analysis technique. This technique is generally used in larger, complex systems. What delineates the STPA method from other conventional hazard analysis methods is the assumption that unsafe interactions between system components could occur, while none of those system may have failed. \
Based on _System Theory_...

## History
_First inception and cause of hazard analysis method. (Year, person/ group, (geographic) location) Abbreviation_ \
STPA is a analysis technique developed by [Nancy Leveson](http://sunnyday.mit.edu/bio-serious.html) and [John P. Thomas](http://web.mit.edu/jthomas4/www/index.htm). It is founded upon _System-Theoretic Accident Model and Process_ (STAMP), which is in turn based on Sytems Theory.

## Underlying systems
_Possible underlying system or system predecessor of current hazard analysis_ \
System Theory - \
STAMP - System-Theoretic Accident and Processes

## Variations
_Specific variations of main hazard analysis method._ \
Causal Analysis based on Sytems Theory (CAST), and is a retroactive analysis method that examines an accident/ incident that has occured and identifies the causal factors involved. It is another analysis method based on STAMP. [p12-13] 

## Application
Used for: (List)\
Most use cases in current day. Type(s) of application domains.

## Method steps
_Specific formulas, symbols and/or terminology. _

The STPA method steps are defined in 4 parts, described below.

### 1. Scope
* What is the purpose of the analysis?
  1. Identify losses
  2. Identify system-level hazards
  3. Identify system-level Constraints
  4. Refine hazards (Optional)
* What type of loss categories are at play (human life, reputation, privacy, security, etc)
* What is the system and its boundary?

[p19]
<Hazard specification> = <System> & <Unsafe Condition> & <Link to Losses>
E.g. H-1 = Aircraft violate minimum separation standards in flight [L-1, L-2, L-4, L-5]



### 2. Control Structure
* Capturing functional relationships and interactions
Factoring in (global) functional relationships and establishing points of control with downward arrows (control actions, and points of feedback with upward arrows.

### 3. Identify Unsafe Control Actions (UCAs)
In the flow of control actions and feedback, what unsafe control actions can occur?

There are broadly 4 possible categorizations of unsafe control actions that can lead to a hazard or loss:
[introduction to stpa video]
[~13:00](https://youtu.be/2W-iqnPbhyc?t=776)
1. **Command not provided causes hazard** \
 A control action that **should** have been provided but isn't, such as not sending a brake command when a collision is imminent;
2. **Command providing causes hazard** \
 A control action that has been provided, but **in a scenario wherein such action is unsafe**, such as sending a brake command when on a highway;
3. **Command provided too early, too late, out of order** \
 A control action that has been provided in a correct situation, but **offset in its timing**, such as sending a brake command seconds later than is warranted;
4. **Stopped too soon, applies too long** \
 A control action that has been provided in a correct situation and timing, but **too long or short in duration**


### 4. Identify Loss Scenario
Two types of loss scenarios are to be considered, namely: [p43] \
a. Why would unsafe Control Action(s) occur?
b. Why would control action(s) be improperly executed?


## Example(s)
_Theoretical example_ 



* _Example of historical factual application_


## Pros and cons
Advantages of STPA over other hazard analysis: [p4]
* Very complex systems can be analyzed
* STPA can be utilized early in concept Analysis
* STPA includes software and human operators in analysis to ensure all potential causal factors in Losses
* STPA provides documentation of system functionality, which may be missing in other hazard analyses in the context of large and complex systems
* Easy integration into the system engineering process and model-based system engineering

Disadvantages of STPA:
* Lesser known analysis technique; few online resources



# Additions/ Notes
## _Things to avoid_
From the STPA Handbook (page 19):
> _A common mistake in defining hazards is to confuse hazards with causes of hazards. For example, “brake failure”, “brake failure not annunciated”, “operator is distracted”, “engine failure”, and “hydraulic leak” are not system-level hazards but potential causes of hazards. To avoid this mistake, make sure the identified hazards do not refer to individual components of the system, like brakes, engines, hydraulic lines, etc. Instead, the hazards should refer to the overall system and system states. 

> **Too many hazards containing unnecessary detail** \
Like losses, there are no hard limits on the number of system-level hazards to include. As a rule of thumb, if you have more than about seven to ten system-level hazards, consider grouping or combining hazards to create a more manageable list. You may be including unnecessary detail and making the list unmanageable, difficult to review, and harder to identify things that are missing. Instead, begin with a more abstract and manageable set of system-level hazards and refine them into sub-hazards later if needed (as explained in the section on refining hazards below). \

> **Ambiguous or recursive wording** \
The system-level hazards define exactly what “unsafe” means at the system level. A common mistake is to use the word “unsafe” in the hazards themselves. Doing so creates a recursive definition and does not add information or value to the analysis. For example, it might be tempting to write “H-1: Aircraft experiences unsafe flight [L-1]”. It can be tempting because it certainly sounds dangerous—an unsafe flight by definition must be hazardous, right? The problem is that it is too vague and does not help specify the actual condition that is unsafe. Some have fallen into the same trap with statements like “H-1: Aircraft experiences an unsafe state [L-1]”, only to struggle with the rest of the analysis and miss important cases. A simple solution is to avoid using the word “unsafe” in the hazard itself and instead specify exactly what is meant by “unsafe”—what system states or conditions would make it unsafe? For example, an aircraft that is uncontrolled or that is too close to other aircraft would be unsafe. As you will see, specifying actual conditions like this is extremely useful during later STPA steps.

> **Confusing hazards with failures** \
Professionals who are experienced in other hazard analysis methods sometimes fall into the trap of writing STPA hazards describing potential deviations from specified technical functions or describing physical component failures. You may be familiar with traditional techniques that begin by searching for a set of deviations, faults, or functional failures in the technical system. To identify a broader set of causes in STPA, we cannot assume that the defined and specified functions are safe and correct, that human operators will perform as expected, that automated behaviors will not induce human error or confusion, that off-nominal cases will not occur, or that the technical design, specification, and requirements are correct. For example, the hazard “Controlled flight of aircraft into terrain” can be included in STPA while it may be omitted by efforts to examine only purely technical functional failures. Hazard identification in STPA is about system states and conditions that are inherently unsafe—regardless of the cause. In fact, the system hazards should be specified at a high-enough level that does not distinguish between causes related to technical failures, design errors, flawed requirements, or human procedures and interactions._

## Used terminology

| Term | Definition |
| - | - |
| Constraints | Conditions or behaviors that need to be satisfied to prevent hazards (and ultimately prevent losses) [p20] |
| Control Action | A directive issued by a controller to another subsystem |
| Control Structure | A hierarchical control structure is a system model that is composed of feedback control loops. An effective control structure will enforce constraints on the behavior of the overall system. |
| Controller | Part of a system (subsystem) that enforces constraints on the bahavior of a system. [p11] |
| Controlled Process | The controlled process is any process that is controlled, such as a physical process or another controller. [p22] |
| Controller Constraint | Specifies the controller behaviors that need to be satisfied to prevent UCAs. [p41] |
| Environment | Part of the scenario outside the operational system boundary, of which there is little to no direct influence by the operator or designer [p17] |
| Hazards | System state or set of conditions that, together with a particular set of worst-case environmental conditions, will lead to a loss. |
| Losses | One or more undesired, safety-critical outcomes to stakeholder(s). It may include a loss of human life or human injury, property damage, environmental pollution, loss of mission, loss of reputation, loss or leak of sensitive information, or any other unacceptable loss. [p16] |
| Loss scenario | Describes the causal factors that can lead to the unsafe control actions and to hazards. [p42] |
| System | Set of components that function together as a whole to achieve a desired goal. A system can contain subsystems, or itself be a subsystem. |
| System Boundary | The transition between internal parts of a system that the designer or analyst has control over, as opposed to the (outside) environment of the system |
| Unsafe Control Action (UCA) | A control action that, in a particular context and worst-case environment, will lead to a hazard. |

## See also
For a more thorough description of the System-Theoretic Process Analysis method including examples and use-cases, see the [STPA Handbook](http://psas.scripts.mit.edu/home/get_file.php?name=STPA_handbook.pdf).

## References




