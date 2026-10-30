# Problem 10. A Polynomial Through Three Points

## Exercise

### Exercise 10. A Polynomial Through Three Points
Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

> **Why this exercise:** shows that finding unknown coefficients can be reduced to solving a linear system.

---

## Answer

$$
p(x)=2x^2+1
$$

That is, $a=2$, $b=0$, $c=1$.

---

## Steps

### Step 1. One equation per point

A point $(x_0,y_0)$ lies on the graph when $p(x_0)=y_0$. The unknowns are the coefficients $a,b,c$; the values $x_0$ are known numbers.

- $(0,1)$: $a\cdot0^2+b\cdot0+c=1$
- $(1,3)$: $a\cdot1^2+b\cdot1+c=3$
- $(2,9)$: $a\cdot2^2+b\cdot2+c=9$

### Step 2. Write the linear system

$$
\begin{cases}
c=1, \\
a+b+c=3, \\
4a+2b+c=9.
\end{cases}
$$

The system is linear in $a,b,c$, even though $p$ is quadratic in $x$.

### Step 3. Augmented matrix (order $a,b,c$)

$$
\begin{pmatrix}
0 & 0 & 1 & \mid & 1 \\
1 & 1 & 1 & \mid & 3 \\
4 & 2 & 1 & \mid & 9 \\
\end{pmatrix}
$$

Operation: $R_1\leftrightarrow R_2$ to get a nonzero pivot in column 1.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
0 & 0 & 1 & \mid & 1 \\
4 & 2 & 1 & \mid & 9 \\
\end{pmatrix}
$$

### Step 4. Clear column 1

Operation: $R_3\to R_3-4R_1$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
0 & 0 & 1 & \mid & 1 \\
0 & -2 & -3 & \mid & -3 \\
\end{pmatrix}
$$

Operation: $R_2\leftrightarrow R_3$ to reach row echelon form.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
0 & -2 & -3 & \mid & -3 \\
0 & 0 & 1 & \mid & 1 \\
\end{pmatrix}
$$

### Step 5. Back substitution

From row 3:

$$
c=1
$$

From row 2:

$$
-2b-3=-3 \quad\Longrightarrow\quad b=0
$$

From row 1:

$$
a+0+1=3 \quad\Longrightarrow\quad a=2
$$

---

## Why it works

The condition $p(x_0)=y_0$ is linear in the coefficients: $a$, $b$, $c$ appear only to the first power, multiplied by known numbers $x_0^2$, $x_0$, $1$. Three points give three linear equations in three unknowns.

The coefficient matrix

$$
\begin{pmatrix}
0 & 0 & 1 \\
1 & 1 & 1 \\
4 & 2 & 1 \\
\end{pmatrix}
$$

has three pivots after elimination, so the solution is unique. This matches the general fact that three points with distinct $x$-coordinates determine exactly one polynomial of degree at most $2$.

---

## Check

Substitute all three points into $p(x)=2x^2+1$:

- $p(0)=0+1=1$ ✓
- $p(1)=2+1=3$ ✓
- $p(2)=8+1=9$ ✓
