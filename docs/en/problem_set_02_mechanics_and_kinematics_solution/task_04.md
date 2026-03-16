# Problem 4 — Circular Motion

> A body moves in a circle of radius $R$ with constant angular velocity $\omega$.

---

## Part 1 — Position, Velocity, Acceleration

### Position vector

$$\vec{r}(t) = \bigl(R\cos(\omega t),\; R\sin(\omega t)\bigr)$$

### Velocity — differentiate $\vec{r}$

$$\vec{v}(t) = \frac{d\vec{r}}{dt} = \bigl(-R\omega\sin(\omega t),\; R\omega\cos(\omega t)\bigr)$$

### Acceleration — differentiate $\vec{v}$

$$\vec{a}(t) = \frac{d\vec{v}}{dt} = \bigl(-R\omega^2\cos(\omega t),\; -R\omega^2\sin(\omega t)\bigr)$$

---

## Part 2 — Magnitudes

$$|\vec{r}(t)| = \sqrt{R^2\cos^2 + R^2\sin^2} = \boxed{R = \text{const}}$$

$$|\vec{v}(t)| = \sqrt{R^2\omega^2\sin^2 + R^2\omega^2\cos^2} = \boxed{R\omega = \text{const}}$$

$$|\vec{a}(t)| = \sqrt{R^2\omega^4\cos^2 + R^2\omega^4\sin^2} = \boxed{R\omega^2 = \text{const}}$$

> All three magnitudes are **constant** — yet the direction of $\vec{v}$ and $\vec{a}$ continuously rotate.

---

## Part 3 — Proof that Acceleration is Centripetal

Compare $\vec{a}(t)$ with $\vec{r}(t)$:

$$\vec{a}(t) = \bigl(-R\omega^2\cos(\omega t),\; -R\omega^2\sin(\omega t)\bigr) = -\omega^2 \bigl(R\cos(\omega t),\; R\sin(\omega t)\bigr)$$

$$\boxed{\vec{a}(t) = -\omega^2\, \vec{r}(t)}$$

Since $\vec{a}$ is a **negative multiple of $\vec{r}$**, it always points **toward the center** (opposite to the position vector). This is precisely the definition of centripetal acceleration.

| Quantity | Value | Meaning |
|----------|-------|---------|
| $\vec{a} \cdot \vec{r}$ | $-R^2\omega^2 < 0$ | opposite directions |
| $\vec{a} \cdot \vec{v}$ | $0$ | perpendicular to velocity |
| Direction of $\vec{a}$ | toward center | centripetal |

---

## Part 4 — Mutual Orientation of Vectors

- $\vec{r}$ points **outward** from center to body.
- $\vec{v}$ is **perpendicular** to $\vec{r}$ (tangent to the circle).
- $\vec{a}$ points **inward** toward the center, antiparallel to $\vec{r}$.

You can verify: $\vec{r} \cdot \vec{v} = R\cos\cdot(-R\omega\sin) + R\sin\cdot(R\omega\cos) = 0$ ✅

---

> 💡 **Why does constant speed not mean zero acceleration?**
> Speed $|\vec{v}| = R\omega$ is constant, but the **direction** of $\vec{v}$ rotates. A changing direction means a non-zero acceleration — even with no change in speed.

---

## Visualization

> 🎬 **See the interactive version:** `problem_03_04_05_parametric_circular_elliptical.html`
> The animation draws the rotating vectors $\vec{r}$ (yellow), $\vec{v}$ (green), $\vec{a}$ (red) in real time. Use the sliders to change $R$ and $\omega$.