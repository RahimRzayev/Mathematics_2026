# Problem 7. Identity Matrix, Zero Matrix, and Powers

## Result

For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

we have

$$
AI = IA = A,\qquad A+0 = A
$$

$$
A^2=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix},\qquad
A^3=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

## Main Steps

**Identity matrix.** $I$ is the matrix with 1 on the diagonal and 0 elsewhere:

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

- $AI$: each row of $A$ times the columns of $I$ returns the same row, so $AI=A$.
- $IA$: each column of $A$ is picked out unchanged, so $IA=A$.

**Zero matrix.** $0$ has all entries equal to 0. Adding it changes nothing: $A+0=A$.

**Square.** $A^2=A\cdot A$.

- Row 1 $(2,\,1)$ with columns $(2,\,0)^T$ and $(1,\,2)^T$: $2\cdot 2+1\cdot 0=4$ and $2\cdot 1+1\cdot 2=4$.
- Row 2 $(0,\,2)$ with the same columns: $0\cdot 2+2\cdot 0=0$ and $0\cdot 1+2\cdot 2=4$.

**Cube.** $A^3=A^2\cdot A$.

- Row 1 $(4,\,4)$ with columns $(2,\,0)^T$ and $(1,\,2)^T$: $8$ and $4+8=12$.
- Row 2 $(0,\,4)$: $0$ and $8$.

## Explanation

$I$ is the **neutral element** for multiplication, just as $1$ is for numbers. $0$ is the neutral element for addition, just as $0$ is for numbers.

The pattern in the powers comes from writing $A$ as a sum of two matrices:

$$
A = 2I + N,\qquad N=
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}
$$

Here $N^2=0$. Then the powers of $A$ follow the pattern

$$
A^n=
\begin{pmatrix}
2^n & n\,2^{n-1} \\
0 & 2^n \\
\end{pmatrix}
$$

This matches what we computed: for $n=2$ we get the matrix with rows $(4,\,4)$ and $(0,\,4)$, and for $n=3$ we get rows $(8,\,12)$ and $(0,\,8)$. The diagonal entries double each time, and the top-right entry grows in a predictable way.

## Verification

The formula for $A^n$ gives the same values for $n=2$ and $n=3$ as the direct multiplication above.
