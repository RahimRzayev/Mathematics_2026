# Problem 13. Determinant by Elimination

## Exercise

### Exercise 13. Determinant by Elimination
Compute the determinant

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.

> **Why this exercise:** reinforces organizing a determinant calculation through row operations without introducing an unnecessary second procedure.

---

## Answer

$$
\det A=1
$$

---

## Steps

### Record of operations

| Step | Operation | Effect on $\det$ | Running factor |
|---|---|---|---|
| 1 | $R_2\leftarrow R_2-2R_1$ | None | $1$ |
| 2 | $R_3\leftarrow R_3-R_1$ | None | $1$ |
| 3 | $R_3\leftarrow R_3+2R_2$ | None | $1$ |

"Running factor" means: $\det A=$ factor $\times$ determinant of the current matrix. It stays $1$ because no swaps or row scalings were used.

### Step 1 and 2. Clear column 1

- $R_2$: $(2,\ 5,\ 7)-2\cdot(1,\ 2,\ 3)=(0,\ 1,\ 1)$.
- $R_3$: $(1,\ 0,\ 2)-(1,\ 2,\ 3)=(0,\ -2,\ -1)$.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{pmatrix}
$$

### Step 3. Clear column 2 below the pivot

- $R_3$: $(0,\ -2,\ -1)+2\cdot(0,\ 1,\ 1)=(0,\ 0,\ 1)$.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

### Step 4. Read off the determinant

Upper triangular, so multiply the diagonal:

$$
\det A=1\cdot\left(1\cdot 1\cdot 1\right)=1
$$

---

## Why it works

Elimination is the standard way to compute determinants of larger matrices:

1. Reduce to upper triangular form.
2. Track every swap (factor $-1$) and every row scaling (factor $c$).
3. Multiply the diagonal and correct by the tracked factors.

For a $3\times 3$ matrix it is about as fast as Sarrus' rule. For $4\times 4$ and larger, it is far faster than cofactor expansion.

$\det A=1\neq 0$, so $A$ is invertible.

---

## Check

Cofactor expansion along row 1 of the original $A$:

$$
\begin{aligned}
\det A &= 1\cdot(5\cdot 2-7\cdot 0)-2\cdot(2\cdot 2-7\cdot 1)+3\cdot(2\cdot 0-5\cdot 1) \\
&= 10+6-15 \\
&= 1
\end{aligned}
$$

Same value. ✓
