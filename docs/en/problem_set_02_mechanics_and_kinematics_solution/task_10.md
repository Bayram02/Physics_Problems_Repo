# Problem 10 — Analysis of Motion from Numerical Data

> **Given:** $x(t) = t + \dfrac{1}{20}t^2$ on $t \in [0, 10]$ with time step $\Delta t = 0.1$

---

## Part 1 — Analytical Solution (reference)

Differentiate $x(t)$ exactly:

$$\boxed{v(t) = \frac{dx}{dt} = 1 + \frac{t}{10}}$$

$$\boxed{a(t) = \frac{dv}{dt} = \frac{1}{10} = 0.1 \; \text{m/s}^2 = \text{const}}$$

> This is simply uniform acceleration — the exact same form as Problem 1.

---

## Part 2 — Finite Difference Approximation for Velocity

The **forward difference** formula approximates the derivative:

$$v_{\text{approx}}(t) \approx \frac{x(t + \Delta t) - x(t)}{\Delta t}$$

**Why does this work?** The definition of the derivative is:

$$v(t) = \lim_{\Delta t \to 0} \frac{x(t + \Delta t) - x(t)}{\Delta t}$$

With a finite (non-zero) $\Delta t$ we get an approximation. The smaller $\Delta t$ is, the closer we are to the true derivative.

**Applying it:**

$$v_{\text{approx}}(t) = \frac{\left[(t+\Delta t) + \frac{(t+\Delta t)^2}{20}\right] - \left[t + \frac{t^2}{20}\right]}{\Delta t} = 1 + \frac{2t + \Delta t}{20} = 1 + \frac{t}{10} + \frac{\Delta t}{20}$$

The error is:

$$v_{\text{exact}} - v_{\text{approx}} = -\frac{\Delta t}{20}$$

> For $\Delta t = 0.1$: error $= 0.005$ m/s — excellent!

---

## Part 3 — Finite Difference Approximation for Acceleration

The **central difference** formula for the second derivative:

$$a_{\text{approx}}(t) \approx \frac{x(t + \Delta t) - 2x(t) + x(t - \Delta t)}{\Delta t^2}$$

**Applying it** (the $t$ and $t^2$ terms cancel neatly):

$$a_{\text{approx}} = \frac{\frac{(t+\Delta t)^2}{20} - 2\frac{t^2}{20} + \frac{(t-\Delta t)^2}{20}}{\Delta t^2} = \frac{\frac{2\Delta t^2}{20}}{\Delta t^2} = \frac{1}{10} = 0.1$$

> For this particular function the central difference gives the **exact result** regardless of $\Delta t$. This is because $x(t)$ is a polynomial of degree 2 — the central difference is exact for quadratics.

---

## Part 4 — Effect of Time Step on Accuracy

| $\Delta t$ | Max $|v$ error$|$ | Max $|a$ error$|$ | Quality |
|-----------|----------------|----------------|---------|
| 0.05 | 0.0025 | ~0 | Excellent |
| 0.10 | 0.0050 | ~0 | Excellent |
| 0.50 | 0.0250 | ~0 | Good |
| 1.00 | 0.0500 | ~0 | Good |
| 2.00 | 0.1000 | ~0 | Fair |

> For acceleration: since the analytical $a = $ const and the central difference is exact for quadratics, the numerical error is practically zero for all $\Delta t$.

---

## Part 5 — General Accuracy Analysis

For a general smooth function, the errors scale as:

| Method | Error order | Meaning |
|--------|-------------|---------|
| Forward difference (velocity) | $O(\Delta t)$ | halving $\Delta t$ halves the error |
| Central difference (acceleration) | $O(\Delta t^2)$ | halving $\Delta t$ quarters the error |

> 💡 **Practical note:** Very small $\Delta t$ causes numerical problems too. For 64-bit floating point, rounding errors dominate below $\Delta t \approx 10^{-8}$. The optimal step is typically $\Delta t \approx 10^{-4}$ to $10^{-6}$ for general functions.

---

## Visualization

> 🎬 **See the interactive version:** `problem_07_08_09_10_advanced.html`
> Use the $\Delta t$ slider to see the analytical and numerical curves overlap or diverge. The error table updates automatically to compare accuracy at different step sizes.