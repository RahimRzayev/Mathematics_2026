# Problem 11. When Do Matrices Commute?

## Exercise

### Exercise 11. When Do Matrices Commute?
Given

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

Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

> **Why this exercise:** deepens the idea of noncommutativity by finding the conditions under which commutativity does hold.

---

## Answer

$AB=BA$ exactly when $c=0$ and $d=a$. The entry $b$ is free.

So every matrix that commutes with $A$ has this form:

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Compute $AB$

$$
AB=
\begin{pmatrix}
a+c & b+d \\
c & d \\
\end{pmatrix}
$$

Row 1 of $A$ is $(1,\,1)$, so row 1 of $AB$ is the sum of the rows of $B$. Row 2 of $A$ is $(0,\,1)$, so row 2 of $AB$ is row 2 of $B$.

### Step 2. Compute $BA$

$$
BA=
\begin{pmatrix}
a & a+b \\
c & c+d \\
\end{pmatrix}
$$

Column 1 of $A$ is $(1,\,0)^T$, so column 1 of $BA$ is column 1 of $B$. Column 2 of $A$ is $(1,\,1)^T$, so column 2 of $BA$ is the sum of the columns of $B$.

### Step 3. Compare entry by entry

| Position | $AB$ | $BA$ | Condition |
|---|---|---|---|
| $(1,1)$ | $a+c$ | $a$ | $c=0$ |
| $(1,2)$ | $b+d$ | $a+b$ | $d=a$ |
| $(2,1)$ | $c$ | $c$ | always true |
| $(2,2)$ | $d$ | $c+d$ | $c=0$ |

The conditions are $c=0$ and $d=a$. The entry $b$ is free.

---

## Why it works

$A$ is a **shear**: it slides the top row sideways and leaves the bottom row alone. For $B$ to commute with it, $B$ must keep the bottom row fixed in the same way. That forces $c=0$, and equal diagonal entries $d=a$.

The free entry $b$ gives the matrix

$$
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}
$$

This is another sideways slide. Sliding in either order gives the same result, so it commutes with $A$.

---

## Check

**Condition holds:** $a=2$, $b=5$, $c=0$, $d=2$. Then

$$
AB=BA=
\begin{pmatrix}
2 & 7 \\
0 & 2 \\
\end{pmatrix}
$$

Equal. ✓

**Condition broken:** same, but $c=1$. Then

$$
AB=
\begin{pmatrix}
3 & 7 \\
1 & 2 \\
\end{pmatrix},\qquad
BA=
\begin{pmatrix}
2 & 7 \\
1 & 3 \\
\end{pmatrix}
$$

Different, as predicted. ✓
