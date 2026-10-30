# Problem 8. Two Systems with the Same Coefficient Matrix

## Exercise

### Exercise 8. Two Systems with the Same Coefficient Matrix
Solve by elimination the two systems

$$
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
$$

$$
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

> **Why this exercise:** shows the role of the coefficient matrix independently of the right-hand side.

---

## Answer

- System 1: $(x,y)=(2,\ 1)$.
- System 2: $(x,y)=\left(\frac53,\ -\frac73\right)$.

The row operations and the resulting coefficient part are identical in both cases. Only the right-hand side column differs, because the choice of row operations depends only on the coefficient matrix

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & -1 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Write both systems as one augmented matrix

Both systems share $A$, so they can be processed together with two right-hand side columns:

$$
\begin{pmatrix}
2 & 1 & \mid & 5 & 1 \\
1 & -1 & \mid & 1 & 4 \\
\end{pmatrix}
$$

### Step 2. Clear column 1

Operation: $R_2\to 2R_2-R_1$ (keeps integers).

$$
\begin{pmatrix}
2 & 1 & \mid & 5 & 1 \\
0 & -3 & \mid & -3 & 7 \\
\end{pmatrix}
$$

Right-hand sides of row 2: $2\cdot1-5=-3$ and $2\cdot4-1=7$.

### Step 3. Back substitution for System 1

From row 2:

$$
-3y=-3 \quad\Longrightarrow\quad y=1
$$

From row 1:

$$
2x+1=5 \quad\Longrightarrow\quad x=2
$$

### Step 4. Back substitution for System 2

From row 2:

$$
-3y=7 \quad\Longrightarrow\quad y=-\frac73
$$

From row 1:

$$
2x-\frac73=1 \quad\Longrightarrow\quad 2x=\frac{10}{3} \quad\Longrightarrow\quad x=\frac53
$$

### Step 5. Compare the steps

| | System 1 | System 2 |
|---|---|---|
| Row operation | $R_2\to 2R_2-R_1$ | $R_2\to 2R_2-R_1$ |
| Coefficient rows after elimination | $(2,\ 1)$ and $(0,\ -3)$ | $(2,\ 1)$ and $(0,\ -3)$ |
| Right-hand side after elimination | $(5,\ -3)$ | $(1,\ 7)$ |
| Divisions in back substitution | by $-3$, then by $2$ | by $-3$, then by $2$ |

---

## Why it works

The row operations are chosen to create zeros below the pivots. Those zeros live in the coefficient matrix, so the choice of operation (which row, which multiplier) is decided by $A$ alone. The right-hand side is just carried along and transformed by the same operations.

Therefore:

- the elimination of $A$ is done once and is valid for every right-hand side,
- only the right-hand side column must be recomputed for each new $b$.

This is why several systems with the same $A$ are solved together as $[A\mid b_1\ b_2]$, and why finding $A^{-1}$ pays off when there are many right-hand sides.

---

## Check

System 1, $(x,y)=(2,1)$:

- $2\cdot2+1=5$ ✓
- $2-1=1$ ✓

System 2, $(x,y)=\left(\frac53,\ -\frac73\right)$:

- $2\cdot\frac53-\frac73=\frac{10-7}{3}=1$ ✓
- $\frac53+\frac73=\frac{12}{3}=4$ ✓
