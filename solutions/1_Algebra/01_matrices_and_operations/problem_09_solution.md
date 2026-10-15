# Problem 9. Composing Transformations

## Exercise

### Exercise 9. Composing Transformations
Let

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad R=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}.
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.
For

$$
x=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

> **Why this exercise:** interprets matrix multiplication as composition of transformations.

---

## Answer

| Product | Meaning | Result |
|---|---|---|
| $RSx$ | apply $S$ first, then $R$ | $(-2,\ 2)^T$ |
| $SRx$ | apply $R$ first, then $S$ | $(-4,\ 1)^T$ |

The results differ, so **the order of the transformations matters**.

---

## Steps

### Step 1. $RSx$: apply $S$ first, then $R$

$$
Sx=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}
$$

$$
R(Sx)=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
$$

### Step 2. $SRx$: apply $R$ first, then $S$

$$
Rx=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
$$

$$
S(Rx)=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
$$

### Step 3. Compare

$(-2,\,2)\neq(-4,\,1)$

---

## Why it works

- $S$ doubles the $x$-coordinate and keeps the $y$-coordinate. It stretches shapes horizontally.
- $R$ rotates every vector by $90^\circ$ counterclockwise.

**Scale then rotate:** the stretch acts on the original $x$-axis, then the picture turns.

**Rotate then scale:** the vector first points in a new direction, so the stretch hits a different part of it.

Matrix multiplication is composition of transformations, and composition is generally not commutative.

---

## Check

Multiply the matrices first:

$$
RS=
\begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix},\qquad
SR=
\begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}
$$

Then $RS\,x=(-2,\,2)^T$ and $SR\,x=(-4,\,1)^T$. Both match the step-by-step results. ✓
