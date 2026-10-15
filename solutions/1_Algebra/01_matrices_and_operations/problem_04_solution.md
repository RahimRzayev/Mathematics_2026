# Problem 4. Matrix Multiplication and Noncommutativity

## Result

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
$$

$$
BA=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
$$

Since $AB\neq BA$, multiplication of these matrices is **not commutative**.

## Main Steps

**Rule.** Entry $(i,j)$ of a product is row $i$ of the first matrix times column $j$ of the second matrix: multiply matching positions and add.

**Computing $AB$.** Rows of $A$ are $(1,\,2)$ and $(0,\,1)$. Columns of $B$ are $(2,\,3)^T$ and $(0,\,1)^T$.

- Row 1, column 1: $1\cdot 2+2\cdot 3=8$.
- Row 1, column 2: $1\cdot 0+2\cdot 1=2$.
- Row 2, column 1: $0\cdot 2+1\cdot 3=3$.
- Row 2, column 2: $0\cdot 0+1\cdot 1=1$.

**Computing $BA$.** Rows of $B$ are $(2,\,0)$ and $(3,\,1)$. Columns of $A$ are $(1,\,0)^T$ and $(2,\,1)^T$.

- Row 1, column 1: $2\cdot 1+0\cdot 0=2$.
- Row 1, column 2: $2\cdot 2+0\cdot 1=4$.
- Row 2, column 1: $3\cdot 1+1\cdot 0=3$.
- Row 2, column 2: $3\cdot 2+1\cdot 1=7$.

**Comparison.** The entries in position $(1,1)$ are $8$ and $2$, which already differ. So $AB\neq BA$.

## Explanation

For ordinary numbers, $ab=ba$ always holds. For matrices it does not, because the rows of the first matrix are combined with the columns of the second matrix. Swapping the order swaps which rows and columns meet, and the result changes.

This is an important warning when you work with matrices: you cannot freely rearrange factors as you do with numbers. Always keep the order of multiplication.

## Verification

Check the trace-like sum of the diagonal entries as a quick sanity test. The diagonal of $AB$ sums to $8+1=9$, and the diagonal of $BA$ sums to $2+7=9$. The sums agree, but the matrices themselves are different. This shows that equal traces do not imply equal products, so the comparison must be made entry by entry.
