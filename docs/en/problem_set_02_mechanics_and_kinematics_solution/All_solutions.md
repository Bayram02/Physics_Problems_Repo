# Problem Set 02 — Mechanics I: Kinematics
### Complete Solutions Notebook

> **How to read this file in VS Code:**
> Press `Ctrl+Shift+V` to open the Markdown Preview. Install the extension **"Markdown All in One"** by Yu Zhang so that all `$...$` math formulas render as proper equations.

---

# Problem 1 — Uniform and Uniformly Accelerated Motion

> **Equation of motion:**
> $$x(t) = x_0 + v_0 t + \frac{1}{2} a t^2$$

## 1.1 — Deriving v(t) and a(t)

**Velocity** is the first derivative of position with respect to time:

$$v(t) = \frac{dx}{dt} = v_0 + at$$

**Acceleration** is the second derivative of position (first derivative of velocity):

$$a(t) = \frac{dv}{dt} = \frac{d^2x}{dt^2} = a = \text{const}$$

> 💡 **Key insight:** In uniformly accelerated motion the acceleration is **constant** — it does not depend on time. The velocity changes linearly.

## 1.2 — Numerical Analysis

### Given parameters

| Symbol | Value | Meaning |
|--------|-------|---------|
| $x_0$  | $0$ m | initial position |
| $v_0$  | $5$ m/s | initial velocity |
| $a$    | $-2$ m/s² | constant deceleration |

The specific equations become:

$$x(t) = 5t - t^2, \qquad v(t) = 5 - 2t, \qquad a(t) = -2 \; \text{m/s}^2$$

### Stopping time

The body stops when $v(t) = 0$:

$$5 - 2t = 0 \implies \boxed{t_{\text{stop}} = 2.5 \; \text{s}}$$

### Maximum velocity

Since $a < 0$ the velocity **decreases** over time. Maximum is at $t = 0$:

$$\boxed{v_{\max} = v_0 = 5 \; \text{m/s}}$$

### Maximum displacement

Maximum displacement occurs at $t_{\text{stop}} = 2.5$ s:

$$x_{\max} = x(2.5) = 5 \cdot 2.5 - (2.5)^2 = 12.5 - 6.25 = \boxed{6.25 \; \text{m}}$$

## 1.3 — Graph Description

| Graph | Shape | Key feature |
|-------|-------|-------------|
| $x(t)$ | Parabola opening downward | Maximum at $t = 2.5$ s |
| $v(t)$ | Straight line, negative slope | Crosses zero at $t = 2.5$ s |
| $a(t)$ | Horizontal line at $-2$ | Constant — never changes |

### Summary

$$\boxed{t_{\text{stop}} = 2.5 \; \text{s}, \quad x_{\max} = 6.25 \; \text{m}, \quad v_{\max} = 5 \; \text{m/s at } t=0}$$

> 🎬 **Interactive visualization:** `problem_01_kinematics.html`

---

# Problem 2 — Projectile Motion

> A body is launched with initial speed $v_0$ at angle $\alpha$ above the horizontal. No air resistance.

## 2.1 — Equations of Motion

### Decompose initial velocity

$$v_{0x} = v_0 \cos\alpha, \qquad v_{0y} = v_0 \sin\alpha$$

### Horizontal direction — no force acts here

$$a_x = 0 \implies v_x(t) = v_0\cos\alpha \implies \boxed{x(t) = v_0 \cos\alpha \cdot t}$$

### Vertical direction — gravity decelerates the body

$$a_y = -g \implies v_y(t) = v_0\sin\alpha - gt \implies \boxed{y(t) = v_0 \sin\alpha \cdot t - \frac{1}{2}g t^2}$$

## 2.2 — Time of Flight

The body lands when $y(t) = 0$:

$$0 = t\!\left(v_0\sin\alpha - \frac{1}{2}g t\right) \implies \boxed{T = \frac{2 v_0 \sin\alpha}{g}}$$

## 2.3 — Maximum Height

