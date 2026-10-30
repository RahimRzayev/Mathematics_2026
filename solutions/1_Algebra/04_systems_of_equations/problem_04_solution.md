# Problem 4. Infinitely Many Solutions

## Exercise

### Exercise 4. Infinitely Many Solutions
Solve

$$
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

> **Why this exercise:** shows the case of multiple solutions and teaches a simple parametric description.

---

## Answer

Infinitely many solutions. Free variable: $z=t$, $t\in\mathbb{R}$.

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}=
\begin{pmatrix}
1-t \\
1 \\
t \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}+t
\begin{pmatrix}
-1 \\
0 \\
1 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Write the augmented matrix

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
2 & 2 & 2 & \mid & 4 \\
1 & -1 & 1 & \mid & 0 \\
\end{pmatrix}
$$

### Step 2. Clear column 1

Operations: $R_2\to R_2-2R_1$ and $R_3\to R_3-R_1$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 0 & 0 & \mid & 0 \\
0 & -2 & 0 & \mid & -2 \\
\end{pmatrix}
$$

Row 2 became $0=0$: the second equation is twice the first and carries no new information.

### Step 3. Reorder to row echelon form

Operation: $R_2\leftrightarrow R_3$.

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & -2 & 0 & \mid & -2 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

Pivots are in columns 1 and 2. Column 3 has no pivot, so $z$ is free.

### Step 4. Back substitution with $z=t$

From row 2:

$$
-2y=-2 \quad\Longrightarrow\quad y=1
$$

From row 1:

$$
x+1+t=2 \quad\Longrightarrow\quad x=1-t
$$

---

## Why it works

There are three unknowns but only two pivots. Each pivot fixes one unknown in terms of the others; the remaining unknown can take any value. No row has the form $0=c$ with $c\neq0$, so the system is consistent.

Hence:

$$
\mathrm{number\ of\ free\ variables}=3-2=1
$$

Geometrically, the solution set is a line in space through $(1,1,0)$ with direction $(-1,0,1)$.

---

## Check

Choose $t=2$. Then $(x,y,z)=(-1,\ 1,\ 2)$:

- $x+y+z=-1+1+2=2$ ✓
- $2x+2y+2z=-2+2+4=4$ ✓
- $x-y+z=-1-1+2=0$ ✓

General check for arbitrary $t$:

- $(1-t)+1+t=2$ ✓
- $2(1-t)+2+2t=4$ ✓
- $(1-t)-1+t=0$ ✓

Every value of $t$ gives a solution.
