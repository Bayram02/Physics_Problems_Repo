# Problem 5 — Elliptical Motion

> **Given:**
> $$x(t) = a\cos(\omega t), \qquad y(t) = b\sin(\omega t)$$

---

## Part 1 — Velocity and Acceleration

### Velocity

$$v_x = \frac{dx}{dt} = -a\omega\sin(\omega t)$$

$$v_y = \frac{dy}{dt} = b\omega\cos(\omega t)$$

$$\vec{v}(t) = \bigl(-a\omega\sin(\omega t),\; b\omega\cos(\omega t)\bigr)$$

### Acceleration

$$a_x = \frac{dv_x}{dt} = -a\omega^2\cos(\omega t) = -\omega^2 x(t)$$

$$a_y = \frac{dv_y}{dt} = -b\omega^2\sin(\omega t) = -\omega^2 y(t)$$

$$\boxed{\vec{a}(t) = -\omega^2\,\vec{r}(t)}$$

> Same form as circular motion — but here the semi-axes $a \neq b$, so the magnitude is not constant.

---

## Part 2 — Is the Speed Constant?

$$|\vec{v}|^2 = a^2\omega^2\sin^2(\omega t) + b^2\omega^2\cos^2(\omega t) = \omega^2\bigl(a^2\sin^2(\omega t) + b^2\cos^2(\omega t)\bigr)$$

This simplifies to a constant **only if** $a = b$ (which would make it a circle). In general:

$$\boxed{|\vec{v}| = \omega\sqrt{a^2\sin^2(\omega t) + b^2\cos^2(\omega t)} \neq \text{const}}$$

---

## Part 3 — Where is the Speed Maximum?

The speed squared $= \omega^2(a^2\sin^2 + b^2\cos^2)$ is maximised when the **larger** semi-axis dominates.

**Case $a > b$** (wider ellipse): maximum when $\sin^2(\omega t) = 1$, i.e. $\omega t = \pi/2$

$$|\vec{v}|_{\max} = a\omega \quad \text{at } x = 0,\; y = \pm b$$

**Case $b > a$** (taller ellipse): maximum when $\cos^2(\omega t) = 1$, i.e. $\omega t = 0$

$$|\vec{v}|_{\max} = b\omega \quad \text{at } x = \pm a,\; y = 0$$

> 💡 **Physical intuition:** The body moves fastest at the **narrow ends** of the ellipse. This is closely related to Kepler's second law in planetary orbits — planets speed up near the Sun (narrow end of their elliptical orbit).

---

## Part 4 — Trajectory Equation

Using $\cos(\omega t) = x/a$ and $\sin(\omega t) = y/b$:

$$\left(\frac{x}{a}\right)^2 + \left(\frac{y}{b}\right)^2 = \cos^2(\omega t) + \sin^2(\omega t) = 1$$

$$\boxed{\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1} \quad \text{(standard equation of an ellipse)}$$

---

## Summary

| Property | Result |
|----------|--------|
| Trajectory | Ellipse: $x^2/a^2 + y^2/b^2 = 1$ |
| $\vec{a}(t)$ | $-\omega^2\vec{r}$ — points toward center |
| Speed constant? | No (unless $a = b$) |
| Speed maximum | At narrow end — $\max(a,b)\cdot\omega$ |

---

## Visualization

> 🎬 **See the interactive version:** `problem_03_04_05_parametric_circular_elliptical.html`
> Use the sliders to change $a$, $b$, $\omega$. Watch how the animated $\vec{v}$ shrinks and grows around the ellipse, and see $|\vec{v}(t)|$ oscillate in the chart.