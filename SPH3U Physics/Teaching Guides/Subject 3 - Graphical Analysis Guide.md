---
type: teaching-guide
subject: 3
tags:
  - SPH3U/kinematics/graphs
---

# Subject 3: Graphical Motion Analysis & Transition Graphs

> [!info] Quick Navigation
> - **Summary Sheet:** [[Subject 3 - Motion Graphs Summary]]
> - **Prerequisite:** [[Subject 2 - Vector Motion Foundations Guide]]
> - **Master Roadmap:** [[Unit 1 Kinematics - Master Study Roadmap]]

---

## SECTION 1: GRAPHICAL ANALYSIS THEORY

Kinematics graphs provide visual, qualitative, and exact quantitative representations of an object's motion over time. By mastering slopes and geometric areas under curves, you can fluidly translate between position, velocity, and acceleration.

> [!question] Why Use Graphs at All? Can't We Just Use Formulas?
> Graphs reveal things formulas hide. A formula gives you a single numerical answer; a graph shows the *entire history* of motion at once — when the object was stopped, when it reversed, when it was speeding up vs. slowing down, whether acceleration was constant or changing. Graphs also provide an intuitive geometric interpretation of the mathematics: slope becomes velocity, area becomes displacement. These geometric connections aren't just conveniences — they are the visual form of **differential calculus** (slope = derivative) and **integral calculus** (area = integral), which is the language all of advanced physics is written in.

### Position-Time (d-t) Graphs

A position-time graph plots the object's position vector $\vec{d}$ along the vertical axis against elapsed clock time $t$ along the horizontal axis. As defined in [[Subject 2 - Vector Motion Foundations Guide#Position, Distance, and Displacement|Position, Distance, and Displacement]], position represents location relative to the chosen reference origin.

![[attachments/dt_constant_velocity.svg]]

#### 1. Slope Equals Velocity
The mathematical slope of a $d-t$ graph represents physical velocity:
$$\text{Slope} = \frac{\text{Rise}}{\text{Run}} = \frac{\Delta \vec{d}}{\Delta t} = \vec{v}$$

> [!question] Why Does Slope Equal Velocity — Is This a Coincidence?
> It is not a coincidence at all. Velocity is **defined** as the rate of change of position with respect to time: $\vec{v} = \Delta\vec{d}/\Delta t$. On a $d-t$ graph, $\Delta\vec{d}$ is the vertical rise (change in position) and $\Delta t$ is the horizontal run (change in time). The slope formula is literally rise/run $= \Delta\vec{d}/\Delta t = \vec{v}$. The graph **is** plotting the ratio that defines velocity. This isn't a neat trick — the relationship is definitional. Whenever you plot any quantity $Y$ against another quantity $X$, the slope of that graph is always $\Delta Y / \Delta X$ by definition.

* **Horizontal Line ($\text{Slope} = 0$):** The object is stationary (at rest) at that specific position coordinate.
* **Straight Line with Constant Positive Slope ($\text{Slope} > 0$):** The object moves forward (or East/North) with constant, unchanging velocity.
* **Straight Line with Constant Negative Slope ($\text{Slope} < 0$):** The object moves backward (or West/South) with constant, unchanging velocity.
* **Steepness:** The steeper the slope (greater absolute value), the higher the speed of the object.

#### 2. Curved Lines & Acceleration
When the slope of a $d-t$ graph changes continuously, the velocity is changing; therefore, the object is undergoing **acceleration** ($\vec{a} \ne 0$).

![[attachments/dt_curved_tangent.svg]]

> [!question] Why Does a Curve on a d-t Graph Mean Acceleration?
> A straight line on a $d-t$ graph has a *constant slope* — meaning velocity never changes — which means zero acceleration. A **curve** means the slope is changing at every instant. Since slope = velocity, a changing slope = changing velocity = acceleration by definition ($\vec{a} = \Delta\vec{v}/\Delta t$). The faster the curve bends (more curvature), the greater the acceleration. A gently curving parabola means small, constant acceleration (like a car on a flat highway beginning to speed up). A sharply curving line means rapid velocity change (like a ball dropped from a building).

