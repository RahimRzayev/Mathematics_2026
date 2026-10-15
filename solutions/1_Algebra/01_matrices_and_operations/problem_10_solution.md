# Problem 10. Columns of a Matrix Product

## Exercise

### Exercise 10. Columns of a Matrix Product
Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

> **Why this exercise:** extends the interpretation of matrix-vector multiplication to a full product of two matrices instead of simply repeating another $Ax$ exercise.

---

## Answer

| Quantity | Result |
|---|---|
| $Ab_1$ | $(-1,\ 2)^T$ |
| $Ab_2$ | $(2,\ 1)^T$ |

$$
AB=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}
$$

The first column of $AB$ is $Ab_1$. The second column of $AB$ is $Ab_2$.

---

## Steps

### Step 1. Columns of $B$

$$
B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

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

### Step 2. Compute $Ab_1$

Rows of $A$: $(1,\,2,\,0)$ and $(0,\,1,\,1)$.

- Row 1 times $b_1$: $1\cdot 1+2\cdot(-1)+0\cdot 3=-1$
- Row 2 times $b_1$: $0\cdot 1+1\cdot(-1)+1\cdot 3=2$

### Step 3. Compute $Ab_2$

- Row 1 times $b_2$: $1\cdot 2+2\cdot 0+0\cdot 1=2$
- Row 2 times $b_2$: $0\cdot 2+1\cdot 0+1\cdot 1=1$

### Step 4. Compute $AB$ directly

Row $i$ of $A$ times column $j$ of $B$ gives the same four numbers: $-1$, $2$, $2$, $1$.

### Step 5. Compare column by column

| Column | Column of $AB$ | $Ab_j$ | Same? |
|---|---|---|---|
| 1 | $(-1,\ 2)^T$ | $Ab_1=(-1,\ 2)^T$ | Yes |
| 2 | $(2,\ 1)^T$ | $Ab_2=(2,\ 1)^T$ | Yes |

---

## Why it works

Column $j$ of $AB$ is row $i$ of $A$ times column $j$ of $B$, for each $i$. That is exactly $A$ times $b_j$.

So **$AB$ is $A$ applied to each column of $B$**. This view helps when $B$ has many columns, because each column can be processed separately.

---

## Check

Steps 2 and 4 were computed separately and agree, so the claim holds. ✓
