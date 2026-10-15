# Problem 12. Formula for a Matrix Power

## Exercise

### Exercise 12. Formula for a Matrix Power
Let

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

> **Why this exercise:** teaches how to recognize a pattern and formulate a generalization from several computations.

---

## Answer

Conjecture:

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
$$

It is proved for every positive integer $n$ by induction (Step 3).

---

## Steps

### Step 1. Compute the first powers

Each power is the previous one times $A$. Multiplying by $A$ adds $1$ to the top-right entry.

| Power | $n$ | Top-right entry |
|---|---|---|
| $A^1$ | $1$ | $1$ |
| $A^2$ | $2$ | $2$ |
| $A^3$ | $3$ | $3$ |
| $A^4$ | $4$ | $4$ |

For example, $A^2=A\cdot A$: row 1, $(1,\,1)$, with columns $(1,\,0)^T$ and $(1,\,1)^T$ gives $1$ and $2$. Row 2, $(0,\,1)$, gives $0$ and $1$.

### Step 2. Read the pattern

- The diagonal stays $1$.
- The bottom-left stays $0$.
- The top-right entry equals the power $n$.

### Step 3. Prove it by induction

**Base case.** $n=1$: $A^1=A$, which matches the formula.

**Inductive step.** Assume $A^n$ has the formula. Then

$$
A^{n+1}=A^nA=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & n+1 \\
0 & 1 \\
\end{pmatrix}
$$

This is exactly the formula with $n+1$ in place of $n$.

---

## Why it works

Checking $A^2$, $A^3$, $A^4$ only suggests the pattern. The formula could still fail at $n=5$. Induction closes that gap:

1. **Base case:** true for $n=1$.
2. **Inductive step:** true for $n$ implies true for $n+1$.

Together, these prove it for all $n$.

Geometrically, $A$ is a **shear**. Applying it $n$ times pushes the top row $n$ times as far.

---

## Check

For $n=4$, the formula gives rows $(1,\,4)$ and $(0,\,1)$, which matches the direct computation of $A^4$. ✓ The induction step was verified symbolically above.
