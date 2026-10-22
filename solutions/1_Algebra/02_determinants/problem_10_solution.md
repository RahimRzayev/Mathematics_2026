# Problem 10. Detecting Dependence

## Exercise

### Exercise 10. Detecting Dependence
Without carrying out a full determinant calculation, explain why

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}=0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

> **Why this exercise:** teaches how to recognize a zero determinant from the structure of a matrix.

---

## Answer

Row 2 is exactly twice row 1:

$$
R_2=2R_1\qquad\Longleftrightarrow\qquad 2R_1-R_2+0\cdot R_3=0
$$

Rows that are dependent force $\det=0$, so the matrix is **not invertible**.

---

## Steps

### Step 1. Spot the dependence

Compare rows 1 and 2:

| Row | Entries |
|---|---|
| $R_1$ | $(1,\ 2,\ 3)$ |
| $R_2$ | $(2,\ 4,\ 6)=2\cdot(1,\ 2,\ 3)$ |

### Step 2. Use a row operation

Apply $R_2\leftarrow R_2-2R_1$. This operation **does not change** the determinant:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5 \\
\end{pmatrix}
$$

### Step 3. Conclude

A matrix with a **zero row** has determinant $0$: every term of the determinant takes one entry from that row, and all of them are $0$.

So the original determinant is $0$.

---

## Why it works

These statements are equivalent for a square matrix $A$:

1. $\det A=0$.
2. The rows of $A$ are linearly dependent.
3. $A$ is not invertible.
4. $Ax=0$ has a nonzero solution $x$.

Here the dependence is $2R_1-R_2=0$. Geometrically, the three rows do not span all of $\mathbb{R}^3$: two of them lie on the same line, so the "volume" they span is flat, and flat volume is $0$.

---

## Check

Find a nonzero $x$ with $Ax=0$. From rows 1 and 3:

$$
\begin{cases}
x_1+2x_2+3x_3=0, \\
x_2+5x_3=0.
\end{cases}
$$

Take $x_3=1$. Then $x_2=-5$ and $x_1=10-3=7$, so $x=(7,\ -5,\ 1)^T$.

| Row | Product with $x$ |
|---|---|
| $(1,\ 2,\ 3)$ | $7-10+3=0$ |
| $(2,\ 4,\ 6)$ | $14-20+6=0$ |
| $(0,\ 1,\ 5)$ | $0-5+5=0$ |

A nonzero solution of $Ax=0$ exists, so $A$ cannot be invertible. ✓
