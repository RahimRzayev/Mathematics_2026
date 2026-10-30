# Problem 15. Classifying Three Systems

## Exercise

### Exercise 15. Classifying Three Systems
For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

$$
\begin{cases}
x+y=2, \\
x-y=0,
\end{cases}
$$

**System 2**

$$
\begin{cases}
x+y=2, \\
2x+2y=4,
\end{cases}
$$

**System 3**

$$
\begin{cases}
x+y=2, \\
2x+2y=5.
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

> **Why this exercise:** brings together the three basic cases and requires recognizing them from the structure after elimination.

---

## Answer

| System | Row 2 after one step | Type | Solutions |
|---|---|---|---|
| 1 | $(0\ \ -2\mid -2)$ | exactly one solution | $(x,y)=(1,1)$ |
| 2 | $(0\ \ 0\mid 0)$ | infinitely many solutions | $x=2-s,\ y=s,\ s\in\mathbb{R}$ |
| 3 | $(0\ \ 0\mid 1)$ | no solution | — |

One elimination step per system is enough to classify it.

---

## Steps

### Step 1. System 1

Operation: $R_2\to R_2-R_1$.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
1 & -1 & \mid & 0 \\
\end{pmatrix}\quad\longrightarrow\quad
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -2 & \mid & -2 \\
\end{pmatrix}
$$

Two pivots for two unknowns, no contradiction: **exactly one solution**. Back substitution gives $y=1$, $x=1$.

### Step 2. System 2

Operation: $R_2\to R_2-2R_1$.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 4 \\
\end{pmatrix}\quad\longrightarrow\quad
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

Row 2 is $0=0$. One pivot for two unknowns, no contradiction: **infinitely many solutions**, with one free variable $y=s$, so $x=2-s$.

### Step 3. System 3

Operation: $R_2\to R_2-2R_1$.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 5 \\
\end{pmatrix}\quad\longrightarrow\quad
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

Row 2 is $0=1$, a contradiction: **no solution**.

---

## Why it works

After elimination, the type of a system is read from two features of row echelon form:

1. Is there a row $(0\ \ 0\mid c)$ with $c\neq0$? If yes: **no solution**.
2. Otherwise, compare the number of pivots with the number of unknowns:
   - equal: **exactly one solution**;
   - fewer pivots: **infinitely many solutions**.

Geometric view of the same three cases:

| System | Lines | Picture |
|---|---|---|
| 1 | slopes $-1$ and $1$ | intersect at one point $(1,1)$ |
| 2 | second equation is twice the first | the same line |
| 3 | $x+y=2$ and $x+y=2.5$ | parallel, distinct lines |

Systems 2 and 3 have the same coefficient matrix, which is not invertible. For such a matrix only "infinitely many" or "none" is possible; the right-hand side decides which.

---

## Check

- System 1, $(1,1)$: $1+1=2$ ✓ and $1-1=0$ ✓.
- System 2, $s=0$ gives $(2,0)$: $2+0=2$ ✓ and $4+0=4$ ✓. $s=3$ gives $(-1,3)$: $-1+3=2$ ✓ and $-2+6=4$ ✓.
- System 3: if $x+y=2$, then $2x+2y=4\neq5$, so the second equation fails ✓.
