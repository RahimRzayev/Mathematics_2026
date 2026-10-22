# Problem 14. A System of Equations and the Determinant

## Exercise

### Exercise 14. A System of Equations and the Determinant
Consider the system $Ax=b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

> **Why this exercise:** connects the determinant with uniqueness of solutions and requires distinguishing the exceptional cases.

---

## Answer

| Case | Result |
|---|---|
| $k\neq 2$ | Exactly one solution for every $b$ |
| $k=2$, $b=(1,\ 2)^T$ | Infinitely many solutions |
| $k=2$, $b=(1,\ 0)^T$ | No solution |

---

## Steps

### Step 1. Compute the determinant

$$
\det A=1\cdot 4-2\cdot k=4-2k
$$

### Step 2. Find when it is nonzero

$$
4-2k=0\qquad\Longleftrightarrow\qquad k=2
$$

So for $k\neq 2$: $\det A\neq 0$, $A$ is invertible, and the unique solution is $x=A^{-1}b$ for **every** $b$.

### Step 3. The exceptional case $k=2$

$$
A=
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix}
$$

Row 2 is $2\times$ row 1. The system is

$$
\begin{cases}
x_1+2x_2=b_1, \\
2x_1+4x_2=b_2.
\end{cases}
$$

The left side of equation 2 is exactly twice the left side of equation 1. So everything depends on whether $b_2=2b_1$.

### Step 4. Infinitely many solutions: $b=(1,\ 2)^T$

$$
\begin{cases}
x_1+2x_2=1, \\
2x_1+4x_2=2.
\end{cases}
$$

Equation 2 is just equation 1 times $2$. Only one real condition remains, $x_1+2x_2=1$. Every point of that line is a solution:

$$
x=
\begin{pmatrix}
1-2s \\
s \\
\end{pmatrix},\qquad s\in\mathbb{R}
$$

### Step 5. No solution: $b=(1,\ 0)^T$

$$
\begin{cases}
x_1+2x_2=1, \\
2x_1+4x_2=0.
\end{cases}
$$

Doubling equation 1 gives $2x_1+4x_2=2$. Equation 2 says the same expression equals $0$. Since $2\neq 0$, the equations contradict each other. No solution.

---

## Why it works

For a square system $Ax=b$:

| $\det A$ | What happens |
|---|---|
| $\neq 0$ | Exactly one solution, for every $b$ |
| $=0$ | Either no solution or infinitely many, depending on $b$ |

Geometrically, each equation is a line in the plane.

- $k\neq 2$: the lines have different slopes and cross at exactly one point.
- $k=2$: the lines are parallel. They are either the **same line** (infinitely many solutions) or **separate parallel lines** (no solution).

---

## Check

Infinite case, take $s=0$ and $s=1$: points $(1,\ 0)$ and $(-1,\ 1)$.

$$
A
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix},\qquad A
\begin{pmatrix}
-1 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
-1+2 \\
-2+4 \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

Two different solutions for the same $b$. ✓
