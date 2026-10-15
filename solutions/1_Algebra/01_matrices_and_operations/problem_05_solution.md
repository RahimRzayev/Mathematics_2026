# Problem 5. Matrix Times Vector

## Result

$$
Ax=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

As a linear combination of the columns of $A$:

$$
Ax=
4\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}+
2\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

## Main Steps

**Direct computation.** Multiply each row of $A$ by the vector $x=(4,\,2)^T$.

- First row $(2,\,-1)$: $2\cdot 4+(-1)\cdot 2=8-2=6$.
- Second row $(1,\,3)$: $1\cdot 4+3\cdot 2=4+6=10$.

**Column view.** The columns of $A$ are $(2,\,1)^T$ and $(-1,\,3)^T$. The entries of $x$ are the weights:

- Weight $4$ on the first column.
- Weight $2$ on the second column.

Add the weighted columns:

$$
4\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix},\qquad
2\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}=
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix}
$$

$$
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

## Explanation

Multiplying a matrix by a vector can be read in two ways that give the same answer:

1. **Row way:** each entry of the result is a row of $A$ dotted with $x$.
2. **Column way:** the result is a mix of the columns of $A$, where the entries of $x$ say how much of each column to take.

The column view is especially useful. It says that $Ax$ always lies in the set of all combinations of the columns of $A$. Here, the answer $(6,\,10)$ is built from the two columns, so it is a point reachable by mixing them.

## Verification

Both methods gave $(6,\,10)$. Check by substitution as well: the first entry is $2\cdot 4-1\cdot 2=6$ and the second is $1\cdot 4+3\cdot 2=10$. These agree with the column calculation.
