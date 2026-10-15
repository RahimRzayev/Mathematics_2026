# Problem 9. Composing Transformations

## Result

$$
RSx=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix},\qquad
SRx=
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
$$

The two results differ, so the order of the transformations matters.

## Main Steps

**Apply $S$ first, then $R$ (this is $RSx$).**

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
0\cdot 2-1\cdot 2 \\
1\cdot 2+0\cdot 2 \\
\end{pmatrix}=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
$$

**Apply $R$ first, then $S$ (this is $SRx$).**

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

**Comparison.** $(-2,\,2)\neq(-4,\,1)$.

## Explanation

- $S$ doubles the $x$-coordinate and leaves the $y$-coordinate alone. It stretches shapes horizontally.
- $R$ rotates every vector by $90^\circ$ counterclockwise.

When we scale first and rotate second, the stretch happens along the original $x$-axis, and then the whole picture turns. When we rotate first, the vector points in a new direction, and then the stretch acts along the *original* $x$-axis, which now affects a different part of the vector. Because the stretch acts on different directions in the two cases, the final points differ.

In short: **the order of transformations matters, just as the order of matrices matters**. Matrix multiplication is the composition of transformations, and composition is generally not commutative.

## Verification

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

Then $RS\,x=(0\cdot1-1\cdot2,\ 2\cdot1+0\cdot2)=(-2,\,2)$ and $SR\,x=(0\cdot1-2\cdot2,\ 1\cdot1+0\cdot2)=(-4,\,1)$. These agree with the step-by-step results.
