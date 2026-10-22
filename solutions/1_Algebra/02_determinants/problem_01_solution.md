# Problem 1. Determinant of a 2×2 Matrix

## Exercise

### Exercise 1. Determinant of a 2×2 Matrix
Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad \det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

> **Why this exercise:** introduces the simplest determinant calculation and immediately connects it with invertibility.

---

## Answer

| Matrix | Determinant | Invertible? |
|---|---|---|
| First | $22$ | Yes, because $22\neq 0$ |
| Second | $0$ | No, because the determinant is $0$ |

Only the **first** matrix is invertible.

---

## Steps

### Step 1. Recall the 2×2 formula

$$
\det
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}=ad-bc
$$

Memory aid: **main diagonal minus the other diagonal**.

### Step 2. First matrix

Main diagonal: $3\cdot 4=12$. Other diagonal: $(-2)\cdot 5=-10$.

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}=12-(-10)=22
$$

Watch the sign: subtracting $-10$ means adding $10$.

### Step 3. Second matrix

Main diagonal: $1\cdot 14=14$. Other diagonal: $7\cdot 2=14$.

$$
\det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}=14-14=0
$$

### Step 4. Decide invertibility

Rule: a square matrix is invertible **exactly when** its determinant is not zero.

- First matrix: $\det=22\neq 0$, so it is invertible.
- Second matrix: $\det=0$, so it is not invertible.

---

## Why it works

For a $2\times 2$ matrix the inverse formula is

$$
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
$$

The determinant sits in the denominator. When it is $0$, the formula breaks: you would divide by zero.

The structure explains the zero as well. In the second matrix, row 2 is exactly $2\times$ row 1:

$$
(2,\ 14)=2\cdot(1,\ 7)
$$

The rows point in the same direction, so they carry no independent information. That is what $\det=0$ detects.

---

## Check

For the first matrix, multiply by the formula inverse:

$$
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}\cdot\frac{1}{22}
\begin{pmatrix}
4 & 2 \\
-5 & 3 \\
\end{pmatrix}=\frac{1}{22}
\begin{pmatrix}
22 & 0 \\
0 & 22 \\
\end{pmatrix}=I
$$

The product is the identity. ✓
