---
type: teaching-guide
subject: 1
tags:
  - SPH3U/intro-skills/math
---

# Subject 1: Unit 0 Introductory Mathematical Skills & Measurement Analysis

> [!info] Quick Navigation
> - **Summary Sheet:** [[Resources/Subject 1 - Intro Skills Summary]]
> - **Master Roadmap:** [[Unit 1 Kinematics - Master Study Roadmap]]

---

## SECTION 1: CORE THEORY & MATHEMATICAL CONCEPTS

Introductory physics relies on the precise language of mathematics to express physical reality. Measurement uncertainty, unit standardization, and rigorous algebraic manipulation form the bedrock of all subsequent mechanics analysis.

### Significant Digits (SD) Counting Rules & Rounding Standards

Every measurement taken with a physical instrument contains uncertainty. **Significant digits (SD)** represent all certain digits plus one final estimated digit that reflects the instrument's precision limit.

> [!question] Why Do Significant Digits Exist?
> Every measuring instrument — a ruler, a stopwatch, a thermometer — has a **physical limit to how finely it can measure**. A typical school ruler can only reliably measure to the nearest 0.1 cm; a vernier caliper to 0.01 cm. The last digit you record is always an *estimate* based on where the needle or line falls between two markings. Significant digits are a system for **encoding that precision limit directly into the number itself**, so that anyone reading your data knows exactly how trustworthy each digit is. If a ruler only reads to 0.1 cm and you write an answer as 14.8372 cm, you are claiming false precision — implying you know the length to $\frac{1}{10,000}$ of a centimetre, which your ruler physically cannot provide.

#### The Fundamental Counting Rules
1. **Non-Zero Digits:** All non-zero digits ($1$ through $9$) are always significant.
   - Example: $482.6\text{ m}$ contains $4$ SD.
2. **Captive (Interior) Zeros:** Any zero located between non-zero digits is always significant.
   - Example: $7008\text{ s}$ contains $4$ SD; $3.004\text{ kg}$ contains $4$ SD.
3. **Leading Zeros:** Zeros preceding the first non-zero digit are place-holders only and are **never** significant, regardless of decimal placement.
   - Example: $0.0052\text{ m}$ contains only $2$ SD ($5$ and $2$); $0.07\text{ s}$ contains $1$ SD.
4. **Trailing Zeros:**
   - **With an explicit decimal point:** Trailing zeros to the right of non-zero digits are intentional statements of precision and are **always significant**.
     - Example: $45.00\text{ m}$ contains $4$ SD; $9.0\text{ s}$ contains $2$ SD; $300.\text{ m}$ contains $3$ SD.
   - **Without an explicit decimal point:** Trailing zeros in a whole number are ambiguous placeholders and are conventionally **not significant**.
     - Example: $5200\text{ m}$ contains $2$ SD. To express $5200$ with $3$ or $4$ SD, scientific notation must be used ($5.20 \times 10^3\text{ m}$ or $5.200 \times 10^3\text{ m}$).
5. **Exact Numbers:** Counted values (e.g., $12$ students) and defined conversion factors (e.g., $1\text{ min} = 60\text{ s}$, $1\text{ m} = 100\text{ cm}$) have infinite precision and do not limit the significant digits of a calculated result.

#### Operational Precision Rules: Addition/Subtraction vs. Multiplication/Division

Physics calculations frequently combine experimental quantities using arithmetic. The rule applied depends strictly on the arithmetic operation:

> [!warning] The Two Golden Precision Rules
> - **Addition and Subtraction:** Governed by **Decimal Places (Precision)**.
> - **Multiplication and Division:** Governed by **Total Significant Digits (Relative Precision)**.

> [!question] Why Are the Rules Different for + vs. ×?
> The two rules exist because addition and multiplication represent **fundamentally different types of imprecision**.
>
> When you **add** $125.17\text{ m} + 4.2\text{ m}$, you're stacking two rulers end-to-end. The second ruler can only resolve to the *tenths place* (0.1 m). Even if the first ruler reads to the *hundredths place*, the combined result can't be known more precisely than the weakest ruler's tenths place — **absolute precision (decimal places)** is the limiting factor.
>
> When you **multiply** $4.8\text{ m} \times 6.2\text{ m}$, you're computing an area. Each measurement has a relative uncertainty — $4.8$ has roughly 1-in-48 imprecision (~2%), and $6.2$ has roughly 1-in-62 imprecision (~2%). These *relative* uncertainties compound on multiplication. The result can only be as *relatively* precise as the less precise input — this is why **significant digits (relative precision)** govern multiplication.

