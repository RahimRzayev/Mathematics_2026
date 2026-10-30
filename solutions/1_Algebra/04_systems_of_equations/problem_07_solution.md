# Problem 7. Choosing a Method Deliberately

## Exercise

### Exercise 7. Choosing a Method Deliberately
Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x-y=3, \\
4y=8;
\end{cases}
$$

2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

> **Why this exercise:** practices choosing a method based on the structure of the problem instead of solving another small system by two methods.

---

## Answer

| Case | Structure | Best method | Reusable / unnecessary |
|---|---|---|---|
| 1 | already triangular, one right-hand side | back substitution only | forward elimination is unnecessary |
| 2 | same $A$, three right-hand sides, $A^{-1}$ known | $x_i=A^{-1}b_i$ | $A^{-1}$ is reused; no elimination needed |
| 3 | one right-hand side, $A^{-1}$ unknown | Gaussian elimination on $[A\mid b]$ | computing $A^{-1}$ is unnecessary |

Case 1 solution:

$$
(x,\ y)=\left(\frac52,\ 2\right)
$$

---

## Steps

### Case 1. Triangular system: back substitution

The coefficient matrix

$$
\begin{pmatrix}
2 & -1 \\
0 & 4 \\
\end{pmatrix}
$$

is upper triangular. It is already in row echelon form, so no elimination step is needed. Both diagonal entries are nonzero, so the solution is unique.

**Step 1.1.** From the last equation:

$$
4y=8 \quad\Longrightarrow\quad y=2
$$

**Step 1.2.** Substitute into the first equation:

$$
2x-2=3 \quad\Longrightarrow\quad x=\frac52
$$

Cost: two divisions and one substitution.

### Case 2. Same $A$, three right-hand sides, $A^{-1}$ known

Plan:

1. Compute $x_1=A^{-1}b_1$.
2. Compute $x_2=A^{-1}b_2$.
3. Compute $x_3=A^{-1}b_3$.

Each step is one matrix–vector product. The expensive part, finding $A^{-1}$, is already done and is reused three times. Running elimination three times would repeat the same row operations on $A$ for nothing.

The three products can also be done at once:

$$
\begin{pmatrix}
x_1 & x_2 & x_3 \\
\end{pmatrix}=A^{-1}
\begin{pmatrix}
b_1 & b_2 & b_3 \\
\end{pmatrix}
$$

### Case 3. One $3\times3$ system, $A^{-1}$ unknown

Plan:

1. Write $[A\mid b]$ (three rows, four columns).
2. Forward elimination to row echelon form.
3. Back substitution.

Computing $A^{-1}$ first would mean running Gauss–Jordan on $[A\mid I]$, which carries three extra columns instead of one, then performing an extra product $A^{-1}b$. With only one right-hand side, none of that work would be reused, so it is unnecessary.

---

## Why it works

The deciding factors are the **structure of the matrix** and the **number of right-hand sides**:

- A triangular matrix has already done the work of elimination; only back substitution remains.
- Finding $A^{-1}$ is costly but pays off when it is already known or when many right-hand sides share the same $A$.
- For a single right-hand side and an unknown inverse, elimination on $[A\mid b]$ performs only the operations actually needed.

The names of the methods do not decide; the cost of what must still be computed does.

---

## Check

Case 1: substitute $(x,y)=\left(\frac52,\ 2\right)$:

- $2\cdot\frac52-2=5-2=3$ ✓
- $4\cdot2=8$ ✓
