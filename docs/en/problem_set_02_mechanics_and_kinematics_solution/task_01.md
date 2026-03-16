# Problem 1 — Uniform and Uniformly Accelerated Motion

> **Equation of motion:**
> $$x(t) = x_0 + v_0 t + \frac{1}{2} a t^2$$

---

## Part 1 — Deriving v(t) and a(t)

**Velocity** is the first derivative of position with respect to time:

$$v(t) = \frac{dx}{dt} = v_0 + at$$

**Acceleration** is the second derivative of position (first derivative of velocity):

$$a(t) = \frac{dv}{dt} = \frac{d^2x}{dt^2} = a = \text{const}$$

> 💡 **Key insight:** In uniformly accelerated motion the acceleration is **constant** — it does not depend on time. The velocity changes linearly with time.

---

## Part 2 — Numerical Analysis

### Given parameters

| Symbol | Value | Meaning |
|--------|-------|---------|
| $x_0$  | $0$ m | initial position |
| $v_0$  | $5$ m/s | initial velocity |
| $a$    | $-2$ m/s² | constant deceleration |

The specific equations become:

$$x(t) = 5t - t^2$$

$$v(t) = 5 - 2t$$

$$a(t) = -2 \; \text{m/s}^2 = \text{const}$$

---

### Stopping time

The body stops when $v(t) = 0$:

$$5 - 2t = 0 \implies t_{\text{stop}} = \frac{5}{2} = \boxed{2.5 \; \text{s}}$$

---

### Maximum velocity

Since $a < 0$ the velocity **decreases** over time. Therefore the maximum velocity is at $t = 0$:

$$v_{\max} = v_0 = \boxed{5 \; \text{m/s}}$$

> **General rule:** If $a > 0$ the speed increases → no finite maximum in the positive direction. If $a < 0$ the body decelerates, stops, then accelerates in the reverse direction.

---

### Maximum displacement

The maximum displacement occurs at the stopping time $t_{\text{stop}} = 2.5$ s (the body is furthest from the origin before reversing):

$$x_{\max} = x(2.5) = 5 \cdot 2.5 - (2.5)^2 = 12.5 - 6.25 = \boxed{6.25 \; \text{m}}$$

---

## Part 3 — Visualization

> 🎬 **See the interactive version:** `problem_01_kinematics.html`
> Open it in a browser to use sliders and see all three graphs update in real time.

### What the graphs look like

| Graph | Shape | Key feature |
|-------|-------|-------------|
| $x(t)$ | Parabola opening downward | Maximum at $t = 2.5$ s |
| $v(t)$ | Straight line with negative slope | Crosses zero at $t = 2.5$ s |
| $a(t)$ | Horizontal line at $-2$ | Constant — never changes |

### Sketch description

```
x(t)  ▲
6.25  |    *
      |  *   *
      | *      *
      |*         *
      +──────────────▶ t
      0   2.5   5

v(t)  ▲
 5    |*
      | *
      |  *
      |   *
    0 |────*─────▶ t
      |    2.5
 -5   |      *

a(t)  ▲
      |
    0 |────────────▶ t
      |
  -2  |────────────  (constant line)
```

---

## Summary

$$\boxed{t_{\text{stop}} = 2.5 \; \text{s}, \quad x_{\max} = 6.25 \; \text{m}, \quad v_{\max} = 5 \; \text{m/s at } t=0}$$