| Operation                 | Rule                                    | Key Idea                                 |
| :------------------------ | :-------------------------------------- | :--------------------------------------- |
| Addition & Subtraction    | Fewest **decimal places** in the inputs | Absolute precision — it's about position |
| Multiplication & Division | Fewest **total SD** in the inputs       | Relative precision — it's about ratio    |

1. **Addition & Subtraction Rule (Decimal Place Limit):**
   The final result cannot be more precise than the least precise measurement. Round the sum or difference to match the operand with the fewest decimal places.
   $$\text{Example: } 125.17\text{ m} + 4.2\text{ m} + 0.089\text{ m} = 129.459\text{ m} \xrightarrow{\text{round to 1 decimal place}} 129.5\text{ m}$$
   *(Since $4.2\text{ m}$ has only $1$ decimal place, the answer must have $1$ decimal place).*

2. **Multiplication & Division Rule (Total SD Limit):**
   The final result cannot contain more significant digits than the operand with the fewest total significant digits.
   $$\text{Example: } v = \frac{148.5\text{ m}}{6.2\text{ s}} = 23.95161...\text{ m/s} \xrightarrow{\text{round to 2 SD}} 24\text{ m/s}$$
   *($148.5\text{ m}$ has $4$ SD, $6.2\text{ s}$ has $2$ SD $\implies$ result must have $2$ SD).*

3. **Multi-Step Calculation Policy:**
   When performing complex multi-step algebra, **never round intermediate values**. Store unrounded intermediate results in calculator memory to prevent rounding compounding error. Apply rounding rules **only once**, on the final recorded value.

   > [!tip] Why Never Round Midway?
   > Each premature rounding introduces a small error. Over 4 or 5 steps those errors **multiply and compound** — a 0.5% error at step 1 can turn into a 2–3% error in the final answer. This is called *rounding error propagation*, and it's why scientists carry full precision through every intermediate calculation before committing to a final rounded result.

---

### Scientific Notation & Arithmetic Operations

Scientific notation standardizes physical quantities as:
$$N \times 10^n \quad \text{where } 1 \le |N| < 10 \text{ and } n \in \mathbb{Z}$$

> [!question] Why Use Scientific Notation?
> Two reasons: **precision and scale**. Consider the mass of an electron: $0.000000000000000000000000000000911\text{ kg}$. Written in decimal, 31 zeros precede the significant digits — it's impossible to read reliably and easy to miscopy a zero. In scientific notation: $9.11 \times 10^{-31}\text{ kg}$. The significant digits ($9.11$) are immediately visible, and the scale ($10^{-31}$) is unambiguous. Scientific notation also makes significant digits crystal-clear: $5.20 \times 10^3$ has exactly 3 SD, while $5200$ is ambiguous.

* **Coefficient $N$:** Expresses the exact significant digits of the measurement.
* **Exponent $n$:** Indicates the order of magnitude ($n > 0$ for numbers $\ge 10$; $n < 0$ for numbers $< 1$).

#### Arithmetic in Scientific Notation
* **Multiplication:** Multiply coefficients and add exponents:
  $$(a \times 10^p) \times (b \times 10^q) = (a \times b) \times 10^{p + q}$$
* **Division:** Divide coefficients and subtract exponents:
  $$\frac{a \times 10^p}{b \times 10^q} = \left(\frac{a}{b}\right) \times 10^{p - q}$$
* **Addition & Subtraction:** Exponents must be converted to match before coefficients are added or subtracted:
  $$(a \times 10^p) + (b \times 10^p) = (a + b) \times 10^p$$

  > [!tip] Why Must Exponents Match for Addition?
  > You can't add $3 \times 10^4$ and $5 \times 10^2$ directly because the digits don't occupy the same *place value* — it's like trying to add 3 hundreds to 5 ones without converting. Converting both to the same power is exactly the same as lining up decimal places in long addition.

