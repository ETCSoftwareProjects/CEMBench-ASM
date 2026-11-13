# CB-002 — How long is long enough?

**Contributor:** Selami Demir  
**Contributor affiliation:** Yıldız Technical University, Department of Environmental Engineering  
**Contributor e-mail:** seldemir@yildiz.edu.tr  
**Version:** 1.0  
**Version date:** 12 August 2026  
**Required CEMBench ASM version:** 1.0.0 or later  

## Activity Overview

| Field | Value |
|---|---|
| Topic | Effect of hydraulic retention time on substrate removal in an activated-sludge process |
| Target students | Undergraduate, beginner level |
| Timing | After the fundamental activated sludge process, RAS and WAS are introduced. |
| Mode of use | In-class activity or homework |
| Guidance level | Guided |
| Estimated time | Approximately 30-40 minutes, excluding any instructor-led discussion |
| Highest Bloom level | Analyze |

## Purpose and Scope

This activity introduces hydraulic retention time (HRT) as an operating and design parameter of an activated-sludge reactor. Students use a fixed activated-sludge topology, while varying only the aerated-reactor volume. For each reactor volume, students calculate HRT, obtain the steady-state effluent substrate concentration using CEMBench ASM, calculate substrate removal efficiency, and examine the relationship between HRT and carbon-removal performance.

## Prerequisites

Basic concepts: activated-sludge treatment, secondary clarification, RAS, WAS, hydraulic retention time, and substrate removal.

Basic CEMBench ASM skills: creating a project from a template, drawing a topology, defining characterizations and unit properties, defining known-flow links, running Project Check, performing a steady-state simulation, and reading steady-state results.

## Activity Learning Outcomes

- **ALO-1:** The student will be able to analyze the effect of reactor hydraulic retention time on steady-state substrate removal using HRT calculations and CEMBench ASM simulation results.

## PO and Bloom Mapping

| Question | ALO | ABET PO | EUR-ACE PO | MÜDEK PO | Bloom Level |
|---|---|---|---|---|---|
| Q1 | ALO-1 | PO-6 | PO-2 | PÇ-4.1 | Analyze |

**ABET PO justification:**

- **Q1:** The student performs several steady-state CEMBench ASM simulations, calculates substrate-removal results, and interprets the relationship between hydraulic retention time and process performance. This requires experimentation, data interpretation, and engineering judgment, matching ABET PO-6: “Experimentation, data interpretation, and engineering judgment.”

**EUR-ACE PO justification:**

- **Q1:** The student breaks the simulation results into HRT and substrate-removal relationships and determines how the variables are related. This matches EUR-ACE PO-2, “Engineering Analysis.”

**MÜDEK PO justification:**

- **Q1:** The student selects and uses CEMBench ASM as a modern engineering tool to model the process, calculate HRT, and analyze the resulting performance. This matches MÜDEK PÇ-4.1: “Ability to develop, select, and use modern techniques and tools required for the analysis and solution of complex problems encountered in engineering practice.”

**Bloom level justification:**

- **Q1:** The student organizes results from multiple simulations, separates the HRT and substrate-removal effects, and determines the relationship between them. This is consistent with Bloom level of Analyze: “Break information into parts and determine relationships.”

## Questions

### Question 1

| Field | Value |
|---|---|
| Estimated time | 30-40 minutes |
| ALO | The student will be able to analyze the effect of reactor hydraulic retention time on steady-state substrate removal using HRT calculations and CEMBench ASM simulation results. |
| ABET PO | PO-6 |
| EUR-ACE PO | PO-2 |
| MÜDEK PO | PÇ4.1 |
| Bloom level | Analyze |

#### Question

Using the prescribed activated-sludge topology and operating conditions below, investigate the effect of hydraulic retention time (HRT) on steady-state substrate removal. Perform a separate steady-state simulation for each specified aerated-reactor surface area, thereby changing the reactor volume while keeping the depth constant. For every case, calculate the reactor HRT, record the effluent readily biodegradable substrate concentration (S<sub>S</sub>), and calculate the substrate removal efficiency. Plot substrate removal efficiency against HRT and explain the relationship observed. Identify the HRT range beyond which further increases in HRT produce only relatively small improvements in substrate removal

#### Topology and CEMBench ASM Setup

| Item | Value |
|---|---|
| Model template | Introductory S-X Model.cbt |
| Influent — Flow | 100 m<sup>3</sup>/h |
| Pattern | Default Multiplicative |
| Characterization | S<sub>O</sub> = 0 mg/L; S<sub>S</sub> = 250 mg/L; X<sub>H</sub> = 0 mg/L |
| Reactor — Area | 10, 20, 40, 60, 80, 120, 160, 200, 400 m<sup>2</sup> |
| Depth | 5 m |
| Aeration | Constant DO @ 2 mg/L |
| Initial conditions | S<sub>O</sub> = 0 mg/L; S<sub>S</sub> = 5 mg/L; X<sub>H</sub> = 1000 mg/L |
| Clarifier — Area | 200 m<sup>2</sup> |
| Depth | 3 m |
| Inlet layer | 5 |
| RAS flow | 100 m<sup>3</sup>/h |
| WAS flow | 1.5 m<sup>3</sup>/h |
| Simulation settings | Steady-state simulation |

#### Topology Figure

![Q1 topology](Activity%20Files/q1-1.png)

#### Instructions

1. Create a new CEMBench ASM project using Introductory S-X Model.cbt.
2. Build the prescribed topology, including the secondary clarifier, RAS line, and WAS line.
3. Define the influent flow, pattern, and characterization given above.
4. Define the aerated-reactor initial characterization, depth, and constant-DO setting.
5. Define the secondary clarifier and set the RAS and WAS flows as specified.
6. Run Project Check and correct any setup errors.
7. Start with an aerated-reactor surface area of 10 m<sup>2</sup>. With a constant depth of 5 m, this corresponds to a reactor volume of 50 m<sup>3</sup>.
8. Record the steady-state effluent SS concentration.
9. Repeat the steady-state simulation for reactor surface areas of 20, 40, 60, 80, 120, 160, 200, and 400 m<sup>2</sup>. Keep the reactor depth at 5 m so that only the reactor volume changes.
10. For every case, obtain the reactor volume calculated by CEMBench ASM and calculate
HRT = V/Q<sub>in</sub>, where Q<sub>in</sub> is the influent flowrate.
11. For every simulation, calculate substrate removal efficiency from the influent and effluent S<sub>S</sub> concentrations as follows:
η = (S<sub>0</sub> - S<sub>e</sub>) / S<sub>0</sub> * 100%
where S<sub>0</sub> and S<sub>e</sub> are the effluent substrate concentrations, respectively.
12. Plot substrate removal efficiency (%) against HRT (h).
13. Examine the shape of the curve and identify the HRT range beyond which additional HRT provides only a relatively small improvement in substrate removal.
14. Explain why substrate removal efficiency changes with HRT.

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

[Rate CB-002]({{FORM_URL}})
