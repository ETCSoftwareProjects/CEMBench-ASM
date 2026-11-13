# CB-003 — Wait... sludge has an age?

**Contributor:** Neslihan Manav Demir  
**Contributor affiliation:** Yıldız Technical University, Department of Environmental Engineering  
**Contributor e-mail:** nmanav@yildiz.edu.tr  
**Version:** 1.0  
**Version date:** 14 August 2026  
**Required CEMBench ASM version:** 1.0.0 or later  

## Activity Overview

| Field | Value |
|---|---|
| Topic | Sludge retention time control and waste solids production in an activated-sludge process |
| Target students | Undergraduate, beginner level |
| Timing | After PR-002 and after introducing the concepts of waste activated sludge and sludge retention time. |
| Mode of use | In-class activity or homework |
| Guidance level | Guided |
| Estimated time | Approximately 30-40 minutes, excluding any instructor-led discussion |
| Highest Bloom level | Analyze |

## Purpose and Scope

This activity introduces sludge retention time (SRT) as an operating parameter of the activated-sludge process. Students use five different waste activated sludge (WAS) flows  while keeping the reactor dimensions, influent conditions, secondary clarifier, RAS flow, and all other model settings constant. WAS flow is varied to investigate how SRT can be controlled in an operating system. Students calculate SRT from steady-state CEMBench ASM results and examine the relationship between WAS flow and SRT. They then use the same results to calculate waste solids production and specific waste solids production and analyze their relationship with SRT.

## Prerequisites

Basic concepts: activated-sludge treatment, secondary clarification, RAS, WAS, hydraulic retention time, sludge retention time, MLSS, and solids mass flow.

Basic CEMBench ASM skills: creating a project from a template, drawing an activated-sludge topology, defining characterizations and unit properties, defining known-flow links, running Project Check, performing steady-state simulations, and reading steady-state results.

Completion of Activity 002 is recommended.

## Activity Learning Outcomes

- **ALO-1:** The student will be able to calculate sludge retention time and explain how waste activated sludge flow is used to control SRT.
- **ALO-2:** The student will be able to relate sludge retention time to waste solids production and specific waste solids production.

## PO and Bloom Mapping

| Question | ALO | ABET PO | EUR-ACE PO | MÜDEK PO | Bloom Level |
|---|---|---|---|---|---|
| Q1 | ALO-1 | PO-6 | PO-2 | PÇ-1.2 | Understand |
| Q2 | ALO-2 | PO-6 | PO-2 | PÇ-2.2 | Analyze |

**ABET PO justification:**

- **Q1:** The student uses steady-state simulation results to calculate SRT and interpret how waste activated sludge flow controls it. This requires experimentation, data interpretation, and engineering judgment, matching ABET PO-6: “Experimentation, data interpretation, and engineering judgment.”
- **Q2:** The student calculates waste-solids quantities and analyzes their relationship with SRT. This requires the same experimentation, data interpretation, and engineering judgment described by ABET PO-6.

**EUR-ACE PO justification:**

- **Q1:** The student interprets the relationship between WAS flow and SRT using calculated and simulated results. This matches EUR-ACE PO-2, “Engineering Analysis.”
- **Q2:** The student separates waste-solids measures and determines their relationship with SRT. This matches EUR-ACE PO-2, “Engineering Analysis.”

**MÜDEK PO justification:**

- **Q1:** The question applies environmental-engineering knowledge of sludge retention time and waste activated sludge control. This matches MÜDEK PÇ-1.2: “Adequate knowledge of subjects specific to Environmental Engineering.”
- **Q2:** The student selects and applies calculation and modeling methods to relate waste-solids production to SRT. This matches MÜDEK PÇ-2.2: “Ability to select and apply appropriate analysis and modeling methods for this purpose.”

**Bloom level justification:**

- **Q1:** The student applies the SRT calculation and explains how WAS flow controls SRT. This is consistent with Bloom level of Understand: “Explain, interpret, summarize, classify, or compare.”
- **Q2:** The student breaks waste-solids production into related measures and determines their relationship with SRT. This is consistent with Bloom level of Analyze: “Break information into parts and determine relationships.”

## Questions

### Question 1

| Field | Value |
|---|---|
| Estimated time | 20-25 minutes |
| ALO | The student will be able to calculate sludge retention time and explain how waste activated sludge flow is used to control SRT. |
| ABET PO | PO-6 |
| EUR-ACE PO | PO-2 |
| MÜDEK PO | PÇ-1.2 |
| Bloom level | Understand |

#### Question

