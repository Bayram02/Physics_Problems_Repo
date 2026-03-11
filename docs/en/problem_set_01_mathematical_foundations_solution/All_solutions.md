# Problem 1 – Vectors and Linear Transformations

## Given vectors

$$
\vec a = (2,-1,3), \qquad
\vec b = (1,4,-2)
$$

These vectors belong to the three–dimensional Euclidean space \( \mathbb{R}^3 \).

---

# 1. Length (magnitude) of the vectors

The length of a vector in three–dimensional space is defined by the Euclidean norm

$$
|\vec v| = \sqrt{v_1^2 + v_2^2 + v_3^2}
$$

This formula comes from the extension of the **Pythagorean theorem** to 3D space.

---

## Length of vector a

Substitute the components of the vector

$$
|\vec a| = \sqrt{2^2 + (-1)^2 + 3^2}
$$

Compute the squares

$$
2^2 = 4, \qquad (-1)^2 = 1, \qquad 3^2 = 9
$$

Substitute again

$$
|\vec a| = \sqrt{4 + 1 + 9}
$$

Add the numbers

$$
4 + 1 + 9 = 14
$$

Therefore

$$
|\vec a| = \sqrt{14}
$$

---

## Length of vector b

Substitute the vector components

$$
|\vec b| = \sqrt{1^2 + 4^2 + (-2)^2}
$$

Compute the squares

$$
1^2 = 1, \qquad 4^2 = 16, \qquad (-2)^2 = 4
$$

Substitute

$$
|\vec b| = \sqrt{1 + 16 + 4}
$$

Add them

$$
1 + 16 + 4 = 21
$$

Thus

$$
|\vec b| = \sqrt{21}
$$

---

# 2. Normalized vector

A normalized vector (unit vector) has length equal to **1** and points in the same direction as the original vector.

The definition is

$$
\hat a = \frac{\vec a}{|\vec a|}
$$

Substitute the values

$$
\hat a = \frac{(2,-1,3)}{\sqrt{14}}
$$

Divide each component by \( \sqrt{14} \)

$$
\hat a =
\left(
\frac{2}{\sqrt{14}},
\frac{-1}{\sqrt{14}},
\frac{3}{\sqrt{14}}
\right)
$$

---

# 3. Dot product

The dot product of two vectors is defined as

$$
\vec a \cdot \vec b =
a_1b_1 + a_2b_2 + a_3b_3
$$

Substitute the vector components

$$
\vec a \cdot \vec b =
2\cdot1 + (-1)\cdot4 + 3\cdot(-2)
$$

Compute step by step

First term

$$
2\cdot1 = 2
$$

Second term

$$
(-1)\cdot4 = -4
$$

Third term

$$
3\cdot(-2) = -6
$$

Add them

$$
2 - 4 - 6
$$

$$
= -8
$$

Thus

$$
\vec a \cdot \vec b = -8
$$

---

# 4. Angle between vectors

The dot product also relates to the angle between vectors

$$
\vec a \cdot \vec b = |\vec a||\vec b|\cos\theta
$$

Solve for cosine

$$
\cos\theta =
\frac{\vec a \cdot \vec b}{|\vec a||\vec b|}
$$

Substitute the values

$$
\cos\theta =
\frac{-8}{\sqrt{14}\sqrt{21}}
$$

Multiply the square roots

$$
\sqrt{14}\sqrt{21} = \sqrt{294}
$$

Thus

$$
\cos\theta = \frac{-8}{\sqrt{294}}
$$

Finally the angle is

$$
\theta =
\arccos\left(\frac{-8}{\sqrt{294}}\right)
$$

Since cosine is negative, the angle is **obtuse**.

---

# 5. Cross product

The cross product produces a vector perpendicular to both vectors.

It is computed using the determinant

$$
\vec a \times \vec b =
\begin{vmatrix}
\mathbf i & \mathbf j & \mathbf k \\
2 & -1 & 3 \\
1 & 4 & -2
\end{vmatrix}
$$

---

## First component

$$
(-1)(-2) - 3(4)
$$

$$
= 2 - 12
$$

$$
= -10
$$

---

## Second component

$$
-(2(-2) - 3(1))
$$

$$
= -(-4 - 3)
$$

$$
= 7
$$

---

## Third component

$$
2(4) - (-1)(1)
$$

$$
= 8 + 1
$$

$$
= 9
$$

---

## Cross product result

$$
\vec a \times \vec b = (-10,7,9)
$$

---

# 6. Area of the parallelogram

The area formed by two vectors equals the magnitude of the cross product

$$
A = |\vec a \times \vec b|
$$

Substitute the components

$$
A = \sqrt{(-10)^2 + 7^2 + 9^2}
$$

Compute squares

$$
100 + 49 + 81
$$

$$
= 230
$$

Thus

$$
A = \sqrt{230}
$$

---

# 7. Matrix

$$
A =
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
$$

---

# 8. Matrix–vector multiplication

Compute

$$
A\vec a
$$

$$
=
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
2 \\
-1 \\
3
\end{pmatrix}
$$

---

## First component

$$
2\cdot2 + 1(-1) + 0(3)
$$

$$
= 4 - 1
$$

$$
= 3
$$

---

## Second component

$$
0(2) + 1(-1) + (-1)(3)
$$

$$
= -1 - 3
$$

$$
= -4
$$

---

## Third component

$$
1(2) + 0(-1) + 1(3)
$$

$$
= 2 + 3
$$

$$
= 5
$$

---

## Result

$$
A\vec a = (3,-4,5)
$$

---

# 9. Determinant

$$
\det A =
\begin{vmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{vmatrix}
$$

Expand along the first row

$$
\det A =
2
\begin{vmatrix}
1 & -1 \\
0 & 1
\end{vmatrix}
-
1
\begin{vmatrix}
0 & -1 \\
1 & 1
\end{vmatrix}
$$

First minor

$$
1\cdot1 - (-1)\cdot0 = 1
$$

Second minor

$$
0\cdot1 - (-1)\cdot1 = 1
$$

Substitute

$$
\det A = 2(1) - 1(1)
$$

$$
= 1
$$

---

# 10. Orientation of the transformation

A linear transformation preserves orientation if

$$
\det A > 0
$$

Since

$$
\det A = 1 > 0
$$

the transformation **preserves orientation**.

---

# Final results

$$
|\vec a| = \sqrt{14}
$$

$$
|\vec b| = \sqrt{21}
$$

$$
\vec a \cdot \vec b = -8
$$

$$
\vec a \times \vec b = (-10,7,9)
$$

$$
A = \sqrt{230}
$$

$$
A\vec a = (3,-4,5)
$$

$$
\det A = 1
$$

The transformation **preserves orientation**.