* **Parabola opening upwards ($\cup$ shape):** Slope is becoming more positive $\implies$ positive acceleration ($\vec{a} > 0$).
* **Parabola opening downwards ($\cap$ shape):** Slope is becoming more negative $\implies$ negative acceleration ($\vec{a} < 0$).

#### 3. Secant Slope vs. Tangent Slope
* **Secant Line $\longrightarrow$ Average Velocity ($\vec{v}_{\text{avg}}$):**
  A secant is a straight line drawn between two separate time coordinates $(t_1, d_1)$ and $(t_2, d_2)$ on a curve:
  $$\vec{v}_{\text{avg}} = \frac{d_2 - d_1}{t_2 - t_1}$$
* **Tangent Line $\longrightarrow$ Instantaneous Velocity ($\vec{v}_{\text{inst}}$):**
  A tangent is a straight line that touches the curve at exactly one single point of tangency without cutting through the curve:
  $$\vec{v}_{\text{inst}} = \left. \frac{\Delta \vec{d}}{\Delta t} \right\vert_{\text{tangent line}} = \frac{y_2 - y_1}{x_2 - x_1}$$

> [!question] Why Does the Tangent Line Give Instantaneous Velocity?
> Imagine zooming in on a curved graph at a specific point — the more you zoom, the more the curve looks like a straight line. At infinite zoom, the curve *is* a straight line — the tangent line. The slope of that line is the slope the curve has *at exactly that instant*. As you take $\Delta t \to 0$ in the secant formula, the two points converge, and the secant line pivots to match the tangent. The tangent slope is therefore the limiting ratio $\lim_{\Delta t \to 0}(\Delta d/\Delta t)$ — which is the formal definition of the derivative, and also the definition of instantaneous velocity. The tangent construction is a hands-on way of computing a derivative without needing calculus notation.

---

## Velocity-Time Graphs

A velocity-time ($v-t$) graph plots instantaneous velocity $\vec{v}$ on the vertical axis against elapsed time $t$ on the horizontal axis. It provides a complete record of both acceleration and displacement.

![[attachments/vt_acceleration_area.svg]]

### 1. Slope Equals Acceleration
The slope of a line segment on a $v-t$ graph represents the physical acceleration of the object:
$$\text{Slope} = \frac{\text{Rise}}{\text{Run}} = \frac{\Delta \vec{v}}{\Delta t} = \frac{\vec{v}_f - \vec{v}_i}{t_f - t_i} = \vec{a}$$

> [!question] Why Is Acceleration the Slope of a v-t Graph?
> By the same logic as before: acceleration is *defined* as $\vec{a} = \Delta\vec{v}/\Delta t$. On a $v-t$ graph, the vertical axis is $\vec{v}$ and the horizontal axis is $t$, so slope = rise/run = $\Delta\vec{v}/\Delta t = \vec{a}$. Notice the pattern: each graph's slope gives the **next level** of the motion hierarchy. Slope of $d-t$ = velocity. Slope of $v-t$ = acceleration. This chain continues in advanced physics: the slope of an $a-t$ graph would give jerk (rate of change of acceleration).

* **Horizontal Line ($\text{Slope} = 0$):** Constant velocity ($\vec{a} = 0$, uniform motion).
* **Positive Slope ($\text{Slope} > 0$):** Positive acceleration ($\vec{a} > 0$).
* **Negative Slope ($\text{Slope} < 0$):** Negative acceleration ($\vec{a} < 0$).
* **Straight Line:** Uniform (constant) acceleration.

### 2. Area Under the Curve Equals Displacement
The geometric area enclosed between the velocity function $\vec{v}(t)$ and the time axis ($v = 0$) represents the net displacement ($\Delta\vec{d}$) of the object during that time interval:
$$\text{Signed Area Under Curve} = \Delta\vec{d}$$

