# CB-001 — Think you don't need a clarifier?

**Contributor:** Selami Demir  
**Contributor affiliation:** Yıldız Technical University, Department of Environmental Engineering  
**Contributor e-mail:** seldemir@yildiz.edu.tr  
**Version:** 1.0  
**Version date:** 12 August 2026  
**Required CEMBench ASM version:** 1.0.0 or later  

## Activity Overview

| Field | Value |
|---|---|
| Topic | Biomass retention in activated sludge systems with and without secondary clarification |
| Target students | Undergraduate, beginner level |
| Mode of use | In-class activity or homework |
| Guidance level | Guided |
| Estimated time | Approximately 20 minutes, excluding any instructor-led discussion |

## Purpose and Scope

This activity demonstrates why biomass cannot be retained in a continuous-flow aerated reactor when suspended solids leave directly with the effluent, and how secondary clarification with return activated sludge enables biomass retention. Students work with two prescribed CEMBench ASM topologies and explain the observed biomass behavior in each case.

## Prerequisites

Basic concepts: activated sludge treatment, heterotrophic biomass growth and decay, and continuous-flow completely mixed reactors.
Basic CEMBench ASM skills: creating a project from a template, drawing a topology, defining influent and reactor data, running Project Check, performing a dynamic simulation, and opening dynamic charts/results.

## Activity Learning Outcomes

- **ALO-1:** The student will be able to explain why activated-sludge biomass cannot be retained in a continuous-flow aerated reactor without solids separation and how secondary sedimentation with return activated sludge enables biomass retention.

## PO and Bloom Mapping

| Question | ALO | ABET PO | EUR-ACE PO | MÜDEK PO | Bloom Level |
|---|---|---|---|---|---|
| Q1 | ALO-1 | PO-6 | PO-1 | PÇ-1.2 | Remember |
| Q2 | ALO-1 | PO-6 | PO-1 | PÇ-1.2 | Understand |

**ABET PO justification:**

- **Q1:** The student runs a CEMBench ASM simulation, observes the change in biomass, and uses the result to explain biomass loss. This requires experimentation, data interpretation, and engineering judgment, matching ABET PO-6: “Experimentation, data interpretation, and engineering judgment.”
- **Q2:** The student compares simulation results and interprets the effect of clarification and return activated sludge on biomass retention. This again requires experimentation, data interpretation, and engineering judgment, matching ABET PO-6.

**EUR-ACE PO justification:**

- **Q1:** The student recognizes the relationship between solids discharge and biomass retention in an activated-sludge process. This supports EUR-ACE PO-1, “Knowledge and Understanding.”
- **Q2:** The student explains how secondary clarification and return activated sludge change the biomass-retention mechanism. This supports EUR-ACE PO-1, “Knowledge and Understanding.”

**MÜDEK PO justification:**

- **Q1:** The question applies subject-specific environmental-engineering knowledge about activated sludge, biomass, and solids separation. This matches MÜDEK PÇ-1.2: “Adequate knowledge of subjects specific to Environmental Engineering.”
- **Q2:** The comparison of clarification and return activated sludge also requires subject-specific environmental-engineering knowledge, matching MÜDEK PÇ-1.2.

**Bloom level justification:**

- **Q1 — Remember:** The student is required to recognize the basic reason for biomass loss when solids leave with the effluent. This is consistent with Bloom level of Remember: “Recall or recognize information.”
- **Q2 — Understand:** The student compares two process configurations and explains the role of clarification and return activated sludge. This is consistent with Bloom level of Understand: “Explain, interpret, summarize, classify, or compare.”

## Questions

### Question 1

| Field | Value |
|---|---|
| Estimated time | 10 minutes |
| ALO | The student will be able to explain why activated-sludge biomass cannot be retained in a continuous-flow aerated reactor without solids separation and how secondary sedimentation with return activated sludge enables biomass retention. |
| ABET PO | PO-6 |
| EUR-ACE PO | PO-1 |
| MÜDEK PO | PÇ-1.2 |
| Bloom level | Remember |

#### Question

Using the prescribed topology and operating conditions below, run the dynamic simulation. The reactor receives biodegradable substrate and is continuously aerated, yet the heterotrophic biomass concentration decreases with time. Explain why the biomass decreases and why continuous aeration and substrate supply alone cannot maintain biomass in the system.

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
| Simulation settings | Dynamic simulation; duration 4 months at 240 sec time-steps |

#### Topology Figure

![Q1 topology](Activity%20Files/q1-1.png)

#### Instructions

1. Create a new CEMBench ASM project using the specified model template.
2. Build the prescribed topology shown in the topology figure.
3. Define the influent characterization and flow rate given above.
4. Define the reactor initial characterization and reactor settings.
5. Run Project Check and correct any setup errors.
6. Run the 4-month dynamic simulation.
7. Inspect the time-dependent heterotrophic biomass (X<sub>H</sub>) and TSS behavior.
8. Answer the question using the simulated behavior and the concept of solids retention.

### Question 2

| Field | Value |
|---|---|
| Estimated time | 10 minutes |
| ALO | The student will be able to explain why activated-sludge biomass cannot be retained in a continuous-flow aerated reactor without solids separation and how secondary sedimentation with return activated sludge enables biomass retention. |
| ABET PO | PO-6 |
| EUR-ACE PO | PO-1 |
| MÜDEK PO | PÇ-1.2 |
| Bloom level | Understand |

#### Question

Using the prescribed topology and operating conditions below, run the dynamic simulation. Compare the biomass behavior with that observed in Q1. Explain how the secondary clarifier and return activated sludge (RAS) flow prevent biomass washout and allow heterotrophic biomass to be retained in the system.

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
| Clarifier — Area | 100 m2 |
| Depth | 4 m |
| Inlet layer | 5 |
| RAS flow | 50 m<sup>3</sup>/h |
| Simulation settings | Dynamic simulation; duration 4 months at 240 sec time-steps |

#### Topology Figure

![Q2 topology](Activity%20Files/q2-1.png)

#### Instructions

1. Create a new CEMBench ASM project using the specified model template.
2. Build the prescribed topology shown in the topology figure, including the secondary clarifier and RAS link.
3. Use the same influent flow, influent characterization, pattern, reactor dimensions, aeration setting, and reactor initial conditions as in Question 1.
4. Define the secondary clarifier using the settings given above.
5. Set the RAS flow to 50 m<sup>3</sup>/h and return the clarifier underflow to the aerated reactor.
6. Run Project Check and correct any setup errors.
7. Run the 4-month dynamic simulation using a 240 s time step.
8. Inspect the time-dependent heterotrophic biomass (X<sub>H</sub>) and TSS behavior.
9. Compare the biomass behavior with Question 1 and explain how secondary clarification and sludge return allow biomass to remain in the system.

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

[Rate CB-001](https://docs.google.com/forms/d/e/1FAIpQLSd-fvzFPO2sYr0FNLKhnR3-aXxAxvOvfE0AztIXEI8Z9IXzCQ/viewform)
