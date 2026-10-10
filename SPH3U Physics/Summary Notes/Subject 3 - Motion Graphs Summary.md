---
type: summary-note
subject: 3
tags:
  - SPH3U/summary
---

[[Unit 1 Kinematics - Master Study Roadmap|← Master Roadmap]] | [[Subject 3 - Graphical Analysis Guide|Full Guide →]]

# Subject 3: Motion Graphs & Transition Graphs Summary

> [!info] 1-Page Quick Reference
> High-yield summary of position-time ($d-t$), velocity-time ($v-t$), and acceleration-time ($a-t$) graphical analysis and transitions for Gr. 11 Physics.

---

### Key Graphical Analysis Rules

#### 1. Position-Time ($d-t$) Graphs
* **Slope = Velocity ($\vec{v} = \frac{\Delta \vec{d}}{\Delta t}$)**
  - Horizontal line $\implies$ Object at rest ($\vec{v} = 0$).
  - Straight line $\implies$ Constant velocity (uniform motion).
  - Curved line $\implies$ Changing velocity (object accelerating).
* **Secant Slope:** Connects two points $(t_1, d_1)$ and $(t_2, d_2) \implies$ **Average Velocity ($\vec{v}_{\text{avg}}$)**.
* **Tangent Slope:** Line touching curve at single point $\implies$ **Instantaneous Velocity ($\vec{v}_{\text{inst}}$)**.
- *Deeper guide:* See [[Subject 3 - Graphical Analysis Guide#Position-Time (d-t) Graphs|Position-Time Graphs Theory]].

#### 2. Velocity-Time ($v-t$) Graphs
* **Slope = Acceleration ($\vec{a} = \frac{\Delta \vec{v}}{\Delta t}$)**
* **Area Under Curve = Displacement ($\Delta\vec{d}$)**
  - Area above time axis ($v > 0$) $\implies$ Positive displacement ($[+]$, forward).
  - Area below time axis ($v < 0$) $\implies$ Negative displacement ($[-]$, backward).
* **Motion States:**
  - Moving **away from** time axis $\implies$ **Speeding Up** ($\vec{v}$ and $\vec{a}$ have same sign).
  - Moving **toward** time axis $\implies$ **Slowing Down** ($\vec{v}$ and $\vec{a}$ have opposite signs).
  - **Crossing the time axis ($v = 0$)** $\implies$ **Reversing direction**.
- *Deeper guide:* See [[Subject 3 - Graphical Analysis Guide#Velocity-Time Graphs|Velocity-Time Graphs Theory]].

---

### Transition Graph Rules ($d-t \longleftrightarrow v-t \longleftrightarrow a-t$)
$$\begin{array}{ccccc}
d-t & \xrightarrow{\text{take slope}} & v-t & \xrightarrow{\text{take slope}} & a-t \\
d-t & \xleftarrow{\text{take area}} & v-t & \xleftarrow{\text{take area}} & a-t
\end{array}$$

* **Connecting Points on $d-t$ Graphs:**
  - If $v-t$ is horizontal ($\vec{a} = 0$) $\implies$ Connect points with a **straight line**.
  - If $v-t$ has a slope ($\vec{a} \ne 0$) $\implies$ Connect points with a **parabolic curve** (bending up for $+a$, bending down for $-a$).

---

### Step-by-Step Problem Solving Checklists

#### 1. Drawing a Tangent Line Checklist ([[Subject 3 - Graphical Analysis Guide#Tangent Line Construction & Instantaneous Velocity|Tangent Line Guide]])
- [ ] Mark contact point $P(t_0, d_0)$ on the curve.
- [ ] Align clear straightedge to balance angles symmetrically on either side of $P$.
- [ ] Draw an extended straight line across grid intersections.
- [ ] Pick two points $(x_1, y_1)$ and $(x_2, y_2)$ on the line (not on the curve).
- [ ] Compute slope: $\vec{v}_{\text{inst}} = \frac{y_2 - y_1}{x_2 - x_1}$.

#### 2. Calculating $v-t$ Area Checklist ([[Subject 3 - Graphical Analysis Guide#Partitioning Geometric Areas Under v-t Curves|v-t Area Partitioning]])
- [ ] Drop dashed boundary lines from graph corners down to the time axis.
- [ ] Split into standard shapes:
  - Rectangle: $\text{Area} = \Delta t \times v$
  - Triangle: $\text{Area} = \frac{1}{2} \times \Delta t \times \Delta v$
  - Trapezoid: $\text{Area} = \left(\frac{v_i + v_f}{2}\right) \times \Delta t$
- [ ] Sum signed areas: $\Delta\vec{d} = \text{Area}_{\text{above}} - |\text{Area}_{\text{below}}|$.

---

### Recommended Video Tutorials
* **$d-t$ Tangent Slopes:** [How to Draw a Tangent Line Tutorial](https://www.youtube.com/watch?v=-Cii752uUkI)
* **$v-t$ Graph Slopes & Areas:** [Physics Classroom: Determining Slope on a v-t Graph](https://www.physicsclassroom.com/class/1DKin/Lesson-4/Determining-the-Slope-on-a-v-t-Graph)
* **Transition Graphs & Simulation:** [Velocity to Position-Time Tutorial](https://www.youtube.com/watch?v=vPhwP-w5tUU) \| [oPhysics Kinematics Simulation](https://ophysics.com/k4b.html)
* *Full catalog:* See [[Unit 1 Physics - Video Directory#Subject 3: Motion Graphs & Transition Graphs|Video Directory: Motion Graphs]]
