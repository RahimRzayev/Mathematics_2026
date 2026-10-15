# Problem 7. Identity Matrix, Zero Matrix, and Powers

## Exercise

### Exercise 7. Identity Matrix, Zero Matrix, and Powers
For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute

$$
AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.
$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

> **Why this exercise:** organizes the roles of neutral elements and reveals regularity in successive powers of a matrix.

---

## Answer

$$
AI=IA=A,\qquad A+0=A
$$

$$
A^2=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix},\qquad
A^3=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Identity and zero matrices

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

| Expression | Result | Why |
|---|---|---|
| $AI$ | $A$ | $I$ leaves each row unchanged |
| $IA$ | $A$ | $I$ leaves each column unchanged |
| $A+0$ | $A$ | adding zeros changes nothing |

### Step 2. Square: $A^2=A\cdot A$

- Row 1, $(2,\,1)$, with columns $(2,\,0)^T$ and $(1,\,2)^T$: $2\cdot 2+1\cdot 0=4$ and $2\cdot 1+1\cdot 2=4$.
- Row 2, $(0,\,2)$: $0\cdot 2+2\cdot 0=0$ and $0\cdot 1+2\cdot 2=4$.

### Step 3. Cube: $A^3=A^2\cdot A$

- Row 1, $(4,\,4)$: $8$ and $4+8=12$.
- Row 2, $(0,\,4)$: $0$ and $8$.

---

## Why it works

- $I$ is the **neutral element for multiplication**, like $1$ for numbers.
- $0$ is the **neutral element for addition**, like $0$ for numbers.

**The pattern.** Split $A$ into two parts:

$$
A=2I+N,\qquad N=
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix},\qquad N^2=0
$$

This gives the general formula:

$$
A^n=
\begin{pmatrix}
2^n & n\,2^{n-1} \\
0 & 2^n \\
\end{pmatrix}
$$

The diagonal doubles each time, and the top-right entry grows in a predictable way.

---

## Check

The formula gives the same values as the direct multiplication:

- $n=2$: $2^2=4$ and $2\cdot 2^{1}=4$. ✓
- $n=3$: $2^3=8$ and $3\cdot 2^{2}=12$. ✓
