# Problem 3. Inconsistent System

## Exercise

### Exercise 3. Inconsistent System
Solve or show that the system is inconsistent:

$$
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

> **Why this exercise:** teaches how to recognize that a system has no solution without guessing.

---

## Answer

The system is **inconsistent** (no solution). Elimination produces the row

$$
\begin{pmatrix}
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

which means $0=1$.

---

## Steps

### Step 1. Write the augmented matrix

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
2 & 4 & \mid & 7 \\
\end{pmatrix}
$$

### Step 2. Clear column 1

Operation: $R_2\to R_2-2R_1$.

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

### Step 3. Read the last row as an equation

Row 2 says

$$
0\cdot x+0\cdot y=1
$$

The left side is $0$ for every choice of $x,y$, so this equation is never satisfied. The system has no solution.

### Step 4. Interpret in terms of the original equations

Multiply the first equation by $2$:

$$
2x+4y=6
$$

The second equation demands $2x+4y=7$. The same expression $2x+4y$ cannot equal both $6$ and $7$. The equations contradict each other.

---

## Why it works

Row operations do not change the solution set. If the final system contains an impossible equation $0=c$ with $c\neq0$, the final system has no solutions, and so neither does the original one.

The typical sign of inconsistency in row echelon form:

- a row of zeros on the coefficient side,
- a nonzero entry on the right-hand side.

Geometrically, both equations describe lines with slope $-\frac12$:

$$
y=\frac{3-x}{2},\qquad y=\frac{7-2x}{4}=\frac{3.5-x}{2}
$$

The lines are parallel and distinct, so they have no common point.

---

## Check

Suppose a solution $(x,y)$ existed. Then $x+2y=3$, so

$$
2x+4y=2(x+2y)=2\cdot3=6\neq7
$$

This contradicts the second equation. No solution exists. ✓
