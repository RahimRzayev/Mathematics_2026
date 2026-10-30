# Problem 2. Gaussian Elimination — One Solution

## Exercise

### Exercise 2. Gaussian Elimination — One Solution
Solve using Gaussian elimination:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

> **Why this exercise:** introduces the basic method for solving a system and builds the habit of checking the result.

---

## Answer

$$
(x,\ y,\ z)=(1,\ 2,\ 3)
$$

The system has exactly one solution.

---

## Steps

### Step 1. Write the augmented matrix

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
2 & -1 & 1 & \mid & 3 \\
1 & 2 & -1 & \mid & 2 \\
\end{pmatrix}
$$

Plan: create zeros below the pivots (forward elimination), then solve from the bottom row up (back substitution).

### Step 2. Clear column 1

Operations: $R_2\to R_2-2R_1$ and $R_3\to R_3-R_1$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & -3 & -1 & \mid & -9 \\
0 & 1 & -2 & \mid & -4 \\
\end{pmatrix}
$$

### Step 3. Swap rows for a simpler pivot

Operation: $R_2\leftrightarrow R_3$. The pivot $1$ avoids fractions.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & -3 & -1 & \mid & -9 \\
\end{pmatrix}
$$

### Step 4. Clear column 2 below the pivot

Operation: $R_3\to R_3+3R_2$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & 0 & -7 & \mid & -21 \\
\end{pmatrix}
$$

The matrix is in row echelon form with three pivots, so the solution is unique.

### Step 5. Back substitution

From row 3:

$$
-7z=-21 \quad\Longrightarrow\quad z=3
$$

From row 2:

$$
y-2z=-4 \quad\Longrightarrow\quad y=-4+6=2
$$

From row 1:

$$
x+y+z=6 \quad\Longrightarrow\quad x=6-2-3=1
$$

---

## Why it works

Each row operation (adding a multiple of one row to another, swapping rows) replaces the system by an equivalent one: every solution of the old system solves the new one, and the operation can be reversed. The solution set therefore never changes.

The triangular form at the end can be solved one unknown at a time. Three unknowns and three pivots leave no free variable, so the solution is unique.

---

## Check

Substitute $(1,2,3)$ into every original equation:

- $x+y+z=1+2+3=6$ ✓
- $2x-y+z=2-2+3=3$ ✓
- $x+2y-z=1+4-3=2$ ✓

All three equations hold, so the system is consistent and $(1,2,3)$ is its solution.