Using the prescribed activated-sludge topology and operating conditions below, investigate how waste activated sludge (WAS) flow affects sludge retention time (SRT). Perform a separate steady-state simulation for each specified WAS flow rate. For every case, record the MLSS concentration in the aerated reactor and the MLSS concentration entering the Sludge Unit, and calculate the corresponding SRT. Plot SRT against WAS flow and explain how WAS flow can be used to control SRT in an activated-sludge system.

#### Topology and CEMBench ASM Setup

| Item | Value |
|---|---|
| Model template | Introductory S-X Model.cbt |
| Influent — Flow | 100 m<sup>3</sup>/h |
| Pattern | Default Multiplicative |
| Characterization | S<sub>O</sub> = 0 mg/L; S<sub>S</sub> = 250 mg/L; X<sub>H</sub> = 0 mg/L |
| Reactor — Area | 120 m<sup>2</sup> |
| Depth | 5 m |
| Aeration | Constant DO @ 2 mg/L |
| Initial conditions | S<sub>O</sub> = 0 mg/L; S<sub>S</sub> = 5 mg/L; X<sub>H</sub> = 1000 mg/L |
| Clarifier — Area | 200 m<sup>2</sup> |
| Depth | 3 m |
| Inlet layer | 5 |
| RAS flow | 100 m<sup>3</sup>/h |
| WAS flow | 0.5, 1.0, 1.5, 2.0, 2.5 m<sup>3</sup>/h |
| Simulation settings | Steady-state simulation |

#### Topology Figure

![Q1 topology](Activity%20Files/q1-1.png)

#### Instructions

1. Create a new CEMBench ASM project using Introductory S-X Model.cbt.
2. Build the prescribed topology, including the secondary clarifier, RAS line, and WAS line.
3. Define the influent flow, pattern, and characterization given above.
4. Define the aerated reactor with a surface area of 120 m<sup>2</sup> and a depth of 5 m. Confirm that CEMBench ASM calculates a reactor volume of 600 m<sup>3</sup>.
5. Define the reactor initial characterization and set constant DO to 2 mg/L.
6. Define the secondary clarifier and set the RAS flow to 100 m<sup>3</sup>/h.
7. Start with a WAS flow of 0.5 m<sup>3</sup>/h.
8. Run Project Check and perform a steady-state simulation.
9. Record the steady-state MLSS concentration in the aerated reactor and the MLSS concentration entering the Sludge Unit.
10. Calculate the corresponding SRT.
11. Repeat the steady-state simulation for WAS flows of 1.0, 1.5, 2.0, 2.5 m<sup>3</sup>/h. Change only the WAS flow and keep all other project settings unchanged.
12. Record the required MLSS concentrations and calculate SRT for every case.
13. Plot SRT (d) against WAS flow (m<sup>3</sup>/h).
14. Explain the relationship between WAS flow and SRT and describe how an operator can use WAS flow to control SRT.

### Question 2

| Field | Value |
|---|---|
| Estimated time | 10-15 minutes |
| ALO | The student will be able to relate sludge retention time to waste solids production and specific waste solids production. |
| ABET PO | PO-6 |
| EUR-ACE PO | PO-2 |
| MÜDEK PO | PÇ-2.2 |
| Bloom level | Analyze |

#### Question

Using the results obtained in Question 1, determine the amount of waste solids discharged from the system at each WAS flow rate and calculate the specific waste solids production per unit volume of influent wastewater. Use the corresponding SRT values obtained in Question 1 to examine the relationship between SRT and specific waste solids production. No additional CEMBench ASM simulations are required.

#### Topology and CEMBench ASM Setup

| Item | Value |
|---|---|
| Simulation settings | No additional simulation is required. Use the steady-state results obtained in Question 1. |

#### Topology Figure

![Q1 topology](Activity%20Files/q1-1.png)

#### Instructions

1. Use the five WAS-flow cases completed in Q1. Do not perform any additional CEMBench ASM simulations.
2. Transfer the WAS flow, SRT, and Sludge Unit influent MLSS concentration for each case from your Q1 results.
3. For every case, calculate the waste solids production in kg/h using the WAS flow and the MLSS concentration entering the Sludge Unit.
4. Calculate the specific waste solids production in kg solids/m³ influent using the influent flow of 100 m³/h.
5. Complete the results table for all five cases.
6. Plot specific waste solids production against SRT.
7. Examine the resulting relationship and explain how waste solids production changes with SRT.
8. Explain the operational implication of changing SRT in terms of the amount of solids that must be removed from the system.

## Video Guide

No video guide yet.

## Activity Rating

<!-- RATING_START -->
**Not yet rated**  
**Responses:** 0
<!-- RATING_END -->

The public rating will be added after sufficient user feedback has been collected.

## Rate This Activity

If you have completed or reviewed this activity, please provide feedback:

[Rate CB-003]({{FORM_URL}})
