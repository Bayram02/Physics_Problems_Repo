# Problem 5 — Superposition of Waves, Beats, and Group Velocity

> **Given two harmonic waves:**
> $$y_1(x,t) = A\sin(kx - \omega t)$$
> $$y_2(x,t) = A\sin(kx - (\omega + \Delta\omega)\,t)$$

---

## Part 1 — Resultant Wave: Product Form

We add the two waves:

$$y = y_1 + y_2 = A\sin(kx - \omega t) + A\sin(kx - (\omega + \Delta\omega)\,t)$$

We use the **sum-to-product identity**:

$$\sin\alpha + \sin\beta = 2\cos\!\left(\frac{\alpha-\beta}{2}\right)\sin\!\left(\frac{\alpha+\beta}{2}\right)$$

Let:

$$\alpha = kx - \omega t \qquad \beta = kx - (\omega + \Delta\omega)\,t$$

Compute the difference and sum:

$$\alpha - \beta = -\omega t + (\omega + \Delta\omega)\,t = \Delta\omega\,t$$

$$\alpha + \beta = 2kx - \left(2\omega + \Delta\omega\right)t$$

Substitute:

$$\boxed{y(x,t) = 2A\cos\!\left(\frac{\Delta\omega}{2}\,t\right)\cdot\sin\!\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)}$$

This is the **product form**: envelope × carrier.

---

## Part 2 — Beat Frequency and Beat Period

At point $x = 0$:

$$y(0,t) = 2A\cos\!\left(\frac{\Delta\omega}{2}\,t\right)\cdot\sin\!\left(-\left(\omega + \frac{\Delta\omega}{2}\right)t\right)$$

The **envelope** oscillates with angular frequency $\Delta\omega/2$.

The amplitude becomes zero (silence) when:

$$\cos\!\left(\frac{\Delta\omega}{2}\,t\right) = 0 \implies \frac{\Delta\omega}{2}\,t = \frac{\pi}{2} + n\pi$$

The time between two consecutive zeros = beat period:

$$\boxed{T_{beat} = \frac{2\pi}{\Delta\omega} = \frac{1}{\Delta f}}$$

$$\boxed{f_{beat} = \frac{\Delta\omega}{2\pi} = \Delta f}$$

> 💡 **Beat frequency equals the difference of the two wave frequencies.**

---

## Part 3 — Physical Interpretation

### Carrier wave
$$\sin\!\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)$$

- Oscillates at the **average frequency** $\bar{\omega} = \omega + \Delta\omega/2$
- This is what you **hear** — the tone
- Travels at **phase velocity**: $v_{phase} = \bar{\omega}/k$

### Envelope
$$2A\cos\!\left(\frac{\Delta\omega}{2}\,t\right)$$

- Oscillates slowly at frequency $\Delta\omega/2$
- **Modulates the amplitude** — makes the sound loud then quiet
- This is what you **hear as beats** — the pulsing
- Travels at **group velocity**: $v_{group} = \Delta\omega/\Delta k$

> 💡 **Musical example:** When tuning a guitar, you hear beats when two strings are slightly out of tune. As you tune them closer together, the beat frequency decreases. When beats disappear — the strings are in perfect tune!

---

## Part 4 — Numerical Example

For $\omega = 20\pi$ rad/s, $\Delta\omega = 2\pi$ rad/s, $k = 4\pi$ rad/m:

| Quantity | Formula | Value |
|----------|---------|-------|
| Carrier frequency | $\bar{f} = \bar{\omega}/2\pi$ | $\approx 10.5$ Hz |
| Beat frequency | $f_{beat} = \Delta\omega/2\pi$ | $1$ Hz |
| Beat period | $T_{beat} = 1/f_{beat}$ | $1$ s |
| Phase velocity | $v_{phase} = \bar{\omega}/k$ | $\approx 2.625$ m/s |

---

## Summary

| Term | Formula | Meaning |
|------|---------|---------|
| Resultant | $2A\cos(\frac{\Delta\omega}{2}t)\cdot\sin(kx - \bar{\omega}t)$ | product form |
| Beat frequency | $f_{beat} = \Delta f$ | difference of frequencies |
| Beat period | $T_{beat} = 1/\Delta f$ | time between loud moments |
| Carrier | fast oscillation at $\bar{\omega}$ | the tone you hear |
| Envelope | slow oscillation at $\Delta\omega/2$ | the pulsing amplitude |

---
