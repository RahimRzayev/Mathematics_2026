# Problem 3. When Can Matrices Be Multiplied?

## Exercise

### Exercise 3. When Can Matrices Be Multiplied?
The matrix sizes are

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.
$$

For the products

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

> **Why this exercise:** forces an understanding of dimension compatibility before carrying out any calculation.

---

## Answer

Sizes: $A$ is $2\times 3$, $B$ is $3\times 4$, $C$ is $4\times 2$, $D$ is $2\times 2$.

| Product | Inner pair | Defined? | Size of result |
|---|---|---|---|
| $AB$ | $3$ and $3$ | Yes | $2\times 4$ |
| $BA$ | $4$ and $2$ | No | — |
| $BC$ | $4$ and $4$ | Yes | $3\times 2$ |
| $CB$ | $2$ and $3$ | No | — |
| $AC$ | $3$ and $4$ | No | — |
| $CA$ | $2$ and $2$ | Yes | $4\times 3$ |
| $AD$ | $3$ and $2$ | No | — |
| $DA$ | $2$ and $2$ | Yes | $2\times 3$ |

---

## Steps

### Step 1. Apply the rule

For $XY$ to exist:

- **Inner pair:** columns of $X$ must equal rows of $Y$.
- **Size of $XY$:** rows of $X$ by columns of $Y$. The outer numbers give the answer.

### Step 2. Worked examples

- $AB$: inner pair $3$ and $3$ match. Defined. Size $2\times 4$.
- $BA$: inner pair $4$ and $2$ differ. Not defined.

Write the two sizes side by side, then compare the inner numbers.

---

## Why it works

Each entry of $XY$ is a row of $X$ times a column of $Y$. Both must have the same length, and that length is the inner number.

A product can exist in one order and not the other. $AB$ exists, but $BA$ does not. So matrix multiplication is not just non-commutative: the order may not be reversible at all.

---

## Check

Outer sizes of $DA$: $2$ and $3$, giving $2\times 3$. This matches the table. ✓
