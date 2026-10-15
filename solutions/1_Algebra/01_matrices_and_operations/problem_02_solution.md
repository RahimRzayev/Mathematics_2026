# Problem 2. Addition and Scalar Multiplication

## Result

$$
A+B=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}
$$

$$
A-B=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}
$$

$$
3A-2B=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}
$$

## Main Steps

**Addition and subtraction.** Add or subtract the entries in the same position.

- Top-left: $1+4=5$, and $1-4=-3$.
- Top-right: $2+(-2)=0$, and $2-(-2)=4$.
- Bottom-left: $-1+0=-1$, and $-1-0=-1$.
- Bottom-right: $3+5=8$, and $3-5=-2$.

**Scalar multiplication.** Multiply every entry by the number.

$$
3A=
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix},\qquad
2B=
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}
$$

**Combining.** Subtract $2B$ from $3A$, entry by entry.

- Top-left: $3-8=-5$.
- Top-right: $6-(-4)=10$.
- Bottom-left: $-3-0=-3$.
- Bottom-right: $9-10=-1$.

## Explanation

Matrix addition works like adding numbers, but position by position. Each entry of $A+B$ is the sum of the entries in the same place of $A$ and $B$. That is why the matrices must have **the same size**: if one matrix has an entry in a position where the other has none, there is nothing to add.

Scalar multiplication is even simpler: the number multiplies each entry separately. The expression $3A-2B$ is just two scalar multiplications followed by one subtraction.

## Verification

Check one entry of $3A-2B$ in a different way. Its bottom-right entry comes from $3\cdot 3-2\cdot 5=9-10=-1$. This matches the value found above.
