# CB-004 — Where did the puppies go, man?

**Contributor:** Neslihan Manav Demir  
**Contributor affiliation:** Yıldız Technical University, Department of Environmental Engineering  
**Contributor e-mail:** nmanav@yildiz.edu.tr  
**Version:** 1.0  
**Version date:** 2 September 2026  
**Required CEMBench ASM version:** 1.0.0 or later  

## Activity Overview

| Field | Value |
|---|---|
| Topic | Model yield, observed yield, and biomass decay in activated sludge systems |
| Target students | Undergraduate, beginner-to-intermediate level |
| Mode of use | In-class activity or homework |
| Guidance level | Guided |
| Estimated time | Approximately 45-50 minutes, excluding any instructor-led discussion |

## Purpose and Scope

This activity investigates the distinction between the model yield coefficient and the observed yield of an activated sludge process. Students perform controlled steady-state simulations in which the model yield coefficient and the specific decay rate are varied independently. For each case, they calculate observed yield and sludge retention time from simulated substrate and biomass results. SRT is used as a comparison variable when interpreting changes in observed yield, allowing students to examine whether differences among the simulation cases can be associated with changes in solids retention. The activity is designed so that students infer the relationships from their own simulation results and calculations rather than being given the expected trends.

## Prerequisites

Basic concepts: activated sludge treatment, substrate removal, biomass growth, yield coefficient, endogenous decay, and steady-state mass balance.
Basic CEMBench ASM skills: creating a project from a template, constructing a prescribed process topology, entering operating conditions, editing model parameters, running Project Check, performing steady-state simulations, and reading reactor, effluent, and Sludge Unit results.

## Activity Learning Outcomes

- **ALO-1:** The student will be able to calculate observed yield and analyze its relationship with the specified model yield coefficient using steady-state simulation results and SRT comparisons.
- **ALO-2:** The student will be able to analyze the effect of the specific decay rate on observed yield while accounting for possible changes in solids retention.

## PO and Bloom Mapping

| Question | ALO | ABET PO | EUR-ACE PO | MÜDEK PO | Bloom Level |
|---|---|---|---|---|---|
| Q1 | ALO-1 | PO-6 | PO-2 | PÇ-5.4 | Analyze |
| Q2 | ALO-2 | PO-6 | PO-2 | PÇ-5.4 | Analyze |

**ABET PO justification:**

- **Q1:** The student conducts controlled steady-state simulations, calculates observed yield and SRT, and interprets the relationship between model yield and observed yield. This requires experimentation, data interpretation, and engineering judgment, matching ABET PO-6: “Experimentation, data interpretation, and engineering judgment.”
- **Q2:** The student varies the specific decay rate, compares observed yield and SRT results, and evaluates competing explanations. This also matches ABET PO-6.

**EUR-ACE PO justification:**

- **Q1:** The student analyzes how model yield, observed yield, and SRT are related across multiple simulation cases. This matches EUR-ACE PO-2, “Engineering Analysis.”
- **Q2:** The student analyzes the effect of decay rate and tests whether changes in SRT can explain the observed response. This matches EUR-ACE PO-2, “Engineering Analysis.”

**MÜDEK PO justification:**

- **Q1:** The student analyzes and interprets results from a controlled investigation of yield and solids retention. This matches MÜDEK PÇ-5.4: “Ability to analyze and interpret experimental results for the investigation of complex engineering problems or discipline-specific research topics.”
- **Q2:** The student analyzes and interprets the results of a second controlled investigation in which decay rate is varied. This also matches MÜDEK PÇ-5.4.

**Bloom level justification:**

- **Q1:** The student separates model yield, observed yield, and SRT, compares the cases, and determines their relationships. This is consistent with the Lists definition of Analyze: “Break information into parts and determine relationships.”
- **Q2:** The student separates the effect of decay rate from possible SRT changes and uses the results to evaluate the relationship. This is also consistent with the Lists definition of Analyze.

## Questions

### Question 1

| Field | Value |
|---|---|
| Estimated time | 20 minutes |
| ALO | The student will be able to calculate observed yield and analyze its relationship with the specified model yield coefficient using steady-state simulation results and SRT comparisons. |
| ABET PO | PO-6 |
| EUR-ACE PO | PO-2 |
| MÜDEK PO | PÇ-5.4 |
| Bloom level | Analyze |

#### Question

Keep the specific decay rate constant at k<sub>d</sub>=0.06 d<sup>-1</sup> and vary only the model yield coefficient, Y. For each case, calculate the observed yield and sludge retention time (SRT). Compare the results and explain how the model yield coefficient is related to the observed yield. Use the calculated SRT values to assess whether changes in solids retention could account for the observed differences.

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
| Initial conditions | S<sub>O</sub> = 2 mg/L; S<sub>S</sub> = 5 mg/L; X<sub>H</sub> = 1000 mg/L |
| Clarifier — Area | 200 m<sup>2</sup> |
| Depth | 3 m |
| Inlet layer | 5 |
| RAS flow | 100 m<sup>3</sup>/h |
| WAS flow | 1.5 m<sup>3</sup>/h |
| Parameter values | Y = 0.4, 0.5, 0.6 mg VSS/mg ucBOD. All other parameters at their defaults. |
| Simulation settings | Steady-state simulation |

#### Topology Figure

![Q1 topology](Activity%20Files/q1-1.png)

#### Instructions

