# Problem 4 — Rotating Loop (Electromagnetic Induction)

> **A loop with area $S$ and $N$ turns is placed in a uniform magnetic field $\vec{B}$.**
> **The loop rotates with angular velocity $\omega$ around an axis perpendicular to $\vec{B}$.**

---

## Part 1 — Magnetic Flux Φ(t)

The magnetic flux through one turn of the loop depends on the angle between $\vec{B}$ and the normal to the loop:

$$\Phi_1(t) = B \cdot S \cdot \cos(\omega t)$$

For $N$ turns total flux:

$$\boxed{\Phi(t) = N \cdot B \cdot S \cdot \cos(\omega t)}$$

> 💡 At $t = 0$ the loop is perpendicular to $\vec{B}$ → flux is maximum.
> As the loop rotates, flux oscillates between $+NBS$ and $-NBS$.

---

## Part 2 — EMF $\mathcal{E}(t)$ — Faraday's Law

By Faraday's law the EMF is the **negative rate of change of flux**:

$$\mathcal{E}(t) = -\frac{d\Phi}{dt}$$

Differentiate $\Phi(t) = NBS\cos(\omega t)$:

$$\mathcal{E}(t) = -NBS \cdot \frac{d}{dt}\cos(\omega t) = -NBS \cdot (-\omega\sin(\omega t))$$

$$\boxed{\mathcal{E}(t) = NBS\omega \cdot \sin(\omega t)}$$

> The EMF is a **sinusoidal function** — this is the basis of all AC generators.

---

## Part 3 — Amplitude $\mathcal{E}_0$

The amplitude of the EMF is:

$$\boxed{\mathcal{E}_0 = NBS\omega}$$

This is the **peak voltage** produced by the generator.

### Numerical example

For $N = 100$, $B = 0.5$ T, $S = 0.02$ m², $\omega = 100\pi$ rad/s:

$$\mathcal{E}_0 = 100 \times 0.5 \times 0.02 \times 100\pi = 100\pi \approx \boxed{314\ \text{V}}$$

---

## Part 4 — Dependence on ω

From $\mathcal{E}_0 = NBS\omega$:

| Parameter | Effect on $\mathcal{E}_0$ |
|-----------|--------------------------|
| Double $\omega$ | $\mathcal{E}_0$ doubles |
| Double $N$ | $\mathcal{E}_0$ doubles |
| Double $B$ | $\mathcal{E}_0$ doubles |
| Double $S$ | $\mathcal{E}_0$ doubles |

$$\mathcal{E}_0 \propto \omega \propto N \propto B \propto S$$

> 💡 **Linear dependence on ω:** The faster the loop rotates, the greater the EMF. This is why power plant generators spin at precisely controlled speeds (50 Hz in Europe = $\omega = 100\pi$ rad/s).

---

## Part 5 — Physical Mechanism of EMF Generation

### Why does EMF appear?

As the loop rotates in the magnetic field, the **free electrons** in the wire experience a **Lorentz force**:

$$\vec{F} = q\vec{v} \times \vec{B}$$

where $\vec{v}$ is the velocity of the wire element due to rotation.

This force **separates charges** — pushing them along the wire → creating a current.

### Connection between Φ and $\mathcal{E}$

$$\mathcal{E}(t) = -\frac{d\Phi}{dt}$$

| Time | Φ(t) | dΦ/dt | $\mathcal{E}(t)$ |
|------|------|-------|---------|
| $\omega t = 0$ | maximum | zero | **zero** |
| $\omega t = π/2$ | zero | maximum negative | **maximum** |
| $\omega t = π$ | minimum | zero | **zero** |
| $\omega t = 3π/2$ | zero | maximum positive | **minimum** |

> 💡 **Key insight:** EMF is maximum when flux is changing fastest (loop parallel to $\vec{B}$). EMF is zero when flux is at its maximum or minimum (loop perpendicular to $\vec{B}$).

---

## Summary

$$\boxed{\Phi(t) = NBS\cos(\omega t)}$$

$$\boxed{\mathcal{E}(t) = NBS\omega\sin(\omega t) = \mathcal{E}_0\sin(\omega t)}$$

$$\boxed{\mathcal{E}_0 = NBS\omega}$$

| Quantity | Formula | Unit |
|----------|---------|------|
| Flux $\Phi(t)$ | $NBS\cos(\omega t)$ | Wb (Weber) |
| EMF $\mathcal{E}(t)$ | $NBS\omega\sin(\omega t)$ | V (Volt) |
| Amplitude $\mathcal{E}_0$ | $NBS\omega$ | V |
| Phase shift | $\mathcal{E}$ leads $\Phi$ by $\pi/2$ | — |

---