> [!question] Why Does Area Under a v-t Graph Equal Displacement? Why Area?
> Think about the simplest case: constant velocity $v$ for a time $\Delta t$. Displacement = $v \times \Delta t$. On the graph, that's a rectangle of height $v$ and width $\Delta t$ — its **area** = $v \times \Delta t$ = displacement. This is not a coincidence; $\text{displacement} = v \times \Delta t$ is geometrically a rectangle.
>
> Now suppose velocity changes. Break the time interval into many tiny slices, each so narrow that velocity is nearly constant within each slice. The displacement during each slice $\approx v_k \times \Delta t_k$ — a tiny rectangle. Sum all the rectangles: total displacement $\approx$ total area. As the slices get infinitely thin, the approximation becomes exact. This is the **Riemann sum definition of integration**. Area under the curve = $\int v\,dt$ = displacement. This is the geometric interpretation of the fundamental theorem of calculus, and it works precisely because displacement is the accumulation of velocity over time.

* **Area Above the Time Axis ($v > 0$):** Represents positive displacement ($\Delta\vec{d} > 0$, forward motion).
* **Area Below the Time Axis ($v < 0$):** Represents negative displacement ($\Delta\vec{d} < 0$, backward motion).
* **Net Displacement vs. Total Distance:**
  $$\Delta\vec{d}_{\text{net}} = \text{Area}_{\text{above}} - |\text{Area}_{\text{below}}| \qquad d_{\text{total}} = |\text{Area}_{\text{above}}| + |\text{Area}_{\text{below}}|$$

### 3. Motion States & Direction Rules on a $v-t$ Graph
* **Direction of Motion:** Determined strictly by whether the curve lies above or below the time axis:
  - If $v > 0$ (above axis), the object is moving forward / East / North.
  - If $v < 0$ (below axis), the object is moving backward / West / South.
* **Speeding Up vs. Slowing Down:**
  - **Speeding Up:** The line moves **away from the time axis** ($|v|$ is increasing). Velocity and acceleration share the same algebraic sign.
  - **Slowing Down:** The line moves **toward the time axis** ($|v|$ is decreasing). Velocity and acceleration have opposite algebraic signs.
* **Turning Around / Reversing Direction:**
  - Occurs at the precise instant the velocity graph **crosses the time axis** ($v = 0$).

---

### Transition Graph Rules ($d-t \longleftrightarrow v-t \longleftrightarrow a-t$)

Transition graphs require systematically translating kinematic motion between all three visual domains:

![[attachments/transition_graphs_trio.svg]]

![[attachments/transition_graph_relationships.svg]]

> [!question] Why Do These Three Graphs Form a Chain Connected by Slope and Area?
> The three kinematic quantities form a **mathematical hierarchy**:
> $$\text{Position} \xrightarrow{\text{differentiate (slope)}} \text{Velocity} \xrightarrow{\text{differentiate (slope)}} \text{Acceleration}$$
> $$\text{Acceleration} \xrightarrow{\text{integrate (area)}} \text{Velocity} \xrightarrow{\text{integrate (area)}} \text{Position}$$
> Each quantity is the derivative of the one before it, or the integral of the one after it. This is not an arbitrary choice — velocity is *defined* as the rate of change of position, and acceleration is *defined* as the rate of change of velocity. The graphs are simply the visual representation of these definitions. The slope operation extracts derivatives; the area operation accumulates integrals.

#### Direction 1: Moving Forward by Taking Slopes ($d-t \longrightarrow v-t \longrightarrow a-t$)
1. **From $d-t$ to $v-t$:**
   - Measure or compute the numerical slope ($\Delta d / \Delta t$) for each interval on the $d-t$ graph.
   - Plot this slope as the vertical coordinate value ($v$) on the $v-t$ graph.
   - If $d-t$ is linear, $v-t$ is a horizontal flat line.
   - If $d-t$ is a parabola, $v-t$ is a sloping straight line.
2. **From $v-t$ to $a-t$:**
   - Compute the numerical slope ($\Delta v / \Delta t$) for each interval on the $v-t$ graph.
   - Plot this slope as a constant horizontal line segment on the $a-t$ graph.

#### Direction 2: Moving Backward by Calculating Areas ($a-t \longrightarrow v-t \longrightarrow d-t$)
1. **From $a-t$ to $v-t$:**
   - The area under each interval on the $a-t$ graph represents change in velocity: $\Delta\vec{v} = a \times \Delta t$.
   - Calculate $\vec{v}_f = \vec{v}_i + \Delta\vec{v}$ to determine vertex points on the $v-t$ graph.
   - Connect points with straight lines (since acceleration is constant).
