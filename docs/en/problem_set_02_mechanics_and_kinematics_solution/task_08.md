# Problem 8 — Relative Motion

> **Given:**
> $$\vec{v}_A = (3,\; 1) \; \text{m/s}, \qquad \vec{v}_B = (1,\; -2) \; \text{m/s}$$

---

## Part 1 — Relative Velocity

The velocity of A as seen from B (i.e. in B's reference frame):

$$\vec{v}_{A/B} = \vec{v}_A - \vec{v}_B = (3-1,\; 1-(-2)) = \boxed{(2,\; 3) \; \text{m/s}}$$

---

## Part 2 — Direction of Relative Motion

$$|\vec{v}_{A/B}| = \sqrt{2^2 + 3^2} = \sqrt{13} \approx 3.61 \; \text{m/s}$$

$$\theta = \arctan\!\left(\frac{3}{2}\right) \approx \boxed{56.3° \text{ above the horizontal}}$$

> Body A moves north-east at $56.3°$ relative to body B.

---

## Part 3 — Three Reference Frames

Assume both bodies start at the origin at $t = 0$. Their positions are:

$$\vec{r}_A(t) = \vec{v}_A \cdot t = (3t,\; t)$$

$$\vec{r}_B(t) = \vec{v}_B \cdot t = (t,\; -2t)$$

### Frame 1 — Origin frame (ground)

Both bodies move from the origin with their respective velocities. A goes right-and-up, B goes right-and-down.

### Frame 2 — Frame attached to body A

In this frame, A is fixed at the origin. B appears to move with velocity:

$$\vec{v}_{B/A} = \vec{v}_B - \vec{v}_A = (1-3,\; -2-1) = (-2,\; -3)$$

B moves south-west relative to A.

### Frame 3 — Frame attached to body B

In this frame, B is fixed at the origin. A appears to move with velocity:

$$\vec{v}_{A/B} = \vec{v}_A - \vec{v}_B = (2,\; 3)$$

A moves north-east relative to B — this is exactly what we calculated in Part 1.

---

## Summary Table

| Frame | A moves with | B moves with |
|-------|-------------|-------------|
| Ground | $(3, 1)$ | $(1, -2)$ |
| A's frame | $(0, 0)$ — fixed | $(-2, -3)$ |
| B's frame | $(2, 3)$ | $(0, 0)$ — fixed |

> 💡 **Key principle:** Relative velocity reverses when you switch observer: $\vec{v}_{A/B} = -\vec{v}_{B/A}$. The physics doesn't change — only the perspective does.

---

## Visualization

> 🎬 **See the interactive version:** `problem_07_08_09_10_advanced.html`
> Three side-by-side panels show the motion in each reference frame. Notice how A appears stationary in the middle panel, and B in the right panel.