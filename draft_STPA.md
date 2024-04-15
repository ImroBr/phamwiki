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
Why did failure occur? 

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



## Additions



## Used terminology

| Term | Definition |
| - | - |
| Constraints | Conditions or behaviors that need to be satisfied to prevent hazards (and ultimately prevent losses) [p20] |
| Control Action | A directive issued by a controller to another subsystem |
| Control Structure | A hierarchical control structure is a system model that is composed of feedback control loops. An effective control structure will enforce constraints on the behavior of the overall system. |
| Controller | - |
| Controlled Process | - |
| Controller Constraint | Specifies the controller behaviors that need to be satisfied to prevent UCAs. [p41] |
| Environment | - |
| Hazards | System state or set of conditions that, together with a particular set of worst-case environmental conditions, will lead to a loss. |
| Losses | One or more undesired, safety-critical outcomes to stakeholder(s). It may include a loss of human life or human injury, property damage, environmental pollution, loss of mission, loss of reputation, loss or leak of sensitive information, or any other unacceptable loss. [p16] |
| Loss scenario | Describes the causal factors that can lead to the unsafe control actions and to hazards. [p42] |
| System | Set of components that function together as a whole to achieve a desired goal. A system can contain subsystems, or itself be a subsystem. |
| System Boundary | - |
| System Hazards | - |
| System input | - |
| System output | - |
| System-Level- | - |
| Unsafe Control Action (UCA) | A control action that, in a particular context and worst-case environment, will lead to a hazard. |


## See also
For a more thorough description of the System-Theoretic Process Analysis method including examples and use-cases, see the [STPA Handbook](http://psas.scripts.mit.edu/home/get_file.php?name=STPA_handbook.pdf).

## References




