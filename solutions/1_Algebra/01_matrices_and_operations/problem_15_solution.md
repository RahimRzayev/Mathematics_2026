# Problem 15. Associativity of Multiplication and Different Calculation Paths

## Result

$$
(AB)C=A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

Both paths give the same matrix, as associativity predicts.

## Main Steps

**Path 1: compute $AB$ first, then $(AB)C$.**

$AB$: rows of $A$ are $(1,\,2,\,0)$ and $(0,\,1,\,1)$. Columns of $B$ are $(1,\,2,\,-1)^T$ and $(0,\,1,\,3)^T$.

- Row 1: $1+4+0=5$ and $0+2+0=2$.
- Row 2: $0+2-1=1$ and $0+1+3=4$.

$$
AB=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}
$$

$(AB)C$: rows of $AB$ are $(5,\,2)$ and $(1,\,4)$. Columns of $C$ are $(2,\,0)^T$ and $(1,\,-1)^T$.

- Row 1: $5\cdot2+2\cdot0=10$ and $5\cdot1+2\cdot(-1)=3$.
- Row 2: $1\cdot2+4\cdot0=2$ and $1\cdot1+4\cdot(-1)=-3$.

$$
(AB)C=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

**Path 2: compute $BC$ first, then $A(BC)$.**

$BC$: rows of $B$ are $(1,\,0)$, $(2,\,1)$, $(-1,\,3)$. Columns of $C$ are $(2,\,0)^T$ and $(1,\,-1)^T$.

- Row 1: $2$ and $1$.
- Row 2: $4$ and $2-1=1$.
- Row 3: $-2$ and $-1-3=-4$.

$$
BC=
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}
$$

$A(BC)$: rows of $A$ are $(1,\,2,\,0)$ and $(0,\,1,\,1)$. Columns of $BC$ are $(2,\,4,\,-2)^T$ and $(1,\,1,\,-4)^T$.

- Row 1: $2+8+0=10$ and $1+2+0=3$.
- Row 2: $0+4-2=2$ and $0+1-4=-3$.

$$
A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

**Comparison.** Both paths give the same $2\times 2$ matrix.

**Number of multiplications.** Count each product of two numbers.

- Path 1: $AB$ is $2\times 2$ with inner size 3, so $4\cdot 3=12$ multiplications. $(AB)C$ is $2\times 2$ with inner size 2, so $4\cdot 2=8$. Total: $20$.
- Path 2: $BC$ is $3\times 2$ with inner size 2, so $6\cdot 2=12$ multiplications. $A(BC)$ is $2\times 2$ with inner size 3, so $4\cdot 3=12$. Total: $24$.

## Explanation

**Associativity** says that $(XY)Z=X(YZ)$. The grouping of the factors does not change the answer, so we may choose whichever grouping is convenient.

In this example, both paths give the same matrix. But they do not cost the same work. Path 1 needs $20$ multiplications and Path 2 needs $24$. When matrices are large, choosing a good grouping can save a lot of time, and this is a real concern in computer calculations.

Note the difference between associativity and commutativity from Problem 4. Associativity lets us *regroup* factors, but it keeps their *order*. Commutativity would let us change the order, and matrix multiplication does not allow that in general.

## Verification

Both paths produced the same matrix entry by entry, so the associativity identity holds for this example.
