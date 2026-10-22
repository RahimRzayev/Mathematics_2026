# Problem 2. Determinant of a 3×3 Matrix

## Exercise

### Exercise 2. Determinant of a 3×3 Matrix
For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

> **Why this exercise:** teaches a basic method for $3\times3$ matrices and builds the habit of checking the result without adding a second full solution.

---

## Answer

$$
\det A=33
$$

Check by the row-replacement property gives the same value, $33$.

---

## Steps

### Step 1. Write the first two columns again on the right

Sarrus' rule works only for $3\times 3$ matrices. Copy columns 1 and 2 to the right of the matrix:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 1 & 2 \\
0 & 3 & 4 & \mid & 0 & 3 \\
2 & 1 & 5 & \mid & 2 & 1 \\
\end{pmatrix}
$$

### Step 2. Add the three "down-right" diagonals

| Diagonal | Product |
|---|---|
| $1\cdot 3\cdot 5$ | $15$ |
| $2\cdot 4\cdot 2$ | $16$ |
| $(-1)\cdot 0\cdot 1$ | $0$ |
| **Sum** | $31$ |

### Step 3. Add the three "up-right" diagonals

These start in the bottom row and go up to the right.

| Diagonal | Product |
|---|---|
| $2\cdot 3\cdot(-1)$ | $-6$ |
| $1\cdot 4\cdot 1$ | $4$ |
| $5\cdot 0\cdot 2$ | $0$ |
| **Sum** | $-2$ |

### Step 4. Subtract

$$
\det A=31-(-2)=33
$$

---

## Why it works

Sarrus' rule is a shortcut that lists all six products of the full $3\times 3$ formula:

$$
\det A=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{13}a_{22}a_{31}-a_{11}a_{23}a_{32}-a_{12}a_{21}a_{33}
$$

Each product takes **exactly one entry from every row and every column**. The down-right diagonals get a plus sign, the up-right diagonals get a minus sign.

Warning: this diagonal trick does **not** extend to $4\times 4$ matrices.

---

## Check

Property used: adding a multiple of one row to another row **does not change** the determinant.

Apply $R_3\leftarrow R_3-2R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & -3 & 7 \\
\end{pmatrix}
$$

Column 1 now has only one nonzero entry. Expand along column 1:

$$
\det A=1\cdot\det
\begin{pmatrix}
3 & 4 \\
-3 & 7 \\
\end{pmatrix}=21-(-12)=33
$$

Same value. ✓
