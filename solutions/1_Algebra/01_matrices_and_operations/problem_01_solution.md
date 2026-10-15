# Problem 1. Matrix Size and Entries

## Result

- $A$ is a $2\times 3$ matrix, and $B$ is a $3\times 2$ matrix.
- $a_{12}=-1$, $a_{23}=5$, $b_{21}=-2$, $b_{32}=1$.
- Second row of $A$: $(0,\ 4,\ 5)$. First column of $B$: $(1,\ -2,\ 4)^T$.

## Main Steps

**Size.** A matrix is written as $m\times n$, where $m$ is the number of rows and $n$ is the number of columns.

- $A$ has 2 rows and 3 columns, so its size is $2\times 3$.
- $B$ has 3 rows and 2 columns, so its size is $3\times 2$.

**Entries.** The notation $a_{ij}$ means "row $i$, column $j$". Count the row first, then the column.

- $a_{12}$: row 1, column 2 of $A$. Row 1 is $(2,\,-1,\,3)$, so the entry is $-1$.
- $a_{23}$: row 2, column 3 of $A$. Row 2 is $(0,\,4,\,5)$, so the entry is $5$.
- $b_{21}$: row 2, column 1 of $B$. Column 1 is $(1,\,-2,\,4)^T$, so the entry is $-2$.
- $b_{32}$: row 3, column 2 of $B$. Row 3 is $(4,\,1)$, so the entry is $1$.

**Rows and columns as vectors.** A row is read across, and a column is read down.

- Second row of $A$: $(0,\ 4,\ 5)$.
- First column of $B$: $(1,\,-2,\,4)^T$.

## Explanation

The main idea is to keep the order straight: **row first, column second**. A quick check helps. An $m\times n$ matrix has $m$ rows, so the row index $i$ in $a_{ij}$ can never be bigger than $m$, and the column index $j$ can never be bigger than $n$. For example, $a_{23}$ exists in $A$ because $A$ has two rows and three columns, but $a_{32}$ would not exist in $A$.

## Verification

Each entry is checked by counting from the top-left corner: go down to the row, then across to the column. For $b_{32}$, go down to the third row of $B$, which is $(4,\,1)$, and then across to the second entry. This gives $b_{32}=1$. The indices also agree with the sizes: $B$ has 3 rows and 2 columns, so the largest valid index is $b_{32}$.
