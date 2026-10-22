# Problem 5. Row Operations

## Exercise

### Exercise 5. Row Operations
For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

> **Why this exercise:** connects determinants with row operations and requires conscious tracking of every step.

---

## Answer

$$
\det A=21
$$

All three operations used are of the type "add a multiple of one row to another", so the determinant never changes.

---

## Steps

### The three rules to track

| Row operation | Effect on $\det$ |
|---|---|
| $R_i\leftarrow R_i+cR_j$ (add a multiple of another row) | No change |
| $R_i\leftrightarrow R_j$ (swap two rows) | Multiply by $-1$ |
| $R_i\leftarrow cR_i$ (scale a row by $c$) | Multiply by $c$ |

### Step 1. Clear column 1 below the pivot

Operations: $R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3+R_1$.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}
$$

Effect: **no change**, the determinant is still $\det A$.

### Step 2. Clear column 2 below the pivot

Operation: $R_3\leftarrow R_3+2R_2$.

Row 3 becomes $(0,\ 6,\ 5)+2\cdot(0,\ -3,\ -6)=(0,\ 0,\ -7)$.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{pmatrix}
$$

Effect: **no change**.

### Step 3. Multiply the diagonal

The matrix is now upper triangular:

$$
\det A=1\cdot(-3)\cdot(-7)=21
$$

---

## Why it works

Row operations turn a hard determinant into a triangular one, where the answer is just the diagonal product.

Adding a multiple of one row to another does not change the determinant because the determinant is linear in each row:

$$
\det(\ldots,\ R_i+cR_j,\ \ldots)=\det(\ldots,\ R_i,\ \ldots)+c\cdot\det(\ldots,\ R_j,\ \ldots)
$$

The second determinant has $R_j$ appearing twice, so it equals $0$. Only the original determinant remains.

---

## Check

Cofactor expansion along row 1 of the original $A$:

$$
\begin{aligned}
\det A &= 1\cdot(1\cdot 2-0\cdot 4)-2\cdot(2\cdot 2-0\cdot(-1))+3\cdot(2\cdot 4-1\cdot(-1)) \\
&= 2-8+27 \\
&= 21
\end{aligned}
$$

Same value. ✓
