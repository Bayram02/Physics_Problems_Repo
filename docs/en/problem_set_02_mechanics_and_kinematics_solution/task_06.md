# Problem 6 — Cycloid: Trajectory of a Point on a Rolling Circle

> **Given:**
> $$x(t) = R(\omega t - \sin(\omega t)), \qquad y(t) = R(1 - \cos(\omega t))$$

---

## Part 1 — Velocity Vector

Differentiate each component:

$$v_x(t) = \frac{dx}{dt} = R\omega(1 - \cos(\omega t))$$

$$v_y(t) = \frac{dy}{dt} = R\omega\sin(\omega t)$$

$$\boxed{\vec{v}(t) = R\omega\bigl(1 - \cos(\omega t),\; \sin(\omega t)\bigr)}$$

---

## Part 2 — Acceleration Vector

$$a_x(t) = \frac{dv_x}{dt} = R\omega^2\sin(\omega t)$$

$$a_y(t) = \frac{dv_y}{dt} = R\omega^2\cos(\omega t)$$

$$\boxed{\vec{a}(t) = R\omega^2\bigl(\sin(\omega t),\; \cos(\omega t)\bigr)}$$

---

## Part 3 — Speed |v(t)|

$$|\vec{v}|^2 = R^2\omega^2\bigl[(1-\cos)^2 + \sin^2\bigr] = R^2\omega^2\bigl[1 - 2\cos + \cos^2 + \sin^2\bigr] = R^2\omega^2\bigl[2 - 2\cos(\omega t)\bigr]$$

Using the half-angle identity $2 - 2\cos\theta = 4\sin^2(\theta/2)$:

$$\boxed{|\vec{v}(t)| = 2R\omega\left|\sin\!\left(\frac{\omega t}{2}\right)\right|}$$

### When does the point stop? ($|\vec{v}| = 0$)

$$\sin\!\left(\frac{\omega t}{2}\right) = 0 \implies \frac{\omega t}{2} = n\pi \implies \boxed{t_n = \frac{2n\pi}{\omega}, \quad n = 0, 1, 2, \ldots}$$

> Every time the point **touches the ground** it momentarily stops — these are the cusps (sharp points) of the cycloid curve.

---

## Part 4 — Maximum Speed

The speed is maximum when $\left|\sin(\omega t/2)\right| = 1$, i.e. $\omega t/2 = \pi/2 + n\pi$:

$$t = \frac{\pi}{\omega}, \frac{3\pi}{\omega}, \ldots \quad \text{(top of the circle)}$$

$$\boxed{|\vec{v}|_{\max} = 2R\omega}$$

> The point moves **twice as fast** at the top of the circle as the center of the circle moves along the ground. This is because at the top, the rolling velocity and the translational velocity add up.

---

## Part 5 — Acceleration Magnitude

$$|\vec{a}(t)| = R\omega^2\sqrt{\sin^2(\omega t) + \cos^2(\omega t)} = \boxed{R\omega^2 = \text{const}}$$

> 💡 **Surprising result:** Although the velocity oscillates between 0 and $2R\omega$, the **magnitude of acceleration is constant** $= R\omega^2$. This equals the centripetal acceleration of circular motion in the rolling circle's own frame.

---

## Part 6 — Comparison with Circular Motion

| Property | Circular motion | Cycloid |
|----------|----------------|---------|
| $|\vec{r}|$ | $R = $ const | varies |
| $|\vec{v}|$ | $R\omega = $ const | oscillates $0 \to 2R\omega$ |
| $|\vec{a}|$ | $R\omega^2 = $ const | $R\omega^2 = $ const ✅ |
| trajectory | circle | cycloid (cusps at ground) |

In the reference frame attached to the circle's center, the point simply moves in a circle. Seen from the ground (lab frame), this combines with the translation of the center → cycloid.

---

## Visualization

> 🎬 **See the interactive version:** `problem_06_cycloid.html`
> Watch the rolling circle, the rim point drawing the cycloid, and the live speed chart showing the oscillation. The velocity (cyan) and acceleration (green) vectors are drawn at every moment.