# Problem 2 — Projectile Motion

> A body is launched with initial speed $v_0$ at angle $\alpha$ above the horizontal. No air resistance.

---

## Part 1 — Equations of Motion

### Decompose initial velocity

$$v_{0x} = v_0 \cos\alpha \qquad v_{0y} = v_0 \sin\alpha$$

### Horizontal direction — no force acts here

$$a_x = 0 \implies v_x(t) = v_0\cos\alpha$$

$$\boxed{x(t) = v_0 \cos\alpha \cdot t}$$

### Vertical direction — gravity decelerates the body

$$a_y = -g \implies v_y(t) = v_0\sin\alpha - gt$$

$$\boxed{y(t) = v_0 \sin\alpha \cdot t - \frac{1}{2}g t^2}$$

---

## Part 2 — Time of Flight

The body lands when $y(t) = 0$ again:

$$0 = t\!\left(v_0\sin\alpha - \frac{1}{2}g t\right)$$

This gives two solutions: $t_1 = 0$ (launch) and

$$\boxed{T = \frac{2 v_0 \sin\alpha}{g}}$$

---

## Part 3 — Maximum Height

The body reaches maximum height when $v_y = 0$:

$$v_0\sin\alpha - g\,t_{\text{peak}} = 0 \implies t_{\text{peak}} = \frac{v_0\sin\alpha}{g} = \frac{T}{2}$$

Substituting into $y(t)$:

$$\boxed{H = \frac{v_0^2 \sin^2\alpha}{2g}}$$

---

## Part 4 — Range

The horizontal distance at landing $t = T$:

$$R = v_0\cos\alpha \cdot T = v_0\cos\alpha \cdot \frac{2v_0\sin\alpha}{g}$$

Using the identity $2\sin\alpha\cos\alpha = \sin 2\alpha$:

$$\boxed{R = \frac{v_0^2 \sin 2\alpha}{g}}$$

---

## Part 5 — Optimal Angle for Maximum Range

The range $R = \dfrac{v_0^2 \sin 2\alpha}{g}$ is maximised when $\sin 2\alpha = 1$:

$$2\alpha = 90° \implies \boxed{\alpha_{\text{opt}} = 45°}$$

> 💡 **Symmetry:** Angles $\alpha$ and $(90° - \alpha)$ give the **same range**. For example, 30° and 60° produce identical $R$, but different heights and flight times.

---

## Part 6 — Numerical Example

For $v_0 = 20$ m/s, $\alpha = 45°$, $g = 9.81$ m/s²:

| Quantity | Formula | Value |
|----------|---------|-------|
| $T$ | $2 v_0\sin\alpha / g$ | $2.89$ s |
| $H$ | $v_0^2\sin^2\alpha / (2g)$ | $10.19$ m |
| $R$ | $v_0^2\sin 2\alpha / g$ | $40.77$ m |

---

## Part 7 — Trajectory Equation (eliminating t)

From $x = v_0\cos\alpha \cdot t$ we get $t = x/(v_0\cos\alpha)$. Substituting into $y(t)$:

$$y = x\tan\alpha - \frac{g}{2v_0^2\cos^2\alpha}\,x^2$$

This is a **parabola** opening downward — the trajectory of every projectile.

---

## Visualization
> Adjust $v_0$ and $\alpha$ live. Toggle multiple angles to compare trajectories and verify the 30°/60° symmetry.

### Summary table — different angles (v₀ = 20 m/s)

| $\alpha$ | $T$ (s) | $H$ (m) | $R$ (m) |
|----------|---------|---------|---------|
| 15° | 1.05 | 1.35 | 20.39 |
| 30° | 2.04 | 5.10 | 35.35 |
| **45°** | **2.89** | **10.19** | **40.77** ← max |
| 60° | 3.53 | 15.29 | 35.35 |
| 75° | 3.94 | 19.05 | 20.39 |

> Note: 30° and 60° share the same range — this confirms the $\alpha \leftrightarrow 90°-\alpha$ symmetry.