# Problem 13. Does Every Equation Add New Information?

## Exercise

### Exercise 13. Does Every Equation Add New Information?
Consider the system

$$
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

> **Why this exercise:** teaches how to recognize redundant equations within a system.

---

## Answer

Infinitely many solutions. With $x_3=t$, $t\in\mathbb{R}$:

$$
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
\end{pmatrix}=
\begin{pmatrix}
2+t \\
8-t \\
t \\
\end{pmatrix}
$$

Not all equations are necessary. The third is the difference of the first two:

$$
(x_1+x_2)-(x_2+x_3)=10-8 \quad\Longrightarrow\quad x_1-x_3=2
$$

Any two of the three equations describe the same solution set.

---

## Steps

### Step 1. Write the augmented matrix

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
1 & 0 & -1 & \mid & 2 \\
\end{pmatrix}
$$

### Step 2. Clear column 1

Operation: $R_3\to R_3-R_1$.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & -1 & -1 & \mid & -8 \\
\end{pmatrix}
$$

### Step 3. Clear column 2

Operation: $R_3\to R_3+R_2$.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

Row 3 became $0=0$. Combining Steps 2 and 3, the zero row is

$$
R_3-R_1+R_2=0
$$

so $R_3=R_1-R_2$: the third equation is the first minus the second.

### Step 4. Back substitution with $x_3=t$

From row 2:

$$
x_2=8-t
$$

From row 1:

$$
x_1=10-x_2=2+t
$$

### Step 5. Which equations are necessary?

The dependence $R_3=R_1-R_2$ can be rearranged:

$$
R_1=R_2+R_3,\qquad R_2=R_1-R_3
$$

So **each** equation follows from the other two. Exactly one equation is redundant, and it does not matter which one is dropped.

Two equations are needed: a single equation such as $x_1+x_2=10$ allows two free variables and describes a plane, not the line found above.

---

## Why it works

An equation is redundant when it is a combination of the others. Elimination detects this automatically: subtracting the right multiples of the other rows turns a redundant row into $0=0$.

Counting:

$$
\mathrm{free\ variables}=3\ \mathrm{unknowns}-2\ \mathrm{pivots}=1
$$

Only two pivots appear, so only two equations carry independent information. Geometrically, the three planes share one common line; any two of them already intersect in that line.

---

## Check

Take $t=0$: $(x_1,x_2,x_3)=(2,\ 8,\ 0)$.

- $x_1+x_2=2+8=10$ ✓
- $x_2+x_3=8+0=8$ ✓
- $x_1-x_3=2-0=2$ ✓

General $t$:

- $(2+t)+(8-t)=10$ ✓
- $(8-t)+t=8$ ✓
- $(2+t)-t=2$ ✓

Redundancy check: first equation minus second equation gives $x_1-x_3=10-8=2$, which is exactly the third equation ✓.
