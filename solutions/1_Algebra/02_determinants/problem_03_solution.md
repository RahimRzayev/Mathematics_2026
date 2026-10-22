# Problem 3. Swapping Two Rows

## Exercise

### Exercise 3. Swapping Two Rows
For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

> **Why this exercise:** gives a second classical calculation with a $3\times3$ determinant while teaching the precise effect of a row swap on the sign of the determinant.

---

## Answer

| Matrix | Determinant |
|---|---|
| $A$ | $6$ |
| $B$ (rows 1 and 2 swapped) | $-6$ |

The prediction $\det B=-\det A=-6$ is confirmed by direct calculation.

---

## Steps

### Step 1. Compute $\det A$ by Sarrus' rule

Copy the first two columns to the right:

$$
\begin{pmatrix}
1 & 2 & 0 & \mid & 1 & 2 \\
0 & 3 & 1 & \mid & 0 & 3 \\
2 & 1 & 1 & \mid & 2 & 1 \\
\end{pmatrix}
$$

| Down-right diagonals | Up-right diagonals |
|---|---|
| $1\cdot 3\cdot 1=3$ | $2\cdot 3\cdot 0=0$ |
| $2\cdot 1\cdot 2=4$ | $1\cdot 1\cdot 1=1$ |
| $0\cdot 0\cdot 1=0$ | $1\cdot 0\cdot 2=0$ |
| **Sum** $=7$ | **Sum** $=1$ |

$$
\det A=7-1=6
$$

### Step 2. Form $B$

Swap row 1 and row 2 of $A$:

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

### Step 3. Predict $\det B$

Property: **swapping two rows multiplies the determinant by $-1$**.

$$
\det B=-\det A=-6
$$

### Step 4. Verify by calculation

Expand $B$ along its first row $(0,\ 3,\ 1)$. Signs along row 1 are $+,\ -,\ +$.

$$
\begin{aligned}
\det B &= 0\cdot\det
\begin{pmatrix}
2 & 0 \\
1 & 1 \\
\end{pmatrix}-3\cdot\det
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
\end{pmatrix}+1\cdot\det
\begin{pmatrix}
1 & 2 \\
2 & 1 \\
\end{pmatrix} \\
&= 0-3\cdot(1-0)+1\cdot(1-4) \\
&= -3-3 \\
&= -6
\end{aligned}
$$

Prediction confirmed.

---

## Why it works

Every term of the determinant takes one entry from each row. A row swap keeps all the same products but flips the sign attached to each one. So the size stays, the sign flips.

Useful consequences:

- An **odd** number of row swaps: sign flips.
- An **even** number of row swaps: sign returns to the original.
- The same rule holds for swapping two **columns**.

---

## Check

Sign table for a $3\times 3$ expansion:

$$
\begin{pmatrix}
+ & - & + \\
- & + & - \\
+ & - & + \\
\end{pmatrix}
$$

The minus sign on the middle term in Step 4 comes from position $(1,2)$. With it, $\det B=-6=-\det A$. ✓
