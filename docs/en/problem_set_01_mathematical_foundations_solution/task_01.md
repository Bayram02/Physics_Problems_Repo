# Problem 1 – Vectors and Linear Transformations

## Given vectors

$$
\vec a = (2,-1,3), \qquad
\vec b = (1,4,-2)
$$

---

# 1. Vector lengths

The length (Euclidean norm) of a vector is

$$
|\vec v|=\sqrt{v_1^2+v_2^2+v_3^2}
$$

### Length of $\vec a$

$$
|\vec a|=\sqrt{2^2+(-1)^2+3^2}
$$

$$
=\sqrt{4+1+9}
$$

$$
=\sqrt{14}
$$

---

### Length of $\vec b$

$$
|\vec b|=\sqrt{1^2+4^2+(-2)^2}
$$

$$
=\sqrt{1+16+4}
$$

$$
=\sqrt{21}
$$

---

# 2. Normalized vector $\hat a$

The normalized vector is defined as

$$
\hat a=\frac{\vec a}{|\vec a|}
$$

Substitute the values:

$$
\hat a=\frac{(2,-1,3)}{\sqrt{14}}
$$

Thus

$$
\hat a=
\left(
\frac{2}{\sqrt{14}},
\frac{-1}{\sqrt{14}},
\frac{3}{\sqrt{14}}
\right)
$$

---

# 3. Dot product and angle between vectors

The dot product is

$$
\vec a \cdot \vec b = a_1 b_1 + a_2 b_2 + a_3 b_3
$$

Substitute the values:

$$
\vec a \cdot \vec b
=2\cdot1+(-1)\cdot4+3\cdot(-2)
$$

$$
=2-4-6
$$

$$
=-8
$$

---

## Angle between vectors

The formula for the angle is

$$
\vec a \cdot \vec b = |\vec a||\vec b|\cos\theta
$$

Solve for $\cos\theta$:

$$
\cos\theta=
\frac{\vec a\cdot\vec b}{|\vec a||\vec b|}
$$

Substitute the values:

$$
\cos\theta=
\frac{-8}{\sqrt{14}\sqrt{21}}
$$

Since

$$
\sqrt{14}\sqrt{21}=\sqrt{294}
$$

we obtain

$$
\cos\theta=\frac{-8}{\sqrt{294}}
$$

Therefore

$$
\theta=\arccos\left(\frac{-8}{\sqrt{294}}\right)
$$

---

# 4. Cross product

The cross product is calculated using the determinant:

$$
\vec a\times\vec b=
\begin{vmatrix}
\mathbf i & \mathbf j & \mathbf k \
2 & -1 & 3 \
1 & 4 & -2
\end{vmatrix}
$$

Compute each component.

### First component

$$
(-1)(-2)-3(4)
$$

$$
=2-12
$$

$$
=-10
$$

---

### Second component

$$
-(2(-2)-3(1))
$$

$$
= -(-4-3)
$$

$$
=7
$$

---

### Third component

$$
2(4)-(-1)(1)
$$

$$
=8+1
$$

$$
=9
$$

---

### Result

$$
\vec a\times\vec b=(-10,7,9)
$$

---

# Area of the parallelogram

The area equals the magnitude of the cross product:

$$
A=|\vec a\times\vec b|
$$

$$
=\sqrt{(-10)^2+7^2+9^2}
$$

$$
=\sqrt{100+49+81}
$$

$$
=\sqrt{230}
$$

---

# Matrix part

Matrix:

$$
A=
\begin{pmatrix}
2 & 1 & 0 \
0 & 1 & -1 \
1 & 0 & 1
\end{pmatrix}
$$

---

# 5. Calculate $A\vec a$

$$
A\vec a=
\begin{pmatrix}
2 & 1 & 0 \
0 & 1 & -1 \
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
2\
-1\
3
\end{pmatrix}
$$

Multiply row by column.

### First component

$$
2\cdot2+1\cdot(-1)+0\cdot3
$$

$$
=4-1
$$

$$
=3
$$

---

### Second component

$$
0\cdot2+1\cdot(-1)+(-1)\cdot3
$$

$$
=-1-3
$$

$$
=-4
$$

---

### Third component

$$
1\cdot2+0\cdot(-1)+1\cdot3
$$

$$
=2+3
$$

$$
=5
$$

---

### Result

$$
A\vec a=(3,-4,5)
$$

---

# 6. Determinant of the matrix

$$
\det A=
\begin{vmatrix}
2 & 1 & 0 \
0 & 1 & -1 \
1 & 0 & 1
\end{vmatrix}
$$

Expand along the first row:

$$
=2
\begin{vmatrix}
1 & -1 \
0 & 1
\end{vmatrix}
-1
\begin{vmatrix}
0 & -1 \
1 & 1
\end{vmatrix}
+0
\begin{vmatrix}
0 & 1 \
1 & 0
\end{vmatrix}
$$

Compute the minors.

### First minor

$$
1\cdot1-(-1)\cdot0
$$

$$
=1
$$

### Second minor

$$
0\cdot1-(-1)\cdot1
$$

$$
=1
$$

Substitute:

$$
\det A=2(1)-1(1)
$$

$$
=2-1
$$

$$
=1
$$

---

# 7. Orientation of the transformation

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

✅ **Final results**

$$
|\vec a|=\sqrt{14}
$$

$$
|\vec b|=\sqrt{21}
$$

$$
\hat a=
\left(
\frac{2}{\sqrt{14}},
\frac{-1}{\sqrt{14}},
\frac{3}{\sqrt{14}}
\right)
$$

$$
\vec a\cdot\vec b=-8
$$

$$
\vec a\times\vec b=(-10,7,9)
$$

$$
A=|\vec a\times\vec b|=\sqrt{230}
$$

$$
A\vec a=(3,-4,5)
$$

$$
\det A=1
$$

Transformation **preserves orientation**.

---
