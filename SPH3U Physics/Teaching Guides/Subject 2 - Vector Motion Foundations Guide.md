---
type: teaching-guide
subject: 2
tags:
  - SPH3U/kinematics/vectors
---

# Subject 2: Scalar & 1D Vector Motion Foundations

> [!info] Quick Navigation
> - **Summary Sheet:** [[Subject 2 - Vector Motion Summary]]
> - **Prerequisite:** [[Subject 1 - Introductory Skills Guide]]
> - **Master Roadmap:** [[Unit 1 Kinematics - Master Study Roadmap]]

---

## SECTION 1: CORE THEORY & DEFINITIONS

Kinematics is the branch of classical mechanics that describes the motion of points, bodies, and systems of objects without considering the forces that cause them to move. Describing motion unambiguously requires a precise physical vocabulary.

### Scalars vs. Vectors

Physical quantities in nature are divided into two fundamental mathematical classes:

* **Scalar Quantities:** Physical quantities that possess **magnitude (numerical amount and physical unit) only**, with no directional information.
  - Examples: A temperature of $22^\circ\text{C}$, a mass of $5.0\text{ kg}$, or a time interval of $12\text{ s}$.
* **Vector Quantities:** Physical quantities that possess **both magnitude AND a spatial direction**.
  - Examples: A car moving at $175\text{ km/h [N]}$, or an airplane displaced $350\text{ m [East]}$.

> [!question] Why Do We Need Vectors At All? Why Not Just Use Numbers?
> A number alone is ambiguous when direction matters. Imagine a navigation app that tells you to walk "5 kilometres" — but in which direction? North? South? Back the way you came? You'd be lost. Or consider a tug-of-war: two people pull a rope with equal force of 100 N. If both pull in the *same* direction, the net effect is 200 N. If they pull in *opposite* directions, the net effect is 0 N. The number "100 N" alone cannot tell you the outcome — direction is essential. **Scalars work perfectly for quantities that are always positive and have no opposing directions** (mass, temperature, time). Vectors are required the moment direction changes the physical result.

#### Categorization of Core Physical Quantities

| Physical Quantity | Classification | Standard Symbol | Standard SI Unit | Description / Meaning |
| :--- | :---: | :---: | :---: | :--- |
| **Mass** | Scalar | $m$ | $\text{kg}$ | Quantity of matter contained in an object |
| **Time (Interval)** | Scalar | $\Delta t$ | $\text{s}$ | Duration or elapsed time between two events |
| **Distance** | Scalar | $d$ | $\text{m}$ | Total ground covered along the actual path traveled |
| **Speed** | Scalar | $v$ | $\text{m/s}$ | Rate of distance covered per unit time |
| **Energy / Work** | Scalar | $E, W$ | $\text{J}$ | Capacity to do work; mechanical work |
| **Position** | Vector | $\vec{d}$ or $\vec{x}$ | $\text{m}$ | Location of an object relative to a chosen reference origin |
| **Displacement** | Vector | $\Delta\vec{d}$ | $\text{m}$ | Straight-line vector change from initial to final position |
| **Velocity** | Vector | $\vec{v}$ | $\text{m/s}$ | Rate of change of position per unit time with direction |
| **Acceleration** | Vector | $\vec{a}$ | $\text{m/s}^2$ | Rate of change of velocity per unit time with direction |

---

### Standard Vector Notation Conventions

In high school physics and formal kinematics, strict notation rules distinguish vectors from scalars:

1. **Vector Over-Arrow:** A small arrow placed directly above the letter symbol identifies it as a vector quantity: $\vec{d}$, $\vec{v}$, $\vec{a}$.
2. **Direction in Square Brackets:** The directional orientation is always appended immediately after the physical unit inside square brackets:
   $$\vec{v} = 175\text{ km/h [N]} \quad \text{or} \quad \Delta\vec{d} = 45.0\text{ m [forward]}$$
3. **Magnitude Only:** The magnitude (scalar absolute value) of a vector is written either by dropping the over-arrow or by using absolute value notation:
   $$v = |\vec{v}| = 175\text{ km/h}$$
