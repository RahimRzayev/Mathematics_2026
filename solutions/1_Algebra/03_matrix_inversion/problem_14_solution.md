# Problem 14. A Matrix That Is Its Own Inverse

## Exercise

### Exercise 14. A Matrix That Is Its Own Inverse
Assume that a square matrix $A$ satisfies

$$
A^2=I.
$$

Show that

$$
A^{-1}=A.
$$

Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

> **Why this exercise:** requires using the definition of the inverse in a short argument and constructing an example independently, without introducing a new topic.

---

## Answer

- Proof: $A\cdot A=I$ in both orders, so $A$ fits the definition of $A^{-1}$.
- Example (swap of coordinates):

$$
A=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix},\qquad A^2=I
$$

---

## Steps

### Step 1. Recall the definition

$B=A^{-1}$ means

$$
AB=I \quad\mathrm{and}\quad BA=I
$$

### Step 2. Test the candidate $B=A$

Both conditions become the same statement:

$$
AB=AA=A^2=I,\qquad BA=AA=A^2=I
$$

Both hold by assumption.

### Step 3. Conclude

$A$ satisfies the definition of the inverse of $A$. The inverse is unique, so

$$
A^{-1}=A
$$

### Step 4. Choose an example

Take the matrix that swaps the two coordinates:

$$
A=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix},\qquad A
\begin{pmatrix}
x \\
y \\
\end{pmatrix}=
\begin{pmatrix}
y \\
x \\
\end{pmatrix}
$$

It is neither $I$ nor $-I$.

---

## Why it works

**Uniqueness of the inverse.** If $B$ and $C$ are both inverses of $A$, then

$$
B=BI=B(AC)=(BA)C=IC=C
$$

So once one inverse is found, it is the inverse. Here that inverse is $A$ itself.

**Geometry of the example.** The swap reflects the plane in the line $y=x$. Reflecting twice returns every point to where it started, so the map undoes itself. Matrices with $A^2=I$ are exactly the transformations that undo themselves (called involutions).

Other examples of the same kind:

$$
\begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix},\qquad
\begin{pmatrix}
-1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

These are reflections in the $x$-axis and the $y$-axis.

---

## Check

$$
A^2=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
0\cdot 0+1\cdot 1 & 0\cdot 1+1\cdot 0 \\
1\cdot 0+0\cdot 1 & 1\cdot 1+0\cdot 0 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

Cross-check with the $2\times 2$ formula: $\det A=0-1=-1$, so

$$
A^{-1}=\frac{1}{-1}
\begin{pmatrix}
0 & -1 \\
-1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}=A
$$

Both computations agree. ✓
