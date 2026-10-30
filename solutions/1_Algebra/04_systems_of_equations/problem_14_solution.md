# Problem 14. A Small Change in the Right-Hand Side

## Exercise

### Exercise 14. A Small Change in the Right-Hand Side
Compare the systems

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3
\end{cases}
$$

and

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

> **Why this exercise:** shows the difference between a consistent and an inconsistent system without introducing new theory.

---

## Answer

| System | Last row after elimination | Type |
|---|---|---|
| with $3x=3$ | $0=0$ | consistent, exactly one solution $(x,y)=(1,1)$ |
| with $3x=3.1$ | $0=0.1$ | inconsistent, no solution |

The third coefficient row equals the sum of the first two, so a solution exists only if the right-hand sides satisfy the same relation: $b_3=b_1+b_2$. This holds for $3=2+1$ and fails for $3.1\neq2+1$.

---

## Steps

### Step 1. Process both systems together

Both systems share the coefficient matrix, so write both right-hand sides in one augmented matrix:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 & 2 \\
2 & -1 & \mid & 1 & 1 \\
3 & 0 & \mid & 3 & 3.1 \\
\end{pmatrix}
$$

### Step 2. Clear column 1

Operations: $R_2\to R_2-2R_1$ and $R_3\to R_3-3R_1$.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 & 2 \\
0 & -3 & \mid & -3 & -3 \\
0 & -3 & \mid & -3 & -2.9 \\
\end{pmatrix}
$$

### Step 3. Clear column 2

Operation: $R_3\to R_3-R_2$.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 & 2 \\
0 & -3 & \mid & -3 & -3 \\
0 & 0 & \mid & 0 & 0.1 \\
\end{pmatrix}
$$

### Step 4. Read off the first system

Row 3 reads $0=0$: consistent. Two pivots for two unknowns, so the solution is unique.

$$
-3y=-3 \quad\Longrightarrow\quad y=1,\qquad x=2-y=1
$$

### Step 5. Read off the second system

Row 3 reads $0=0.1$: a contradiction. The second system has no solution.

---

## Why it works

There are three equations but only two unknowns. Two non-parallel lines already fix a unique point; a third line must pass through **exactly that point** for the system to be consistent.

The first two equations meet at $(1,1)$. The coefficients of the third row are a combination of the first two:

$$
(3,\ 0)=(1,\ 1)+(2,\ -1)
$$

So adding the first two equations gives $3x=2+1=3$. The third equation must agree with this:

- $3x=3$ agrees, so the third line passes through $(1,1)$;
- $3x=3.1$ demands $x=\frac{3.1}{3}\approx1.033$, a vertical line slightly to the right of $(1,1)$, which misses that point.

Consistency here is an **exact equality condition** ($b_3=b_1+b_2$) on the right-hand side. Any change of $b_3$, no matter how small, breaks the equality. In contrast, a square system with an invertible matrix (such as the first two equations alone) stays uniquely solvable under small changes of the right-hand side: the solution only moves slightly.

---

## Check

First system, $(x,y)=(1,1)$:

- $1+1=2$ ✓
- $2-1=1$ ✓
- $3\cdot1=3$ ✓

Second system: the first two equations force $(x,y)=(1,1)$, and then

$$
3x=3\neq3.1
$$

so the third equation fails. No solution exists ✓.
