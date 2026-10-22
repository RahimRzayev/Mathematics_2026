# Problem 15. Combining Determinant Properties

## Exercise

### Exercise 15. Combining Determinant Properties
Let $A$ and $B$ be invertible $2\times2$ matrices with

$$
\det A=-2,\qquad \det B=3.
$$

Without finding the entries of the matrices, compute

$$
\det\left(B^{-1}A^TB\right).
$$

State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

> **Why this exercise:** tests the transfer of several known properties into one short problem instead of checking a single property again with numbers.

---

## Answer

$$
\det\left(B^{-1}A^TB\right)=-2
$$

The result equals $\det A$. The $B$ factors cancel because $\det(B^{-1})\cdot\det B=1$.

---

## Steps

### Step 1. Split the product (product rule)

Property: $\det(XYZ)=\det X\cdot\det Y\cdot\det Z$.

$$
\det\left(B^{-1}A^TB\right)=\det(B^{-1})\cdot\det(A^T)\cdot\det B
$$

### Step 2. Handle the inverse (inverse rule)

Property: $\det(B^{-1})=\dfrac{1}{\det B}$. Valid because $B$ is invertible.

$$
\det(B^{-1})=\frac{1}{3}
$$

### Step 3. Handle the transpose (transpose rule)

Property: $\det(A^T)=\det A$.

$$
\det(A^T)=-2
$$

### Step 4. Multiply

$$
\det\left(B^{-1}A^TB\right)=\frac{1}{3}\cdot(-2)\cdot 3=-2
$$

---

## Why it works

After Step 1, everything is a product of **ordinary numbers**. Numbers can be reordered freely:

$$
\det(B^{-1})\cdot\det(A^T)\cdot\det B=\underbrace{\det(B^{-1})\cdot\det B}_{=\,1}\cdot\det(A^T)
$$

So the $B$ factors cancel completely. The value of $\det B$ does not matter at all: any invertible $B$ gives the same answer.

| Order | Property | Result |
|---|---|---|
| 1 | $\det(XY)=\det X\cdot\det Y$ | Split into three numbers |
| 2 | $\det(B^{-1})=1/\det B$ | $1/3$ |
| 3 | $\det(A^T)=\det A$ | $-2$ |
| 4 | Numbers commute | $B$ factors cancel |

General lesson: a **similarity** $B^{-1}MB$ never changes the determinant of $M$. Here $M=A^T$.

The matrix $B^{-1}A^TB$ itself is usually **not** equal to $A^T$. Only its determinant is the same.

---

## Check

Take simple diagonal matrices with the required determinants:

$$
A=
\begin{pmatrix}
-2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

Diagonal matrices commute and $A^T=A$, so $B^{-1}A^TB=A$, and $\det A=-2$. ✓
