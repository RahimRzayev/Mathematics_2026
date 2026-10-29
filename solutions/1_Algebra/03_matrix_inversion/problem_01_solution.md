# Problem 1. Definition of the Inverse

## Exercise

### Exercise 1. Definition of the Inverse
For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

> **Why this exercise:** starts from the definition of the inverse through multiplication before any formulas or computational methods are introduced.

---

## Answer

| Product | Result |
|---|---|
| $AB$ | $I$ |
| $BA$ | $I$ |

Both products equal the identity, so **yes**, $B=A^{-1}$.

---

## Steps

### Step 1. Recall the definition

A matrix $B$ is the inverse of a square matrix $A$ when

$$
AB=I \quad\mathrm{and}\quad BA=I
$$

No formula is needed: multiply and look at the result.

### Step 2. Compute $AB$

Each entry is (row of $A$) times (column of $B$):

- Row 1, column 1: $2\cdot 1+1\cdot(-1)=1$
- Row 1, column 2: $2\cdot(-1)+1\cdot 2=0$
- Row 2, column 1: $1\cdot 1+1\cdot(-1)=0$
- Row 2, column 2: $1\cdot(-1)+1\cdot 2=1$

$$
AB=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=I
$$

### Step 3. Compute $BA$

- Row 1, column 1: $1\cdot 2+(-1)\cdot 1=1$
- Row 1, column 2: $1\cdot 1+(-1)\cdot 1=0$
- Row 2, column 1: $(-1)\cdot 2+2\cdot 1=0$
- Row 2, column 2: $(-1)\cdot 1+2\cdot 1=1$

$$
BA=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=I
$$

### Step 4. Conclude

Both conditions of the definition hold, so $B=A^{-1}$ (and also $A=B^{-1}$).

---

## Why it works

The identity matrix $I$ plays the role of the number $1$: $IM=MI=M$ for every matrix $M$ of matching size.

For numbers, $a^{-1}$ is the number with $a\cdot a^{-1}=1$. For matrices, $A^{-1}$ is the matrix with $AA^{-1}=A^{-1}A=I$.

Matrix multiplication is not commutative in general, so the definition asks for **both** orders. For square matrices it is a theorem that one order already forces the other, but checking both here confirms it directly.

---

## Check

Compare with the $2\times 2$ formula. Here $\det A=2\cdot 1-1\cdot 1=1$, so

$$
A^{-1}=\frac{1}{1}
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}=B
$$

The formula gives the same matrix. ✓
