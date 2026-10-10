---
type: teaching-guide
subject: 4
tags:
  - SPH3U/kinematics/equations
---

# Subject 4: Kinematic Equations & Advanced Kinematics Guide

> [!info] Quick Navigation
> - **Summary Sheet:** [[Subject 4 - Advanced Kinematics Summary]]
> - **Prerequisite:** [[Subject 3 - Graphical Analysis Guide]]
> - **Master Roadmap:** [[Unit 1 Kinematics - Master Study Roadmap]]

---

## SECTION 1: CORE THEORY & KINEMATIC DERIVATIONS

When an object accelerates uniformly (constant acceleration $\vec{a} = \text{constant}$), its motion can be predicted algebraically using five fundamental kinematic equations. These equations synthesize the graphical principles established in [[Subject 3 - Graphical Analysis Guide#Velocity-Time Graphs|Velocity-Time Graphs]] into powerful algebraic tools.

### Definition of Acceleration & Vector Signs

**Acceleration ($\vec{a}$)** is defined as the time rate of change of velocity:
$$\vec{a} = \frac{\Delta \vec{v}}{\Delta t} = \frac{\vec{v}_f - \vec{v}_i}{\Delta t}$$

* Standard SI Unit: $\text{m/s}^2$ (read as "metres per second per second").
* Vector Nature: Acceleration has both magnitude and spatial direction.

#### Acceleration Vector Signs vs. Speed Changes
A common misconception in introductory physics is assuming that negative acceleration always means "slowing down." In reality, whether an object speeds up or slows down depends entirely on the **relative signs of velocity and acceleration**:

| Velocity Sign | Acceleration Sign | Physical Motion | Explanation |
| :---: | :---: | :---: | :--- |
| $+$ (East) | $+$ (East) | **Speeding Up** | $\vec{a}$ pulls in same direction as $\vec{v}$ |
| $+$ (East) | $-$ (West) | **Slowing Down** | $\vec{a}$ opposes current velocity |
| $-$ (West) | $-$ (West) | **Speeding Up** | $\vec{a}$ pulls in same direction as $\vec{v}$ |
| $-$ (West) | $+$ (East) | **Slowing Down** | $\vec{a}$ opposes current velocity |

> [!question] Why Can Negative Acceleration Mean Speeding Up?
> "Negative" only means "opposite to the chosen positive direction" — it is a label, not a judgment about faster or slower. Speeding up and slowing down depend on whether the force (acceleration) is *helping or fighting* the current velocity. A car moving west ($v = -20\text{ m/s}$) that experiences westward acceleration ($a = -3\text{ m/s}^2$) is getting faster in the westward direction — both $v$ and $a$ are negative, so $|v|$ increases. It's only when they have opposite signs that $|v|$ decreases. **The magnitude of velocity ($|v|$), not the sign, determines speed.**

> [!tip] Direction Rule for Acceleration
> - **Speeding Up:** Velocity vector and Acceleration vector point in the **SAME** direction ($\vec{v}$ and $\vec{a}$ share identical algebraic signs).
> - **Slowing Down:** Velocity vector and Acceleration vector point in **OPPOSITE** directions ($\vec{v}$ and $\vec{a}$ have opposite algebraic signs).

---

### Derivation of the "Big 5" Kinematic Equations

All five kinematic equations apply strictly under **uniformly accelerated motion** ($\vec{a} = \text{constant}$) and are derived directly from the linear geometry and shaded areas of [[Subject 3 - Graphical Analysis Guide#Velocity-Time Graphs|Velocity-Time Graphs]].

> [!question] Why Are There Exactly 5 Kinematic Equations — No More, No Less?
> There are exactly **5 kinematic variables** in uniform acceleration: $\{\vec{v}_i,\ \vec{v}_f,\ \vec{a},\ \Delta\vec{d},\ \Delta t\}$. Any solvable problem gives you 3 of these and asks for a 4th. There are exactly $\binom{5}{1} = 5$ ways to choose which one variable to leave out of a four-variable equation. Each of the Big 5 leaves out a *different* one of the five variables. So the set of 5 equations is the **mathematically complete and minimal set** that covers every possible combination of 4 variables from the 5. You couldn't solve every possible problem with fewer than 5 equations, and you don't need more than 5.

![[attachments/displacement_formula_vt_graph.png]]
*Above: The v-t trapezoid from which all five kinematic equations are geometrically derived. Image: Wikimedia Commons*

#### Equation 1: Velocity as a Function of Time (from Slope)
By definition, the slope of a linear $v-t$ graph is constant acceleration:
$$\vec{a} = \frac{\vec{v}_f - \vec{v}_i}{\Delta t}$$
Multiply both sides by $\Delta t$ and isolate $\vec{v}_f$:
$$\vec{a}\Delta t = \vec{v}_f - \vec{v}_i \implies \vec{v}_f = \vec{v}_i + \vec{a}\Delta t \tag{1}$$
*(This equation does not contain displacement $\Delta\vec{d}$).*

#### Equation 2: Displacement from Average Velocity (Trapezoid Area)
The area under the linear $v-t$ graph between $t = 0$ and $\Delta t$ forms a trapezoid whose parallel sides have lengths $\vec{v}_i$ and $\vec{v}_f$, and whose height is $\Delta t$:
$$\text{Area} = \Delta\vec{d} = \left(\frac{\vec{v}_i + \vec{v}_f}{2}\right)\Delta t \tag{2}$$
*(This equation does not contain acceleration $\vec{a}$).*

> [!question] Why Is the Average of $v_i$ and $v_f$ Used for Displacement Here?
> When acceleration is constant, velocity changes at a **steady, uniform rate** from $v_i$ to $v_f$. The average value of a quantity that changes linearly is simply the midpoint: $\bar{v} = (v_i + v_f)/2$. Geometrically, this midpoint velocity is the height of a rectangle with the same area as the trapezoid formed by the actual (linearly changing) velocity profile. So displacement = $\bar{v} \times \Delta t$ = trapezoid area. **This formula only works for constant acceleration** — if acceleration varied, the midpoint would not equal the true average velocity.

#### Equation 3: Displacement as a Function of Initial Velocity & Acceleration
Decompose the trapezoid into a lower rectangle (height $\vec{v}_i$, width $\Delta t$) plus an upper triangle (base $\Delta t$, height $\vec{v}_f - \vec{v}_i$):
$$\Delta\vec{d} = \text{Area}_{\text{rect}} + \text{Area}_{\text{tri}} = \vec{v}_i\Delta t + \frac{1}{2}(\vec{v}_f - \vec{v}_i)\Delta t$$
From Equation (1), we know that $(\vec{v}_f - \vec{v}_i) = \vec{a}\Delta t$. Substituting this in:
$$\Delta\vec{d} = \vec{v}_i\Delta t + \frac{1}{2}(\vec{a}\Delta t)\Delta t \implies \Delta\vec{d} = \vec{v}_i\Delta t + \frac{1}{2}\vec{a}\Delta t^2 \tag{3}$$
*(This equation does not contain final velocity $\vec{v}_f$).*

> [!question] Why Does This Equation Have a $\Delta t^2$ Term — Where Does It Come From?
> The $\Delta t^2$ term comes from the **upper triangle** of the trapezoid (the velocity gained due to acceleration). The triangle's base is $\Delta t$ and its height is $\vec{a}\Delta t$ (how much velocity changes over that time). Area = $\frac{1}{2} \times \Delta t \times \vec{a}\Delta t = \frac{1}{2}\vec{a}\Delta t^2$. The squaring of time is a geometric consequence of the fact that velocity is *linearly increasing* in time (due to constant $a$), and the accumulation of a linearly-growing quantity over time grows as $t^2$. This is why accelerating objects cover **disproportionately more ground** as time goes on — not just twice as far in twice the time, but *four times* as far.

#### Equation 4: Displacement as a Function of Final Velocity & Acceleration
Alternatively, express the area as the bounding outer rectangle (dimensions $\vec{v}_f \times \Delta t$) minus the upper triangle above the line ($\frac{1}{2}\vec{a}\Delta t^2$):
$$\Delta\vec{d} = \vec{v}_f\Delta t - \frac{1}{2}\vec{a}\Delta t^2 \tag{4}$$
*(This equation does not contain initial velocity $\vec{v}_i$).*

#### Equation 5: Timeless Equation Relating Velocities and Displacement
To eliminate time $\Delta t$, rearrange Equation (1) for time: $\Delta t = \frac{\vec{v}_f - \vec{v}_i}{\vec{a}}$.
Substitute this into Equation (2):
$$\Delta\vec{d} = \left(\frac{\vec{v}_f + \vec{v}_i}{2}\right)\left(\frac{\vec{v}_f - \vec{v}_i}{\vec{a}}\right) = \frac{v_f^2 - v_i^2}{2a}$$
Multiply both sides by $2a$ and rearrange:
$$2a\Delta d = v_f^2 - v_i^2 \implies v_f^2 = v_i^2 + 2a\Delta d \tag{5}$$
*(This equation does not contain time $\Delta t$).*

> [!question] Why Is Equation 5 So Useful — When Would You Actually Pick It?
> Equation 5 eliminates time entirely — use it when **time is neither given nor asked for**. Classic situations: "A car travelling at 30 m/s brakes to rest over 45 m. Find the deceleration." Time is never mentioned. Trying to solve with time as an intermediary forces you to find it first (one extra equation, more work). Equation 5 connects $v_i$, $v_f$, $a$, and $\Delta d$ directly. It also emerges beautifully from algebra — the $(v_f + v_i)(v_f - v_i)$ product is a **difference of squares**: $v_f^2 - v_i^2$, which is why the equation naturally leads to a "squares" form.

---

### Vertical Free-Fall Motion

Free fall is vertical motion in which gravity is the sole force acting upon an object (ignoring air resistance).

* **Acceleration due to Gravity ($g$):** On the surface of Earth, every free-falling object experiences a constant downward acceleration:
  $$\vec{g} = 9.81\text{ m/s}^2\text{ [down]}$$
* **Direction Convention:** Standard convention declares $[\text{Up}] = (+)$. Therefore, acceleration is substituted as:
  $$\vec{a} = -9.81\text{ m/s}^2$$

> [!question] Why Does Every Object Fall at the Same Rate Regardless of Mass?
> This was first demonstrated definitively by Galileo (apocryphal story: dropping balls from the Leaning Tower of Pisa). The gravitational force on an object is $F = mg$ — proportional to its mass. Newton's second law says $F = ma$, so $ma = mg$, which gives $a = g$. The mass cancels exactly! Whether the object is a feather or a cannonball, the same $g = 9.81\text{ m/s}^2$ applies (in vacuum). In air, drag forces DO depend on shape and mass, which is why a feather floats — but that's air resistance, not gravity.

> [!question] Why Is Velocity Zero at the Peak of a Throw But Acceleration Is Still 9.81 m/s²?
> This confuses nearly every student. At the peak, the object has momentarily **stopped moving vertically** — $v = 0$ — but gravity hasn't stopped. Gravity is a constant force that always pulls downward at $9.81\text{ m/s}^2$, regardless of what the object is doing. Think of it this way: one instant before the peak, the ball is moving up but slowing. One instant after the peak, it's moving down and speeding up. Gravity is the agent causing this velocity change, and it never pauses. If gravity switched off at the peak ($a = 0$ at $v = 0$), the ball would float there forever — which doesn't happen.

#### Core Physical Principles of Vertical Free Fall:
1. **Peak Height Condition:** At the absolute highest point of a vertical throw, the object momentarily halts before reversing direction:
   $$\vec{v}_{\text{top}} = 0\text{ m/s}$$
   *(Note: Even though velocity is zero at the peak, acceleration is still $-9.81\text{ m/s}^2$).*
2. **Trajectory Symmetry:** For symmetrical launches (where the object returns to its release height):
   - Time of ascent equals time of descent: $t_{\text{up}} = t_{\text{down}} = \frac{1}{2}t_{\text{total}}$.
   - Impact speed equals release speed: $|\vec{v}_{\text{impact}}| = |\vec{v}_{\text{launch}}|$ but with opposite sign ($\vec{v}_{\text{impact}} = -\vec{v}_{\text{launch}}$).
   - Net displacement over the complete flight is zero: $\Delta\vec{d}_{\text{round trip}} = 0\text{ m}$.

> [!question] Why Is the Trajectory Perfectly Symmetric?
> Symmetry arises because the acceleration ($g = 9.81\text{ m/s}^2$ downward) is **constant throughout the entire flight** — both going up and coming down. Going up, $g$ decelerates the ball by $9.81\text{ m/s}$ each second. Coming down from the same height, $g$ accelerates it by $9.81\text{ m/s}$ each second. The process is completely time-reversible — like a video played backwards. The only way symmetry would break is if a non-constant force acted during part of the flight (e.g., if you threw it from a moving platform, or there was wind).

---

### Consecutive Interval Motion (Multi-Stage Kinematics)

Consecutive interval problems describe scenarios where an object's motion changes regimes across consecutive stages (e.g., a car accelerates from rest for $5\text{ s}$, cruises at constant velocity for $10\text{ s}$, then brakes uniformly to a stop).

> [!question] Why Can't You Just Use One Kinematic Equation for the Whole Journey?
> The Big 5 equations are derived assuming **constant acceleration throughout the entire interval**. If acceleration changes partway through (e.g., the car stops accelerating and cruises), the mathematics breaks down — $a$ is no longer a single constant, so you can't use any one equation for the full trip. You must break the journey at every point where acceleration changes and apply the equations separately to each segment with its own constant $a$. The **coupling condition** ($v_{f,\text{Stage 1}} = v_{i,\text{Stage 2}}$) stitches the segments together.

#### Coupling Principles:
* **Inter-Stage Velocity Handoff:** The instantaneous velocity at the very end of Stage 1 becomes the initial velocity at the start of Stage 2:
  $$\vec{v}_{f,\text{Stage 1}} = \vec{v}_{i,\text{Stage 2}}$$
* **Cumulative Displacement:** Total displacement is the vector sum of individual stage displacements:
  $$\Delta\vec{d}_{\text{total}} = \Delta\vec{d}_1 + \Delta\vec{d}_2 + \dots$$
* **Cumulative Time:** Total elapsed duration is the scalar sum of stage durations:
  $$\Delta t_{\text{total}} = \Delta t_1 + \Delta t_2 + \dots$$

![[attachments/consecutive_intervals_profile.svg]]

---

### Two-Body Motion: Chase & Collision Problems

Chase and collision problems involve two separate bodies ($A$ and $B$) moving independently along the same coordinate axis.

* **Chase Scenario:** Object $A$ and Object $B$ travel in the same direction. Object $B$ starts behind Object $A$ (or starts later) but travels faster, eventually overtaking Object $A$.
* **Collision Scenario:** Object $A$ and Object $B$ travel toward one another from separate starting points until they meet.

#### Fundamental Mathematical Condition:
At the exact instant of intercept or collision ($t_{\text{meet}}$), both objects must occupy the **exact same coordinate position**:
$$x_A(t) = x_B(t)$$

* **Head Starts & Initial Position Offsets:** If Object $A$ begins with an initial spatial lead $d_{\text{lead}}$, write $x_A(0) = d_{\text{lead}}$ while $x_B(0) = 0$.
* **Delayed Clock Starts:** If Object $B$ begins moving $\Delta t_{\text{delay}}$ seconds after Object $A$:
  $$t_A = t \qquad \text{and} \qquad t_B = t - \Delta t_{\text{delay}} \quad (\text{for } t \ge \Delta t_{\text{delay}})$$

> [!question] Why Does the Chase/Collision Problem Always Produce a Quadratic Equation?
> Each object's position is described by $x(t) = x_0 + v_i t + \frac{1}{2}at^2$ — a **polynomial in $t$ with a $t^2$ term** (if the object accelerates). Setting the two position functions equal:
> $$x_{A0} + v_{Ai}\,t + \tfrac{1}{2}a_A t^2 = x_{B0} + v_{Bi}\,t + \tfrac{1}{2}a_B t^2$$
> Rearranging brings all terms to one side:
> $$\tfrac{1}{2}(a_A - a_B)t^2 + (v_{Ai} - v_{Bi})t + (x_{A0} - x_{B0}) = 0$$
> This is exactly $At^2 + Bt + C = 0$ — a quadratic. **The $t^2$ term appears because at least one object accelerates.** If both objects moved at constant speed (no acceleration), the $t^2$ terms would vanish and you'd get a linear equation with one solution. When there's acceleration, the position functions are parabolas that can intersect at 0, 1, or 2 points — hence 0, 1, or 2 time solutions from the quadratic formula.

> [!question] What Do the Two Roots of the Quadratic Mean Physically?
> The quadratic formula typically gives two time values. In a chase scenario:
> - The **first (smaller) root** is the moment the faster object catches up to the slower one — the actual intercept you're solving for.
> - The **second (larger) root** is a second crossing: after the faster object passes the slower one, if it then decelerates and the slower one is still moving, they may meet again. Whether this is physically meaningful depends on the specific problem context.
> - A **negative root** means the crossing would have occurred before the clock started — physically extraneous, discard it.

![[attachments/chase_collision_intercept.svg]]

---

## SECTION 2: EMBEDDED INSTRUCTIONAL VIDEOS

![[Unit 1 Physics - Video Directory#Subject 4: Kinematic Equations & Advanced Kinematics]]

---

## SECTION 3: HOW-TO WORKBOOK PROBLEM SOLVING GUIDES

This section details systematic problem-solving algorithms for the exercise sets in `Last Kinematics WB.pdf` (Pages 1–18).

### The "3-4-5 Rule" for Equation Selection
*(Last Kinematics Workbook, Pages 1–4)*

Every uniformly accelerated motion problem involves 5 kinematic variables:
$$\{\vec{v}_i, \vec{v}_f, \vec{a}, \Delta\vec{d}, \Delta t\}$$

> [!question] Why Does the "3-4-5 Rule" Work Every Time?
> It works because the Big 5 equations are a **complete and non-redundant system**: each equation uniquely omits one of the five variables. Given 3 knowns and 1 unknown (4 variables total), there is always exactly one equation that contains precisely those 4 variables and omits the 5th (the irrelevant one). This is guaranteed by the mathematical structure: you need at least as many independent equations as unknowns, and the Big 5 form exactly such a system for uniform acceleration. The rule is a structured shortcut for identifying which equation that is.

#### The 3-4-5 Strategy:
* **3 Knowns:** Any solvable 1D uniform acceleration problem provides exactly 3 known variables (either stated explicitly or implied by key phrases).
* **4th Variable:** Identify the single variable you are tasked with solving for.
* **5th Variable:** Identify the variable that is neither given nor requested (the "ignored" variable).

#### Variable Selection Lookup Matrix:
Select the equation that completely omits the "ignored" variable:

| Missing / Ignored Variable | Required Kinematic Equation |
| :---: | :--- |
| $\Delta\vec{d}$ (Displacement) | $\vec{v}_f = \vec{v}_i + \vec{a}\Delta t$ |
| $\vec{a}$ (Acceleration) | $\Delta\vec{d} = \left(\frac{\vec{v}_i + \vec{v}_f}{2}\right)\Delta t$ |
| $\vec{v}_f$ (Final Velocity) | $\Delta\vec{d} = \vec{v}_i\Delta t + \frac{1}{2}\vec{a}\Delta t^2$ |
| $\vec{v}_i$ (Initial Velocity) | $\Delta\vec{d} = \vec{v}_f\Delta t - \frac{1}{2}\vec{a}\Delta t^2$ |
| $\Delta t$ (Time) | $v_f^2 = v_i^2 + 2a\Delta d$ |

#### Implied Physics Phrases:
- *"Starts from rest"* $\implies \vec{v}_i = 0\text{ m/s}$
- *"Comes to a complete stop"* $\implies \vec{v}_f = 0\text{ m/s}$
- *"Reaches maximum height"* $\implies \vec{v}_{\text{top}} = 0\text{ m/s}$
- *"Dropped"* $\implies \vec{v}_i = 0\text{ m/s}$ and $\vec{a} = 9.81\text{ m/s}^2\text{ [down]}$

---

### Well-Labelled Line Diagram Setup Protocol
*(Last Kinematics Workbook, Pages 1–4)*

Before writing any equation, construct a clear line diagram:

1. **Draw Motion Vector Arrow:** Draw a prominent arrow representing the displacement path.
2. **Label the Sign Convention:** Declare direction above the diagram: $\text{Let } [\text{Forward}] = (+)$.
3. **Number Boundary States:** Label the start as $(1)$ and end as $(2)$.
4. **Attach Knowns and Unknowns:**
   - At state $(1)$, write $\vec{v}_i = \dots$
   - At state $(2)$, write $\vec{v}_f = \dots$
   - Along the arrow body, write $\Delta\vec{d} = \dots$, $\vec{a} = \dots$, and $\Delta t = \dots$
5. **Substitute Signed Values:** Insert all quantities into the selected equation respecting signs.

---

### Vertical Free-Fall Problem Setup
*(Last Kinematics Workbook, Pages 5–8)*

For vertical gravity problems, adopt the standard sign convention: **Let $[\text{Up}] = (+)$**, which fixes $\vec{a} = -9.81\text{ m/s}^2$.

#### Three Standard Free-Fall Archetypes:
1. **Object Dropped from Rest:**
   - $\vec{v}_i = 0\text{ m/s}$
   - $\vec{a} = -9.81\text{ m/s}^2$
   - Displacement is downward: $\Delta\vec{d} = -h$
   - Use $\Delta\vec{d} = \frac{1}{2}\vec{a}\Delta t^2 \implies -h = -\frac{1}{2}(9.81)\Delta t^2 \implies \Delta t = \sqrt{\frac{2h}{9.81}}$
2. **Object Thrown Upward from Ground and Landing on Ground:**
   - $\vec{v}_i > 0$
   - $\vec{a} = -9.81\text{ m/s}^2$
   - Full flight displacement: $\Delta\vec{d} = 0\text{ m}$
   - Peak height: set $\vec{v}_f = 0\text{ m/s}$ and use $v_f^2 = v_i^2 + 2a\Delta d$ to find maximum height $h_{\text{max}} = \frac{v_i^2}{2(9.81)}$.
3. **Object Thrown Upward from a Cliff Edge / Building:**
   - $\vec{v}_i > 0$
   - Net displacement upon reaching the ground below the cliff is negative: $\Delta\vec{d} = -h_{\text{cliff}}$
   - Set up the quadratic: $-h_{\text{cliff}} = v_i\Delta t - \frac{1}{2}(9.81)\Delta t^2$
   - Rearrange to standard form: $4.905\Delta t^2 - v_i\Delta t - h_{\text{cliff}} = 0$ and solve for positive time $t$.

> [!question] Why Does Throwing from a Cliff Produce a Quadratic Even With One Object?
> When the object lands *below* the launch point, $\Delta\vec{d} \ne 0$, so you cannot use the neat symmetry tricks of the "equal height" case. Using Equation (3): $\Delta\vec{d} = v_i\Delta t + \frac{1}{2}(-9.81)\Delta t^2$. The $\Delta t^2$ term is non-cancellable because you have a specific nonzero $\Delta\vec{d}$ — you can't isolate $\Delta t$ linearly. Rearranging gives $4.905\Delta t^2 - v_i\Delta t - h = 0$ — a quadratic in $\Delta t$. The two roots correspond to: the positive time (object thrown upward, rises, then falls all the way down to the base), and a negative time (mathematically valid, but physically represents the past — where the ball would have been if launched from below).

---

### Consecutive Interval Multi-Stage Algorithm
*(Last Kinematics Workbook, Pages 9–12)*

When motion involves multiple stages (e.g., accelerating, then constant speed, then braking):

#### Step-by-Step Procedure:
1. **Stage 1 (Acceleration Phase):**
   - Identify $\vec{v}_{i1}, \vec{a}_1, \Delta t_1$ (or $\Delta\vec{d}_1$).
   - Solve for final velocity: $\vec{v}_{f1} = \vec{v}_{i1} + \vec{a}_1\Delta t_1$.
   - Solve for stage displacement: $\Delta\vec{d}_1 = \vec{v}_{i1}\Delta t_1 + \frac{1}{2}\vec{a}_1\Delta t_1^2$.
2. **The Coupling Handoff:**
   - Set $\vec{v}_{i2} = \vec{v}_{f1}$.
3. **Stage 2 (Uniform Motion or Secondary Acceleration Phase):**
   - If uniform motion ($\vec{a}_2 = 0$), use $\Delta\vec{d}_2 = \vec{v}_{i2}\Delta t_2$.
   - If accelerating, use the 3-4-5 rule with $\vec{v}_{i2}$.
4. **Synthesize Totals:**
   $$\Delta\vec{d}_{\text{total}} = \Delta\vec{d}_1 + \Delta\vec{d}_2 + \dots \qquad \Delta t_{\text{total}} = \Delta t_1 + \Delta t_2 + \dots$$
   $$v_{\text{avg, journey}} = \frac{d_{\text{total}}}{\Delta t_{\text{total}}}$$

---

### Chase & Collision T-Chart & Quadratic Solution Algorithm
*(Last Kinematics Workbook, Pages 13–18)*

For problems with two independently moving objects:

#### Step 1: Construct a Two-Column T-Chart

| Variable | **Object A** | **Object B** |
| :--- | :--- | :--- |
| Initial position | $x_{A0} = \dots$ | $x_{B0} = \dots$ |
| Initial velocity | $\vec{v}_{Ai} = \dots$ | $\vec{v}_{Bi} = \dots$ |
| Acceleration | $\vec{a}_A = \dots$ | $\vec{a}_B = \dots$ |
| Time variable | $t_A = t$ | $t_B = t - \Delta t_{\text{delay}}$ |

#### Step 2: Formulate Position Functions $x(t)$
Using $x(t) = x_0 + v_i t + \frac{1}{2} a t^2$:
* For Object A: $x_A(t) = x_{A0} + v_{Ai} t + \frac{1}{2} a_A t^2$
* For Object B: $x_B(t) = x_{B0} + v_{Bi} (t - \Delta t_{\text{delay}}) + \frac{1}{2} a_B (t - \Delta t_{\text{delay}})^2$

#### Step 3: Equate Position Functions
Set $x_A(t) = x_B(t)$ and expand all algebraic terms:
$$x_{A0} + v_{Ai} t + \frac{1}{2} a_A t^2 = x_{B0} + v_{Bi}(t - \Delta t) + \frac{1}{2} a_B (t - \Delta t)^2$$

#### Step 4: Collect Terms into Standard Quadratic Form
Move all terms to one side to yield:
$$A t^2 + B t + C = 0$$

> [!tip] Why Collect Into $At^2 + Bt + C = 0$ Form Before Solving?
> The quadratic formula requires the equation to be in standard form with zero on the right side. Moving all terms to one side also helps you **identify the coefficients** $A$, $B$, $C$ clearly, reduces the chance of sign errors, and confirms whether the equation is actually quadratic (if $A = 0$, it's linear and both objects have the same acceleration — use linear solving instead).

#### Step 5: Solve for Intercept Time $t$
Apply the quadratic formula:
$$t = \frac{-B \pm \sqrt{B^2 - 4AC}}{2A}$$
* Discard any negative time solutions (as physically extraneous for events occurring after start).
* If two positive roots occur in a chase scenario, the first root is when the chaser catches and overtakes the leader; the second root is when the decelerating chaser would be overtaken again if paths crossed.

#### Step 6: Determine Catch-up Position
Substitute the positive time $t$ back into the simpler position function $x_A(t)$ to find the exact location of contact.
