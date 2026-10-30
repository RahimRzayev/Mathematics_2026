# Problem 9. A System from a Sum Condition

## Exercise

### Exercise 9. A System from a Sum Condition
Find numbers $x,y$ satisfying

$$
x+y=10,\qquad 2x+5y=32.
$$

Solve the system and explain geometrically why the solution is unique.

> **Why this exercise:** reinforces the transition from two linear conditions to the intersection point of two lines.

---

## Answer

$$
(x,\ y)=(6,\ 4)
$$

The solution is unique because the two equations describe non-parallel lines (slopes $-1$ and $-\frac25$), which meet in exactly one point.

---

## Steps

### Step 1. Write the augmented matrix

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
2 & 5 & \mid & 32 \\
\end{pmatrix}
$$

### Step 2. Clear column 1

Operation: $R_2\to R_2-2R_1$.

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
0 & 3 & \mid & 12 \\
\end{pmatrix}
$$

Two pivots for two unknowns: the solution is unique.

### Step 3. Back substitution

From row 2:

$$
3y=12 \quad\Longrightarrow\quad y=4
$$

From row 1:

$$
x+4=10 \quad\Longrightarrow\quad x=6
$$

### Step 4. Geometric picture

Solve each equation for $y$:

$$
y=10-x,\qquad y=\frac{32-2x}{5}=\frac{32}{5}-\frac25x
$$

| Line | Slope | Passes through |
|---|---|---|
| $x+y=10$ | $-1$ | $(10,0)$, $(0,10)$ |
| $2x+5y=32$ | $-\frac25$ | $(16,0)$, $(0,\ 6.4)$ |

The slopes differ, so the lines are not parallel and intersect in exactly one point, $(6,4)$.

---

## Why it works

Each linear equation in two unknowns describes a line in the plane. A solution of the system is a point lying on both lines. Two lines in the plane can:

- intersect in one point (different slopes),
- be parallel and distinct (no common point),
- coincide (infinitely many common points).

Here the slopes differ. Algebraically, the same fact is expressed by a nonzero determinant:

$$
\det
\begin{pmatrix}
1 & 1 \\
2 & 5 \\
\end{pmatrix}=5-2=3\neq0
$$

The coefficient rows $(1,1)$ and $(2,5)$ are not proportional, so the normal directions of the lines differ.

---

## Check

Substitute $(6,4)$:

- $6+4=10$ ✓
- $2\cdot6+5\cdot4=12+20=32$ ✓
