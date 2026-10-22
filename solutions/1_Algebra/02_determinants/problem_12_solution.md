# Problem 12. A Parameter Revealed by a Row Operation

## Exercise

### Exercise 12. A Parameter Revealed by a Row Operation
For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

$$
R_2\leftarrow R_2-2R_1
$$

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

> **Why this exercise:** combines a parameter, row operations, and recognition of dependence in one short argument.

---

## Answer

$$
\det A(t)=6-t
$$

$A(t)$ is **not invertible only for** $t=6$.

At $t=6$, row 2 becomes $(2,\ 4,\ 6)$, which is exactly $2\times$ row 1.

---

## Steps

### Step 1. Apply $R_2\leftarrow R_2-2R_1$

Row 2 becomes $(2,\ 4,\ t)-2\cdot(1,\ 2,\ 3)=(0,\ 0,\ t-6)$.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t-6 \\
0 & 1 & 1 \\
\end{pmatrix}
$$

Effect on $\det$: **none**.

### Step 2. Swap rows 2 and 3 to get a triangle

Operation: $R_2\leftrightarrow R_3$. Effect: determinant **flips sign**.

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & t-6 \\
\end{pmatrix}
$$

This triangular matrix has determinant $1\cdot 1\cdot(t-6)=t-6$.

### Step 3. Undo the sign flip

$$
\det A(t)=-(t-6)=6-t
$$

### Step 4. Solve $\det A(t)=0$

$$
6-t=0\qquad\Longrightarrow\qquad t=6
$$

---

## Why it works

After Step 1, all of row 2 except the last entry is zero. The only thing that can stop row 2 from becoming a full zero row is $t-6$.

| Value of $t$ | Row 2 after the operation | Determinant | Invertible? |
|---|---|---|---|
| $t\neq 6$ | $(0,\ 0,\ t-6)$, not zero | $6-t\neq 0$ | Yes |
| $t=6$ | $(0,\ 0,\ 0)$ | $0$ | No |

**What happens to the rows at $t=6$:** the original row 2 is $(2,\ 4,\ 6)=2\cdot(1,\ 2,\ 3)$. So $R_2=2R_1$. The rows are linearly dependent, which is exactly why the determinant vanishes.

---

## Check

Cofactor expansion along row 1 of the original $A(t)$:

$$
\begin{aligned}
\det A(t) &= 1\cdot(4\cdot 1-t\cdot 1)-2\cdot(2\cdot 1-t\cdot 0)+3\cdot(2\cdot 1-4\cdot 0) \\
&= (4-t)-4+6 \\
&= 6-t
\end{aligned}
$$

Same formula. ✓
