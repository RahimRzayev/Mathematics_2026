# Problem 8. Determinant of a Product

## Exercise

### Exercise 8. Determinant of a Product
Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

> **Why this exercise:** organizes how determinants behave with respect to products and inverses.

---

## Answer

| Expression | Value |
|---|---|
| $\det(AB)$ | $-15$ |
| $\det(BA)$ | $-15$ |
| $\det(A^{-1}B)$ | $-\dfrac{5}{3}$ |

$A^{-1}$ exists because $\det A=3\neq 0$. The matrices $A$ and $B$ are assumed to have the same size, so the products are defined.

---

## Steps

### Step 1. $\det(AB)$

Product rule:

$$
\det(AB)=\det A\cdot\det B=3\cdot(-5)=-15
$$

### Step 2. $\det(BA)$

Same rule, factors in the other order:

$$
\det(BA)=\det B\cdot\det A=(-5)\cdot 3=-15
$$

### Step 3. Does $A^{-1}$ exist?

Yes. $\det A=3\neq 0$, so $A$ is invertible.

### Step 4. $\det(A^{-1})$

From $AA^{-1}=I$ and $\det I=1$:

$$
\det A\cdot\det(A^{-1})=1\qquad\Longrightarrow\qquad\det(A^{-1})=\frac{1}{\det A}=\frac{1}{3}
$$

### Step 5. $\det(A^{-1}B)$

$$
\det(A^{-1}B)=\det(A^{-1})\cdot\det B=\frac{1}{3}\cdot(-5)=-\frac{5}{3}
$$

---

## Why it works

Matrices usually do **not** commute: $AB\neq BA$ in general.

But $\det A$ and $\det B$ are **ordinary numbers**, and numbers always commute:

$$
\det(AB)=\det A\cdot\det B=\det B\cdot\det A=\det(BA)
$$

So $AB$ and $BA$ can be different matrices, yet always have the same determinant.

Key facts used:

1. $\det(AB)=\det A\cdot\det B$.
2. $\det(A^{-1})=1/\det A$, valid only when $\det A\neq 0$.

---

## Check

Example with $\det A=3$ and $\det B=-5$:

$$
A=
\begin{pmatrix}
3 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 1 \\
0 & -5 \\
\end{pmatrix}
$$

$$
AB=
\begin{pmatrix}
3 & 3 \\
0 & -5 \\
\end{pmatrix},\qquad BA=
\begin{pmatrix}
3 & 1 \\
0 & -5 \\
\end{pmatrix}
$$

$AB\neq BA$, but both are triangular with diagonal $3,\ -5$, so both determinants equal $-15$. ✓