4. **Units Standardization:** When evaluating vector motion algebraically, ensure all length, time, and mass quantities are converted into standard SI units via [[Subject 1 - Introductory Skills Guide#Metric MKS Conversions|Metric MKS Conversions]] ($\text{m}$, $\text{kg}$, $\text{s}$).

---

## Position, Distance, and Displacement

Understanding the subtle physical distinctions between where an object is, how much ground it covered, and where it ended up relative to where it started is crucial.

![[attachments/position_displacement_1d_axis.svg]]

> [!tip] Distance vs. Displacement on a 1D Axis
> ![[attachments/distancedisplacement.svg]]
> *Image: Wikimedia Commons*

> [!question] Why Is Displacement Different From Distance — and Why Does It Matter?
> Consider someone who walks $8\text{ m East}$, then turns around and walks $5\text{ m West}$. Their total **distance** is $13\text{ m}$ (every step counted). Their **displacement** is only $3\text{ m [East]}$ — just the net vector from start to finish. This difference matters enormously in physics because kinematic equations are built on **displacement**, not distance. If you use distance in a velocity formula when the object reversed direction, you'll get the wrong answer. For example, a round-trip (leaving home and returning) has zero displacement — so average velocity is zero — even though the car was moving the whole time and average speed is nonzero.

### 1. Position ($\vec{d}$)
* **Definition:** The specific coordinate location of an object at a given moment in time **relative to an established reference point (the origin, $0$)**.
* **Vector Nature:** Position requires both distance from origin and direction from origin: e.g., $\vec{d}_1 = +4.0\text{ m [E]}$.
* **Reference Frame:** If no origin is explicitly stated, you must declare one (e.g., "Let the school be the origin $\vec{d} = 0$").

### 2. Distance ($d$)
* **Definition:** The total length of the actual path traversed by a moving object during a given time interval.
* **Scalar Nature:** Distance has no direction and can **never be negative**: $d \ge 0$.
* **Path Dependency:** If an object walks $5\text{ m [East]}$ and then turns around and walks $5\text{ m [West]}$, the total distance traveled is $d = 5\text{ m} + 5\text{ m} = 10\text{ m}$.

### 3. Displacement ($\Delta\vec{d}$)
* **Definition:** The straight-line vector pointing from the object's initial position directly to its final position, representing the net change in position:
  $$\Delta\vec{d} = \vec{d}_f - \vec{d}_i$$
* **Independence of Path:** Displacement depends solely on starting and ending endpoints; it does not care what path was taken between them.
* **Zero Net Displacement:** In any closed-loop journey (where an object returns to its starting point), $\vec{d}_f = \vec{d}_i$, so net displacement is identically zero: $\Delta\vec{d} = 0\text{ m}$.

---

### One-Dimensional Direction Conventions & Sign Assignments

In one-dimensional (1D) kinematics, motion is restricted to a single straight axis. Vector directions can be represented algebraically by assigning positive ($+$) and negative ($-$) signs.

> [!question] Why Use + and − Signs for Direction Instead of Words Like "North" and "South"?
> When you assign $[\text{North}] = +$ and $[\text{South}] = -$, you unlock the full power of algebra. You can add and subtract displacements as plain numbers, and the sign automatically encodes direction. For example: $+10\text{ km} + (-20\text{ km}) = -10\text{ km} \implies 10\text{ km [South]}$. This approach works because motion along a straight line is genuinely one-dimensional — every direction is either "with" or "against" the chosen positive axis. Writing words like "North" in an equation makes arithmetic impossible; signs make it automatic.

#### Standard Coordinate Systems:
* **Horizontal Axis ($x$-axis):**
  $$\text{Let } [\text{East}], [\text{Right}], \text{ or } [\text{Forward}] = (+) \qquad \iff \qquad [\text{West}], [\text{Left}], \text{ or } [\text{Backward}] = (-)$$
* **Vertical Axis ($y$-axis):**
  $$\text{Let } [\text{North}] \text{ or } [\text{Up}] = (+) \qquad \iff \qquad [\text{South}] \text{ or } [\text{Down}] = (-)$$

> [!tip] The Sign Convention Rule
> Always declare your direction convention at the very start of every problem (e.g., $\text{Let } [\text{E}] = +$). Once declared, any vector pointing West is treated as a negative number in your algebraic formulas. After solving, convert negative signs back into explicit bracketed directions: $-15\text{ m} \longrightarrow 15\text{ m [W]}$.

---

### Average Speed vs. Average Velocity

Just as distance and displacement differ, the rates at which they occur represent distinct physical quantities:

> [!question] Why Do Speed and Velocity Need to Be Different Concepts?
> They capture different aspects of motion. **Speed** tells you how hard you've been working (total ground covered per time). **Velocity** tells you your net progress toward a destination. GPS navigation cares about velocity (are you heading toward the destination?); a fuel gauge cares about speed (how fast are you burning fuel?). The classic example: a runner completes one lap of a 400 m track in 60 s. Average speed = $400/60 \approx 6.7\text{ m/s}$. Average velocity = $0/60 = 0\text{ m/s}$ (because they ended where they started). Knowing only speed, you'd think they made great progress; knowing velocity, you know they're back where they began.

#### 1. Average Speed ($v_{\text{avg}}$)
A scalar quantity measuring the total path distance covered per unit of elapsed time:
$$v_{\text{avg}} = \frac{d_{\text{total}}}{\Delta t_{\text{total}}} = \frac{\text{Total Distance}}{\text{Total Time Elapsed}}$$
* Since total distance is always positive, average speed is always non-negative: $v_{\text{avg}} \ge 0$.
* Units: $\text{m/s}$ or $\text{km/h}$.

#### 2. Average Velocity ($\vec{v}_{\text{avg}}$)
A vector quantity measuring the net change in position (displacement) per unit of elapsed time:
$$\vec{v}_{\text{avg}} = \frac{\Delta\vec{d}_{\text{total}}}{\Delta t_{\text{total}}} = \frac{\vec{d}_f - \vec{d}_i}{\Delta t_{\text{total}}}$$
* Velocity shares the exact same spatial direction as the displacement vector $\Delta\vec{d}$.
* If an object returns to its initial position, its average velocity is zero ($\vec{v}_{\text{avg}} = 0\text{ m/s}$), even if its average speed was very high.

---

### Constant vs. Instantaneous Motion

* **Instantaneous Speed ($v$):** The speed of an object at an exact, infinitesimally small instant in time ($t$). This is the reading displayed on an automobile's speedometer.
* **Instantaneous Velocity ($\vec{v}$):** The velocity (speed + current direction of motion) of an object at a specific instant in time.
* **Constant Speed / Velocity (Uniform Motion):** Occurs when an object covers equal distances in equal time intervals without changing direction.
  $$\text{If } \vec{v} = \text{constant} \implies \vec{v}_{\text{instantaneous}} = \vec{v}_{\text{avg}} \text{ at all moments in time.}$$

> [!question] Why Does Instantaneous Velocity Require Calculus to Define Properly?
> Velocity is $\Delta d / \Delta t$, but "instantaneous" means $\Delta t \to 0$. If $\Delta t = 0$, you get $0/0$ — which is mathematically undefined. Calculus resolves this through the concept of a **limit**: as $\Delta t$ gets infinitely small (approaching but never reaching zero), the ratio $\Delta d / \Delta t$ approaches a specific finite value — the instantaneous velocity. In high school physics, you approximate this by drawing a **tangent line** to a curved position-time graph at the point of interest — the slope of that tangent *is* the limiting value. This is why the tangent line method (covered in [[Subject 3 - Graphical Analysis Guide]]) is so important: it's a geometric approximation of differentiation.

---

## SECTION 2: EMBEDDED INSTRUCTIONAL VIDEOS

![[Unit 1 Physics - Video Directory#Subject 2: Scalar & 1D Vector Motion Foundations]]

---

## SECTION 3: HOW-TO WORKBOOK PROBLEM SOLVING GUIDES

This section details procedural methodologies and problem-solving strategies for the exercises in `Intro to Vector Motion WB blank.pdf` (Pages 1–8).

### Constructing 1D Motion Line Diagrams
*(Intro to Vector Motion Workbook, Pages 1–3)*

A line diagram is an essential sketch that visualizes positions and displacements along a 1D reference axis.

> [!tip] Why Draw a Line Diagram Before Solving?
> The diagram forces you to **commit to a sign convention** and **visualize what the problem describes** before numbers are touched. Students who skip the diagram frequently flip signs mid-problem or lose track of which direction is positive. The diagram also lets you catch impossible situations (e.g., a displacement that somehow skips past the start point) before algebra begins.

#### Step-by-Step Construction Procedure:
1. **Draw a Horizontal or Vertical Reference Axis:** Draw a straight line with an arrow at the positive end.
2. **Establish the Reference Origin ($0$):** Mark a clear vertical tick mark at position $0$ representing the reference origin (e.g., school, home, intersection).
3. **Establish Sign Convention:** Write your convention clearly above the line: $\text{e.g., } [E] = +$.
4. **Plot Initial Position ($\vec{d}_i$):** If the problem starts at a coordinate other than $0$, mark $\vec{d}_i$ with a dot and label its signed value (e.g., $+10\text{ km}$).
5. **Draw Displacement Vector Arrows ($\Delta\vec{d}_i$):**
   - For each leg of the journey, draw an arrow along the axis.
   - Vectors pointing in the positive direction point right/up; vectors in the negative direction point left/down.
   - Place arrows tip-to-tail sequentially to represent multi-interval journeys.
6. **Identify Final Position ($\vec{d}_f$):** Mark the terminus of the final arrow as $\vec{d}_f$.

---

### Multi-Interval Displacement & Position Algorithm
*(Intro to Vector Motion Workbook, Pages 4–6)*

Workbook questions frequently describe people or vehicles traveling across several sequential linear intervals (e.g., $10\text{ km [N]}$, then $20\text{ km [S]}$, then $5\text{ km [N]}$).

> [!question] Why Is Multi-Interval Displacement Just a Signed Sum?
> Each displacement vector in 1D is fully described by a signed number. Because all motion is on the same straight axis, vectors in the positive direction add positively and vectors in the negative direction add negatively — like a number line. The final displacement is simply the algebraic (signed) sum of all the individual legs. This works because **vector addition in 1D reduces to ordinary arithmetic with signs**. The same trick doesn't extend to 2D (where you'd need component form), but for straight-line 1D motion it's exact.

#### Step-by-Step Solution Algorithm:

```
Step 1: Declare Sign Convention
   └── Example: Let [North] = (+) and [South] = (-)

Step 2: Convert All Intervals into Signed Scalar Values
   ├── Δd₁ = +10 km
   ├── Δd₂ = -20 km
   └── Δd₃ = +5 km

Step 3: Calculate Net Total Displacement (Vector Sum)
   └── Δd_total = Σ Δd_k = Δd₁ + Δd₂ + Δd₃ = (+10) + (-20) + (+5) = -5 km

Step 4: Calculate Final Position
   └── d_f = d_i + Δd_total

Step 5: Convert Back to Physical Vector Notation
   └── -5 km ──► 5 km [S]
```

#### Total Distance vs. Total Displacement Comparison:
- **Total Distance:** Sum the absolute magnitudes of every interval:
  $$d_{\text{total}} = |\Delta\vec{d}_1| + |\Delta\vec{d}_2| + |\Delta\vec{d}_3| = 10\text{ km} + 20\text{ km} + 5\text{ km} = 35\text{ km}$$
- **Total Displacement:** Sum the signed directional vectors:
  $$\Delta\vec{d}_{\text{total}} = (+10) + (-20) + (+5) = -5\text{ km} \implies 5\text{ km [S]}$$

---

### Speed vs. Velocity Multi-Interval Word Problem Strategy
*(Intro to Vector Motion Workbook, Pages 7–8)*

When solving comprehensive motion word problems comparing average speed and average velocity:

#### Step-by-Step Problem-Solving Protocol:
1. **Partition the Motion by Leg:** Create a structured table listing each leg ($1, 2, \dots$):
   - Leg $1$: $d_1$, $\Delta\vec{d}_1$, $\Delta t_1$
   - Leg $2$: $d_2$, $\Delta\vec{d}_2$, $\Delta t_2$
2. **Harmonize Units:** Ensure all distances are in meters ($\text{m}$) or kilometers ($\text{km}$), and all times are in seconds ($\text{s}$) or hours ($\text{h}$) using [[Subject 1 - Introductory Skills Guide#Metric MKS Conversions|Metric MKS Conversions]].
3. **Calculate Total Elapsed Time:**
   $$\Delta t_{\text{total}} = \Delta t_1 + \Delta t_2 + \dots$$
   *(Note: Any resting or stopping intervals must be included in $\Delta t_{\text{total}}$).*
4. **Compute Average Speed (Scalar Calculation):**
   $$v_{\text{avg}} = \frac{d_1 + d_2 + \dots}{\Delta t_{\text{total}}}$$
5. **Compute Average Velocity (Vector Calculation):**
   $$\vec{v}_{\text{avg}} = \frac{\Delta\vec{d}_1 + \Delta\vec{d}_2 + \dots}{\Delta t_{\text{total}}}$$
6. **Format Final Answers:**
   - Average speed: numerical value + unit (no direction brackets).
   - Average velocity: numerical value + unit + `[direction bracket]`.
   - Apply correct significant digits based on original givens.
