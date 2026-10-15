# Problem 12. Formula for a Matrix Power

## Result

$$
A^2=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad
A^3=
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix},\qquad
A^4=
\begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}
$$

Conjecture:

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
$$

## Main Steps

**Computing the first powers.** Each power is the previous one times $A$. Multiplying a matrix of this form by $A$ adds 1 to the top-right entry.

- $A^2=A\cdot A$: row 1 $(1,\,1)$ with columns $(1,\,0)^T$ and $(1,\,1)^T$ gives $1$ and $2$. Row 2 $(0,\,1)$ gives $0$ and $1$.
- $A^3=A^2\cdot A$: row 1 $(1,\,2)$ gives $1$ and $3$. Row 2 $(0,\,1)$ gives $0$ and $1$.
- $A^4=A^3\cdot A$: row 1 $(1,\,3)$ gives $1$ and $4$. Row 2 gives $0$ and $1$.

**Pattern.** The diagonal stays $1$, the bottom-left stays $0$, and the top-right entry is the power number. So the conjecture is the matrix above with $n$ in the top-right corner.

**Proof by induction.** Assume the formula holds for some $n$:

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
$$

Then

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
1\cdot1+n\cdot0 & 1\cdot1+n\cdot1 \\
0\cdot1+1\cdot0 & 0\cdot1+1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & n+1 \\
0 & 1 \\
\end{pmatrix}
$$

This is exactly the formula with $n+1$ in place of $n$.

## Explanation

Checking $A^2$, $A^3$, $A^4$ only suggests the pattern. It does not prove it: the formula could fail at $n=5$. The induction argument closes this gap in two steps:

1. **Base case:** the formula is true for $n=1$, since $A^1=A$.
2. **Inductive step:** if it is true for $n$, it is true for $n+1$.

Together these show it is true for every positive integer $n$. This is a standard way to prove formulas about powers.

Geometrically, $A$ is a *shear*: it pushes the top row to the right by the height of the point. Applying the shear $n$ times pushes by $n$ times as much, which is why the top-right entry grows by 1 each time.

## Verification

For $n=4$, the formula gives the matrix with rows $(1,\,4)$ and $(0,\,1)$, which matches the direct computation of $A^4$. The induction step was verified symbolically above.
