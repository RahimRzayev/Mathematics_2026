# Problem 12. Finding Inverses Without Starting from Scratch

## Exercise

### Exercise 12. Finding Inverses Without Starting from Scratch
It is known that

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

> **Why this exercise:** teaches how to use inverse properties instead of carrying out unnecessary full calculations.

---

## Answer

| Matrix | Property | Result |
|---|---|---|
| $(3A)^{-1}$ | $(kA)^{-1}=\frac1k A^{-1}$ | $\frac13 A^{-1}$ |
| $(A^T)^{-1}$ | $(A^T)^{-1}=(A^{-1})^T$ | transpose of $A^{-1}$ |
| $(A^2)^{-1}$ | $(A^2)^{-1}=(A^{-1})^2$ | square of $A^{-1}$ |

$$
(3A)^{-1}=
\begin{pmatrix}
\frac23 & -\frac13 \\
-1 & \frac23 \\
\end{pmatrix},\qquad (A^T)^{-1}=
\begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix},\qquad (A^2)^{-1}=
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. $(3A)^{-1}$

Property: for a nonzero number $k$,

$$
(kA)^{-1}=\frac1k A^{-1}
$$

Reason: $(kA)\left(\frac1k A^{-1}\right)=\left(k\cdot\frac1k\right)AA^{-1}=I$.

With $k=3$:

$$
(3A)^{-1}=\frac13
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
\frac23 & -\frac13 \\
-1 & \frac23 \\
\end{pmatrix}
$$

### Step 2. $(A^T)^{-1}$

Property:

$$
(A^T)^{-1}=(A^{-1})^T
$$

Reason: $(AB)^T=B^TA^T$, so $A^T(A^{-1})^T=(A^{-1}A)^T=I^T=I$.

Transpose $A^{-1}$ (rows become columns):

$$
(A^T)^{-1}=
\begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}
$$

### Step 3. $(A^2)^{-1}$

Property: inverse of a product with reversed order, here with both factors equal to $A$:

$$
(A^2)^{-1}=(AA)^{-1}=A^{-1}A^{-1}=(A^{-1})^2
$$

Square $A^{-1}$:

- Row 1, column 1: $2\cdot 2+(-1)\cdot(-3)=4+3=7$
- Row 1, column 2: $2\cdot(-1)+(-1)\cdot 2=-2-2=-4$
- Row 2, column 1: $(-3)\cdot 2+2\cdot(-3)=-6-6=-12$
- Row 2, column 2: $(-3)\cdot(-1)+2\cdot 2=3+4=7$

$$
(A^2)^{-1}=
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}
$$

---

## Why it works

Each property comes from the definition $MM^{-1}=I$: propose a candidate, multiply, and show the product collapses to $I$.

- Scalars commute with matrices, so $k$ and $\frac1k$ cancel on their own.
- Transposing reverses products, so the transpose of $A^{-1}A=I$ gives $A^T(A^{-1})^T=I$.
- A power is a product, and products invert in reversed order. With equal factors the order does not change anything.

None of the three answers needed $A$ itself.

---

## Check

For checking only, recover $A=(A^{-1})^{-1}$. Since $\det A^{-1}=4-3=1$,

$$
A=
\begin{pmatrix}
2 & 1 \\
3 & 2 \\
\end{pmatrix}
$$

**$(3A)^{-1}$:**

$$
\begin{pmatrix}
6 & 3 \\
9 & 6 \\
\end{pmatrix}
\begin{pmatrix}
\frac23 & -\frac13 \\
-1 & \frac23 \\
\end{pmatrix}=
\begin{pmatrix}
4-3 & -2+2 \\
6-6 & -3+4 \\
\end{pmatrix}=I
$$

**$(A^T)^{-1}$:**

$$
\begin{pmatrix}
2 & 3 \\
1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
4-3 & -6+6 \\
2-2 & -3+4 \\
\end{pmatrix}=I
$$

**$(A^2)^{-1}$:** first $A^2$:

$$
A^2=
\begin{pmatrix}
2 & 1 \\
3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
3 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
7 & 4 \\
12 & 7 \\
\end{pmatrix}
$$

$$
\begin{pmatrix}
7 & 4 \\
12 & 7 \\
\end{pmatrix}
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}=
\begin{pmatrix}
49-48 & -28+28 \\
84-84 & -48+49 \\
\end{pmatrix}=I
$$

All three products are the identity. ✓
