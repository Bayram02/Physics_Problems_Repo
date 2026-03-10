Below is a **VS Code–ready Markdown solution** for **Problem 1**.
You can **copy it directly into `task_01.md`**, and it will render correctly in **VS Code Markdown Preview** because all math uses `$$ ... $$`.

---

# Problem 1 – Vectors and Linear Transformations

## Given vectors

$$
\vec a = (2,-1,3), \qquad
\vec b = (1,4,-2)
$$

---

# 1. Lengths of the vectors

The length of a vector is defined as

$$
|\vec v| = \sqrt{v_x^2 + v_y^2 + v_z^2}
$$

### Length of $\vec a$

$$
|\vec a|
========

\sqrt{2^2 + (-1)^2 + 3^2}
$$

# $$

\sqrt{4 + 1 + 9}
$$

# $$

\sqrt{14}
$$

---

### Length of $\vec b$

$$
|\vec b|
========

\sqrt{1^2 + 4^2 + (-2)^2}
$$

# $$

\sqrt{1 + 16 + 4}
$$

# $$

\sqrt{21}
$$

---

# 2. Normalized vector $\hat a$

The normalized vector is defined as

$$
\hat a = \frac{\vec a}{|\vec a|}
$$

Substituting values:

$$
\hat a
======

\frac{(2,-1,3)}{\sqrt{14}}
$$

Therefore

$$
\hat a =
\left(
\frac{2}{\sqrt{14}},
\frac{-1}{\sqrt{14}},
\frac{3}{\sqrt{14}}
\right)
$$

---

# 3. Dot product and angle between vectors

### Dot product

The dot product is

$$
\vec a \cdot \vec b
===================

a_x b_x + a_y b_y + a_z b_z
$$

Substitute values:

# $$

2\cdot1 + (-1)\cdot4 + 3\cdot(-2)
$$

# $$

2 -4 -6
$$

# $$

-8
$$

---

### Angle between vectors

The formula for the angle between vectors is

$$
\vec a \cdot \vec b = |\vec a||\vec b|\cos\theta
$$

Thus

$$
\cos\theta
==========

\frac{\vec a\cdot\vec b}{|\vec a||\vec b|}
$$

Substitute values:

$$
\cos\theta =
\frac{-8}{\sqrt{14}\sqrt{21}}
$$

Since

$$
\sqrt{14}\sqrt{21} = \sqrt{294}
$$

we obtain

$$
\cos\theta =
\frac{-8}{\sqrt{294}}
$$

Therefore

$$
\theta =
\arccos
\left(
\frac{-8}{\sqrt{294}}
\right)
$$

---

# 4. Cross product

The cross product is computed using the determinant:

$$
\vec a \times \vec b =
\begin{vmatrix}
\mathbf i & \mathbf j & \mathbf k \
2 & -1 & 3 \
1 & 4 & -2
\end{vmatrix}
$$

Expand the determinant:

# $$

\mathbf i
\begin{vmatrix}
-1 & 3 \
4 & -2
\end{vmatrix}
-------------

\mathbf j
\begin{vmatrix}
2 & 3 \
1 & -2
\end{vmatrix}
+
\mathbf k
\begin{vmatrix}
2 & -1 \
1 & 4
\end{vmatrix}
$$

---

### Calculate determinants

First:

$$
(-1)(-2) - (3)(4) = 2 - 12 = -10
$$

Second:

$$
(2)(-2) - (3)(1) = -4 - 3 = -7
$$

Third:

$$
(2)(4) - (-1)(1) = 8 + 1 = 9
$$

---

### Final result

$$
\vec a \times \vec b =
(-10,,7,,9)
$$

(Note the minus sign before the $\mathbf j$ term.)

---

# 5. Area of the parallelogram

The area of the parallelogram spanned by the vectors is

$$
A = |\vec a \times \vec b|
$$

Compute the magnitude:

# $$

\sqrt{(-10)^2 + 7^2 + 9^2}
$$

# $$

\sqrt{100 + 49 + 81}
$$

# $$

\sqrt{230}
$$

---

# Matrix transformation

Given matrix

$$
A =
\begin{pmatrix}
2 & 1 & 0 \
0 & 1 & -1 \
1 & 0 & 1
\end{pmatrix}
$$

---

# 6. Calculate $A\vec a$

Multiply the matrix by vector $\vec a=(2,-1,3)$.

First component:

$$
2\cdot2 + 1\cdot(-1) + 0\cdot3
==============================

# 4-1

3
$$

Second component:

$$
0\cdot2 + 1\cdot(-1) + (-1)\cdot3
=================================

# -1-3

-4
$$

Third component:

$$
1\cdot2 + 0\cdot(-1) + 1\cdot3
==============================

# 2+3

5
$$

Thus

$$
A\vec a =
(3,-4,5)
$$

---

# 7. Determinant of $A$

$$
\det A =
\begin{vmatrix}
2 & 1 & 0 \
0 & 1 & -1 \
1 & 0 & 1
\end{vmatrix}
$$

Expand along the first row:

# $$

2
\begin{vmatrix}
1 & -1 \
0 & 1
\end{vmatrix}
-------------

1
\begin{vmatrix}
0 & -1 \
1 & 1
\end{vmatrix}
+
0
\begin{vmatrix}
0 & 1 \
1 & 0
\end{vmatrix}
$$

Compute minors:

First:

$$
1\cdot1 - (-1)\cdot0 = 1
$$

Second:

$$
0\cdot1 - (-1)\cdot1 = 1
$$

Thus

$$
\det A = 2(1) - 1(1) = 1
$$

---

# 8. Orientation of the transformation

The orientation of a linear transformation depends on the sign of the determinant.

* If
  $$
  \det A > 0
  $$
  orientation is preserved.

* If
  $$
  \det A < 0
  $$
  orientation is reversed.

Since

$$
\det A = 1 > 0
$$

the transformation **preserves orientation**.

---

If you want, I can also generate:

* **Problem 2–10 fully solved in the same VS Code Markdown style**
* **HTML/JS templates for problems 6–9**
* **clean repo-ready files (`task_01.md`, `task_02.md`, …)** so you can paste them directly into your repository.