The body peaks when $v_y = 0$, i.e. at $t_{\text{peak}} = v_0\sin\alpha / g = T/2$:

$$\boxed{H = \frac{v_0^2 \sin^2\alpha}{2g}}$$

## 2.4 — Range

$$R = v_0\cos\alpha \cdot T = \frac{2v_0^2\sin\alpha\cos\alpha}{g} \implies \boxed{R = \frac{v_0^2 \sin 2\alpha}{g}}$$

## 2.5 — Optimal Angle

$R$ is maximised when $\sin 2\alpha = 1$:

$$2\alpha = 90° \implies \boxed{\alpha_{\text{opt}} = 45°}$$

> 💡 **Symmetry:** Angles $\alpha$ and $(90°-\alpha)$ give the **same range** but different heights and flight times. For example, 30° and 60° produce identical $R$.

## 2.6 — Trajectory Equation (eliminating t)

From $x = v_0\cos\alpha \cdot t$ we get $t = x/(v_0\cos\alpha)$. Substituting into $y(t)$:

$$\boxed{y = x\tan\alpha - \frac{g}{2v_0^2\cos^2\alpha}\,x^2}$$

This is a **parabola** — the trajectory of every projectile.

## 2.7 — Numerical Example ($v_0 = 20$ m/s, $\alpha = 45°$, $g = 9.81$ m/s²)

| Quantity | Value |
|----------|-------|
| $T$ | $2.89$ s |
| $H$ | $10.19$ m |
| $R$ | $40.77$ m |

> 🎬 **Interactive visualization:** `problem_02_projectile.html`

---

# Problem 3 — Parametric Path: x = 2t², y = 3t³

## 3.1 — Eliminate the Parameter t

From $x(t) = 2t^2$:

$$t^2 = \frac{x}{2} \implies t = \sqrt{\frac{x}{2}}$$

Substitute into $y = 3t^3 = 3t \cdot t^2$:

$$\boxed{y = \frac{3}{2\sqrt{2}}\, x^{3/2}}$$

This is a power-law curve $y \sim x^{1.5}$, steeper than a parabola.

## 3.2 — Velocity Vector

$$v_x(t) = \frac{dx}{dt} = 4t, \qquad v_y(t) = \frac{dy}{dt} = 9t^2$$

$$\vec{v}(t) = (4t,\; 9t^2), \qquad |\vec{v}(t)| = \sqrt{16t^2 + 81t^4} = t\sqrt{16 + 81t^2}$$

## 3.3 — Acceleration Vector

$$a_x(t) = \frac{dv_x}{dt} = 4 \quad \text{(constant)}, \qquad a_y(t) = \frac{dv_y}{dt} = 18t \quad \text{(grows with time)}$$

$$\vec{a}(t) = (4,\; 18t), \qquad |\vec{a}(t)| = \sqrt{16 + 324t^2}$$

## 3.4 — Is the Acceleration Constant?

| Component | Value | Constant? |
|-----------|-------|-----------|
| $a_x$ | $4$ | ✅ Yes |
| $a_y$ | $18t$ | ❌ No |
| $\|\vec{a}\|$ | $\sqrt{16+324t^2}$ | ❌ No |
| direction of $\vec{a}$ | $\arctan(18t/4)$ | ❌ No |

$$\boxed{\text{Acceleration is NOT constant.}}$$

> 💡 Although $a_x = 4$ is constant, $a_y = 18t$ grows linearly. Both the magnitude and direction of $\vec{a}$ change over time.

> 🎬 **Interactive visualization:** `problem_03_04_05_parametric_circular_elliptical.html`

---

# Problem 4 — Circular Motion

> A body moves in a circle of radius $R$ with constant angular velocity $\omega$.

## 4.1 — Position, Velocity, Acceleration

$$\vec{r}(t) = \bigl(R\cos(\omega t),\; R\sin(\omega t)\bigr)$$

