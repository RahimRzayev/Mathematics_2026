# Problem 7. Using Properties Instead of Recomputing

## Exercise

### Exercise 7. Using Properties Instead of Recomputing
Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

> **Why this exercise:** teaches how to use determinant properties instead of repeating a full calculation.

---

## Answer

| Expression | Property | Value |
|---|---|---|
| $\det(2A)$ | $\det(cA)=c^n\det A$ | $-32$ |
| $\det(A^T)$ | $\det(A^T)=\det A$ | $-4$ |
| $\det(A^2)$ | $\det(AB)=\det A\cdot\det B$ | $16$ |
| $\det(-A)$ | $\det(cA)=c^n\det A$ with $c=-1$ | $4$ |

Here $n=3$ is the size of the matrix.

---

## Steps

### Step 1. $\det(2A)$

$2A$ multiplies **every row** by $2$. Each row scaling multiplies the determinant by $2$. There are $3$ rows:

$$
\det(2A)=2^3\det A=8\cdot(-4)=-32
$$

Common mistake: writing $2\cdot(-4)=-8$. That would scale only one row.

### Step 2. $\det(A^T)$

Transposing swaps rows and columns but keeps the determinant:

$$
\det(A^T)=\det A=-4
$$

### Step 3. $\det(A^2)$

$A^2=A\cdot A$. The determinant of a product is the product of the determinants:

$$
\det(A^2)=\det A\cdot\det A=(-4)^2=16
$$

### Step 4. $\det(-A)$

$-A=(-1)\cdot A$, so use the scaling rule with $c=-1$:

$$
\det(-A)=(-1)^3\det A=(-1)\cdot(-4)=4
$$

---

## Why it works

The scaling rule is the one to remember:

$$
\det(cA)=c^n\det A\qquad\mathrm{for\ an}\ n\times n\ \mathrm{matrix}
$$

The factor $c$ comes out **once per row**, so it appears $n$ times.

For $\det(-A)$ the sign depends on the size:

- $n$ odd (like $3$): $\det(-A)=-\det A$.
- $n$ even (like $2$): $\det(-A)=\det A$.

---

## Check

Test with a simple matrix that has $\det=-4$:

$$
A=
\begin{pmatrix}
-4 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

Then $2A$ has diagonal $-8,\ 2,\ 2$, so $\det(2A)=-32$. And $-A$ has diagonal $4,\ -1,\ -1$, so $\det(-A)=4$. ✓
