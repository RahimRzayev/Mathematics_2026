# Problem 13. Undoing a Composite Transformation

## Exercise

### Exercise 13. Undoing a Composite Transformation
The matrices

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad H=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

> **Why this exercise:** reinforces the inverse of a product in a less direct configuration.

---

## Answer

Both methods give

$$
T^{-1}=S^{-1}H^{-1}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}
$$

The wrong order gives a different matrix:

$$
H^{-1}S^{-1}=
\begin{pmatrix}
\frac12 & -1 \\
0 & 1 \\
\end{pmatrix}\neq T^{-1}
$$

---

## Steps

### Step 1. Method 1: compute $T$

$$
T=HS=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

### Step 2. Method 1: invert $T$

$$
\det T=2\cdot 1-1\cdot 0=2
$$

$$
T^{-1}=\frac12
\begin{pmatrix}
1 & -1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}
$$

### Step 3. Method 2: invert each factor

$S$ is diagonal, so invert the diagonal entries. $H$ shears by $+1$, so its inverse shears by $-1$:

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad H^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
$$

### Step 4. Method 2: multiply in reversed order

$$
S^{-1}H^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}
$$

Same as method 1.

### Step 5. The wrong order

$$
H^{-1}S^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & -1 \\
0 & 1 \\
\end{pmatrix}
$$

The top-right entry is $-1$ instead of $-\frac12$, so $H^{-1}S^{-1}\neq T^{-1}$.

---

## Why it works

Read $T=HS$ as acting on a vector $v$:

$$
Tv=H(Sv)
$$

The matrix nearest to $v$ acts first. So $T$ means: **first** scale by $S$, **then** shear by $H$.

To return to $v$, undo the last operation first:

1. Remove the shear: apply $H^{-1}$.
2. Remove the scaling: apply $S^{-1}$.

$$
S^{-1}\left(H^{-1}(Tv)\right)=S^{-1}\left(H^{-1}H\,Sv\right)=S^{-1}Sv=v
$$

Written as one matrix, "apply $H^{-1}$, then $S^{-1}$" is $S^{-1}H^{-1}$, because the first operation is written closest to $v$, on the right.

The wrong order $H^{-1}S^{-1}$ tries to undo the scaling while the shear is still in place. The shear has already mixed the coordinates, so the scaling cannot be removed cleanly.

---

## Check

**Correct order:**

$$
T\,(S^{-1}H^{-1})=
\begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
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

**Wrong order:**

$$
T\,(H^{-1}S^{-1})=
\begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & -1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & -2+1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
$$

The correct order gives $I$. The wrong order leaves a leftover shear. ✓
