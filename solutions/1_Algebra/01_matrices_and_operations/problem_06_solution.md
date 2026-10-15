# Problem 6. Transpose

## Result

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix},\qquad
B^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
$$

$$
AB=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}
$$

Check: $(AB)^T$ has rows $(2,\,8)$ and $(11,\,23)$, and the next section confirms that $B^TA^T$ has the same entries.

## Main Steps

**Transpose.** The transpose $M^T$ is obtained by turning rows into columns: row $i$ of $M$ becomes column $i$ of $M^T$. An $m\times n$ matrix becomes $n\times m$.

- $A$ is $2\times 3$, so $A^T$ is $3\times 2$. Its first column is the first row of $A$, which is $(1,\,2,\,3)$.
- $B$ is $3\times 2$, so $B^T$ is $2\times 3$. Its first row is the first column of $B$, which is $(1,\,2,\,-1)$.

**Product $AB$.** $A$ is $2\times 3$ and $B$ is $3\times 2$, so $AB$ is $2\times 2$.

- Row 1 of $A$ is $(1,\,2,\,3)$. Column 1 of $B$ is $(1,\,2,\,-1)$: $1+4-3=2$. Column 2 of $B$ is $(0,\,1,\,3)$: $0+2+9=11$.
- Row 2 of $A$ is $(4,\,5,\,6)$. Column 1 of $B$: $4+10-6=8$. Column 2 of $B$: $0+5+18=23$.

**Property check.** Compute $B^TA^T$ and compare with $(AB)^T$.

- $B^T$ has rows $(1,\,2,\,-1)$ and $(0,\,1,\,3)$. $A^T$ has columns $(1,\,2,\,3)^T$ and $(4,\,5,\,6)^T$.
- Row 1 times column 1: $1+4-3=2$. Row 1 times column 2: $4+10-6=8$.
- Row 2 times column 1: $0+2+9=11$. Row 2 times column 2: $0+5+18=23$.

So $B^TA^T$ has rows $(2,\,8)$ and $(11,\,23)$, which is exactly $(AB)^T$.

## Explanation

Transposing reflects the matrix across its main diagonal. The rule $(AB)^T=B^TA^T$ says that when you transpose a product, the order of the factors reverses. This happens because the rows of $AB$ are built from the rows of $A$ and the columns of $B$; after transposing, the roles are swapped and the factors must be placed in reverse order to match.

Remember this rule when you work with transposes: it is the transpose of the product, not the product of the transposes, that reverses the order.

## Verification

The two sides matched entry by entry: $(2,\,8,\,11,\,23)$ on both sides, in the same positions after transposing.
