# Problem 15. Associativity of Multiplication and Different Calculation Paths

## Exercise

### Exercise 15. Associativity of Multiplication and Different Calculation Paths
Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\quad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\quad C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}.
$$

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

> **Why this exercise:** reinforces associativity by comparing two mathematically equivalent calculation paths.

---

## Answer

$$
(AB)C=A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

Both paths give the same matrix, as associativity predicts. The paths differ in cost.

---

## Steps

### Step 1. Path 1: $AB$ first, then $(AB)C$

$$
AB=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}
$$

- Row 1 of $A$, $(1,\,2,\,0)$: with column 1 of $B$ gives $1+4+0=5$; with column 2 gives $0+2+0=2$.
- Row 2 of $A$, $(0,\,1,\,1)$: with column 1 gives $0+2-1=1$; with column 2 gives $0+1+3=4$.

$$
(AB)C=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

- Row 1, $(5,\,2)$: $5\cdot 2+2\cdot 0=10$ and $5\cdot 1+2\cdot(-1)=3$.
- Row 2, $(1,\,4)$: $1\cdot 2+4\cdot 0=2$ and $1\cdot 1+4\cdot(-1)=-3$.

### Step 2. Path 2: $BC$ first, then $A(BC)$

$$
BC=
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}
$$

- Row 1 of $B$, $(1,\,0)$: $2$ and $1$.
- Row 2 of $B$, $(2,\,1)$: $4$ and $2-1=1$.
- Row 3 of $B$, $(-1,\,3)$: $-2$ and $-1-3=-4$.

$$
A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

- Row 1 of $A$, $(1,\,2,\,0)$: with $(2,\,4,\,-2)^T$ gives $2+8=10$; with $(1,\,1,\,-4)^T$ gives $1+2=3$.
- Row 2 of $A$, $(0,\,1,\,1)$: $4-2=2$ and $1-4=-3$.

### Step 3. Compare the cost

Count the multiplications of two numbers. A product of size $p\times q$ with inner size $r$ needs $p\cdot q\cdot r$.

| Path | Product | Size | Inner size | Multiplications |
|---|---|---|---|---|
| 1 | $AB$ | $2\times 2$ | $3$ | $12$ |
| 1 | $(AB)C$ | $2\times 2$ | $2$ | $8$ |
| | | | **Path 1 total** | **20** |
| 2 | $BC$ | $3\times 2$ | $2$ | $12$ |
| 2 | $A(BC)$ | $2\times 2$ | $3$ | $12$ |
| | | | **Path 2 total** | **24** |

---

## Why it works

**Associativity** says $(XY)Z=X(YZ)$. Regrouping does not change the answer, so pick the cheaper grouping.

Here Path 1 costs $20$ multiplications and Path 2 costs $24$. For large matrices, grouping matters a lot in computer calculations.

Compare with Problem 4: associativity lets you **regroup** factors but keeps their **order**. Commutativity would let you change the order, and matrix multiplication does not allow that in general.

---

## Check

Both paths gave the same matrix entry by entry. ✓
