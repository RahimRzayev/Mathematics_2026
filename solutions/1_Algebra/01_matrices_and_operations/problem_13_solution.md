# Problem 13. A Recurrence Written in Matrix Form

## Exercise

### Exercise 13. A Recurrence Written in Matrix Form
Let

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence

$$
0,1,1,2,3,5,8,\ldots
$$

and describe the relationship you observe. Then compute

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}
$$

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

> **Why this exercise:** shows the connection between matrix powers and a simple numerical recurrence.

---

## Answer

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
\end{pmatrix}
$$

$$
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

| Power | Fibonacci numbers inside |
|---|---|
| $F^2$ | $2,\ 1,\ 1$ |
| $F^3$ | $3,\ 2,\ 1$ |
| $F^4$ | $5,\ 3,\ 2$ |
| $F^5$ | $8,\ 5,\ 3$ |

The powers of $F$ are built from Fibonacci numbers.

---

## Steps

### Step 1. Compute the powers

Each power is the previous one times

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

- $F^2$: row 1, $(1,\,1)$, with columns $(1,\,1)^T$ and $(1,\,0)^T$ gives $2$ and $1$. Row 2, $(1,\,0)$, gives $1$ and $1$.
- $F^3=F^2\cdot F$: row 1, $(2,\,1)$, gives $3$ and $2$. Row 2, $(1,\,1)$, gives $2$ and $1$.
- $F^4=F^3\cdot F$: row 1, $(3,\,2)$, gives $5$ and $3$. Row 2, $(2,\,1)$, gives $3$ and $2$.
- $F^5=F^4\cdot F$: row 1, $(5,\,3)$, gives $8$ and $5$. Row 2, $(3,\,2)$, gives $5$ and $3$.

### Step 2. Find the general pattern

The Fibonacci sequence is $0,\,1,\,1,\,2,\,3,\,5,\,8,\ldots$, where each term is the sum of the two before it. In general,

$$
F^n=
\begin{pmatrix}
F_{n+1} & F_n \\
F_n & F_{n-1} \\
\end{pmatrix}
$$

where $F_k$ is the $k$-th Fibonacci number.

### Step 3. One recurrence step

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

The first entry is the sum $a+b$. The second entry keeps the old $a$ for the next step.

---

## Why it works

$F$ is a machine for the Fibonacci recurrence. Start from the pair $(1,\,0)$ and apply $F$ repeatedly:

| Step | Pair $(a,\,b)$ | $F\cdot(a,\,b)^T$ |
|---|---|---|
| 0 | $(1,\,0)$ | $(1,\,1)$ |
| 1 | $(1,\,1)$ | $(2,\,1)$ |
| 2 | $(2,\,1)$ | $(3,\,2)$ |
| 3 | $(3,\,2)$ | $(5,\,3)$ |

Each step adds the two numbers and keeps one of them. That is how Fibonacci numbers are built.

Since $F^n$ jumps $n$ steps at once, it gives Fibonacci numbers directly, without computing every term for large $n$.

---

## Check

Apply $F$ to $(1,\,0)$ five times: $(1,0)\to(1,1)\to(2,1)\to(3,2)\to(5,3)\to(8,5)$. The top-left entry of $F^5$ is $8=F_6$. ✓
