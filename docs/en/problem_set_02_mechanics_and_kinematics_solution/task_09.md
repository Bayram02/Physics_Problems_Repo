# Problem 9 — Change of Reference Frame: Heliocentric → Geocentric

> Earth and Mars orbit the Sun in circles in the same direction.

---

## Part 1 — Heliocentric Model

$$\vec{r}_Z(t) = R_Z\bigl(\cos(\omega_Z t),\; \sin(\omega_Z t)\bigr)$$

$$\vec{r}_M(t) = R_M\bigl(\cos(\omega_M t),\; \sin(\omega_M t)\bigr)$$

### Orbital parameters (simplified)

| Body | Radius | Period | Angular velocity |
|------|--------|--------|-----------------|
| Earth | $R_Z = 1$ AU | $T_Z = 1$ yr | $\omega_Z = 2\pi/1$ rad/yr |
| Mars | $R_M = 1.52$ AU | $T_M = 1.88$ yr | $\omega_M = 2\pi/1.88$ rad/yr |

> Earth completes a full orbit in 1 year. Mars is slower — it takes 1.88 years. This difference in angular velocity is what creates the retrograde illusion.

---

## Part 2 — Geocentric Position of Mars

We subtract Earth's position from Mars's position to shift to Earth's reference frame:

$$\vec{r}_{M/Z}(t) = \vec{r}_M(t) - \vec{r}_Z(t)$$

**Components:**

$$\boxed{x_{M/Z}(t) = R_M\cos(\omega_M t) - R_Z\cos(\omega_Z t)}$$

$$\boxed{y_{M/Z}(t) = R_M\sin(\omega_M t) - R_Z\sin(\omega_Z t)}$$

---

## Part 3 — Retrograde Motion Explained

This is one of the most important results in the history of astronomy.

### What is retrograde motion?

Normally Mars moves eastward across the sky (in the direction of increasing angle). But roughly every 26 months, Mars appears to **reverse direction** for a few weeks, then continue forward. Ancient astronomers found this deeply puzzling.

### Kinematic explanation

Using the geocentric formula above, we can show:

- When $\omega_Z \approx \omega_M$ (same angular speed) → Mars traces a nearly circular path as seen from Earth.
- When Earth **overtakes** Mars (Earth is faster, both on the same side of the Sun), the angle of Mars relative to Earth **temporarily decreases** — this is retrograde motion.

$$\text{Retrograde when: } \frac{d}{dt}\!\left[\arctan\!\left(\frac{y_{M/Z}}{x_{M/Z}}\right)\right] < 0$$

### No epicycles needed!

The **Ptolemaic geocentric model** required complex epicycles (circles on circles) to explain this. The **Copernican heliocentric model** explains it with pure kinematics — it is simply the result of two bodies orbiting at different speeds.

---

## Part 4 — Synodic Period

How often does retrograde occur? This is determined by the **synodic period** $T_S$:

$$\frac{1}{T_S} = \frac{1}{T_Z} - \frac{1}{T_M} = \frac{1}{1} - \frac{1}{1.88} \approx 0.468 \; \text{yr}^{-1}$$

$$T_S = \frac{1}{0.468} \approx \boxed{2.14 \; \text{years}}$$

> Earth and Mars are in the same relative configuration (Mars opposition) every $\approx 2$ years and 50 days.

---

## Visualization

> 🎬 **See the interactive version:** `problem_07_08_09_10_advanced.html`
> Press **▶ Animate Orbits** to watch the simulation. The left panel shows the heliocentric view with both circular orbits. The right panel shows Mars's geocentric path — you can clearly see the retrograde loops forming every ~2 years.