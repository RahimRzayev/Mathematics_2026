# Problem 6. A System with a Parameter — Which Cases Actually Occur?

## Exercise

### Exercise 6. A System with a Parameter — Which Cases Actually Occur?
Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

> **Why this exercise:** teaches how to analyze a parameter without assuming in advance that all theoretically possible cases must occur in a specific system.

---

## Answer

| Value of $a$ | Type | Solutions |
|---|---|---|
| $a=2$ | infinitely many | $x=2-s,\ y=s,\ s\in\mathbb{R}$ |
| $a\neq2$ | no solution | — |
| any $a$ | exactly one solution | **never occurs** |

Exactly one solution is impossible because the coefficient rows $(1,1)$ and $(a,a)$ are always proportional.

---

## Steps

### Step 1. Write the augmented matrix

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a & a & \mid & 4 \\
\end{pmatrix}
$$

### Step 2. Clear column 1

Operation: $R_2\to R_2-aR_1$. This step uses no division, so it is valid for every $a$.

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 4-2a \\
\end{pmatrix}
$$

The coefficient part of row 2 is zero for **every** $a$. Only the right-hand side depends on $a$.

### Step 3. Case $4-2a\neq0$, that is $a\neq2$

Row 2 reads $0=4-2a\neq0$, a contradiction. No solution.

This includes $a=0$, where the second equation itself becomes $0=4$.

### Step 4. Case $4-2a=0$, that is $a=2$

Row 2 reads $0=0$. Only one equation remains:

$$
x+y=2
$$

There is one pivot and two unknowns, so one variable is free. With $y=s$:

$$
x=2-s,\qquad y=s
$$

### Step 5. Why exactly one solution never occurs

A unique solution needs a pivot in every column, that is, two pivots. After Step 2, row 2 has no pivot for any $a$. Equivalently,

$$
\det
\begin{pmatrix}
1 & 1 \\
a & a \\
\end{pmatrix}=a-a=0
$$

for every $a$, so the coefficient matrix is never invertible.

---

## Why it works

Whether a system has exactly one solution depends only on the coefficient matrix. Here the second row of coefficients is $a$ times the first, for every $a$. The two equations always describe parallel (or identical) lines:

- for $a\neq0$, the second equation is $x+y=\frac4a$, a line parallel to $x+y=2$;
- the lines coincide exactly when $\frac4a=2$, that is $a=2$;
- for $a=0$, the second equation has no solutions at all.

Two parallel lines never meet in exactly one point. So only two of the three theoretically possible cases occur.

---

## Check

- $a=2$, $s=0$: $(x,y)=(2,0)$. Then $2+0=2$ ✓ and $2\cdot2+2\cdot0=4$ ✓.
- $a=2$, $s=5$: $(x,y)=(-3,5)$. Then $-3+5=2$ ✓ and $-6+10=4$ ✓.
- $a=1$: the equations become $x+y=2$ and $x+y=4$, which contradict each other ✓.
- $a=0$: the second equation becomes $0=4$, impossible ✓.