1. Use the prescribed CEMBench ASM project, topology, and operating conditions. Fix k<sub>d</sub> at 0.06 d<sup>-1</sup>.
2. Perform steady-state simulations for Y = 0.4, 0.5, 0.6 mg VSS/mg ucBOD. Change only Y.
3. For each case, record steady-state effluent substrate concentration (S<sub>e</sub>), and biomass concentration in reactor (X<sub>H,R</sub>), Effluent (X<sub>H,E</sub>), and Sludge Unit (X<sub>H,W</sub>).
4. Calculate substrate removal rate (P<sub>S</sub>):\
P<sub>S</sub> = Q<sub>in</sub>(S<sub>0</sub>-S<sub>e</sub>)\
where Q<sub>in</sub> is influent flowrate.
5. Calculate observed biomass output rate (P<sub>B</sub>) as the sum of biomass leaving the system through Effluent and Sludge Unit. Use the following formula:\
P<sub>B</sub> = Q<sub>W</sub>*X<sub>H,W</sub> + (Q<sub>in</sub>-Q<sub>W</sub>)X<sub>H,E</sub>\
where Q<sub>W</sub> is the WAS flowrate.
6. Calculate sludge retention time (SRT):\
SRT = V<sub>R</sub>X<sub>H,R</sub>/(Q<sub>W</sub>X<sub>H,W</sub>) 
7. Calculate the observed yield (Y<sub>obs</sub>) as the ratio of observed biomass output rate and the substrate removal rate:\
Y<sub>obs</sub> = P<sub>B</sub>/P<sub>S</sub>
8. Complete the results table and plot Y<sub>obs</sub> against Y.
9. Compare calculated SRT values before interpreting the observed-yield trend.
10. Answer the question using your numerical results and calculations.

### Question 2

| Field | Value |
|---|---|
| Estimated time | 25-30 minutes |
| ALO | The student will be able to analyze the effect of the specific decay rate on observed yield while accounting for possible changes in solids retention. |
| ABET PO | PO-6 |
| EUR-ACE PO | PO-2 |
| MÜDEK PO | PÇ-5.4 |
| Bloom level | Analyze |

#### Question

Keep the model yield coefficient constant at 0.60 mg VSS/mg ucBOD and vary only the specific decay rate, k<sub>d</sub>. For each case, calculate the observed yield and sludge retention time (SRT). Compare the results and explain how the specific decay rate affects the observed yield. Use the calculated SRT values to assess whether changes in solids retention could account for the observed differences.

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
| Initial conditions | S<sub>O</sub> = 2 mg/L; S<sub>S</sub> = 5 mg/L; X<sub>H</sub> = 1000 mg/L |
| Clarifier — Area | 200 m<sup>2</sup> |
| Depth | 3 m |
| Inlet layer | 5 |
| RAS flow | 100 m<sup>3</sup>/h |
| WAS flow | 1.5 m<sup>3</sup>/h |
| Parameter values | Y = 0.6 mg VSS/mg ucBOD and k<sub>d</sub> = 0.02, 0.06, 0.12 d<sup>-1</sup>. All other parameters at their defaults. |
| Simulation settings | Steady-state simulation |

#### Topology Figure

![Q2 topology](Activity%20Files/q2-1.png)

#### Instructions

1. Use the same CEMBench ASM project and operating conditions as in Question 1. Fix Y at 0.6 mg VSS/mg ucBOD.
2. Perform steady-state simulations for k<sub>d</sub> = 0.02, 0.06, and 0.12 d<sup>-1</sup>. Change only k<sub>d</sub>.
3. For each case, record steady-state effluent substrate concentration (S<sub>e</sub>), and biomass concentration in reactor (X<sub>H,R</sub>), Effluent (X<sub>H,E</sub>), and Sludge Unit (X<sub>H,W</sub>).
4. Calculate substrate removal rate (P<sub>S</sub>):\
P<sub>S</sub> = Q<sub>in</sub>(S<sub>0</sub>-S<sub>e</sub>)
where Q<sub>in</sub> is influent flowrate.
5. Calculate observed biomass output rate (P<sub>B</sub>) as the sum of biomass leaving the system through Effluent and Sludge Unit. Use following formula:\
P<sub>B</sub> = Q<sub>W</sub>*X<sub>H,W</sub> + (Q<sub>in</sub>-Q<sub>W</sub>)X<sub>H,E</sub>\
where Q<sub>W</sub> is the WAS flowrate.
6. Calculate sludge retention time (SRT):\
SRT = V<sub>R</sub>X<sub>H,R</sub>/(Q<sub>W</sub>X<sub>H,W</sub>) 
7. Calculate the observed yield (Y<sub>obs</sub>) as the ratio of observed biomass output rate and the substrate removal rate:\
Y<sub>obs</sub> = P<sub>B</sub>/P<sub>S</sub>
8. Complete the results table and plot Y<sub>obs</sub> against k<sub>d</sub>.
9. Compare calculated SRT values before interpreting the observed-yield trend.
10. Determine whether the changes in observed yield are accompanied by substantial changes in SRT. Use this comparison to support your interpretation of the effect of k<sub>d</sub>.

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

[Rate CB-004](https://docs.google.com/forms/d/e/1FAIpQLSdB4x-vvC8dEnMk8E2Eqhb-f_mgZaspf3pkmwba7re8KyAzsA/viewform?usp=publish-editor)
