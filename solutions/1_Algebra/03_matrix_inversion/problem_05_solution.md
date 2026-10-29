# Problem 5. A 3×3 Matrix

## Exercise

### Exercise 5. A 3×3 Matrix
Use Gauss–Jordan elimination to find the inverse of

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}.
$$

Check the result by multiplication.

> **Why this exercise:** provides necessary practice with the full method in a situation where the $2\times2$ formula no longer applies.

---

## Answer

$$
A^{-1}=\frac12
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Write $[A\mid I]$

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
1 & 0 & 1 & \mid & 0 & 0 & 1 \\
\end{pmatrix}
$$

Plan: clear below the pivots (top to bottom), then clear above them (bottom to top).

### Step 2. Clear column 1

Operation: $R_3\to R_3-R_1$.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & -1 & 1 & \mid & -1 & 0 & 1 \\
\end{pmatrix}
$$

### Step 3. Clear column 2 below the pivot

Operation: $R_3\to R_3+R_2$.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 2 & \mid & -1 & 1 & 1 \\
\end{pmatrix}
$$

### Step 4. Scale the third pivot

Operation: $R_3\to \frac12 R_3$.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 1 & \mid & -\frac12 & \frac12 & \frac12 \\
\end{pmatrix}
$$

### Step 5. Clear column 3 above the pivot

Operation: $R_2\to R_2-R_3$.

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 0 & \mid & \frac12 & \frac12 & -\frac12 \\
0 & 0 & 1 & \mid & -\frac12 & \frac12 & \frac12 \\
\end{pmatrix}
$$

### Step 6. Clear column 2 above the pivot

Operation: $R_1\to R_1-R_2$.

$$
\begin{pmatrix}
1 & 0 & 0 & \mid & \frac12 & -\frac12 & \frac12 \\
0 & 1 & 0 & \mid & \frac12 & \frac12 & -\frac12 \\
0 & 0 & 1 & \mid & -\frac12 & \frac12 & \frac12 \\
\end{pmatrix}
$$

### Step 7. Read off the inverse

The left block is $I$, so the right block is $A^{-1}$. Factor out $\frac12$:

$$
A^{-1}=\frac12
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}
$$

---

## Why it works

The method is the same as for $2\times 2$ matrices. Each row operation is a left multiplication by an elementary matrix. The combined product $E$ turns $A$ into $I$, so $E=A^{-1}$, and the right block (which started as $I$) ends as $E$.

The pivot $2$ in Step 3 is the determinant in disguise. Adding multiples of rows does not change the determinant, so

$$
\det A=1\cdot 1\cdot 2=2
$$

That explains the factor $\frac12$ in the answer.

---

## Check

Compute $A\cdot\left(2A^{-1}\right)$ and expect $2I$:

$$
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1+1 & -1+1 & 1-1 \\
1-1 & 1+1 & -1+1 \\
1-1 & -1+1 & 1+1 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2 \\
\end{pmatrix}
$$

So $AA^{-1}=\frac12\cdot 2I=I$. ✓
