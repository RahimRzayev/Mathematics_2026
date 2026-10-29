# Problem 11. Parameter and Invertibility

## Exercise

### Exercise 11. Parameter and Invertibility
For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

> **Why this exercise:** combines a parameter, determinant, and an explicit inverse formula in one problem.

---

## Answer

$A(t)$ is invertible for all $t\neq\pm 1$, and then

$$
A(t)^{-1}=\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}
$$

At $t=\pm 1$ the denominator is $0$: the formula is undefined and the matrix has no inverse.

---

## Steps

### Step 1. Compute the determinant

$$
\det A(t)=1\cdot 1-t\cdot t=1-t^2
$$

### Step 2. Find where it vanishes

$$
1-t^2=0 \quad\Longleftrightarrow\quad t^2=1 \quad\Longleftrightarrow\quad t=\pm 1
$$

So $A(t)$ is invertible for every real $t$ except $t=1$ and $t=-1$.

### Step 3. Apply the $2\times 2$ formula

Swap the main diagonal ($1$ and $1$ stay the same), negate the other diagonal, divide by the determinant:

$$
A(t)^{-1}=\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix},\qquad t\neq\pm 1
$$

### Step 4. Excluded values

At $t=1$:

$$
A(1)=
\begin{pmatrix}
1 & 1 \\
1 & 1 \\
\end{pmatrix}
$$

The rows are equal.

At $t=-1$:

$$
A(-1)=
\begin{pmatrix}
1 & -1 \\
-1 & 1 \\
\end{pmatrix}
$$

The second row is $-1$ times the first.

In both cases the rows are dependent, the determinant is $0$, and the factor $\frac{1}{1-t^2}$ divides by zero.

---

## Why it works

The formula is valid exactly where the determinant is nonzero. As $t$ approaches $\pm 1$, the denominator $1-t^2$ approaches $0$, so the entries of $A(t)^{-1}$ grow without bound. For example:

| $t$ | $1-t^2$ | Entry $\frac{1}{1-t^2}$ |
|---|---|---|
| $0.9$ | $0.19$ | $\approx 5.3$ |
| $0.99$ | $0.0199$ | $\approx 50.3$ |
| $0.999$ | $0.001999$ | $\approx 500.3$ |

Geometrically, the two columns of $A(t)$ become closer and closer to parallel. The map squashes the plane more and more, so undoing it needs larger and larger stretching. At $t=\pm 1$ the plane collapses onto a line, and no finite matrix can undo that.

---

## Check

Multiply $A(t)$ by the unscaled matrix:

$$
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1-t^2 & -t+t \\
t-t & -t^2+1 \\
\end{pmatrix}=(1-t^2)
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

Dividing by $1-t^2$ gives $I$. ✓

Sanity check at $t=0$: $A(0)=I$ and the formula gives $A(0)^{-1}=I$. ✓
