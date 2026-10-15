# Problem 6. Transpose

## Exercise

### Exercise 6. Transpose
For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$
(AB)^T=B^TA^T.
$$

> **Why this exercise:** teaches transposition and an important property that reverses the order of factors.

---

## Answer

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}
$$

$$
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

---

## Steps

### Step 1. Transposes: rows become columns

- $A$ is $2\times 3$, so $A^T$ is $3\times 2$. Row 1 of $A$, $(1,\,2,\,3)$, becomes column 1 of $A^T$.
- $B$ is $3\times 2$, so $B^T$ is $2\times 3$. Column 1 of $B$, $(1,\,2,\,-1)$, becomes row 1 of $B^T$.

### Step 2. Product $AB$ (size $2\times 2$)

- Row 1 of $A$ is $(1,\,2,\,3)$. With column 1 of $B$: $1+4-3=2$. With column 2 of $B$, $(0,\,1,\,3)$: $0+2+9=11$.
- Row 2 of $A$ is $(4,\,5,\,6)$. With column 1 of $B$: $4+10-6=8$. With column 2: $0+5+18=23$.

### Step 3. Check $(AB)^T=B^TA^T$

Compute $B^TA^T$: rows of $B^T$ are $(1,\,2,\,-1)$ and $(0,\,1,\,3)$. Columns of $A^T$ are $(1,\,2,\,3)^T$ and $(4,\,5,\,6)^T$.

| Position | $(AB)^T$ | $B^TA^T$ | Equal? |
|---|---|---|---|
| $(1,1)$ | $2$ | $1+4-3=2$ | Yes |
| $(1,2)$ | $8$ | $4+10-6=8$ | Yes |
| $(2,1)$ | $11$ | $0+2+9=11$ | Yes |
| $(2,2)$ | $23$ | $0+5+18=23$ | Yes |

---

## Why it works

Transposing swaps rows and columns. Transposing a product **reverses the order** of the factors:

$$
(AB)^T=B^TA^T
$$

Remember it as: **the transpose of a product**, not the product of transposes, reverses the order.

---

## Check

All four entries match in the table above. ✓