$$\vec{v}(t) = \frac{d\vec{r}}{dt} = \bigl(-R\omega\sin(\omega t),\; R\omega\cos(\omega t)\bigr)$$

$$\vec{a}(t) = \frac{d\vec{v}}{dt} = \bigl(-R\omega^2\cos(\omega t),\; -R\omega^2\sin(\omega t)\bigr)$$

## 4.2 — Magnitudes

$$|\vec{r}(t)| = \boxed{R = \text{const}}, \qquad |\vec{v}(t)| = \boxed{R\omega = \text{const}}, \qquad |\vec{a}(t)| = \boxed{R\omega^2 = \text{const}}$$

All three magnitudes are **constant** — yet the directions of $\vec{v}$ and $\vec{a}$ continuously rotate.

## 4.3 — Proof that Acceleration is Centripetal

Compare $\vec{a}(t)$ with $\vec{r}(t)$:

$$\vec{a}(t) = \bigl(-R\omega^2\cos(\omega t),\; -R\omega^2\sin(\omega t)\bigr) = -\omega^2\bigl(R\cos(\omega t),\; R\sin(\omega t)\bigr)$$

$$\boxed{\vec{a}(t) = -\omega^2\, \vec{r}(t)}$$

Since $\vec{a}$ is a **negative multiple** of $\vec{r}$, it always points directly **toward the center**. This is the definition of centripetal acceleration.

We can also verify mutual perpendicularity:

$$\vec{r} \cdot \vec{v} = R\cos\cdot(-R\omega\sin) + R\sin\cdot(R\omega\cos) = 0 \; ✅$$

> 💡 **Why does constant speed not mean zero acceleration?** Speed $|\vec{v}| = R\omega$ is constant, but the *direction* of $\vec{v}$ rotates. A changing direction means a non-zero acceleration.

> 🎬 **Interactive visualization:** `problem_03_04_05_parametric_circular_elliptical.html`

---

# Problem 5 — Elliptical Motion

> **Given:** $x(t) = a\cos(\omega t)$, $y(t) = b\sin(\omega t)$

## 5.1 — Velocity and Acceleration

$$\vec{v}(t) = \bigl(-a\omega\sin(\omega t),\; b\omega\cos(\omega t)\bigr)$$

$$\vec{a}(t) = \bigl(-a\omega^2\cos(\omega t),\; -b\omega^2\sin(\omega t)\bigr) = \boxed{-\omega^2\,\vec{r}(t)}$$

## 5.2 — Is the Speed Constant?

$$|\vec{v}| = \omega\sqrt{a^2\sin^2(\omega t) + b^2\cos^2(\omega t)}$$

This equals a constant only if $a = b$ (which gives a circle). In general:

$$\boxed{|\vec{v}| \neq \text{const}}$$

## 5.3 — Where is Speed Maximum?

**If $a > b$:** maximum when $\sin^2 = 1$ → $\omega t = \pi/2$ → at $(0, \pm b)$, speed $= a\omega$

**If $b > a$:** maximum when $\cos^2 = 1$ → $\omega t = 0$ → at $(\pm a, 0)$, speed $= b\omega$

$$\boxed{|\vec{v}|_{\max} = \max(a,b)\cdot\omega \quad \text{at the narrow end of the ellipse}}$$

> 💡 **Connection to Kepler's second law:** Planets speed up near the Sun (narrow end of their elliptical orbit) — the same effect.

## 5.4 — Trajectory Equation

Using $\cos(\omega t) = x/a$ and $\sin(\omega t) = y/b$:

$$\boxed{\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1}$$

> 🎬 **Interactive visualization:** `problem_03_04_05_parametric_circular_elliptical.html`

---

# Problem 6 — Cycloid: Trajectory of a Point on a Rolling Circle

> **Given:** $x(t) = R(\omega t - \sin(\omega t))$, $y(t) = R(1 - \cos(\omega t))$

## 6.1 — Velocity Vector

