# Problem 8. Row Operations and Their Reversibility

## Result

Start with

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

After step 1, $R_2\leftarrow R_2-2R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

After step 2, $R_3\leftarrow R_3+R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

After step 3, swap $R_2$ and $R_3$:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

**Reversing operations:**

- Undo step 3 by swapping $R_2$ and $R_3$ again.
- Undo step 2 by $R_3\leftarrow R_3-R_1$.
- Undo step 1 by $R_2\leftarrow R_2+2R_1$.

## Main Steps

**Step 1.** Compute $R_2-2R_1 = (2,\,4,\,1)-2(1,\,2,\,-1) = (2-2,\ 4-4,\ 1+2) = (0,\,0,\,3)$.

**Step 2.** Compute $R_3+R_1 = (-1,\,1,\,3)+(1,\,2,\,-1) = (0,\,3,\,2)$.

**Step 3.** Rows 2 and 3 are exchanged: the new row 2 is $(0,\,3,\,2)$ and the new row 3 is $(0,\,0,\,3)$.

**Reversal.** Each row operation changes the matrix in a way that can be exactly undone:

- Adding $-2R_1$ to $R_2$ cancels the earlier $+(-2)R_1$ addition, returning $R_2$ to $(2,\,4,\,1)$.
- Subtracting $R_1$ from $R_3$ removes the earlier $+R_1$, returning $R_3$ to $(-1,\,1,\,3)$.
- Swapping rows twice puts them back in their original positions.

## Explanation

Row operations are the basic tools of elimination. Each one is simple, and each has an **inverse** operation that undoes it. This is why they are called *reversible*: no information is lost. Adding a multiple of one row to another can always be undone by subtracting the same multiple, and a swap can always be undone by swapping back.

This reversibility is the reason that row operations do not change the solutions of a system of equations. Solving the system with row operations is therefore safe.

## Verification

Reverse the three steps in the opposite order, starting from the final matrix.

- Undo step 3 by swapping rows 2 and 3 again. The rows become $(1,\,2,\,-1)$, $(0,\,0,\,3)$, and $(0,\,3,\,2)$.
- Undo step 2 by $R_3\leftarrow R_3-R_1$. Row 3 becomes $(0,\,3,\,2)-(1,\,2,\,-1)=(-1,\,1,\,3)$, so the rows are $(1,\,2,\,-1)$, $(0,\,0,\,3)$, and $(-1,\,1,\,3)$.
- Undo step 1 by $R_2\leftarrow R_2+2R_1$. Row 2 becomes $(0,\,0,\,3)+(2,\,4,\,-2)=(2,\,4,\,1)$.

The original matrix $A$ is recovered, which confirms that each operation is reversible.
