# Problem 2. Formula for a 2×2 Matrix

## Exercise

### Exercise 2. Formula for a 2×2 Matrix
Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

> **Why this exercise:** teaches the simplest explicit formula for an inverse and requires verification using the definition.

---

## Answer

$$
A^{-1}=\frac12
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
2 & -1 \\
-\frac52 & \frac32 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Recall the formula

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

Memory aid: **swap** the main diagonal, **negate** the other diagonal, **divide** by the determinant.

### Step 2. Compute the determinant

Here $a=3$, $b=2$, $c=5$, $d=4$:

$$
\det A=3\cdot 4-2\cdot 5=12-10=2
$$

Since $2\neq 0$, the inverse exists.

### Step 3. Swap and negate

Swap $3$ and $4$ on the main diagonal. Change the signs of $2$ and $5$:

$$
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}
$$

### Step 4. Divide by the determinant

$$
A^{-1}=\frac12
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
2 & -1 \\
-\frac52 & \frac32 \\
\end{pmatrix}
$$

---

## Why it works

Multiply $A$ by the swapped-and-negated matrix:

$$
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}=
\begin{pmatrix}
ad-bc & 0 \\
0 & ad-bc \\
\end{pmatrix}=(ad-bc)\,I
$$

The off-diagonal entries cancel exactly, and the diagonal entries equal the determinant. Dividing by $ad-bc$ turns this into $I$. That is why the determinant must be nonzero.

---

## Check

Compute $AA^{-1}$:

- Row 1, column 1: $3\cdot 2+2\cdot\left(-\frac52\right)=6-5=1$
- Row 1, column 2: $3\cdot(-1)+2\cdot\frac32=-3+3=0$
- Row 2, column 1: $5\cdot 2+4\cdot\left(-\frac52\right)=10-10=0$
- Row 2, column 2: $5\cdot(-1)+4\cdot\frac32=-5+6=1$

$$
AA^{-1}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=I
$$

The product is the identity. ✓