$$v_x(t) = R\omega(1 - \cos(\omega t)), \qquad v_y(t) = R\omega\sin(\omega t)$$

$$\boxed{\vec{v}(t) = R\omega\bigl(1 - \cos(\omega t),\; \sin(\omega t)\bigr)}$$

## 6.2 — Acceleration Vector

$$a_x(t) = R\omega^2\sin(\omega t), \qquad a_y(t) = R\omega^2\cos(\omega t)$$

$$\boxed{\vec{a}(t) = R\omega^2\bigl(\sin(\omega t),\; \cos(\omega t)\bigr)}$$

## 6.3 — Speed |v(t)|

$$|\vec{v}|^2 = R^2\omega^2\bigl[(1-\cos)^2 + \sin^2\bigr] = R^2\omega^2\bigl[2 - 2\cos(\omega t)\bigr]$$

Using the half-angle identity $2 - 2\cos\theta = 4\sin^2(\theta/2)$:

$$\boxed{|\vec{v}(t)| = 2R\omega\left|\sin\!\left(\frac{\omega t}{2}\right)\right|}$$

## 6.4 — When Does the Point Stop?

$$\sin\!\left(\frac{\omega t}{2}\right) = 0 \implies \boxed{t_n = \frac{2n\pi}{\omega}, \quad n = 0, 1, 2, \ldots}$$

Every time the point **touches the ground** it momentarily stops — these are the sharp cusps of the cycloid.

## 6.5 — Maximum Speed and Acceleration

$$\boxed{|\vec{v}|_{\max} = 2R\omega} \quad \text{at the top of the circle } (\omega t = \pi, 3\pi, \ldots)$$

$$|\vec{a}(t)| = R\omega^2\sqrt{\sin^2 + \cos^2} = \boxed{R\omega^2 = \text{const}}$$

> 💡 **Surprising result:** Although speed oscillates between 0 and $2R\omega$, the magnitude of acceleration is constant $= R\omega^2$.

## 6.6 — Comparison: Cycloid vs Circular Motion

| Property | Circular | Cycloid |
|----------|----------|---------|
| $|\vec{v}|$ | $R\omega$ = const | oscillates $0 \to 2R\omega$ |
| $|\vec{a}|$ | $R\omega^2$ = const | $R\omega^2$ = const ✅ |
| Trajectory | Circle | Cycloid with cusps |

> 🎬 **Interactive visualization:** `problem_06_cycloid.html`

---

# Problem 7 — 2D Motion with Given Acceleration

> **Given:** $\vec{a} = (2,\; -3)$ m/s², $\vec{v}(0) = (1,\; 0)$ m/s, $\vec{r}(0) = (0,\; 0)$ m

## 7.1 — Velocity v(t)

Using $\vec{v}(t) = \vec{v}(0) + \vec{a}\,t$:

$$v_x(t) = 1 + 2t, \qquad v_y(t) = -3t$$

$$\boxed{\vec{v}(t) = (1 + 2t,\; -3t)}$$

## 7.2 — Position r(t)

Using $\vec{r}(t) = \vec{r}(0) + \vec{v}(0)\,t + \tfrac{1}{2}\vec{a}\,t^2$:

$$x(t) = t + t^2, \qquad y(t) = -\frac{3}{2}t^2$$

$$\boxed{\vec{r}(t) = \bigl(t + t^2,\; -\tfrac{3}{2}t^2\bigr)}$$

## 7.3 — Trajectory Shape

From $y = -\tfrac{3}{2}t^2$ and $x = t + t^2$ we can eliminate $t$ to get a rotated **parabola** in 2D.

## 7.4 — Vectors at Selected Moments

| $t$ (s) | $x$ (m) | $y$ (m) | $v_x$ | $v_y$ | $\|\vec{v}\|$ |
|---------|---------|---------|-------|-------|----------|
| 0 | 0 | 0 | 1 | 0 | 1.00 |
| 1 | 2 | −1.5 | 3 | −3 | 4.24 |
| 2 | 6 | −6 | 5 | −6 | 7.81 |
| 3 | 12 | −13.5 | 7 | −9 | 11.40 |

