---
type: summary-note
subject: 1
tags:
  - SPH3U/summary
---

[[Unit 1 Kinematics - Master Study Roadmap|← Master Roadmap]] | [[Subject 1 - Introductory Skills Guide|Full Guide →]]

# Subject 1: Intro Mathematical Skills & Measurement Summary

> [!info] 1-Page Quick Reference
> High-yield summary of measurement precision, rounding mechanics, formula manipulation, and unit conversion rules for Gr. 11 Physics.

---

### Core Rules & Definitions
* **Significant Digits (SD):** Reflect measurement precision. All non-zero digits ($1$–$9$) and captive zeros ($7003$) count. Leading zeros ($0.004$) **never** count. Trailing zeros count **only if** an explicit decimal point is present ($45.00$ has $4$ SD; $4500$ has $2$ SD).
  - *Deeper theory:* See [[Subject 1 - Introductory Skills Guide#Significant Digits (SD) Counting Rules & Rounding Standards|Significant Digits Counting Rules]].
* **Scientific Notation:** $N \times 10^n$ where $1 \le |N| < 10$. Standardizes measurements and makes significant trailing zeros completely unambiguous (e.g., $4.50 \times 10^3\text{ m}$ has $3$ SD).
* **Percent Error (Accuracy):** Measures closeness of an experimental value to accepted truth:
  $$\% \text{Error} = \left\vert \frac{\text{Exp} - \text{Acc}}{\text{Acc}} \right\vert \times 100\%$$
* **Percent Difference (Precision):** Measures repeatability between two experimental trials:
  $$\% \text{Diff} = \frac{\vert \text{Meas}_1 - \text{Meas}_2 \vert}{\text{Average}} \times 100\% = \frac{\vert \text{Meas}_1 - \text{Meas}_2 \vert}{\frac{\text{Meas}_1 + \text{Meas}_2}{2}} \times 100\%$$

---

### Operational Precision & Rounding Rules
| Operation | Precision Governing Rule | Example |
| :--- | :--- | :--- |
| **Addition & Subtraction** | Round to the **fewest decimal places** | $12.1\text{ cm} + 3.456\text{ cm} = 15.556\text{ cm} \to \mathbf{15.6\text{ cm}}$ |
| **Multiplication & Division** | Round to the **fewest total SDs** | $4.50\text{ m} \times 2.1\text{ m} = 9.45\text{ m}^2 \to \mathbf{9.5\text{ m}^2}$ |
| **Multi-Step Work** | **Do not round intermediate steps** | Store values in calculator; round once on final line. |

---

### Formula Reference Block
* Average Speed:
  $$v_{\text{avg}} = \frac{\Delta d}{\Delta t}$$
* Accuracy:
  $$\% \text{Error} = \left\vert \frac{\text{Exp} - \text{Acc}}{\text{Acc}} \right\vert \times 100\%$$
* Precision:
  $$\% \text{Diff} = \frac{\vert \text{Meas}_1 - \text{Meas}_2 \vert}{\text{Average}} \times 100\%$$

---

### Quick How-To Checklists

#### 1. Unit Conversion Checklist ([[Subject 1 - Introductory Skills Guide#Metric MKS Conversions|MKS Conversions]])
- [ ] Identify given unit and target MKS unit ($\text{m}, \text{kg}, \text{s}$).
- [ ] Set up conversion fraction equal to $1$ so unwanted unit cancels out diagonally.
- [ ] Speed shortcut: $\text{km/h} \xrightarrow{\div 3.6} \text{m/s}$ and $\text{m/s} \xrightarrow{\times 3.6} \text{km/h}$.
- [ ] Ensure all inputs into physics formulas are in base MKS before solving.

#### 2. Formula Isolation Checklist ([[Subject 1 - Introductory Skills Guide#Formula Manipulation & Algebraic Isolation Techniques|Formula Manipulation Guide]])
- [ ] Eliminate fractions first by multiplying both sides by common denominators.
- [ ] Move non-target terms away using addition or subtraction.
- [ ] Divide both sides by any coefficients attached to target variable.
- [ ] Invert exponents (take $\sqrt{\dots}$ for $x^2$) as the final algebraic step.

---

### Recommended Video Tutorials
* **Formula Isolation:** [Rearranging Equations & Formulas Tutorial](https://www.youtube.com/watch?v=_W2n5r9QZcQ)
* **Metric Conversions:** [Unit Conversion via Dimensional Analysis](https://www.youtube.com/watch?v=HRe1mire4Gc)
* **Significant Digits:** [Significant Figures Made Easy](https://www.youtube.com/watch?v=5U3Ks7_4-g4)
* *Full catalog:* See [[Unit 1 Physics - Video Directory#Subject 1: Introductory Mathematical Skills|Video Directory: Intro Skills]]
