# Problem 11. When Do Matrices Commute?

## Result

Let

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}.
$$

$AB=BA$ exactly when

$$
c=0 \quad \mathrm{and} \quad d=a
$$

with $a$ and $b$ arbitrary. So all matrices that commute with $A$ have the form

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}
$$

## Main Steps

**Compute $AB$.** Rows of $A$ are $(1,\,1)$ and $(0,\,1)$. Columns of $B$ are $(a,\,c)^T$ and $(b,\,d)^T$.

- Row 1: $1\cdot a+1\cdot c=a+c$, and $1\cdot b+1\cdot d=b+d$.
- Row 2: $0\cdot a+1\cdot c=c$, and $0\cdot b+1\cdot d=d$.

$$
AB=
\begin{pmatrix}
a+c & b+d \\
c & d \\
\end{pmatrix}
$$

**Compute $BA$.** Rows of $B$ are $(a,\,b)$ and $(c,\,d)$. Columns of $A$ are $(1,\,0)^T$ and $(1,\,1)^T$.

- Row 1: $a\cdot1+b\cdot0=a$, and $a\cdot1+b\cdot1=a+b$.
- Row 2: $c\cdot1+d\cdot0=c$, and $c\cdot1+d\cdot1=c+d$.

$$
BA=
\begin{pmatrix}
a & a+b \\
c & c+d \\
\end{pmatrix}
$$

**Compare entry by entry.**

- Position $(1,1)$: $a+c=a$, so $c=0$.
- Position $(1,2)$: $b+d=a+b$, so $d=a$.
- Position $(2,1)$: $c=c$, always true.
- Position $(2,2)$: $d=c+d$, so $c=0$ again.

The conditions are $c=0$ and $d=a$. The entry $b$ is free.

## Explanation

Commuting means that $A$ and $B$ "work well together" in both orders. Here the matrix $A$ is a shear: it slides the top row sideways and leaves the bottom row alone. For $B$ to commute with it, $B$ must have a zero in the bottom-left corner, so that $B$ keeps the bottom row fixed in the same way $A$ does, and its two diagonal entries must be equal.

The free entry $b$ corresponds to the matrix

$$
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}
$$

which is itself a "sideways slide". Sliding in either order gives the same result, so it commutes with $A$.

## Verification

Test a specific choice. Take $a=2$, $b=5$, $c=0$, $d=2$, so $B$ has rows $(2,\,5)$ and $(0,\,2)$. Then $AB$ and $BA$ both have rows $(2,\,7)$ and $(0,\,2)$, so they are equal.

Now take $c=1$ (violating the condition), keeping $a=2$, $b=5$, $d=2$. Then $AB$ has rows $(3,\,7)$ and $(1,\,2)$, while $BA$ has rows $(2,\,7)$ and $(1,\,3)$. They differ, as predicted.