> 🎬 **Interactive visualization:** `problem_07_08_09_10_advanced.html`

---

# Problem 8 — Relative Motion

> **Given:** $\vec{v}_A = (3,\; 1)$ m/s, $\vec{v}_B = (1,\; -2)$ m/s

## 8.1 — Relative Velocity

$$\vec{v}_{A/B} = \vec{v}_A - \vec{v}_B = (3-1,\; 1-(-2)) = \boxed{(2,\; 3) \; \text{m/s}}$$

$$|\vec{v}_{A/B}| = \sqrt{4 + 9} = \sqrt{13} \approx 3.61 \; \text{m/s}$$

## 8.2 — Direction of Relative Motion

$$\theta = \arctan\!\left(\frac{3}{2}\right) \approx \boxed{56.3° \text{ above the horizontal}}$$

Body A moves north-east relative to body B.

## 8.3 — Three Reference Frames

Positions (starting from origin at $t = 0$):
$\vec{r}_A(t) = (3t, t)$, $\quad \vec{r}_B(t) = (t, -2t)$

| Frame | A moves with | B moves with |
|-------|-------------|-------------|
| Ground | $(3, 1)$ | $(1, -2)$ |
| A's frame | $(0, 0)$ — fixed | $(-2, -3)$ |
| B's frame | $(2, 3)$ | $(0, 0)$ — fixed |

> 💡 **Key principle:** $\vec{v}_{A/B} = -\vec{v}_{B/A}$. The physics doesn't change — only the perspective does.

> 🎬 **Interactive visualization:** `problem_07_08_09_10_advanced.html`

---

# Problem 9 — Earth–Mars: Heliocentric → Geocentric

## 9.1 — Heliocentric Model

$$\vec{r}_Z(t) = R_Z\bigl(\cos(\omega_Z t),\; \sin(\omega_Z t)\bigr), \qquad \vec{r}_M(t) = R_M\bigl(\cos(\omega_M t),\; \sin(\omega_M t)\bigr)$$

| Body | Radius | Period | Angular velocity |
|------|--------|--------|-----------------|
| Earth | $R_Z = 1$ AU | $T_Z = 1$ yr | $\omega_Z = 2\pi$ rad/yr |
| Mars | $R_M = 1.52$ AU | $T_M = 1.88$ yr | $\omega_M = 2\pi/1.88$ rad/yr |

## 9.2 — Geocentric Position of Mars

$$\vec{r}_{M/Z}(t) = \vec{r}_M(t) - \vec{r}_Z(t)$$

$$\boxed{x_{M/Z}(t) = R_M\cos(\omega_M t) - R_Z\cos(\omega_Z t)}$$

$$\boxed{y_{M/Z}(t) = R_M\sin(\omega_M t) - R_Z\sin(\omega_Z t)}$$

## 9.3 — Retrograde Motion Explained

When Earth **overtakes Mars** (Earth is faster), the angle of Mars relative to Earth temporarily **decreases** — this is the apparent retrograde (backward) motion visible from Earth.

The **Ptolemaic geocentric model** required complex epicycles to explain this. The **Copernican heliocentric model** explains it with pure kinematics — a natural consequence of two bodies orbiting at different speeds.

## 9.4 — Synodic Period

How often does retrograde occur?

$$\frac{1}{T_S} = \frac{1}{T_Z} - \frac{1}{T_M} = 1 - \frac{1}{1.88} \approx 0.468 \; \text{yr}^{-1} \implies \boxed{T_S \approx 2.14 \; \text{years}}$$

> 🎬 **Interactive visualization:** `problem_07_08_09_10_advanced.html` — Press ▶ to watch the retrograde loops form.

---

# Problem 10 — Numerical Differentiation

> **Given:** $x(t) = t + \dfrac{1}{20}t^2$ on $t \in [0,10]$, time step $\Delta t = 0.1$

