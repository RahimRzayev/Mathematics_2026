# Problem 11. Shortening the Calculation with Row Operations

## Exercise

### Exercise 11. Shortening the Calculation with Row Operations
Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

> **Why this exercise:** develops planning instead of mechanically repeating the same procedure.

---

## Answer

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}=1
$$

Operations that **do not change** the determinant: adding a multiple of one row to a **different** row, $R_i\leftarrow R_i+cR_j$ with $i\neq j$. All three operations below are of this type.

---

## Steps

### Step 0. Plan

Column 1 is $(1,\ 1,\ 1)^T$. Subtracting row 1 from the other rows clears it in one move. No fractions, no swaps.

### Step 1. Clear column 1

Operations: $R_2\leftarrow R_2-R_1$ and $R_3\leftarrow R_3-R_1$.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}
$$

Determinant: **unchanged**.

### Step 2. Clear column 2 below the pivot

Operation: $R_3\leftarrow R_3-2R_2$.

Row 3 becomes $(0,\ 2,\ 3)-2\cdot(0,\ 1,\ 1)=(0,\ 0,\ 1)$.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

Determinant: **unchanged**.

### Step 3. Multiply the diagonal

$$
\det=1\cdot 1\cdot 1=1
$$

---

## Why it works

Effect of each type of row operation:

| Operation | Effect on $\det$ | Used here? |
|---|---|---|
| $R_i\leftarrow R_i+cR_j$, $i\neq j$ | None | Yes, three times |
| $R_i\leftrightarrow R_j$ | Sign flips | No |
| $R_i\leftarrow cR_i$ | Multiplied by $c$ | No |

Planning tip: choose a pivot equal to $1$ when possible. Then every elimination multiplier is an integer and the work stays clean.

---

## Check

Cofactor expansion along row 1 of the original matrix:

$$
\begin{aligned}
\det &= 1\cdot(3\cdot 6-4\cdot 4)-2\cdot(1\cdot 6-4\cdot 1)+3\cdot(1\cdot 4-3\cdot 1) \\
&= 1\cdot 2-2\cdot 2+3\cdot 1 \\
&= 1
\end{aligned}
$$

Same value. ✓
