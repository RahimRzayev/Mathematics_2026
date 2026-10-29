# Problem 7. Inverse of a Product

## Exercise

### Exercise 7. Inverse of a Product
For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

> **Why this exercise:** reinforces the inverse-of-a-product property and requires its interpretation.

---

## Answer

$$
(AB)^{-1}=B^{-1}A^{-1}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}
$$

The order reverses because the **last** operation applied must be the **first** one undone.

---

## Steps

### Step 1. Compute $AB$

$$
AB=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
$$

### Step 2. Invert $AB$

$$
\det(AB)=2\cdot 3-3\cdot 0=6
$$

$$
(AB)^{-1}=\frac16
\begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}
$$

### Step 3. Invert $A$ and $B$ separately

$\det A=1$, so

$$
A^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
$$

$B$ is diagonal, so invert each diagonal entry:

$$
B^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13 \\
\end{pmatrix}
$$

### Step 4. Compute $B^{-1}A^{-1}$

$$
B^{-1}A^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}
$$

This matches Step 2.

### Step 5. Compare with the wrong order

$$
A^{-1}B^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -\frac13 \\
0 & \frac13 \\
\end{pmatrix}
$$

The top-right entry differs, so $A^{-1}B^{-1}\neq(AB)^{-1}$.

---

## Why it works

Algebraic reason: multiply $AB$ by $B^{-1}A^{-1}$ and regroup.

$$
(AB)(B^{-1}A^{-1})=A(BB^{-1})A^{-1}=AIA^{-1}=AA^{-1}=I
$$

The inner pair $BB^{-1}$ cancels first, then the outer pair $AA^{-1}$. This only works when the inverses come in reversed order.

Meaning: $(AB)x=A(Bx)$, so $B$ acts **first** and $A$ acts **second**. To undo, remove the last action first ($A^{-1}$), then the earlier one ($B^{-1}$):

$$
x=B^{-1}\left(A^{-1}\left(ABx\right)\right)
$$

Everyday version: put on socks, then shoes. To undo, take off shoes first, then socks.

---

## Check

$$
(AB)(B^{-1}A^{-1})=
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}=
\begin{pmatrix}
1 & -1+1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

The product is the identity. ✓
