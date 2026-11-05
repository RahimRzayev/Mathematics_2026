# Problem 3. Vector Normalization

## Exercise

### Exercise 3. Vector Normalization
For $v=(3,4)$ find a unit vector $e$ with the same direction and orientation. Check that $\|e\|=1$, reconstruct $v$ in the form $v=\|v\|e$, and explain what changes during normalization and what remains unchanged.

> **Why this exercise:** teaches how to separate direction from vector length.

---

## Answer

$$
e=\left(\frac35,\frac45\right)
$$

- Changes: the length, from $\|v\|=5$ to $\|e\|=1$.
- Remains unchanged: the direction and the orientation.

---

## Steps

### Step 1. Length of the vector

$$
\|v\|=\sqrt{3^2+4^2}=\sqrt{25}=5
$$

### Step 2. Divide by the length

Since $v\neq0$, division by $\|v\|$ is allowed:

$$
e=\frac{v}{\|v\|}=\frac15(3,4)=\left(\frac35,\frac45\right)
$$

### Step 3. Check the unit length

$$
\|e\|=\sqrt{\left(\frac35\right)^2+\left(\frac45\right)^2}=\sqrt{\frac{9}{25}+\frac{16}{25}}=\sqrt{\frac{25}{25}}=1
$$

### Step 4. Reconstruct $v$

$$
\|v\|e=5\left(\frac35,\frac45\right)=(3,4)=v
$$

---

## Why it works

For a scalar $c$, the length of a multiple satisfies

$$
\|cv\|=|c|\,\|v\|
$$

Choosing $c=\frac{1}{\|v\|}$ gives length exactly $1$:

$$
\|e\|=\frac{1}{\|v\|}\,\|v\|=1
$$

The scalar $c=\frac15$ affects the two properties of the vector differently:

- It is a multiple of $v$, so $e$ lies on the same line through the origin. The direction is unchanged.
- It is positive, so $e$ points the same way along that line. The orientation is unchanged.
- It is not equal to $1$, so the length changes.

The form $v=\|v\|e$ separates the vector into two independent pieces of information: how long it is ($5$) and where it points ($e$).

The vector $-e=\left(-\frac35,-\frac45\right)$ is also a unit vector on the same line, but it has the opposite orientation. It does not satisfy the requirement of the exercise.

---

## Check

The direction is confirmed by the ratio of the coordinates, which is the same for both vectors:

$$
\frac{4}{3}=\frac{4/5}{3/5}\ \checkmark
$$

The orientation is confirmed by the dot product, which equals the product of the lengths when the angle is $0$:

$$
v\cdot e=3\cdot\frac35+4\cdot\frac45=\frac{9+16}{5}=5=\|v\|\,\|e\|\ \checkmark
$$