2. **From $v-t$ to $d-t$:**
   - Partition each interval on the $v-t$ graph into geometric shapes (rectangles, triangles, trapezoids).
   - Compute the signed area to find interval displacement: $\Delta\vec{d} = \text{Area}$.
   - Add interval displacement to prior position: $\vec{d}_f = \vec{d}_i + \Delta\vec{d}$ to locate key coordinates on the $d-t$ graph.
   - Connect the plotted coordinates:
     - For uniform motion ($v = \text{const}$, horizontal line on $v-t$), connect with a **straight line**.
     - For accelerated motion (sloping line on $v-t$), connect with a **smooth parabolic curve**.

---

## SECTION 2: EMBEDDED INSTRUCTIONAL VIDEOS

![[Unit 1 Physics - Video Directory#Subject 3: Motion Graphs & Transition Graphs]]

---

## SECTION 3: HOW-TO WORKBOOK PROBLEM SOLVING GUIDES

This section details step-by-step methodologies for the exercises in `2026kinwb#3curvedDTto Transitions.pdf` (Pages 1–27).

### Tangent Line Construction & Instantaneous Velocity
*(Workbook Pages 1–9)*

Workbook exercises require finding instantaneous velocity at specific time coordinates on curved position-time graphs (e.g., a ball rolling down an incline).

> [!question] Why Must the Tangent Line Be Extended Far Across the Graph?
> A short tangent line segment is very sensitive to small angular errors in how you aligned your ruler. Even a 1° misalignment over a 2 cm line can produce a slope error of 5–10%. Extending the line across the full grid width (say, 20 cm) means that same 1° error produces a much smaller proportional effect on the measured slope — the longer the line, the more stable and accurate your rise/run calculation. This is why you always pick two grid-intersection points that are **far apart** on the tangent line.

#### Step-by-Step Tangent Protocol:
1. **Locate and Mark the Point of Contact:**
   Find the requested time on the horizontal axis ($t_0$), move vertically up to the curve, and mark the point of tangency $P(t_0, d_0)$ with a sharp pencil dot.
2. **Position the Straightedge (Clear Ruler):**
   Place a clear ruler against the curve at point $P$. Rotate the ruler until it glances off the curve at only that single point, ensuring the angles between the ruler edge and the curve on either side of $P$ appear perfectly balanced and symmetrical.
3. **Draw an Extended Tangent Line:**
   Draw a long, straight line extending across the full grid beyond the contact point. A longer line significantly reduces slope measurement error.
4. **Select Two Grid Intersection Points:**
   Do **not** use the point of tangency itself or points from the curved data line. Instead, search along the drawn straight line for two distinct points that pass cleanly through grid intersections: $(x_1, y_1)$ and $(x_2, y_2)$. Circle both points.
5. **Calculate the Tangent Slope:**
   $$\vec{v}_{\text{inst}} = \frac{y_2 - y_1}{x_2 - x_1} = \frac{\Delta\vec{d}}{\Delta t}$$
   Include appropriate physical units ($\text{m/s}$) and direction.

---

### Partitioning Geometric Areas Under v-t Curves
*(Workbook Pages 10–19)*

To calculate net displacement from multi-segment velocity-time graphs:

#### Geometric Partitioning Toolkit:
Divide complex piecewise velocity profiles into three standard geometric shapes bounded by the time axis ($v = 0$):

![[attachments/vt_area_partition_shapes.svg]]

> [!question] Why Can We Use Simple Geometry (Rectangles, Triangles, Trapezoids) for This?
> The kinematic equations we use assume **constant acceleration** within each interval. Constant acceleration means velocity changes at a *constant rate* — which means the $v-t$ graph within each interval is a straight line. A straight-line $v-t$ profile between two endpoints creates exactly a trapezoid (or a rectangle if velocity is constant, or a triangle if starting from rest). Because the profile is made of straight lines, **exact geometric area formulas apply** — no calculus required. If acceleration were not constant, the $v-t$ curve would be curved and we'd need integration. The straight-line assumption is what makes simple geometry sufficient.

1. **Rectangle:** $\text{Area} = \text{base} \times \text{height} = \Delta t \times v$
2. **Triangle:** $\text{Area} = \frac{1}{2} \times \text{base} \times \text{height} = \frac{1}{2} \times \Delta t \times \Delta v$
3. **Trapezoid:** $\text{Area} = \left(\frac{v_i + v_f}{2}\right) \times \Delta t$

#### Step-by-Step Area Summation:
1. Draw vertical dashed boundary lines from the time axis up/down to every vertex or slope inflection point.
2. Label each enclosed region: $A_1, A_2, A_3, \dots$
3. Calculate the area of each shape independently, recording physical units ($\text{m/s} \times \text{s} = \text{m}$).
4. Assign positive signs ($+$) to regions above $v = 0$ and negative signs ($-$) to regions below $v = 0$.
5. Compute net displacement:
   $$\Delta\vec{d}_{\text{net}} = \sum \text{Signed Areas}$$

---

### Transition Graph Construction Protocol
*(Workbook Pages 20–27)*

Workbook exercises present a piecewise velocity-time graph and ask for corresponding displacement-time ($d-t$) and acceleration-time ($a-t$) graphs.

> [!question] Why Do We Construct d-t and a-t Graphs by Transforming the v-t Graph Rather Than Drawing Them from Scratch?
> The $v-t$ graph is the most information-rich starting point for uniform-acceleration motion. From it, you can extract acceleration (via slopes) and displacement (via areas) with simple arithmetic — no additional physics assumptions needed. Going in the other direction (starting from $d-t$) requires taking a derivative, which is geometrically harder. The $v-t$ graph acts as the **pivot point** of the motion hierarchy: it connects directly to both the position world (via area) and the acceleration world (via slope). This is why transition problems almost always give you the $v-t$ graph as the starting point.

#### 5-Step Construction Workflow:
1. **Identify Time Intervals:**
   List all boundary times where slope changes occur ($t = 0, t_1, t_2, \dots$). These exact time intervals form the horizontal columns for all three graphs.
2. **Calculate Slopes to Build the $a-t$ Graph:**
   For each interval $k$:
   $$\vec{a}_k = \frac{\vec{v}_{f,k} - \vec{v}_{i,k}}{t_{f,k} - t_{i,k}}$$
   Draw a horizontal line segment at height $\vec{a}_k$ spanning that time interval on the $a-t$ grid.
3. **Calculate Areas to Determine Position Milestones:**
   For each interval $k$, compute geometric area $\Delta\vec{d}_k$.
   If initial position is given (or assumed $0\text{ m}$):
   $$\vec{d}_1 = \vec{d}_0 + \Delta\vec{d}_1, \quad \vec{d}_2 = \vec{d}_1 + \Delta\vec{d}_2, \quad \dots$$
4. **Plot Discrete Coordinates on the $d-t$ Grid:**
   Plot each coordinate point $(t_k, \vec{d}_k)$ clearly with a pencil dot.
5. **Connect Points with the Correct Curvature:**
   * **If interval has $\vec{a} = 0$ (constant velocity):** Connect the two endpoints with a **straight ruler line**.
   * **If interval has $\vec{a} > 0$ (speeding up forward or slowing down backward):** Connect with a **parabolic curve bending upwards** ($\cup$).
   * **If interval has $\vec{a} < 0$ (slowing down forward or speeding up backward):** Connect with a **parabolic curve bending downwards** ($\cap$).

> [!tip] Why Does Constant Acceleration Produce a Parabola on the d-t Graph?
> From Equation (3): $\Delta\vec{d} = \vec{v}_i\Delta t + \frac{1}{2}\vec{a}\Delta t^2$. This is a polynomial in $t$ with a $t^2$ term — the definition of a parabola. When $\vec{a} = 0$, the $t^2$ term vanishes and you get a linear function (straight line on $d-t$). When $\vec{a} \ne 0$, the $t^2$ term dominates at larger $t$, producing the characteristic parabolic bend. The direction of the opening (up or down) depends on the sign of $\vec{a}$.
