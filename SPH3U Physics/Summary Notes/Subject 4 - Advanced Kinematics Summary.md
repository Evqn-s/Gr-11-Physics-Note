---
type: summary-note
subject: 4
tags:
  - SPH3U/summary
---

[[Unit 1 Kinematics - Master Study Roadmap|← Master Roadmap]] | [[Subject 4 - Advanced Kinematics Guide|Full Guide →]]

# Subject 4: Kinematic Equations & Advanced Kinematics Summary

> [!info] 1-Page Quick Reference
> High-yield summary of the Big 5 equations, vertical free fall under gravity, consecutive interval multi-stage motion, and chase/collision systems for Gr. 11 Physics.

---

### Core Formulas & Constants

* **Acceleration Definition:**
  $$\vec{a} = \frac{\Delta \vec{v}}{\Delta t} = \frac{\vec{v}_f - \vec{v}_i}{\Delta t}$$
  * **Why it works:** Acceleration is the rate at which velocity changes. $Δ\vec{v}$ over $Δ t$ gives how much velocity changes per second.
* **Acceleration Due to Gravity (Earth):**
  $$\vec{g} = 9.81\text{ m/s}^2\text{ [down]} \implies a = -9.81\text{ m/s}^2 \quad (\text{with } [\text{Up}] = +)$$

#### The "Big 5" Kinematic Equations (Uniform Acceleration Only)
*See complete geometric derivations in [[Subject 4 - Advanced Kinematics Guide#Derivation of the "Big 5" Kinematic Equations|Big 5 Derivations]].*

1. $\vec{v}_f = \vec{v}_i + \vec{a}\Delta t$ *(omits $\Delta\vec{d}$)*
   * **Why:** Rearranged from $\vec{a} = \frac{\vec{v}_f - \vec{v}_i}{\Delta t}$ (definition of constant/average acceleration).
2. $\Delta\vec{d} = \left(\frac{\vec{v}_i + \vec{v}_f}{2}\right)\Delta t$ *(omits $\vec{a}$)*
   * **Why:** With constant acceleration, velocity increases linearly. Average velocity is the arithmetic mean $(v_i+v_f)/2$, and displacement = average velocity × time.
3. $\Delta\vec{d} = \vec{v}_i\Delta t + \frac{1}{2}\vec{a}\Delta t^2$ *(omits $\vec{v}_f$)*
   * **Why:** Total displacement is initial velocity part ($v_iΔ t$) plus extra displacement from acceleration. The $rac{1}{2}a(Δ t)^2$ comes from the triangle area under a linear $v$–$t$ curve.
4. $\Delta\vec{d} = \vec{v}_f\Delta t - \frac{1}{2}\vec{a}\Delta t^2$ *(omits $\vec{v}_i$)*
   * **Why:** Symmetric to (3): think in terms of final velocity minus the acceleration-over-time term (area subtracted when starting slower).
5. $v_f^2 = v_i^2 + 2a\Delta d$ *(omits $\Delta t$)*
   * **Why:** Algebraic combination of (1) and (2) — eliminate $Δ t$ to relate $v^2$, $a$, and displacement directly.

---

### High-Yield Problem Solving Checklists

#### 1. The "3-4-5 Rule" Equation Selector ([[Subject 4 - Advanced Kinematics Guide#The "3-4-5 Rule" for Equation Selection|3-4-5 Rule Details]])
- [ ] List all 5 variables: $\vec{v}_i, \vec{v}_f, \vec{a}, \Delta\vec{d}, \Delta t$.
- [ ] Extract **3 knowns** (watch for implied values: "from rest" $\implies v_i = 0$; "stops" $\implies v_f = 0$; "peak" $\implies v = 0$).
- [ ] Identify the **4th variable** (target unknown to solve).
- [ ] Identify the **5th ignored variable** and choose the equation that does not contain it.

#### 2. Vertical Free-Fall Setup ([[Subject 4 - Advanced Kinematics Guide#Vertical Free-Fall Problem Setup|Free-Fall Problem Setup]])
- [ ] Declare direction: `Let [Up] = (+)`, which fixes $a = -9.81\text{ m/s}^2$.
- [ ] Dropped from rest: $v_i = 0$; $\Delta\vec{d} = -h$.
- [ ] Thrown upwards: $v_i > 0$; at top of flight, $v_{\text{top}} = 0\text{ m/s}$.
- [ ] Round-trip symmetry: $t_{\text{up}} = t_{\text{down}}$, and $v_{\text{impact}} = -v_{\text{launch}}$.

#### 3. Consecutive Intervals Multi-Stage Setup ([[Subject 4 - Advanced Kinematics Guide#Consecutive Interval Multi-Stage Algorithm|Consecutive Interval Algorithm]])
- [ ] Divide motion into distinct stages (Stage 1, Stage 2).
- [ ] Solve Stage 1 for final velocity $\vec{v}_{f1}$.
- [ ] **Pass variables:** Set initial velocity of Stage 2: $\vec{v}_{i2} = \vec{v}_{f1}$.
- [ ] Compute displacements separately, then sum: $\Delta\vec{d}_{\text{total}} = \Delta\vec{d}_1 + \Delta\vec{d}_2$.

#### 4. Chase & Collision T-Chart Setup ([[Subject 4 - Advanced Kinematics Guide#Chase & Collision T-Chart & Quadratic Solution Algorithm|Chase and Collision Algorithm]])
- [ ] Build a 2-column T-chart for Object A and Object B.
- [ ] Write position functions: $x_A(t) = x_{A0} + v_{Ai}t + \frac{1}{2}a_A t^2$ and $x_B(t) = x_{B0} + v_{Bi}(t - \Delta t) + \frac{1}{2}a_B(t - \Delta t)^2$.
- [ ] Equate positions: $x_A(t) = x_B(t)$.
- [ ] Rearrange to standard quadratic form: $At^2 + Bt + C = 0$.
- [ ] Solve for positive time using $t = \frac{-B \pm \sqrt{B^2 - 4AC}}{2A}$.

---

### Recommended Video Tutorials
* **Concept of Acceleration:** [EUREKA! Acceleration Episode 2](https://www.youtube.com/watch?v=uCG5jjzMJgU)
* **Lunar Free-Fall:** [Apollo 15 Feather and Hammer Experiment (David Scott)](https://youtu.be/Oo8TaPVsn9Y)
* **Vacuum Chamber Drop:** [BBC / Brian Cox Vacuum Chamber Drop Test](https://www.youtube.com/watch?v=E43-CfukEgs)
* **Chase & Collision Setup:** [Chase and Collision Problem Solving Tutorial](https://www.youtube.com/watch?v=Fw83cXoWTkI)
* *Full catalog:* See [[Unit 1 Physics - Video Directory#Subject 4: Kinematic Equations & Advanced Kinematics|Video Directory: Kinematics]]
