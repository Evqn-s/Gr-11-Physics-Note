# Matplotlib Kinematics Graph Skill

When asked to construct quantitative motion graphs, kinematic plot curves, or shaded integration areas under $v-t$ graphs, generate and execute a Python script using Matplotlib.

## Execution Rules
1. **Output Format:** Save all generated figures as scalable vector graphics (`.svg`) inside the vault's `attachments/` directory.
2. **Obsidian Embedding:** Embed the generated graph directly into the markdown note using Obsidian syntax: `![[attachments/<filename>.svg]]`.
3. **Styling Guidelines:**
   - Use a clean background suitable for dark/light vault themes (`#fdfdfd` or transparent).
   - Draw explicit horizontal ($y=0$) and vertical ($x=0$) axis lines.
   - Use clear LaTeX labels for axes: `r'Time $t \text{ (s)}$'`, `r'Velocity $\vec{v} \text{ (m/s)}$'`, `r'Displacement $\Delta \vec{d} \text{ (m)}$'`.
   - Always shade integration areas (displacement under $v-t$ curves or change in velocity under $a-t$ curves) using `ax.fill_between()`.

## Python Generation Template

```python
import matplotlib.pyplot as plt
import numpy as np
import os

# Ensure attachments folder exists
os.makedirs('attachments', exist_ok=True)

# Create high-resolution plot
fig, ax = plt.subplots(figsize=(6, 3.5), dpi=300)
ax.set_facecolor('#fdfdfd')

# Example Motion Data: Constant acceleration followed by uniform motion
t1 = np.linspace(0, 4, 100)
v1 = 2.5 * t1  # Acceleration phase

t2 = np.linspace(4, 10, 100)
v2 = np.full_like(t2, 10)  # Constant velocity phase

# Plot piecewise lines
ax.plot(t1, v1, color='#1f77b4', lw=2.5, label=r'Phase 1: $\vec{a} = 2.5 \text{ m/s}^2$')
ax.plot(t2, v2, color='#ff7f0e', lw=2.5, label=r'Phase 2: $\vec{v} = 10 \text{ m/s}$')

# Area shading for displacement
ax.fill_between(t1, v1, color='#1f77b4', alpha=0.2)
ax.fill_between(t2, v2, color='#ff7f0e', alpha=0.2)

# Axis Configuration
ax.axhline(0, color='black', linewidth=1)
ax.axvline(0, color='black', linewidth=1)
ax.set_xlabel(r'Time $t \text{ (s)}$', fontsize=11)
ax.set_ylabel(r'Velocity $\vec{v} \text{ (m/s)}$', fontsize=11)
ax.set_title(r'1D Kinematics: Velocity vs. Time', fontsize=12, fontweight='bold')
ax.grid(True, linestyle='--', alpha=0.5)
ax.legend(loc='lower right', fontsize=9)

plt.tight_layout()

# Save image directly to Obsidian attachments
output_path = 'attachments/kinematics_vt_graph.svg'
plt.savefig(output_path, format='svg')
plt.close()