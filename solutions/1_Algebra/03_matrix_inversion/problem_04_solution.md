# Problem 4. Gauss–Jordan

## Exercise

### Exercise 4. Gauss–Jordan
Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

> **Why this exercise:** introduces the Gauss–Jordan method together with its meaning, not merely as a sequence of operations.

---

## Answer

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Write $[A\mid I]$

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}
$$

Goal: turn the left block into $I$ using row operations. Apply each operation to the whole row.

### Step 2. Clear below the first pivot

Operation: $R_2\to R_2-3R_1$.

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}
$$

### Step 3. Make the second pivot equal to $1$

Operation: $R_2\to -R_2$.

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

### Step 4. Clear above the second pivot

Operation: $R_1\to R_1-2R_2$.

$$
\begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

### Step 5. Read off the inverse

The left block is $I$. The right block is $A^{-1}$:

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}
$$

---

## Why it works

Every row operation equals multiplication on the left by an **elementary matrix**. For example, $R_2\to R_2-3R_1$ is multiplication by

$$
E_1=
\begin{pmatrix}
1 & 0 \\
-3 & 1 \\
\end{pmatrix}
$$

The three operations above form a product $E=E_3E_2E_1$. Applying them to $[A\mid I]$ gives

$$
E\,[A\mid I]=[EA\mid EI]=[EA\mid E]
$$

The left block ended as $I$, so $EA=I$. That means $E$ is exactly $A^{-1}$. The right block started as $I$ and became $EI=E$, so it records the inverse.

In short: the right side keeps a log of every operation, and the operations that turn $A$ into $I$ are, combined, the inverse of $A$.

---

## Check

Compute $AA^{-1}$:

$$
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}=
\begin{pmatrix}
-5+6 & 2-2 \\
-15+15 & 6-5 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

Cross-check with the formula: $\det A=5-6=-1$, so $A^{-1}=-1\cdot$ (swap and negate), which gives the same matrix. ✓
