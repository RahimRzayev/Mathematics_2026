# Problem 6. Solving a System Using the Inverse

## Exercise

### Exercise 6. Solving a System Using the Inverse
Solve

$$
Ax=b,
$$

where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix},
$$

using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

> **Why this exercise:** shows the connection between inverse matrices and solving a linear system.

---

## Answer

$$
x=
\begin{pmatrix}
\frac85 \\
\frac95 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Find $A^{-1}$

$$
\det A=2\cdot 3-1\cdot 1=5
$$

Swap the main diagonal, negate the other diagonal, divide by $5$:

$$
A^{-1}=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

### Step 2. Multiply $A^{-1}b$

$$
x=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix}=\frac15
\begin{pmatrix}
15-7 \\
-5+14 \\
\end{pmatrix}=\frac15
\begin{pmatrix}
8 \\
9 \\
\end{pmatrix}
$$

So $x_1=\frac85$ and $x_2=\frac95$.

---

## Why it works

Start from $Ax=b$ and multiply both sides **on the left** by $A^{-1}$:

$$
A^{-1}(Ax)=A^{-1}b
$$

By associativity, $A^{-1}(Ax)=(A^{-1}A)x=Ix=x$. So

$$
x=A^{-1}b
$$

The left side matters: $x$ is to the right of $A$, so $A^{-1}$ must go on the left to meet $A$ directly. The solution is also **unique**, because $A^{-1}b$ is one specific vector.

---

## Check

Substitute into the original system, written as equations:

$$
\begin{cases}
2x_1+x_2=5, \\
x_1+3x_2=7.
\end{cases}
$$

- First equation: $2\cdot\frac85+\frac95=\frac{16+9}{5}=\frac{25}{5}=5$
- Second equation: $\frac85+3\cdot\frac95=\frac{8+27}{5}=\frac{35}{5}=7$

Both equations hold. ✓