---

### Formula Manipulation & Algebraic Isolation Techniques

In physics, equations describe relationships between measurable physical variables. You must master rearranging literal equations algebraically to isolate the unknown variable before plugging in numbers.

> [!question] Why Isolate the Variable Before Substituting Numbers?
> If you plug numbers into an un-rearranged formula and manipulate numbers, you risk arithmetic errors and lose track of the symbolic structure. Isolating the variable *first* means you're doing one clean algebraic operation — and then one clean numerical substitution. It also means your rearranged formula can be reused for any values of the problem, not just the specific numbers in front of you.

#### Systematic Isolation Protocol
1. **Clear Denominators:** Multiply all terms by common denominators to eliminate fractions.
2. **Expand or Group Terms:** Group terms containing the target variable on one side of the equals sign; move all terms not containing the target variable to the opposite side using inverse operations.
3. **Factor Out Target Variable:** If the target variable appears in multiple terms on the same side, factor it out as a common factor: $x(A + B)$.
4. **Divide by the Coefficient / Factor:** Isolate the target variable.
5. **Invert Powers or Roots:** If the target variable is squared ($x^2$), take the square root ($\sqrt{\dots}$); if under a radical ($\sqrt{x}$), square both sides.

---

## Metric MKS Conversions

The International System of Units (SI) in mechanics is founded on the **MKS system**:
* **M**eter ($\text{m}$) for length and displacement.
* **K**ilogram ($\text{kg}$) for mass.
* **S**econd ($\text{s}$) for time.

Derived units in kinematics (such as velocity in $\text{m/s}$ and acceleration in $\text{m/s}^2$) strictly require input values to be expressed in standard MKS units.

> [!question] Why Does Everyone Use the Same Unit System?
> In 1999, NASA's Mars Climate Orbiter was destroyed because one engineering team used imperial units (pound-force seconds) and another used metric (newton-seconds) — the spacecraft fired its thrusters at the wrong rate and burned up in the Martian atmosphere, costing \$327 million. A shared unit system isn't bureaucracy — it's how **numbers stay meaningful when they travel between people, equations, and instruments**. The MKS system (metres, kilograms, seconds) is chosen because all derived physical laws (force = $ma$, energy = $\frac{1}{2}mv^2$, etc.) are written assuming these base units.

### Metric Prefixes Hierarchy
| Prefix | Symbol | Multiplication Factor | Power of 10 |
| :--- | :---: | :---: | :---: |
| **kilo-** | $\text{k}$ | $1000$ | $10^3$ |
| *(base)* | — | $1$ | $10^0$ |
| **deci-** | $\text{d}$ | $0.1$ | $10^{-1}$ |
| **centi-** | $\text{c}$ | $0.01$ | $10^{-2}$ |
| **milli-** | $\text{m}$ | $0.001$ | $10^{-3}$ |
| **micro-** | $\mu$ | $0.000\,001$ | $10^{-6}$ |

### Dimensional Analysis & Unit Cancellation Factors
Dimensional analysis uses conversion factor fractions equal to $1$ arranged so that the unit to eliminate appears on the opposite side of the fraction bar (numerator vs. denominator), allowing direct cancellation.

> [!question] Why Does Multiplying by a Conversion Factor Not Change the Value?
> A conversion factor like $\frac{1000\text{ m}}{1\text{ km}}$ equals exactly $1$ — because $1000\text{ m} = 1\text{ km}$ is a true statement. Multiplying any measurement by $1$ doesn't change its physical quantity — only the label (unit) it's expressed in changes. This is why the method is called *dimensional analysis*: you're analyzing and canceling the units as algebraic symbols, just like canceling variables in a fraction. If the units cancel cleanly to the desired target unit, you know the algebra is set up correctly.

