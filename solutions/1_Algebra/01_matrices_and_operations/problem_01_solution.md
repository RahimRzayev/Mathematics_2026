# Problem 1. Matrix Size and Entries

## Exercise

### Exercise 1. Matrix Size and Entries
Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

> **Why this exercise:** builds basic fluency with matrix notation, indices, rows, and columns.

---

## Answer

| Question | Result |
|---|---|
| Size of $A$ | $2\times 3$ (2 rows, 3 columns) |
| Size of $B$ | $3\times 2$ (3 rows, 2 columns) |
| $a_{12}$ and $a_{23}$ | $-1$ and $5$ |
| $b_{21}$ and $b_{32}$ | $-2$ and $1$ |
| Row 2 of $A$ | $(0,\ 4,\ 5)$ |
| Column 1 of $B$ | $(1,\,-2,\,4)^T$ |

---

## Steps

### Step 1. Count the size

Size is always **rows × columns**, written $m\times n$.

- $A$: 2 rows, 3 columns, so $2\times 3$.
- $B$: 3 rows, 2 columns, so $3\times 2$.

### Step 2. Find each entry

Rule: $a_{ij}$ means **row $i$, column $j$**. Row first, column second.

| Entry | Row | Column | Value |
|---|---|---|---|
| $a_{12}$ | row 1: $(2,\,-1,\,3)$ | column 2 | $-1$ |
| $a_{23}$ | row 2: $(0,\,4,\,5)$ | column 3 | $5$ |
| $b_{21}$ | row 2: $(-2,\,3)$ | column 1 | $-2$ |
| $b_{32}$ | row 3: $(4,\,1)$ | column 2 | $1$ |

### Step 3. Read rows and columns as vectors

- Row 2 of $A$, read across: $(0,\ 4,\ 5)$.
- Column 1 of $B$, read down: $(1,\,-2,\,4)^T$.

---

## Why it works

Keep the order straight: **row first, column second**.

An $m\times n$ matrix has rows $1$ to $m$ and columns $1$ to $n$. So $a_{23}$ exists in $A$, but $a_{32}$ does not, because $A$ has only 2 rows.

---

## Check

Count from the top-left corner: down to the row, then across to the column.

For $b_{32}$: the third row of $B$ is $(4,\,1)$, and its second entry is $1$. ✓
