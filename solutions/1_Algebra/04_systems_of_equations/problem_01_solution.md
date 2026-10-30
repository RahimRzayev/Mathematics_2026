# Problem 1. From a System to a Matrix

## Exercise

### Exercise 1. From a System to a Matrix
Write the system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
$$

in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

> **Why this exercise:** teaches how to move between a system of equations and matrix notation.

---

## Answer

$$
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}=
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

- Coefficient matrix: the $3\times3$ matrix $A$ on the left.
- Vector of unknowns: $x=(x,y,z)^T$.
- Right-hand side vector: $b=(4,1,7)^T$.

Row $i$ of $A$ holds the coefficients of equation $i$; entry $i$ of $b$ holds its right-hand side.

---

## Steps

### Step 1. Fix the order of the unknowns

Use the order $x,\ y,\ z$ in every equation. Each column of $A$ then belongs to one unknown:

- column 1: coefficients of $x$,
- column 2: coefficients of $y$,
- column 3: coefficients of $z$.

### Step 2. Read the coefficients row by row

Write every coefficient explicitly, including signs and hidden $1$'s:

| Equation | $x$ | $y$ | $z$ | Right-hand side |
|---|---|---|---|---|
| $2x-y+z=4$ | $2$ | $-1$ | $1$ | $4$ |
| $x+3y-2z=1$ | $1$ | $3$ | $-2$ | $1$ |
| $3x+y+z=7$ | $3$ | $1$ | $1$ | $7$ |

### Step 3. Assemble $A$, $x$, $b$

$$
A=
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

### Step 4. Augmented matrix

For elimination, the same data is stored as $[A\mid b]$:

$$
\begin{pmatrix}
2 & -1 & 1 & \mid & 4 \\
1 & 3 & -2 & \mid & 1 \\
3 & 1 & 1 & \mid & 7 \\
\end{pmatrix}
$$

---

## Why it works

The product $Ax$ is computed row by row: entry $i$ of $Ax$ is row $i$ of $A$ times the column $x$. For row 1:

$$
(2,\ -1,\ 1)\cdot(x,\ y,\ z)=2x-y+z
$$

This is exactly the left-hand side of equation 1. So the single matrix equation $Ax=b$ states that entry $i$ of $Ax$ equals entry $i$ of $b$ for every $i$, which is the whole system.

Consequences:

- number of rows of $A$ = number of equations,
- number of columns of $A$ = number of unknowns,
- a missing unknown in an equation gives a $0$ in that position.

---

## Check

Multiply $A$ by $x$ and compare with the original equations:

$$
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}=
\begin{pmatrix}
2x-y+z \\
x+3y-2z \\
3x+y+z \\
\end{pmatrix}
$$

Setting this equal to $(4,1,7)^T$ gives back the three original equations. ✓