## 10.1 — Analytical Solution (reference)

$$\boxed{v(t) = \frac{dx}{dt} = 1 + \frac{t}{10}}, \qquad \boxed{a(t) = \frac{dv}{dt} = 0.1 \; \text{m/s}^2 = \text{const}}$$

## 10.2 — Finite Difference for Velocity (forward difference)

$$\boxed{v_{\text{approx}}(t) \approx \frac{x(t + \Delta t) - x(t)}{\Delta t}}$$

This is the definition of the derivative with $\Delta t$ kept finite rather than sent to zero.

**Applying it to our function:**

$$v_{\text{approx}}(t) = \frac{\left[(t+\Delta t) + \frac{(t+\Delta t)^2}{20}\right] - \left[t + \frac{t^2}{20}\right]}{\Delta t} = 1 + \frac{t}{10} + \frac{\Delta t}{20}$$

The error is exactly $\dfrac{\Delta t}{20}$. For $\Delta t = 0.1$: error $= 0.005$ m/s.

## 10.3 — Finite Difference for Acceleration (central difference)

$$\boxed{a_{\text{approx}}(t) \approx \frac{x(t + \Delta t) - 2x(t) + x(t - \Delta t)}{\Delta t^2}}$$

For our quadratic function the central difference gives the **exact result** regardless of $\Delta t$, because all higher-order terms vanish for a degree-2 polynomial.

## 10.4 — Effect of Step Size

| $\Delta t$ | Max $|v \text{ error}|$ | Max $|a \text{ error}|$ | Quality |
|-----------|----------------------|----------------------|---------|
| 0.05 | 0.0025 | ~0 | Excellent |
| 0.10 | 0.0050 | ~0 | Excellent |
| 0.50 | 0.0250 | ~0 | Good |
| 1.00 | 0.0500 | ~0 | Good |
| 2.00 | 0.1000 | ~0 | Fair |

## 10.5 — General Accuracy

| Method | Error order | Meaning |
|--------|-------------|---------|
| Forward difference | $O(\Delta t)$ | halving $\Delta t$ halves the error |
| Central difference | $O(\Delta t^2)$ | halving $\Delta t$ quarters the error |

> 💡 Very small $\Delta t$ causes floating-point rounding errors. The practical sweet spot is $\Delta t \approx 10^{-4}$ to $10^{-2}$ for general functions.

> 🎬 **Interactive visualization:** `problem_07_08_09_10_advanced.html` — Use the $\Delta t$ slider to see analytical vs numerical curves and the error table.

---

## Quick Reference — All Key Results

| # | Problem | Key result |
|---|---------|-----------|
| 1 | Uniform acceleration | $t_{\text{stop}} = v_0 / \|a\|$, $\quad x_{\max} = v_0^2 / (2\|a\|)$ |
| 2 | Projectile | $R = v_0^2\sin 2\alpha / g$, max at $\alpha = 45°$ |
| 3 | Parametric $x=2t^2, y=3t^3$ | $y = \frac{3}{2\sqrt{2}}x^{3/2}$, acceleration not constant |
| 4 | Circular motion | $\vec{a} = -\omega^2\vec{r}$ — centripetal proof |
| 5 | Elliptical motion | Speed not constant; $\vec{a} = -\omega^2\vec{r}$ |
| 6 | Cycloid | $\|\vec{v}\| = 2R\omega\|\sin(\omega t/2)\|$, $\|\vec{a}\| = R\omega^2$ = const |
| 7 | 2D constant $\vec{a}$ | $\vec{r}(t) = (t+t^2,\;-1.5t^2)$ — rotated parabola |
| 8 | Relative motion | $\vec{v}_{A/B} = (2,3)$, three reference frames |
| 9 | Earth–Mars | Retrograde from kinematics, $T_S \approx 2.14$ yr |
| 10 | Finite differences | Forward: $O(\Delta t)$ error; Central: $O(\Delta t^2)$ error |
