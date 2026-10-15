# Problem 4. Matrix Multiplication and Noncommutativity

## Exercise

### Exercise 4. Matrix Multiplication and Noncommutativity
For

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

> **Why this exercise:** shows one of the most important differences between matrix multiplication and multiplication of numbers.

---

## Answer

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

Since $AB\neq BA$, multiplication here is **not commutative**.

---

## Steps

### Step 1. Rule

Entry $(i,j)$ = row $i$ of the first matrix times column $j$ of the second. Multiply matching positions, then add.

### Step 2. Compute $AB$

Rows of $A$: $(1,\,2)$ and $(0,\,1)$. Columns of $B$: $(2,\,3)^T$ and $(0,\,1)^T$.

- $(1,1)$: $1\cdot 2+2\cdot 3=8$
- $(1,2)$: $1\cdot 0+2\cdot 1=2$
- $(2,1)$: $0\cdot 2+1\cdot 3=3$
- $(2,2)$: $0\cdot 0+1\cdot 1=1$

### Step 3. Compute $BA$

Rows of $B$: $(2,\,0)$ and $(3,\,1)$. Columns of $A$: $(1,\,0)^T$ and $(2,\,1)^T$.

- $(1,1)$: $2\cdot 1+0\cdot 0=2$
- $(1,2)$: $2\cdot 2+0\cdot 1=4$
- $(2,1)$: $3\cdot 1+1\cdot 0=3$
- $(2,2)$: $3\cdot 2+1\cdot 1=7$

### Step 4. Compare position by position

| Position | $AB$ | $BA$ | Equal? |
|---|---|---|---|
| $(1,1)$ | $8$ | $2$ | No |
| $(1,2)$ | $2$ | $4$ | No |
| $(2,1)$ | $3$ | $3$ | Yes |
| $(2,2)$ | $1$ | $7$ | No |

One mismatch is enough: $AB\neq BA$.

---

## Why it works

For numbers, $ab=ba$ always holds. For matrices it does not. The rows of the first matrix meet the columns of the second. Swap the order and different rows and columns meet, so the result changes.

**Keep the order of factors.**

---

## Check

Diagonal sums: $AB$ gives $8+1=9$, and $BA$ gives $2+7=9$.

The sums are equal, but the matrices differ. Equal traces do not prove equal products, so the comparison must be entry by entry.
