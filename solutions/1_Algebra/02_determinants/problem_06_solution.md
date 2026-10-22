# Problem 6. Parameter and Invertibility

## Exercise

### Exercise 6. Parameter and Invertibility
For

$$
A(t)=
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

> **Why this exercise:** shows how the determinant can be used to study a family of matrices depending on a parameter.

---

## Answer

$A(t)$ is **not invertible** exactly for

$$
t=\sqrt{2}\qquad\mathrm{or}\qquad t=-\sqrt{2}
$$

For every other real $t$, the matrix is invertible.

---

## Steps

### Step 1. Write the determinant as a function of $t$

$$
\det A(t)=t\cdot t-1\cdot 2=t^2-2
$$

### Step 2. Set the determinant equal to zero

Not invertible means $\det A(t)=0$:

$$
t^2-2=0
$$

### Step 3. Solve

$$
t^2=2\qquad\Longrightarrow\qquad t=\pm\sqrt{2}
$$

---

## Why it works

Rule: a square matrix is invertible **if and only if** its determinant is nonzero.

So the question "for which $t$ is $A(t)$ not invertible?" becomes the equation $\det A(t)=0$.

| Value of $t$ | $\det A(t)=t^2-2$ | Invertible? |
|---|---|---|
| $t=0$ | $-2$ | Yes |
| $t=1$ | $-1$ | Yes |
| $t=\sqrt{2}$ | $0$ | No |
| $t=-\sqrt{2}$ | $0$ | No |
| $t=3$ | $7$ | Yes |

The determinant turns a matrix question into a one-variable equation.

---

## Check

Take $t=\sqrt{2}$:

$$
A(\sqrt{2})=
\begin{pmatrix}
\sqrt{2} & 1 \\
2 & \sqrt{2} \\
\end{pmatrix}
$$

Row 2 equals $\sqrt{2}$ times row 1, because $\sqrt{2}\cdot(\sqrt{2},\ 1)=(2,\ \sqrt{2})$. The rows are dependent, so the matrix cannot be invertible. ✓
