# Problem 13. A Recurrence Written in Matrix Form

## Result

$$
F^2=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad
F^3=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix},\qquad
F^4=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix},\qquad
F^5=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}
$$

The numbers $1,\,2,\,3,\,5,\,8$ in these matrices are Fibonacci numbers. Also

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}=
\begin{pmatrix}
a+b \\
a \\
\end{pmatrix}
$$

## Main Steps

**Powers of $F$.** Each power is the previous one times

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

- $F^2$: row 1 $(1,\,1)$ with columns $(1,\,1)^T$ and $(1,\,0)^T$ gives $2$ and $1$. Row 2 $(1,\,0)$ gives $1$ and $1$.
- $F^3=F^2\cdot F$: row 1 $(2,\,1)$ gives $3$ and $2$. Row 2 $(1,\,1)$ gives $2$ and $1$.
- $F^4=F^3\cdot F$: row 1 $(3,\,2)$ gives $5$ and $3$. Row 2 $(2,\,1)$ gives $3$ and $2$.
- $F^5=F^4\cdot F$: row 1 $(5,\,3)$ gives $8$ and $5$. Row 2 $(3,\,2)$ gives $5$ and $3$.

**Comparison with Fibonacci.** The sequence is $0,\,1,\,1,\,2,\,3,\,5,\,8,\ldots$, where each term is the sum of the two before it. Look at the numbers in the powers:

- $F^2$ contains $2,\,1,\,1$.
- $F^3$ contains $3,\,2,\,1$.
- $F^4$ contains $5,\,3,\,2$.
- $F^5$ contains $8,\,5,\,3$.

In general, $F^n$ has the form

$$
F^n=
\begin{pmatrix}
F_{n+1} & F_n \\
F_n & F_{n-1} \\
\end{pmatrix}
$$

where $F_k$ is the $k$-th Fibonacci number.

**One recurrence step.** Multiply $F$ by the vector $(a,\,b)^T$:

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot a+1\cdot b \\
1\cdot a+0\cdot b \\
\end{pmatrix}=
\begin{pmatrix}
a+b \\
a \\
\end{pmatrix}
$$

The first entry is the sum $a+b$, and the second entry keeps the old $a$.

## Explanation

The matrix $F$ is a machine for the Fibonacci recurrence. Starting from the pair $(F_1,\,F_0)=(1,\,0)$, each multiplication by $F$ creates the next pair:

$$
(1,0)\ \to\ (1,1)\ \to\ (2,1)\ \to\ (3,2)\ \to\ (5,3)\ \to\ \cdots
$$

Each step adds the two numbers and keeps one of them to continue. That is exactly how Fibonacci numbers are built.

Because of this, powers of $F$ give Fibonacci numbers directly. Computing $F^n$ jumps ahead $n$ steps at once, which is much faster than generating every term one by one for large $n$.

## Verification

Starting from $(1,\,0)$, apply $F$ repeatedly: $(1,0)\to(1,1)\to(2,1)\to(3,2)\to(5,3)$. The first entries $1,\,1,\,2,\,3,\,5$ are Fibonacci numbers, and they match the entries of the powers above. For example, the top-left entry of $F^5$ is $8=F_6$.
