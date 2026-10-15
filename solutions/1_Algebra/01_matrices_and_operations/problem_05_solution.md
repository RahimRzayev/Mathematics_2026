# Problem 5. Matrix Times Vector

## Exercise

### Exercise 5. Matrix Times Vector
Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}.
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

> **Why this exercise:** shows that multiplying a matrix by a vector can be understood as a linear combination of the matrix columns.

---

## Answer

$$
Ax=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

As a combination of the columns of $A$: $\;4\cdot(2,\,1)^T+2\cdot(-1,\,3)^T=(6,\,10)^T$.

---

## Steps

### Step 1. Row way (dot products)

| Row of $A$ | Times $x=(4,\,2)^T$ | Result |
|---|---|---|
| $(2,\,-1)$ | $2\cdot 4+(-1)\cdot 2=8-2$ | $6$ |
| $(1,\,3)$ | $1\cdot 4+3\cdot 2=4+6$ | $10$ |

### Step 2. Column way (weighted columns)

The entries of $x$ are the weights: $4$ on column 1, $2$ on column 2.

$$
4\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}+
2\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}=
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix}+
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix}=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

---

## Why it works

Two readings give the same answer:

1. **Row way:** each entry of the result is a row of $A$ dotted with $x$.
2. **Column way:** the result is a mix of the columns of $A$, with the weights taken from $x$.

So $Ax$ always lies in the set of all combinations of the columns of $A$.

---

## Check

Both methods gave $(6,\,10)^T$. ✓ Substitution agrees: $2\cdot 4-1\cdot 2=6$ and $1\cdot 4+3\cdot 2=10$.
