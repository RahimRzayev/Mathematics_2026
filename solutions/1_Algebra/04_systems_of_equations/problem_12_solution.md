# Problem 12. Homogeneous System

## Exercise

### Exercise 12. Homogeneous System
Solve

$$
\begin{cases}
x+2y-z=0, \\
2x+4y-2z=0, \\
x-y+2z=0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

> **Why this exercise:** shows the special case of a system with a zero right-hand side without introducing additional theory.

---

## Answer

Infinitely many solutions. With the free variable $z=t$, $t\in\mathbb{R}$:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}=t
\begin{pmatrix}
-1 \\
1 \\
1 \\
\end{pmatrix}
$$

$(0,0,0)$ is always a solution because substituting zeros makes every left-hand side $0$, which equals the zero right-hand side.

---

## Steps

### Step 1. Write the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
2 & 4 & -2 & \mid & 0 \\
1 & -1 & 2 & \mid & 0 \\
\end{pmatrix}
$$

The right-hand side column is zero and stays zero under every row operation.

### Step 2. Clear column 1

Operations: $R_2\to R_2-2R_1$ and $R_3\to R_3-R_1$.

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
\end{pmatrix}
$$

Row 2 vanished: the second equation is twice the first.

### Step 3. Reorder to row echelon form

Operation: $R_2\leftrightarrow R_3$.

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

Pivots in columns 1 and 2; $z$ is free.

### Step 4. Back substitution with $z=t$

From row 2:

$$
-3y+3t=0 \quad\Longrightarrow\quad y=t
$$

From row 1:

$$
x+2t-t=0 \quad\Longrightarrow\quad x=-t
$$

---

## Why it works

**Why $(0,0,0)$ always works.** Every equation of a homogeneous system has the form

$$
a_1x_1+a_2x_2+\dots+a_nx_n=0
$$

Substituting $x_1=\dots=x_n=0$ gives $a_1\cdot0+\dots+a_n\cdot0=0$, which holds for any coefficients. In matrix form, $A\cdot0=0$ for every matrix $A$.

Consequences:

- a homogeneous system is **never** inconsistent;
- the only question is whether $(0,0,0)$ is the only solution or one of infinitely many;
- here there are $3$ unknowns and $2$ pivots, so one free variable gives infinitely many solutions.

The solution set is a line through the origin with direction $(-1,1,1)$. Setting $t=0$ recovers the zero solution.

---

## Check

Take $t=1$: $(x,y,z)=(-1,\ 1,\ 1)$.

- $x+2y-z=-1+2-1=0$ ✓
- $2x+4y-2z=-2+4-2=0$ ✓
- $x-y+2z=-1-1+2=0$ ✓

Any multiple $t(-1,1,1)$ also works, because each left-hand side is multiplied by $t$ and $t\cdot0=0$.