#### Fundamental Conversion Factors:
* Length: $1\text{ km} = 1000\text{ m}$; $1\text{ m} = 100\text{ cm} = 1000\text{ mm}$
* Time: $1\text{ h} = 60\text{ min} = 3600\text{ s}$; $1\text{ min} = 60\text{ s}$
* Speed ($\text{km/h} \longleftrightarrow \text{m/s}$):
  $$1\text{ km/h} = \left(\frac{1\text{ km}}{1\text{ h}}\right) \times \left(\frac{1000\text{ m}}{1\text{ km}}\right) \times \left(\frac{1\text{ h}}{3600\text{ s}}\right) = \frac{1000}{3600}\text{ m/s} = \frac{1}{3.6}\text{ m/s}$$

> [!tip] Direct Speed Conversion Rule
> - To convert $\text{km/h} \longrightarrow \text{m/s}$: **Divide by $3.6$**
> - To convert $\text{m/s} \longrightarrow \text{km/h}$: **Multiply by $3.6$**

---

### Percentage Error vs. Percentage Difference

Physics labs distinguish between **accuracy** (how close an experimental result is to the accepted scientific constant) and **precision** (how repeatable two experimental measurements are with each other).

> [!question] Why Do We Need Two Different Error Formulas?
> The two formulas answer two *fundamentally different* questions:
> - **% Error** asks: *"How far off is my result from the truth?"* — This requires knowing the truth (the accepted value) as the reference baseline. Think of it as comparing your measured $g$ against the accepted $9.81\text{ m/s}^2$.
> - **% Difference** asks: *"How consistent are my two measurements with each other?"* — When no official truth exists (you measured the same rope twice with two methods), you can only judge *repeatability* against the average of your own data.
>
> Using % Error when no accepted value exists would mean dividing by zero or a meaningless reference — hence the need for two separate tools.

![[attachments/accuracy_and_precision.svg]]
*Above: The four target combinations illustrating accuracy (closeness to centre = truth) vs. precision (tightness of grouping = repeatability). Source: Wikimedia Commons, CC BY-SA 3.0*

#### 1. Percentage Error (Measures Experimental Accuracy)
Used when a single experimental result ($\text{Exp}$) is compared against a well-established theoretical or accepted reference value ($\text{Acc}$), such as $g = 9.81\text{ m/s}^2$:
$$\% \text{Error} = \left\vert \frac{\text{Exp} - \text{Acc}}{\text{Acc}} \right\vert \times 100\%$$
* Absolute value bars ensure the error is expressed as a positive percentage.
* A smaller percentage error indicates high accuracy.

#### 2. Percentage Difference (Measures Precision & Repeatability)
Used when comparing two experimental trials ($\text{Meas}_1$ and $\text{Meas}_2$) where neither value is an official theoretical standard:
$$\% \text{Diff} = \frac{\vert \text{Meas}_1 - \text{Meas}_2 \vert}{\text{Average}} \times 100\% = \frac{\vert \text{Meas}_1 - \text{Meas}_2 \vert}{\frac{\text{Meas}_1 + \text{Meas}_2}{2}} \times 100\%$$
* A smaller percentage difference indicates high experimental repeatability and measurement precision.

---

## SECTION 2: EMBEDDED INSTRUCTIONAL VIDEOS

