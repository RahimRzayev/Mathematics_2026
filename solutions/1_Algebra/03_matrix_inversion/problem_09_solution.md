# Problem 9. Matrix Equation

## Exercise

### Exercise 9. Matrix Equation
Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

> **Why this exercise:** teaches that order matters in matrix equations and must guide the solution.

---

## Answer

$A^{-1}$ goes on the **left**: $X=A^{-1}B$.

$$
X=
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Decide the side

In $AX=B$, the matrix $A$ stands to the **left** of $X$. To cancel it, $A^{-1}$ must sit directly next to it, also on the left:

$$
A^{-1}(AX)=A^{-1}B \quad\Longrightarrow\quad X=A^{-1}B
$$

Multiplying on the right would give $AXA^{-1}=BA^{-1}$, where $A$ and $A^{-1}$ are separated by $X$ and cannot cancel.

### Step 2. Find $A^{-1}$

$\det A=1\cdot 1-2\cdot 0=1$. Swap the main diagonal, negate the other diagonal:

$$
A^{-1}=
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
$$

### Step 3. Multiply $A^{-1}B$

- Row 1, column 1: $1\cdot 3+(-2)\cdot 2=-1$
- Row 1, column 2: $1\cdot 1+(-2)\cdot 4=-7$
- Row 2, column 1: $0\cdot 3+1\cdot 2=2$
- Row 2, column 2: $0\cdot 1+1\cdot 4=4$

$$
X=A^{-1}B=
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}
$$

---

## Why it works

Matrix multiplication is not commutative, so "dividing by $A$" has two different versions:

| Equation | Solution |
|---|---|
| $AX=B$ | $X=A^{-1}B$ |
| $XA=B$ | $X=BA^{-1}$ |

The inverse always goes on the **same side** where $A$ stands next to $X$.

Using the wrong side gives a different matrix:

$$
BA^{-1}=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
3 & -5 \\
2 & 0 \\
\end{pmatrix}
$$

This solves $XA=B$, not $AX=B$.

---

## Check

Compute $AX$:

$$
AX=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}=
\begin{pmatrix}
-1+4 & -7+8 \\
2 & 4 \\
\end{pmatrix}=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}=B
$$

The product equals $B$. ✓
