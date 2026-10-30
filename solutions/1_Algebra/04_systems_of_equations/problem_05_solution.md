# Problem 5. Row Echelon Form and Number of Solutions

## Exercise

### Exercise 5. Row Echelon Form and Number of Solutions
For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

> **Why this exercise:** teaches how to read information about solutions directly from row echelon form.

---

## Answer

Infinitely many solutions, with one free variable $x_3=t$, $t\in\mathbb{R}$:

$$
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
\end{pmatrix}=
\begin{pmatrix}
1+5t \\
1-2t \\
t \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}+t
\begin{pmatrix}
5 \\
-2 \\
1 \\
\end{pmatrix}
$$

---

## Steps

### Step 1. Check consistency

The only zero row on the coefficient side is row 3, and its right-hand side is $0$. It reads $0=0$. No contradiction appears, so the system is consistent.

### Step 2. Locate the pivots

- Row 1: pivot in column 1 ($x_1$).
- Row 2: pivot in column 2 ($x_2$).
- Column 3 ($x_3$) has no pivot.

Free variables are those without a pivot:

$$
3\ \mathrm{unknowns}-2\ \mathrm{pivots}=1\ \mathrm{free\ variable}
$$

### Step 3. Write the equations

$$
\begin{cases}
x_1+2x_2-x_3=3, \\
x_2+2x_3=1.
\end{cases}
$$

### Step 4. Back substitution with $x_3=t$

From row 2:

$$
x_2=1-2t
$$

From row 1:

$$
x_1=3-2x_2+x_3=3-2(1-2t)+t=1+5t
$$

---

## Why it works

Row echelon form answers both questions directly:

1. **Consistency.** A row $(0\ \ 0\ \ 0\mid c)$ with $c\neq0$ means no solution. Here no such row exists.
2. **Number of solutions.** If consistent, each pivot column gives one dependent unknown and each non-pivot column gives one free unknown.
   - No free unknowns: exactly one solution.
   - At least one free unknown: infinitely many solutions.

Here one free unknown remains, so the solution set is a line in $\mathbb{R}^3$.

---

## Check

Take $t=1$: $(x_1,x_2,x_3)=(6,\ -1,\ 1)$.

- Row 1: $6+2(-1)-1=3$ ✓
- Row 2: $-1+2\cdot1=1$ ✓

General check for arbitrary $t$:

- Row 1: $(1+5t)+2(1-2t)-t=1+2+5t-4t-t=3$ ✓
- Row 2: $(1-2t)+2t=1$ ✓