![[Unit 1 Physics - Video Directory#Subject 1: Introductory Mathematical Skills]]

---

## SECTION 3: HOW-TO WORKBOOK PROBLEM SOLVING GUIDES

This section provides step-by-step methodologies and problem-solving strategies for the exercise sets in `Intro Skills WB SPH3U.pdf` (Pages 1–16).

### 1. Significant Digits Counting & Rounding Methodology (Pages 1–4)

When analyzing an unfamiliar numerical measurement in the workbook, execute this 4-step decision tree:

> [!note] Significant Digits Decision Chart
> ![[attachments/significant_digits_rules.svg]]
> *Original diagram generated for SPH3U Physics*

#### Step-by-Step Rounding Procedure:
1. Identify the target number of significant digits (or decimal places for addition/subtraction).
2. Count from the leftmost non-zero digit to the target position.
3. Look at the immediate next digit (the first digit to be dropped):
   - If that digit is $\ge 5$, round up the target digit by $1$.
   - If that digit is $< 5$, leave the target digit unchanged.
4. Replace dropped whole-number places with placeholder zeros or convert directly to scientific notation.

---

### 2. Formula Isolation Step-by-Step Algebraic Procedure (Pages 5–8)

Workbook exercises require isolating target variables from complex multi-term physics formulas.

#### Exemplar Algorithm: Isolating $v$ from Total Energy
Consider the mechanical energy equation:
$$E_T = mg\Delta h + \frac{1}{2}mv^2$$
To isolate $v$:

* **Step 1: Isolate the term containing the target variable.**
  Subtract the gravitational potential energy term $mg\Delta h$ from both sides:
  $$E_T - mg\Delta h = \frac{1}{2}mv^2$$

* **Step 2: Clear the fractional coefficient.**
  Multiply the entire equation by $2$:
  $$2(E_T - mg\Delta h) = mv^2$$

* **Step 3: Eliminate multiplying factors on the target variable.**
  Divide both sides by mass $m$:
  $$\frac{2(E_T - mg\Delta h)}{m} = v^2$$

* **Step 4: Invert the exponent.**
  Take the positive square root of both sides to isolate the speed $v$:
  $$v = \sqrt{\frac{2(E_T - mg\Delta h)}{m}}$$

#### General Checklist for Workbook Rearrangement Problems:
- [ ] Circle the target variable in the original formula.
- [ ] Move terms not attached to the target variable to the other side using addition/subtraction.
- [ ] Clear fractions by cross-multiplying or multiplying by denominators.
- [ ] Factor out the target variable if it appears in more than one term.
- [ ] Divide by unwanted factors.
- [ ] Invert any powers or radicals as the final step.

---

### 3. Physics Road Trip & Multi-Step Conversion Framework (Pages 9–14)

Workbook road trip and speed conversion problems involve multi-segment journeys where times are recorded in minutes or hours and distances in kilometers, requiring final average speeds in standard MKS units ($\text{m/s}$).

#### 4-Step Solution Framework:
1. **Tabulate Given Quantities:**
   Separate the problem into individual legs or intervals. Record distance ($d_1, d_2$) and elapsed time ($\Delta t_1, \Delta t_2$) for each leg.
2. **Convert all Distances to Meters ($\text{m}$):**
   $$d \,(\text{m}) = d \,(\text{km}) \times \left(\frac{1000\text{ m}}{1\text{ km}}\right)$$
3. **Convert all Times to Seconds ($\text{s}$):**
   $$\Delta t \,(\text{s}) = \Delta t \,(\text{min}) \times \left(\frac{60\text{ s}}{1\text{ min}}\right) \quad \text{or} \quad \Delta t \,(\text{s}) = \Delta t \,(\text{h}) \times \left(\frac{3600\text{ s}}{1\text{ h}}\right)$$
4. **Compute Total Quantities & Apply Average Speed Formula:**
   $$d_{\text{total}} = d_1 + d_2 + \dots \qquad \Delta t_{\text{total}} = \Delta t_1 + \Delta t_2 + \dots$$
   $$v_{\text{avg}} = \frac{d_{\text{total}}}{\Delta t_{\text{total}}} \quad [\text{in m/s}]$$
5. **Apply Significant Digits:** Inspect original givens; round the final speed to the fewest significant digits present in the initial measurements.

---

### 4. Error Analysis Experimental Decision Guide (Pages 15–16)

When presented with experimental measurement data in the workbook, use this decision framework to determine whether to apply Percentage Error or Percentage Difference:

> [!note] Error Analysis Decision Flowchart
> ![[attachments/error_analysis_decision_tree.svg]]
> *Original diagram generated for SPH3U Physics*

#### Step-by-Step Calculation Guide:
1. **Identify the Given Values:** Label the values as either $(\text{Exp}, \text{Acc})$ or $(\text{Meas}_1, \text{Meas}_2)$.
2. **Compute the Numerator (Absolute Difference):**
   Subtract the two values and take the absolute value so the numerator is strictly non-negative.
3. **Compute the Denominator:**
   - For Percent Error: Use the accepted value $\text{Acc}$.
   - For Percent Difference: Calculate the arithmetic mean $\frac{\text{Meas}_1 + \text{Meas}_2}{2}$.
4. **Divide and Multiply by $100\%$:** Express the decimal fraction as a percentage.
5. **Round Properly:** Match significant digits to the precision of the experimental instruments.
