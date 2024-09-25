# Process Hazard Analysis Wiki (phamwiki)
In an evolving automotive industry, there must exist an equal or greater evolving need for safety. Many `Process Hazard Analyses (PHA)` exist to mitigate risks, but may risk falling behind in a world where processes increase in complexity, creating unforeseen risks.
As such, a need arises for a robust foundation and contrast of PHA methodologies. This project aims to add to this foundation in the form of online documentation for future use.

This GitHub WIKI-environment contains documentation about Hazard Analysis (HA) methodologies. A _Hazard Analysis_ entails identification of undesired events that may lead to a hazard, analysis of underlying causes of this hazard, and coupled with an estimation of hazard likeliness and magnitude of harmful effects.

### Disclaimer
All content in this WIKI is purely for informational purposes and is not intended as an instruction for real-world implementation. Descriptions of hazard analyses on this WIKI are global in nature, and can differ in standard or implementation from real-world applications, depending the respective industry and product use case among other things.

## Goal of this Wiki
This Wiki documents Process Hazard Analyses, aiming to support (automotive/ RDW) inspectors/ auditors operating on behalf of a Type Approval Authority, in better understanding (Process) Hazard Analyses performed by (automotive) OEM's (_Original Equipment Manufacturers_). 

Hazard analysis pages within this Wiki contain at least the following topics:
* Method name and description
* Method steps
* Advantages and disadvantages
* Example(s)
* Related literature/ studies

This Wiki tool may aid in: 
* Formulating better informed advice regarding OEM's PHA decision choice(s)
* Better validating process methodology steps 

### Wiki scope and regulatory foundation
This wiki is (in the process of) being deployed as a consequence of:
* In the ontext of _ALKS (Assisted Lane Keeping System)_; [UN Regulation No. 157 <sup>[1]</sup>](#references) annex 4, 3.4.4 (p. 34 of pdf), namely:

> **3.4.4**: ... The Type Approval Authority shall perform an assessment of the application 
of the analytical approach(es):  

> **(b)<sub>(1st)</sub>**: Inspection of the safety approach at the system level including a top down (from possible hazard to design) and bottom up approach (from design to possible hazards). The safety approach may be based on a Failure Mode and Effect Analysis (FMEA), a Fault Tree Analysis (FTA) and a System-Theoretic Process Analysis (STPA) or any similar process appropriate to system functional and operational safety. 

* And in the more broader context of ADS; [EU 2022/1426 <sup>[2]</sup>](#references) 3.5.5.2, namely:
> **3.5.5.2** ... The type-approval authority shall assess the application of the analytical approach(es): 

> **(b)**: Inspection of the safety approach at the ADS level including a top down (from possible hazard to design) and bottom-up approach (from design to possible hazards). The safety approach may be based on a failure mode and effect analysis (FMEA), a fault tree analysis (FTA) and a System-theoretic process analysis (STPA) or any similar process appropriate to system functional and operational safety.

From the quoted text, the following conclusions can be made:
* An inspection ***shall*** require a top-down and bottom-up approach
* The hazard analyses ***may*** include FMEA, FTA and STPA or any similar process

The 3 Hazard Analyses stated above are the basis for inclusion in this wiki, with the addition of ETA (Event Tree Analysis). This is because ETA is a method that may neatly and easily converge with an FTA top event, and because conforms to the top-down (FTA) and bottom-up (ETA) binary requirement. 

Additionally, the contours of the project interface with the [ISO 26262 <sup>[[3]](#references)</sup>] standard.

### PHA distinctions and scope
Although the PHA methodology mostly applies to physical industrial processes, the other [Hazard Analyses](#available-hazard-analysis-methods) are described in a global manner. Meaning, additional factors that go beyond industrial processes can be taken into consideration. These additional factors can be in a human context such as personnel safety, customer satisfaction or company reputation, or more abstract context such as computational scenarios or software interaction (which can also include emerging or future technology such a AI or quantum computing).

As such, these other methodologies in this WIKI are considered parallel or complimentary in relation to PHA, rather than an instance or subset of PHA. Rather, these other methodologies and indeed the PHA method are considered a subset of _Hazard Analyses_.

## Available hazard analysis methods
Following are the available HA pages on this WIKI:
* [System-Theoretic Process Analysis (STPA)](/STPA.md) _(Top-down approach)_
* [Failure Mode and Effect Analysis (FMEA)](/FMEA.md) _(Bottom-up approach)_
* [Failure Tree Analysis (FTA)](/FTA.md) _(Top-down approach)_
* [Event Tree Analysis (ETA)](/ETA.md) _(Bottom-up approach)_

## Future additions
This WIKI may be supplemented with additional documents and features going forward, depending on available time and functional-utilitary demand. Some of these feature are already known and may be included in the next project update:

### Future Hazard Analyses methodologies
* Process Hazard Analysis (PHA) (stand-alone description)
* Hazard and Operability Study (HAZOP)
* Bowtie-analysis
* Layer of Protection Analysis (LOPA)
* [Kepner-Tregoe method](https://kepner-tregoe.com/faqs/)
* Safety Integrity Level (SIL)
* Root Cause Analysis (RCA)
* Reliability Block Diagram (RBD)

### Features to be added
* Further theoretical expansion of method descriptions and literature
* Better visual support along with method steps
* (More advanced) examples
* (Advanced) cross-comparisons between Hazard Analysis methods

### References
1. [UN Regulation No. 157](https://unece.org/transport/documents/2021/03/standards/un-regulation-no-157-automated-lane-keeping-systems-alks), 22<sup>th</sup> of January 2021
2. [Commision Emplementing Regulation EU 2022/1426](https://eur-lex.europa.eu/eli/reg_impl/2022/1426/oj), 5<sup>th</sup> of August 2022
3. [ISO 26262-1:2018](https://www.iso.org/standard/68383.html); Road vehicles - Functional Safety, December 2018

<sub>_This project is currently maintained by [Imro Brammerloo, advisor at RDW](mailto:ibrammerloo@rdw.nl)._ </sub> 


<!-- Hidden [SUCCESFUL DESKTOP] !-->
