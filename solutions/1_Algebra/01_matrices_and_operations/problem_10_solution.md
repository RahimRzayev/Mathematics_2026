# Problem 10. Columns of a Matrix Product

## Result

$$
Ab_1=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix},\qquad
Ab_2=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

$$
AB=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}
$$

The first column of $AB$ is $Ab_1$, and the second column of $AB$ is $Ab_2$.

## Main Steps

**Columns of $B$.** Since

$$
B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

the columns are

$$
b_1=
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix},\qquad
b_2=
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
$$

**Computing $Ab_1$.** Rows of $A$ are $(1,\,2,\,0)$ and $(0,\,1,\,1)$.

- Row 1 times $b_1$: $1\cdot1+2\cdot(-1)+0\cdot3=1-2=-1$.
- Row 2 times $b_1$: $0\cdot1+1\cdot(-1)+1\cdot3=-1+3=2$.

**Computing $Ab_2$.**

- Row 1 times $b_2$: $1\cdot2+2\cdot0+0\cdot1=2$.
- Row 2 times $b_2$: $0\cdot2+1\cdot0+1\cdot1=1$.

**Computing $AB$ directly.** Rows of $A$ times columns of $B$ give the same four numbers:

- Row 1 with column 1 of $B$: $-1$. Row 1 with column 2 of $B$: $2$.
- Row 2 with column 1 of $B$: $2$. Row 2 with column 2 of $B$: $1$.

**Comparison.** Column 1 of $AB$ is $(-1,\,2)^T=Ab_1$, and column 2 of $AB$ is $(2,\,1)^T=Ab_2$.

## Explanation

Each column of $AB$ is obtained by multiplying the matrix $A$ by the matching column of $B$. In the product $AB$, the entries of column $j$ come from computing row $i$ of $A$ times column $j$ of $B$ for each $i$. That is exactly the calculation of $A$ times $b_j$.

So a matrix product can be read column by column: **$AB$ is $A$ applied to each column of $B$**. This view is handy when $B$ has many columns, because you can process each one separately.

## Verification

The columns of $AB$ we computed directly, $(-1,\,2)^T$ and $(2,\,1)^T$, are exactly $Ab_1$ and $Ab_2$. This confirms the claim.
