# Problem 7. Linear Dependence Without Heavy Computation

## Exercise

### Exercise 7. Linear Dependence Without Heavy Computation
Given

$$
u=(1,2,3),\qquad v=(2,4,6),\qquad w=(0,1,1).
$$

Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

> **Why this exercise:** develops the habit of recognizing structure before applying a computational procedure.

---

## Answer

- Relation: $v=2u$.
- The vectors $u,v,w$ cannot be linearly independent, because $2u-v+0\cdot w=0$ is a nontrivial relation.
- No long calculation is needed, because this relation exists for any third vector $w$.

---

## Steps

### Step 1. Compare the coordinates of $u$ and $v$

Each coordinate of $v$ is twice the corresponding coordinate of $u$:

$$
2=2\cdot1,\qquad 4=2\cdot2,\qquad 6=2\cdot3
$$

Therefore $v=2u$.

### Step 2. Rewrite as a linear relation

Moving all terms to one side and including $w$ with coefficient $0$ gives

$$
2u-v+0\cdot w=0
$$

### Step 3. Apply the definition

Vectors are linearly independent only if the zero combination with all coefficients equal to $0$ is the only combination that gives the zero vector. The relation in Step 2 has coefficients $(2,-1,0)$, which are not all zero. The three vectors are therefore linearly dependent.

---

## Why it works

**The coefficient of $w$ does not matter.** The coefficient $0$ removes $w$ from the relation, so the conclusion holds for every choice of $w$. A set containing a dependent subset is always dependent.

**No determinant or elimination is required.** Those procedures answer the question for vectors with no visible relation. Here the relation is visible directly from the coordinates, and a single nontrivial relation is sufficient evidence.

**Geometric meaning.** The vectors $u$ and $v$ lie on one line through the origin. They contribute only one direction, so together with $w$ at most two directions are available. Three independent vectors in $\mathbb R^3$ would have to supply three directions.

The vector $w$ is not a multiple of $u$, because its first coordinate is $0$ while its other coordinates are not. The three vectors therefore span a plane, not all of $\mathbb R^3$.

---

## Check

Substituting into the relation gives the zero vector:

$$
2(1,2,3)-(2,4,6)+0\cdot(0,1,1)=(2-2,\ 4-4,\ 6-6)=(0,0,0)\ \checkmark
$$

An independent check uses the matrix whose rows are the three vectors. Its first two rows are proportional, so its determinant must vanish:

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 1 \\
\end{pmatrix}=1\cdot(4-6)-2\cdot(2-0)+3\cdot(2-0)=-2-4+6=0\ \checkmark
$$
