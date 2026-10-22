# Problem 4. Triangular Matrix

## Exercise

### Exercise 4. Triangular Matrix
Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

> **Why this exercise:** reinforces an important property of triangular matrices.

---

## Answer

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}=2\cdot(-3)\cdot 7=-42
$$

**Rule:** the determinant of any triangular matrix (upper or lower) is the **product of its diagonal entries**.

---

## Steps

### Step 1. Recognize the shape

All entries **below** the main diagonal are $0$. This is an **upper triangular** matrix.

### Step 2. Read the diagonal

| Position | Entry |
|---|---|
| $a_{11}$ | $2$ |
| $a_{22}$ | $-3$ |
| $a_{33}$ | $7$ |

### Step 3. Multiply

$$
2\cdot(-3)\cdot 7=-42
$$

The entries $4$, $1$, $5$ above the diagonal do not matter at all.

---

## Why it works

Every term of a $3\times 3$ determinant picks **one entry from each row and each column**.

Build such a term starting from the bottom row:

1. Row 3 has only one nonzero entry: $7$ in column 3. Any other choice gives a $0$ factor.
2. Row 2 must now avoid column 3. Its only remaining nonzero option is $-3$ in column 2.
3. Row 1 must avoid columns 2 and 3. Its only option is $2$ in column 1.

So exactly one term survives: the diagonal product $2\cdot(-3)\cdot 7$. Every other term contains a zero.

The same argument works for any size $n$ and for lower triangular matrices (start from the top row instead).

---

## Check

Expand along column 1, which has only one nonzero entry:

$$
\det=2\cdot\det
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}=2\cdot(-21-0)=-42
$$

Same value. ✓
