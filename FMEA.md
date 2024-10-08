# Failure Mode and Effect Analysis (FMEA)

## Introduction 
[[Failure Mode and Effects Analysis (FMEA) - asq.org](https://asq.org/quality-resources/fmea)] \
Failure Mode and Effect Analysis (FMEA) is an inductive bottom-up hazard analysis method, used for identifying all possible failures in a manufacturing/ assembly process, product or service. Best implemented early in the design phase, the goal of FMEA if to eliminate or mitigate failures. Through the FMEA process, failures are identified and numerically prioritized starting from the least desired outcome.

## History
Procedures for FMEA were first described November 9th 1949 by the U.S. Department of Defense (MIL-P-1629) [x] as FMECA (Failure Mode, Effects and Criticality Analysis). Primarily utilized in the military industry, it was later adopted by the space industry (NASA). In the 1970 in was introduced to the automotive industry (Ford). More information about FMEA history can be found through the [link is the _See Also_ heading](#see-also). 

## Application
FMEA is widely used across various industries today. Here is a list of industries where FMEA is applied:
* Automotive industry <sup>[[2]](#references)</sup>
* Aerospace industry ([SAE ARP 5580](#fmea-standards))
* Healthcare and medical devices
* Electronics and semiconductor industry
* Oil and gas industy

## Method steps
Below are the steps necessary to utilize the FMEA method.

### 1. Define scope
What is the goal of the process? Is it in the realm of concept design, system or service? Is there a desired level of detail and what are the boundaries? The result should be clear.

### 2. Assemble interdisciplinary team
A team of experts specializing in fields pertaining to the project should be assembled. 

### 3. Identify scope functions
Utilizing flowcharts, attempt to encompass the purpose and desired expectation of the system, design, process or service. Use it with a verb followed by a noun. Where necessary, break the scope down into smaller parts, and identify the function of those parts. 

### 4. Define Failure Modes
For all identified functions, identify every way that function might fail. Failure modes can generally fill in 1 of 3 categories:
1. Loss of function: The item, functional block or subsystem is no longer operating and the function previously performed by it is gone.
2. Erroneous function: The item or functional block is operating within design thresholds and parameters, but not in the desired way.
3. Incorrect function: The item or functional block is operating outside design thresholds and parameters.

### 5. Determine failure severity
For each identified failure, determine the the severity. Signified as "S", severity denoted the degree of negative impact of a potential failure. Noted as "S" on the FMEA sheet, severity is usually noted on a 1-10 scale, in which 10 can be likened to catastrophe and 1 to insignificant. 

Take note of first properly defining the number scaling with correlatory terms, which shall be known to everyone, before commiting the numbers to paper. \
For example, a Severity rating regarding a scenario of driving with a flat tire:
1. Inconvenience: Slight delay in travel plans.
2. Reduced Fuel Efficiency: Slight increase in fuel consumption.
3. Handling Issues: Minor difficulty in steering and control.
4. Increased Wear: Accelerated wear and tear on the tire and vehicle components.
5. Vibration: Noticeable vibrations making driving uncomfortable.
6. Damage to Wheel: Potential damage to the wheel rim.
7. Overheating: Tire overheating and risk of further damage.
8. Blowout Risk: Increased risk of the tire completely blowing out.
9. Loss of Control: Significant loss of vehicle control, particularly at high speeds.
10. Accident: High potential for a serious accident leading to injury or fatality.

### 6. Determine potential root causes
For each identified failure, identify all possible root causes. Utilize expertise and cause analysis tools to encompass as many causes possible, and add them to the FMEA sheet.

### 7. Determine occurence rating
For each identified failure, estimate the probability of the failure actually occurring. Occurence is noted on a 1-10 scale, in which 10 can be likened to inevitability and 1 to (extreme) unlikeliness. Note: similarly to [step 5](#5.-determine-failure-severity), assign an explicit occurence corresponding to the numbers, before commiting the numbers to paper.

### 8. Determine process controls
For each identified failure, put measures in place that prevent or maximally mitigate a failure from reaching a potential customer or the rest of the system. 

### 9. Determine detection rating
For each failure, determine the rate a process control can detect a failure, before the rest of the system or outside world (customer) are affected. Noted as "D" on hte FMEA worksheet, detection is usually between a 1-10 scale, in which 10 can be likened to a problem being certainly undetectable (or no process control present) and 1 is a certainty of detecting a problem. Note: similarly to [step 5](#5.-determine-failure-severity), assign explicit detection terms corresponding to the numbers, before commiting the numbers to paper.

### 10. Calculate the Risk Priority Number (RPN)
Multiply the S<sub>(everity)</sub>, O<sub>(ccurence)</sub> and D<sub>(etection)</sub> ratings into a Risk Priority Number. This number is the potential failure score for the corresponding failure, and can be used to prioritize relevance.

### 11. Implement changes
Assign actions that lower the RPN, by focusing on mitigating the underlying Severity, Occurence and Detention rating. These actions should be assigned to an expert with a corresponding completion date.

### 12. Measure effectiveness and evaluate
Measure the effectiveness of the assigned actions and log their progress.

## Example(s)
Now we will go through the [steps](#method-steps) wherein we fill in an FMEA worksheet. These steps will start from #3 through #11. The worksheet layout used will be the same as the FMEA worksheet image displayed above.

The example scenario will be in the context of and _ADS (Automated Driving System)_ detecting an object while on the road. 

Note that the example FMEA sheet may vary depending on the context and scope of the hazard. Here are some ways other FMEA sheets may vary from the example or vice versa:
* The FMEA sheet column order may be in the same order as the method execution steps, from left to right. This may make filing an FMEA sheet quicker and easier for the individual filing it, due to only having to shift to the right and adhering to the column name. Though this may make it (marginally) harder to interpret.
* The detection process controls (or any) may not be present in some variations
* Some FMEA contain a [_Criticality_](#used-references) rating column typically similar to the Severity, Occurence and Detection rating. If present, this must be taken into account for RPN calculation, usually also by way of multiplication. This will make this a [FMECA](#variations) sheet.
* This sheets utilizes some color coding, to signify difference in the numerical values. This is purely visual and optional.

| Step | Description | Visualization |
| - | - | - |
| 1-2 | Define scope <br>Assemble Interdisciplinary team<br>Identify scope functions | Due to these steps already being defined, these steps will be skipped for the purposes of this example case. |
| 3 | Identify scope functions: In the scenario of an ADS detecting an obstacle, what are the main functions or (sub)systems that are involved in that scenario? For this excercise, these will be: <br>Obstacle Identification <br>Decision Making <br>Braking System <br>Driver Intervention. | ![FMEA Example step 3](images/fmea_example_step03.png) |
| 4 | Define failure modes: Find the maximum amount of ways each of the above (sub)systems may fail, following by what would be the consequence of that failure.  | ![FMEA Example step 4](images/fmea_example_step04.png) |
| 5 | Determine failure severity: For each failure mode, assign a severity rating under `S`. | ![FMEA Example step 5](images/fmea_example_step05.png) | 
| 6 | Determine potential root causes: Write down the (potential) root cause for the failure. | ![FMEA Example step 6](images/fmea_example_step06.png) |
| 7 | Determine occurence rating: Calculate the occurence and write it down (next to the Severity rating) | ![FMEA Example step 7](images/fmea_example_step07.png) |
| 8 | Determine process controls: Write down the procedure, test or mechanism that prevent or mitigate the (root) cause from happening under _Process Controls for Prevention_. <br>Similary, write down the procedure or mechanism that detects failure after the cause happened but before the entire failure comes to fruition under _Process Controls for Detection_.  | ![FMEA Example step 8](images/fmea_example_step08.png) |
| 9 | Determine detection rating: Write down the likelihood the _Process Control for Detection_ can successfully detect the cause or its failure under `D`. | ![FMEA Example step 8](images/fmea_example_step09.png) |
| 10 | Calculate Risk Priority Number: Multiply the `S`, `O` and `D` rating and write the answer down under the corresponding RPN column. | ![FMEA Example step 8](images/fmea_example_step10.png) |
| 11 | Implement changes: The last step (possibly iterative) step that contains multiple actions, which typically starts with the designation of an assigned team or person(s) and a (due) date. Then, note the action that the designated entity will undertake which will reduce the initial RPN value. Upon testing by theory or the iterative practice, write down the updated `S`, `O` and `D` rating on the right hand side. Then calculate these value for the final RPN value. | ![FMEA Example step 8](images/fmea_example_step11.png) |
| 12 | Measure effectiveness and evaluate | - |

## Variations
* **FMECA** (*Failure Modes, effects and criticality analysis*): 
  * In addition to the FMEA process, FMECA also includes a Criticality Analysis (CA) that ultimately produces a [(C)riticality Ranking](#used-references). A Criticality ranking associated with a failure mode is a measurements or indicator that usually reflects safety or compliance with government regulations and need special controls. Criticality rankings have a high importance because of this, and thus FMECA is usually applied when increased reliability and safety are required. Note: FMECA is sometimes used interchangably with FMEA. 
* **DFMEA** (Design FMEA)
  * A variation of FMEA that focuses on the design phase of a product, focusing on omproving reliability, safety and performance before the manufactuing of the product
* **PFMEA** (Process FMEA) 
  * Pertains to uncovering risks within new or existing processes. PFMEA is done before a new process is implemented or, in the case of existing processes, is conducted before changes made to old processes take effect.
* **AFMEA** (Advanced FMEA)
* Revised FMEA standard **(AIAG & VDA FMEA 2022)**<sup>[[2]](#references)</sup> for Automotive:
  A more detailed, structured and automotive industry-specific opproach to FMEA. Key differences to the traditional FMEA include:
  * A more structured and systematic approach, better distinguishing between design FMEA (DFMEA) and process FMEA (PFMEA)
  * Consist of 7 steps:
    1. Planning and Preparation
	2. Structure analysis
	3. Function analysis
	4. Failure analysis
	5. Risk analysis
	6. Optimization
	7. Results documentation
  * Removal of the RPN ranking, instead a new parameter [AP (_Action Priority_)](#used-terminology) is used. This was done to address some of the [disadvantages of the RPN rating](#disadvantages).
  * Additional emphasis on communication of FMEA results, ensuring all stakeholders are informed and involved.

## Pros and cons
In relation to other Hazard Analyses, FMEA has both advantageous and disadvantageous characteristics. Some of these are described below.

### Disadvantages
* Possibly labor intensive: FMEA can become time-consuming and laborious when in the case of complex systems with numerous components and potential failure modes
* Subjectivity: Assignment of Severity, Occurence and Detection can be subjective, making it harder to find concensus (similar RPN scores) between (many) analysts, which may lead to inconsistent results
* FMEA focuses more on individual single-point failures, and is not equipped for subsystem-interactive failures
* FMEA does not formally encapsulate time-based effects of system components, potentially missing failure modes that are time-dependent
* Regarding the RPN:
  * The Severity, Occurence and Detection 1 to 10 scale numbers represent categorical ordinal variables; actually rankings representing scenarios, and do not necessarily reflect the evenly spaced numerical 1-10 relation (quantitative discrete variables). This can cause differing S, O and D numbers, especially when multiplied to get the RPN number, a risk value not proportional to other FMEA failure mode or real-life scenarios.
  * The is no standard RPN value from which corrective action should be taken
* Tendency towards high Severity ratings <sup>[[3]](#references)</sup>

### Advantages
* One of the most widely used and available hazard analysis methods
* Detailed focus on overview and analysis of individual components and subsystems
* (Advanced) probabilistic techniques not required for implementation
* Encourages a proactive approach to identify and mitigate potential failure modes before they occur, enhancing reliability and safety


## Used terminology
Glossary containing as many relevant and specific terms 

| Term | Definition |
| - | - |
| Action Priority (AP) | A new parameter from the AIAG/ VDA handbook<sup>[[2]](#references)</sup>, replacing the classical FMEA RPN and risk matrix. The AP puts a higher emphasis on the Severity value, and quantification of the AP does not come about through multiplication, but instead through evaluation using a decision table/ matrix. |
| Criticality rating | An rating similar to the RPN, but differs in calculation: `(C)riticality = Expected Failures * Mode Ratio of Unreliability * Probability of Loss`. |
| Detection | Signified as "D", detection denotes the degree a process controls can detect either the failure mode or its cause before the client is affected. Usually noted on a 1-10 scale, in which 10 may signify being undetectable (or no process control present) and 1 is a certainty of detecting a problem (in time). |
| End Effect | Consequence a failure mode has upon operation, function or status at the highest indenture level |
| Failure | Any error, defects or abnormalities that negatively impact system functionality, especially affecting the customer. |
| Failure Effect | The immediate consequence of a failure during operation.  |
| Indenture levels | Levels which indentify or describe (relative) complexity of a function or assembly. |
| Local Effect | The consequence a failure mode has on the current specific operation, function or status under analysis. |
| Next higher level effect | Consequence a failure mode has on operation, function or status at the next higher indenture level above the currently analyzed item. |
| Occurrence | Signified as "O", occurrence denotes a (probabilistic) chance of a failure occurring. Usually noted on a 1-10 scale, in which 10 can be likened to inevitability and 1 to (extreme) unlikeliness. |
| Process Control | Preventative or mitigating procedures, mechanisms or tests that attempt to prevent, or detect a failure before the client is affected. |
| Risk Priority Number (RPN) | A multiplication of $`S \times O \times D`$, the total score helps prioritize failures by overall criticality. |
| Severity | Signified as "S", severity denoted the degree of negative impact of a potential failure. Usually noted on a 1-10 scale, in which 10 can be likened to catastrophe and 1 to insignificant. |
| Single Point of Failure (SPOF)<br>Single Failure Points (SFP) | Part of a system that, if it fails, will stop the whole system form working. |

## Additions/ Notes
<img align="right" src="images/fmea_example02.png" width="274" height="81"> 

A FMEA example Excel worksheet (as visible on the right) can be found [here](example_files/fmea_testsheet_95.xls).

<br clear="right"/>

## See also
A more extensive history and standards regarding FMEA can be found at [here](https://www.superengineer.net/blog/fmea-history).

### FMEA Standards
* [MIL-STD 1629A](http://everyspec.com/MIL-STD/MIL-STD-1600-1699/MIL_STD_1629A_1556/) - “Procedures for performing a failure mode and effect analysis” (FMECA) (November 24<sup>th</sup> 1980)
* MIL-HDBK-338B
* IEC 60812  - [“Procedures for failure mode and effect analysis (FMEA)”](https://webstore.iec.ch/publication/26359) _(2018-18-10)_
* BS 5760-5  - [“Guide to failure modes, effects and criticality analysis (FMEA and
FMECA)”](https://knowledge.bsigroup.com/products/reliability-of-systems-equipment-and-components-guide-to-failure-modes-effects-and-criticality-analysis-fmea-and-fmeca?version=standard) _(Withdrawn June 6<sup>th</sup> 2006)_
* SAE ARP 5580 - [“Recommended failure modes and effects analysis (FMEA) practices for non-automobile applications”](https://www.sae.org/standards/content/arp5580/) _(Reaffirmed 2020-08-07)_
* SAE J1739  - [“Potential Failure Mode and effects Analysis in Design (Design FMEA) and Potential Failure Mode and effects Analysis in Manufacturing and Assembly Processes (Process FMEA) and effects Analysis for Machinery (Machinery FMEA)”](https://www.sae.org/standards/content/j1739_202101/) _(Revised 2021-01-13)_
* SEMATECH (1992) - [“Failure Modes and effects Analysis (FMEA): A Guide for Continuous Improvement for the Semiconductor Equipment Industry”](https://www.yumpu.com/en/document/view/3574368/failure-mode-and-effects-analysis-fmea-a-guide-for-sematech)
* FMEAAV-1 - _AIAG & VDA FMEA Handbook_ <sup>[[2]](#references)</sup> _(Automotive) (August 2022)_ 

## References
1. [What is FMEA? Failure Mode & Effects Analysis | ASQ](https://asq.org/quality-resources/fmea) \
2. [AIAG & VDA FMEA Handbook 2022](https://www.aiag.org/store/publications/details?ProductCode=FMEAAV-1) _(Automotive) (August 2022)_
3. [FMECA Vs FMEA (What is the Difference Between Them?)](https://www.twi-global.com/technical-knowledge/faqs/fmeca-vs-fmea#FMEA); TWI
