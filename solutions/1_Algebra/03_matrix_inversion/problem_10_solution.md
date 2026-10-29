# Problem 10. Inverse of a Diagonal Matrix

## Exercise

### Exercise 10. Inverse of a Diagonal Matrix
Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

> **Why this exercise:** teaches how to recognize invertibility and the inverse without using a full procedure when the matrix structure gives the answer immediately.

---

## Answer

| Matrix | Diagonal entries | Determinant | Invertible? |
|---|---|---|---|
| $D$ | $2,\ -3,\ 5$ | $-30$ | Yes |
| $E$ | $2,\ 0,\ 5$ | $0$ | No |

$$
D^{-1}=
\begin{pmatrix}
\frac12 & 0 & 0 \\
0 & -\frac13 & 0 \\
0 & 0 & \frac15 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Rule for diagonal matrices

A diagonal matrix is invertible **exactly when** every diagonal entry is nonzero. Its inverse is the diagonal matrix of reciprocals.

### Step 2. Test $D$

Diagonal entries $2,\ -3,\ 5$ are all nonzero. The determinant of a diagonal matrix is the product of the diagonal:

$$
\det D=2\cdot(-3)\cdot 5=-30\neq 0
$$

So $D$ is invertible.

### Step 3. Test $E$

The middle diagonal entry is $0$:

$$
\det E=2\cdot 0\cdot 5=0
$$

So $E$ is not invertible.

### Step 4. Write $D^{-1}$

Take the reciprocal of each diagonal entry. Keep the sign of $-3$:

$$
D^{-1}=
\begin{pmatrix}
\frac12 & 0 & 0 \\
0 & -\frac13 & 0 \\
0 & 0 & \frac15 \\
\end{pmatrix}
$$

---

## Why it works

A diagonal matrix scales each coordinate axis separately:

$$
D
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}=
\begin{pmatrix}
2x \\
-3y \\
5z \\
\end{pmatrix}
$$

Each scaling is undone by dividing by the same factor, which gives the reciprocals.

For $E$, the second coordinate is multiplied by $0$:

$$
E
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}=
\begin{pmatrix}
2x \\
0 \\
5z \\
\end{pmatrix}
$$

The value of $y$ is erased. For instance $E(0,\ 1,\ 0)=E(0,\ 0,\ 0)=0$. Information that is erased cannot be recovered, so no inverse exists. Algebraically, $\frac10$ is undefined.

---

## Check

Product of diagonal matrices: multiply the diagonals entry by entry.

$$
DD^{-1}=
\begin{pmatrix}
2\cdot\frac12 & 0 & 0 \\
0 & (-3)\cdot\left(-\frac13\right) & 0 \\
0 & 0 & 5\cdot\frac15 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

The product is the identity. ✓
