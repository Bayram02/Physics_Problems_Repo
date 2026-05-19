# Problem 6 — Equivalent Resistance & Currents

> **Resistors:** R1=r, R2=2r, R3=r, R4=r, R5=6r
> **Find:** R_eq between A and B, and currents through each resistor.

---

## Circuit Structure

```
A ──[r]─── C ──[2r]── B
           |
          [6r]
           |
A ──[r]─── D ──[r]─── B
```

**Nodes:** A (input), B (output), C (top middle), D (bottom middle)

**Resistors:**
- R1 = r → from A to C (top left)
- R2 = 2r → from C to B (top right)
- R3 = r → from A to D (bottom left)
- R4 = r → from D to B (bottom right)
- R5 = 6r → from C to D (vertical middle)

---

## Method — Node Voltage Analysis

Set $V_A = U$ (input voltage), $V_B = 0$ (reference).

Find $V_C$ and $V_D$ using **Kirchhoff's Current Law (KCL)** at each node.

---

## Step 1 — KCL at Node C

Current in = current out:

$$\frac{V_A - V_C}{r} = \frac{V_C - V_B}{2r} + \frac{V_C - V_D}{6r}$$

Multiply both sides by 6r:

$$6(U - V_C) = 3V_C + (V_C - V_D)$$

$$6U = 10V_C - V_D \quad \cdots (1)$$

---

## Step 2 — KCL at Node D

$$\frac{V_A - V_D}{r} + \frac{V_C - V_D}{6r} = \frac{V_D - V_B}{r}$$

Multiply both sides by 6r:

$$6(U - V_D) + (V_C - V_D) = 6V_D$$

$$6U = 13V_D - V_C \quad \cdots (2)$$

---

## Step 3 — Solve the System

From equations (1) and (2):

$$10V_C - V_D = 13V_D - V_C$$

$$11V_C = 14V_D \implies V_C = \frac{14}{11}V_D$$

Substitute into (2):

$$6U = 13V_D - \frac{14}{11}V_D = \frac{129}{11}V_D$$

$$\boxed{V_D = \frac{22U}{43}} \qquad \boxed{V_C = \frac{28U}{43}}$$

---

## Step 4 — Calculate Currents

$$I_1 = \frac{V_A - V_C}{r} = \frac{U - \frac{28U}{43}}{r} = \boxed{\frac{15U}{43r}}$$

$$I_2 = \frac{V_C - V_B}{2r} = \frac{\frac{28U}{43}}{2r} = \boxed{\frac{14U}{43r}}$$

$$I_3 = \frac{V_A - V_D}{r} = \frac{U - \frac{22U}{43}}{r} = \boxed{\frac{21U}{43r}}$$

$$I_4 = \frac{V_D - V_B}{r} = \frac{\frac{22U}{43}}{r} = \boxed{\frac{22U}{43r}}$$

$$I_5 = \frac{V_C - V_D}{6r} = \frac{\frac{28U - 22U}{43}}{6r} = \boxed{\frac{U}{43r}}$$

---

## Step 5 — Verify with KCL

**At node C:** $I_1 = I_2 + I_5$
$$\frac{15U}{43r} = \frac{14U}{43r} + \frac{U}{43r} = \frac{15U}{43r} \quad ✅$$

**At node D:** $I_3 + I_5 = I_4$
$$\frac{21U}{43r} + \frac{U}{43r} = \frac{22U}{43r} \quad ✅$$

---

## Step 6 — Equivalent Resistance

Total current from A:

$$I_{total} = I_1 + I_3 = \frac{15U}{43r} + \frac{21U}{43r} = \frac{36U}{43r}$$

$$R_{eq} = \frac{U}{I_{total}} = \frac{U}{\frac{36U}{43r}} = \frac{43r}{36}$$

$$\boxed{R_{eq} = \frac{43r}{36} \approx 1.194r}$$

---

## Summary Table

| Resistor | Value | Current | Direction |
|----------|-------|---------|-----------|
| R1 | r | $\frac{15U}{43r}$ | A → C |
| R2 | 2r | $\frac{14U}{43r}$ | C → B |
| R3 | r | $\frac{21U}{43r}$ | A → D |
| R4 | r | $\frac{22U}{43r}$ | D → B |
| R5 | 6r | $\frac{U}{43r}$ | C → D |
| **R_eq** | **43r/36** | $\frac{36U}{43r}$ | A → B |

---


