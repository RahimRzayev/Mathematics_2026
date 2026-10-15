# Problem 8. Row Operations and Their Reversibility

## Exercise

### Exercise 8. Row Operations and Their Reversibility
For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:

1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

> **Why this exercise:** prepares for elimination by showing that row operations are controlled and reversible transformations of a matrix.

---

## Answer

Final matrix after all three operations:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

| Step | Operation | Undo |
|---|---|---|
| 1 | $R_2\leftarrow R_2-2R_1$ | $R_2\leftarrow R_2+2R_1$ |
| 2 | $R_3\leftarrow R_3+R_1$ | $R_3\leftarrow R_3-R_1$ |
| 3 | swap $R_2$ and $R_3$ | swap $R_2$ and $R_3$ |

---

## Steps

### Step 1. $R_2\leftarrow R_2-2R_1$

$(2,\,4,\,1)-2(1,\,2,\,-1)=(0,\,0,\,3)$

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

### Step 2. $R_3\leftarrow R_3+R_1$

$(-1,\,1,\,3)+(1,\,2,\,-1)=(0,\,3,\,2)$

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

### Step 3. Swap $R_2$ and $R_3$

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

---

## Why it works

Each row operation has an inverse that undoes it:

- Adding $-2R_1$ to $R_2$ is undone by adding $+2R_1$.
- Adding $R_1$ to $R_3$ is undone by subtracting $R_1$.
- A swap is undone by the same swap.

No information is lost, so the solutions of a system do not change. This is why elimination is safe.

---

## Check

Undo the steps in reverse order, starting from the final matrix.

1. Swap rows 2 and 3 back: rows $(1,\,2,\,-1)$, $(0,\,0,\,3)$, $(0,\,3,\,2)$.
2. $R_3\leftarrow R_3-R_1$: $(0,\,3,\,2)-(1,\,2,\,-1)=(-1,\,1,\,3)$.
3. $R_2\leftarrow R_2+2R_1$: $(0,\,0,\,3)+(2,\,4,\,-2)=(2,\,4,\,1)$.

The original $A$ is recovered. ✓
