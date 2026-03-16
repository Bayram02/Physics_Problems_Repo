# Problem 7 — 2D Motion with Given Acceleration

> **Given:**
> $$\vec{a} = (2,\; -3) \; \text{m/s}^2, \qquad \vec{v}(0) = (1,\; 0) \; \text{m/s}, \qquad \vec{r}(0) = (0,\; 0) \; \text{m}$$

---

## Part 1 — Velocity v(t)

We integrate the acceleration (constant), using $\vec{v}(t) = \vec{v}(0) + \vec{a}\,t$:

$$v_x(t) = 1 + 2t$$

$$v_y(t) = 0 + (-3)t = -3t$$

$$\boxed{\vec{v}(t) = (1 + 2t,\; -3t)}$$

---

## Part 2 — Position r(t)

We integrate the velocity, using $\vec{r}(t) = \vec{r}(0) + \vec{v}(0)\,t + \tfrac{1}{2}\vec{a}\,t^2$:

$$x(t) = 0 + 1\cdot t + \frac{1}{2}\cdot 2\cdot t^2 = t + t^2$$

$$y(t) = 0 + 0\cdot t + \frac{1}{2}\cdot(-3)\cdot t^2 = -\frac{3}{2}t^2$$

$$\boxed{\vec{r}(t) = \bigl(t + t^2,\; -\tfrac{3}{2}t^2\bigr)}$$

---

## Part 3 — Trajectory Equation (eliminating t)

From $y = -\tfrac{3}{2}t^2$ we get $t^2 = -\tfrac{2}{3}y$.

From $x = t + t^2 = t - \tfrac{2}{3}y$ we get $t = x + \tfrac{2}{3}y$.

Substituting back into $t^2 = -\tfrac{2}{3}y$:

$$\left(x + \frac{2}{3}y\right)^2 = -\frac{2}{3}y$$

This is a **parabola** in the $xy$-plane (but rotated relative to the axes).

---

## Part 4 — Vectors at selected moments

| $t$ (s) | $x$ (m) | $y$ (m) | $v_x$ | $v_y$ | $\|v\|$ |
|---------|---------|---------|-------|-------|---------|
| 0 | 0 | 0 | 1 | 0 | 1.00 |
| 1 | 2 | −1.5 | 3 | −3 | 4.24 |
| 2 | 6 | −6 | 5 | −6 | 7.81 |
| 3 | 12 | −13.5 | 7 | −9 | 11.40 |

> 💡 The body moves to the right and downward. Because $a_x > 0$ and $a_y < 0$, the trajectory curves right-and-down, like a projectile with a horizontal push.

---

## Visualization

> 🎬 **See the interactive version:** `problem_07_08_09_10_advanced.html`
> The trajectory is drawn with $\vec{v}$ (cyan) and $\vec{a}$ (pink) vectors shown at $t = 1.5, 3, 4.5$ s.  