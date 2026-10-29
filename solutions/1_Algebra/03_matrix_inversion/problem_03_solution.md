# Problem 3. When Does the Inverse Not Exist?

## Exercise

### Exercise 3. When Does the Inverse Not Exist?
For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

> **Why this exercise:** connects two signs of noninvertibility instead of treating them as unrelated facts.

---

## Answer

| Method | Observation | Conclusion |
|---|---|---|
| Determinant | $\det A=0$ | No inverse |
| Rows | Row 1 $=2\cdot$ Row 2 | No inverse |

Both tests say the same thing: $A^{-1}$ **does not exist**.

---

## Steps

### Step 1. Determinant

$$
\det A=2\cdot 2-4\cdot 1=4-4=0
$$

The $2\times 2$ inverse formula contains the factor $\frac{1}{\det A}$. With $\det A=0$ that factor is undefined, so no inverse exists.

### Step 2. Dependence between the rows

Compare the rows:

$$
(2,\ 4)=2\cdot(1,\ 2)
$$

The first row is twice the second, so the rows are linearly dependent.

### Step 3. Why dependent rows block the inverse

Suppose $A^{-1}$ existed. Every vector $y$ in the plane would then be an output: $y=A\left(A^{-1}y\right)$.

But for any input $x=(x_1,\ x_2)$,

$$
Ax=
\begin{pmatrix}
2x_1+4x_2 \\
x_1+2x_2 \\
\end{pmatrix}=(x_1+2x_2)
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

Every output lies on the single line spanned by $(2,\ 1)$. A vector such as $(1,\ 0)$ is never reached. So $A$ cannot be undone, and $A^{-1}$ does not exist.

---

## Why it works

The two tests are the same fact seen from two sides.

- **Determinant:** $|\det A|$ is the area scaling factor of the map $x\mapsto Ax$. Zero means the plane is squashed onto a line (area $0$).
- **Rows:** dependent rows are exactly what makes the determinant zero. If one row is a multiple of the other, $ad-bc$ cancels to $0$.

Once the plane is squashed onto a line, different inputs land on the same output, and the lost information cannot be recovered.

---

## Check

Find two different inputs with the same output. Take $x=(2,\ -1)$:

$$
A
\begin{pmatrix}
2 \\
-1 \\
\end{pmatrix}=
\begin{pmatrix}
4-4 \\
2-2 \\
\end{pmatrix}=
\begin{pmatrix}
0 \\
0 \\
\end{pmatrix}
$$

So $A(2,\ -1)=A(0,\ 0)=0$. If $A^{-1}$ existed, applying it to $0$ would have to return both $(2,\ -1)$ and $(0,\ 0)$. That is impossible. ✓
