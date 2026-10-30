# Problem 11. A Parameter in a System of Three Equations

## Exercise

### Exercise 11. A Parameter in a System of Three Equations
Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

> **Why this exercise:** develops parametric analysis while still relying only on elimination.

---

## Answer

| Value of $t$ | Type | Solution |
|---|---|---|
| $t\neq1$ | exactly one solution | $x=\frac{t-4}{t-1},\ y=\frac{1}{t-1},\ z=\frac{2}{t-1}$ |
| $t=1$ | no solution | — |

Infinitely many solutions never occur.

---

## Steps

### Step 1. Write the augmented matrix

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
1 & t & 1 & \mid & 2 \\
1 & 1 & t & \mid & 3 \\
\end{pmatrix}
$$

### Step 2. Clear column 1

Operations: $R_2\to R_2-R_1$ and $R_3\to R_3-R_1$. No division, valid for every $t$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & t-1 & 0 & \mid & 1 \\
0 & 0 & t-1 & \mid & 2 \\
\end{pmatrix}
$$

The matrix is already in triangular form. The diagonal entries $t-1$ will be used as pivots.

### Step 3. Identify the critical value

Back substitution divides by the pivots $t-1$. This step is valid only when

$$
t-1\neq0 \quad\Longleftrightarrow\quad t\neq1
$$

So $t=1$ must be analyzed separately.

### Step 4. Case $t\neq1$

Three nonzero pivots, so exactly one solution.

From row 3:

$$
(t-1)z=2 \quad\Longrightarrow\quad z=\frac{2}{t-1}
$$

From row 2:

$$
(t-1)y=1 \quad\Longrightarrow\quad y=\frac{1}{t-1}
$$

From row 1:

$$
x=1-y-z=1-\frac{3}{t-1}=\frac{t-4}{t-1}
$$

### Step 5. Case $t=1$

Substitute $t=1$ into the matrix from Step 2:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & 0 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 2 \\
\end{pmatrix}
$$

Row 2 reads $0=1$. The system is inconsistent: no solution.

### Step 6. Why infinitely many solutions never occur

Infinitely many solutions require a consistent system with a missing pivot. A pivot is missing only for $t=1$, and for that value the system is inconsistent. So the case does not occur for any $t$.

---

## Why it works

The determinant of the coefficient matrix confirms the critical value. Using the triangular form from Step 2 (row additions do not change the determinant):

$$
\det
\begin{pmatrix}
1 & 1 & 1 \\
1 & t & 1 \\
1 & 1 & t \\
\end{pmatrix}=1\cdot(t-1)\cdot(t-1)=(t-1)^2
$$

It vanishes only at $t=1$. For $t\neq1$ the matrix is invertible and the solution is unique.

At $t=1$ all three equations have the same left-hand side $x+y+z$ but different right-hand sides $1,2,3$. They describe three parallel planes, which share no point.

---

## Check

Take $t=2$: the formulas give $(x,y,z)=(-2,\ 1,\ 2)$.

- $x+y+z=-2+1+2=1$ ✓
- $x+2y+z=-2+2+2=2$ ✓
- $x+y+2z=-2+1+4=3$ ✓

Take $t=0$: the formulas give $(x,y,z)=(4,\ -1,\ -2)$.

- $x+y+z=4-1-2=1$ ✓
- $x+0\cdot y+z=4-2=2$ ✓
- $x+y+0\cdot z=4-1=3$ ✓

Take $t=1$: equations 1 and 2 read $x+y+z=1$ and $x+y+z=2$, a contradiction ✓.
