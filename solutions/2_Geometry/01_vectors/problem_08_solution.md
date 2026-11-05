# Problem 8. Linear Combination and Checking the Result

## Exercise

### Exercise 8. Linear Combination and Checking the Result
Check whether $w=(5,1)$ can be written as

$$
w=au+bv,
$$

where $u=(1,1)$ and $v=(2,-1)$. If so, find $a,b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

> **Why this exercise:** connects linear combinations with the geometry of directions.

---

## Answer

Yes, $w$ can be written in this form, with unique coefficients

$$
a=\frac73,\qquad b=\frac43
$$

Geometrically, $u$ and $v$ point in different directions, so they span the whole plane. The coefficients state how far to travel along each direction to reach $w$.

---

## Steps

### Step 1. Write the equation in coordinates

$$
a(1,1)+b(2,-1)=(a+2b,\ a-b)=(5,1)
$$

Equating coordinates gives a linear system:

$$
\begin{cases}
a+2b=5, \\
a-b=1.
\end{cases}
$$

### Step 2. Eliminate $a$

Subtracting the second equation from the first gives

$$
3b=4\quad\Longrightarrow\quad b=\frac43
$$

### Step 3. Back-substitute

$$
a=1+b=1+\frac43=\frac73
$$

### Step 4. Reconstruct $w$

$$
\frac73(1,1)+\frac43(2,-1)=\left(\frac73+\frac83,\ \frac73-\frac43\right)=\left(\frac{15}{3},\ \frac33\right)=(5,1)=w
$$

---

## Why it works

**Existence and uniqueness.** The coefficient matrix of the system has the vectors $u$ and $v$ as its columns:

$$
\det
\begin{pmatrix}
1 & 2 \\
1 & -1 \\
\end{pmatrix}=1\cdot(-1)-2\cdot1=-3\neq0
$$

A nonzero determinant means the system has exactly one solution for every right-hand side. Every vector in $\mathbb R^2$, not only $w$, can therefore be written as a combination of $u$ and $v$ in exactly one way.

**Geometric meaning.** The vectors $u$ and $v$ are not parallel. Together they define a slanted coordinate grid covering the plane. The pair $\left(\frac73,\frac43\right)$ gives the coordinates of $w$ in that grid. The vector $w$ is the diagonal of the parallelogram with sides $\frac73u$ and $\frac43v$.

If $u$ and $v$ were parallel, every combination would lie on one line, and vectors off that line could not be reached.

---

## Check

Both equations of the system hold:

$$
a+2b=\frac73+\frac83=5\ \checkmark,\qquad a-b=\frac73-\frac43=1\ \checkmark
$$
