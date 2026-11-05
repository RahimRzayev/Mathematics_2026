# Problem 4. Dot Product and Perpendicularity

## Exercise

### Exercise 4. Dot Product and Perpendicularity
For $u=(1,2,-1)$ and $v=(2,-1,3)$ compute $u\cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w=(2,-1,a)$ is perpendicular to $u$, and check the result.

> **Why this exercise:** shows the dot product as both a test and a tool for constructing a perpendicularity condition.

---

## Answer

- $u\cdot v=-3\neq0$, so $u$ and $v$ are not perpendicular.
- $a=0$, so $w=(2,-1,0)$ is perpendicular to $u$.

---

## Steps

### Step 1. Compute the dot product

The dot product is the sum of the products of corresponding coordinates:

$$
u\cdot v=1\cdot2+2\cdot(-1)+(-1)\cdot3=2-2-3=-3
$$

### Step 2. Apply the test

Two nonzero vectors are perpendicular exactly when their dot product equals $0$. Here $u\cdot v=-3\neq0$, so $u$ and $v$ are not perpendicular.

### Step 3. Write the condition for $w$

The requirement $w\perp u$ is equivalent to the equation $u\cdot w=0$:

$$
u\cdot w=1\cdot2+2\cdot(-1)+(-1)\cdot a=2-2-a=-a
$$

### Step 4. Solve for $a$

$$
-a=0\quad\Longrightarrow\quad a=0
$$

Therefore $w=(2,-1,0)$.

---

## Why it works

The dot product and the angle $\theta$ between two vectors are related by

$$
u\cdot v=\|u\|\,\|v\|\cos\theta
$$

For nonzero vectors the lengths are positive, so the dot product vanishes exactly when $\cos\theta=0$, that is, when $\theta=90^\circ$.

This single relation gives the dot product two roles:

- **Test.** For given vectors, the sign and value of $u\cdot v$ can be computed. A nonzero result excludes perpendicularity.
- **Construction.** With an unknown coordinate, $u\cdot w=0$ is a linear equation in that unknown. Solving it produces a vector with the required property.

In this exercise the first two terms of $u\cdot w$ cancel, so the equation reduces to $-a=0$ and the solution is unique.

---

## Check

Substituting $a=0$ into the dot product confirms the condition:

$$
u\cdot w=(1,2,-1)\cdot(2,-1,0)=2-2+0=0\ \checkmark
$$

The first result is consistent with the angle formula. Here $\|u\|=\sqrt6$ and $\|v\|=\sqrt{14}$, so

$$
\cos\theta=\frac{-3}{\sqrt6\,\sqrt{14}}=\frac{-3}{\sqrt{84}}\approx-0.327
$$

The cosine is negative and nonzero, so the angle is obtuse and is not $90^\circ$ ✓.
