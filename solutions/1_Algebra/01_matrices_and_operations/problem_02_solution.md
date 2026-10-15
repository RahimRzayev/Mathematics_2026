# Problem 2. Addition and Scalar Multiplication

## Exercise

### Exercise 2. Addition and Scalar Multiplication
For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

> **Why this exercise:** reinforces entry-by-entry operations and the importance of compatible dimensions.

---

## Answer

$$
A+B=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}
$$

$$
A-B=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}
$$

$$
3A-2B=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Add and subtract position by position

| Position | $A+B$ | $A-B$ |
|---|---|---|
| top-left | $1+4=5$ | $1-4=-3$ |
| top-right | $2+(-2)=0$ | $2-(-2)=4$ |
| bottom-left | $-1+0=-1$ | $-1-0=-1$ |
| bottom-right | $3+5=8$ | $3-5=-2$ |

### Step 2. Scalar multiples

$$
3A=
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix},\qquad
2B=
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}
$$

### Step 3. Combine into $3A-2B$

| Position | $3A$ | $2B$ | $3A-2B$ |
|---|---|---|---|
| top-left | $3$ | $8$ | $-5$ |
| top-right | $6$ | $-4$ | $10$ |
| bottom-left | $-3$ | $0$ | $-3$ |
| bottom-right | $9$ | $10$ | $-1$ |

---

## Why it works

- **Addition** works position by position. Both matrices need **the same size**, because an entry with no partner has nothing to add to.
- **Scalar multiplication** multiplies every entry by the number.

---

## Check

Bottom-right of $3A-2B$, computed directly: $3\cdot 3-2\cdot 5=9-10=-1$. ✓ Matches Step 3.
