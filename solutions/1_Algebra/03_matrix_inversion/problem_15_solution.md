# Problem 15. Two Methods for Solving the Same System

## Exercise

### Exercise 15. Two Methods for Solving the Same System
For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

solve $Ax=b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

> **Why this exercise:** compares two known methods and prepares the student to choose a solution method consciously.

---

## Answer

$$
x=
\begin{pmatrix}
\frac{13}{5} \\
\frac95 \\
\end{pmatrix}
$$

| Method | Essential steps | Result |
|---|---|---|
| $A^{-1}b$ | 3 (determinant, inverse, product) | $\left(\frac{13}{5},\ \frac95\right)$ |
| Gaussian elimination | 2 (one row operation, back substitution) | $\left(\frac{13}{5},\ \frac95\right)$ |

Both methods give the same vector. **Gaussian elimination** was simpler here.

---

## Steps

### Method 1. Using $A^{-1}b$

**Step 1.1. Determinant.**

$$
\det A=2\cdot 3-1\cdot 1=5
$$

**Step 1.2. Inverse.** Swap the main diagonal, negate the other diagonal, divide by $5$:

$$
A^{-1}=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

**Step 1.3. Product.**

$$
x=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}=\frac15
\begin{pmatrix}
21-8 \\
-7+16 \\
\end{pmatrix}=\frac15
\begin{pmatrix}
13 \\
9 \\
\end{pmatrix}
$$

### Method 2. Gaussian elimination

**Step 2.1. Augmented matrix and one row operation.**

$$
\begin{pmatrix}
2 & 1 & \mid & 7 \\
1 & 3 & \mid & 8 \\
\end{pmatrix}
$$

Operation: $R_2\to 2R_2-R_1$ (keeps integers).

$$
\begin{pmatrix}
2 & 1 & \mid & 7 \\
0 & 5 & \mid & 9 \\
\end{pmatrix}
$$

**Step 2.2. Back substitution.**

From row 2:

$$
5x_2=9 \quad\Longrightarrow\quad x_2=\frac95
$$

From row 1:

$$
2x_1=7-\frac95=\frac{26}{5} \quad\Longrightarrow\quad x_1=\frac{13}{5}
$$

---

## Why it works

Both methods rest on the same row operations. Computing $A^{-1}$ amounts to solving $Ax=b$ for **every** possible $b$ at once: it is Gauss–Jordan applied to $[A\mid I]$. For one specific $b$ that is extra work.

When to prefer each method:

| Situation | Better choice |
|---|---|
| One system, one right-hand side | Gaussian elimination |
| Same $A$, many right-hand sides | Find $A^{-1}$ once, then multiply |
| $A^{-1}$ already known | $A^{-1}b$ (one product) |

The last row applies here: the same $A$ appears in Problem 6, where $A^{-1}$ was already computed. With that inverse reused, method 1 costs only one matrix–vector product.

For large matrices, elimination is also numerically safer and cheaper than forming the inverse.

---

## Check

Substitute $x=\left(\frac{13}{5},\ \frac95\right)$ into the system:

$$
\begin{cases}
2x_1+x_2=7, \\
x_1+3x_2=8.
\end{cases}
$$

- First equation: $2\cdot\frac{13}{5}+\frac95=\frac{26+9}{5}=\frac{35}{5}=7$
- Second equation: $\frac{13}{5}+3\cdot\frac95=\frac{13+27}{5}=\frac{40}{5}=8$

Both equations hold. ✓
