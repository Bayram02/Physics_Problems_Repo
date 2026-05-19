# Problem 3 — Equivalent Resistance Circuit

> **All resistors: R = 10 Ω**
> **Find the equivalent resistance between the two terminals.**

---

## Circuit Analysis — Reading the Diagram

The circuit has **7 resistors** all equal to 10 Ω. After careful reading of the diagram:

```
○──[R7=10Ω]──┬──[R1=10Ω]──┬──○
             │             │
           [R2]         [R3][R5]
           [10Ω]        [R4][R6]
             │           10Ω 10Ω
             └─────────────┘
```

**Structure:**
- **R7** — horizontal, bottom rail (series with everything)
- **R1** — horizontal, top rail
- **R2** — vertical, left branch (single resistor)
- **R3 + R4** — vertical, middle branch (two resistors in series)
- **R5 + R6** — vertical, right branch (two resistors in series)

---

## Step-by-Step Solution

### Step 1 — Simplify the middle branch

R3 and R4 are in **series**:

$$R_{34} = R_3 + R_4 = 10 + 10 = \boxed{20\ \Omega}$$

### Step 2 — Simplify the right branch

R5 and R6 are in **series**:

$$R_{56} = R_5 + R_6 = 10 + 10 = \boxed{20\ \Omega}$$

### Step 3 — Middle and right branches in parallel

R34 and R56 are in **parallel**:

$$\frac{1}{R_{3456}} = \frac{1}{R_{34}} + \frac{1}{R_{56}} = \frac{1}{20} + \frac{1}{20} = \frac{2}{20} = \frac{1}{10}$$

$$\boxed{R_{3456} = 10\ \Omega}$$

### Step 4 — R1 in series with R3456

$$R_{top} = R_1 + R_{3456} = 10 + 10 = \boxed{20\ \Omega}$$

### Step 5 — R2 in parallel with R_top

$$\frac{1}{R_{mid}} = \frac{1}{R_2} + \frac{1}{R_{top}} = \frac{1}{10} + \frac{1}{20} = \frac{2}{20} + \frac{1}{20} = \frac{3}{20}$$

$$\boxed{R_{mid} = \frac{20}{3} \approx 6.67\ \Omega}$$

### Step 6 — R7 in series with R_mid

$$R_{eq} = R_7 + R_{mid} = 10 + \frac{20}{3} = \frac{30}{3} + \frac{20}{3} = \frac{50}{3}$$

$$\boxed{R_{eq} = \frac{50}{3} \approx 16.7\ \Omega}$$

---

## Simplification Summary

| Step | Operation | Result |
|------|-----------|--------|
| 1 | R3 + R4 (series) | 20 Ω |
| 2 | R5 + R6 (series) | 20 Ω |
| 3 | R34 ∥ R56 (parallel) | 10 Ω |
| 4 | R1 + R3456 (series) | 20 Ω |
| 5 | R2 ∥ R_top (parallel) | 20/3 ≈ 6.67 Ω |
| 6 | R7 + R_mid (series) | **50/3 ≈ 16.7 Ω** |

---

## Key Formulas Used

**Series resistors** — resistances add:
$$R_{series} = R_1 + R_2 + \ldots$$

**Parallel resistors** — reciprocals add:
$$\frac{1}{R_{parallel}} = \frac{1}{R_1} + \frac{1}{R_2} + \ldots$$

**Two equal parallel resistors** — result is half:
$$R_1 = R_2 = R \implies R_{parallel} = \frac{R}{2}$$

---

## Final Answer

$$\boxed{R_{eq} = \frac{50}{3}\ \Omega \approx 16.7\ \Omega}$$

---


