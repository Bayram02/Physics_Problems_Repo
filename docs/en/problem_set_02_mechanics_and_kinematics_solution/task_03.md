# Problem 3 — Parametric Path: Elimination of Time & Acceleration Analysis

> **Given:**
> $$x(t) = 2t^2, \qquad y(t) = 3t^3$$

---

## Part 1 — Eliminate the Parameter t

From $x(t) = 2t^2$ solve for $t$:

$$t^2 = \frac{x}{2} \implies t = \sqrt{\frac{x}{2}} \quad (t \geq 0)$$

Substitute into $y(t) = 3t^3 = 3t \cdot t^2$:

$$y = 3 \cdot \sqrt{\frac{x}{2}} \cdot \frac{x}{2} = \frac{3}{2\sqrt{2}}\, x^{3/2}$$

$$\boxed{y = \frac{3}{2\sqrt{2}}\, x^{3/2}}$$

This is a **power-law curve** $y \sim x^{1.5}$, steeper than a parabola.

---

## Part 2 — Velocity Vector

Differentiate each component with respect to $t$:

$$v_x(t) = \frac{dx}{dt} = 4t$$

$$v_y(t) = \frac{dy}{dt} = 9t^2$$

$$\vec{v}(t) = (4t,\; 9t^2)$$

**Magnitude:**

$$|\vec{v}(t)| = \sqrt{(4t)^2 + (9t^2)^2} = \sqrt{16t^2 + 81t^4} = t\sqrt{16 + 81t^2}$$

> At $t = 0$: the body is momentarily at rest ($|\vec{v}| = 0$).

---

## Part 3 — Acceleration Vector

Differentiate the velocity components:

$$a_x(t) = \frac{dv_x}{dt} = 4 \quad \text{(constant!)}$$

$$a_y(t) = \frac{dv_y}{dt} = 18t \quad \text{(grows with time)}$$

$$\vec{a}(t) = (4,\; 18t)$$

**Magnitude:**

$$|\vec{a}(t)| = \sqrt{16 + (18t)^2} = \sqrt{16 + 324t^2}$$

---

## Part 4 — Is the Acceleration Constant?

| Component | Value | Constant? |
|-----------|-------|-----------|
| $a_x$ | $4$ | ✅ Yes |
| $a_y$ | $18t$ | ❌ No — changes with time |
| $\|\vec{a}\|$ | $\sqrt{16+324t^2}$ | ❌ No — increases |
| direction of $\vec{a}$ | $\arctan(18t/4)$ | ❌ No — rotates |

$$\boxed{\text{Acceleration is NOT constant.}}$$

Although the horizontal component $a_x = 4$ is constant, the vertical component $a_y = 18t$ grows linearly. The **vector** $\vec{a}$ changes both its magnitude and direction over time.

> 💡 **Physical interpretation:** The $x$-direction behaves like uniform acceleration (constant force), while the $y$-direction has a force that grows in time — this is an unusual but valid kinematic setup for a mathematical path.

---

## Visualization

> 🎬 **See the interactive version:** `problem_03_04_05_parametric_circular_elliptical.html`
> Shows the trajectory $y$ vs $x$ and plots of $|\vec{v}(t)|$ and $|\vec{a}(t)|$ side by side.