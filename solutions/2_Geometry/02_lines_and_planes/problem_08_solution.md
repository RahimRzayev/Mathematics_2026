# Problem 8. Intersection Point of a Line and a Plane

## Exercise

### Exercise 8. Intersection Point of a Line and a Plane
Find the intersection point of

$$
(x,y,z)=(1,0,2)+t(1,2,-1)
$$

with the plane $x+y+z=4$. Check the result by substituting it into both descriptions.

> **Why this exercise:** practices the most important computational case of the line–plane relationship.

---

## Answer

$$
t=\frac12,\qquad Q=\left(\frac32,\ 1,\ \frac32\right)
$$

The point $Q$ lies on the line for $t=\frac12$ and satisfies the plane equation: $\frac32+1+\frac32=4$.

---

## Steps

### Step 1. Coordinates of a point of the line

$$
x=1+t,\qquad y=2t,\qquad z=2-t
$$

### Step 2. Substitute into the plane equation

$$
(1+t)+2t+(2-t)=4
$$

### Step 3. Solve for $t$

$$
3+2t=4\quad\Longrightarrow\quad t=\frac12
$$

### Step 4. Intersection point

$$
Q=(1,0,2)+\frac12\ (1,2,-1)=\left(1+\frac12,\ 0+1,\ 2-\frac12\right)=\left(\frac32,\ 1,\ \frac32\right)
$$

---

## Why it works

The line is given in parametric form, which generates points. The plane is given in general form, which tests points. Substituting the first into the second asks which generated point passes the test. The three unknown coordinates are replaced by the single unknown $t$, so one linear equation is enough.

**A unique solution was expected.** With $v=(1,2,-1)$ and $n=(1,1,1)$,

$$
v\cdot n=1+2-1=2\neq0
$$

The line is not parallel to the plane, so it crosses the plane exactly once. This value $2$ is the coefficient of $t$ in the equation $3+2t=4$.

**General formula.** For a line $P_0+tv$ and a plane $n\cdot X=d$,

$$
t=\frac{d-n\cdot P_0}{n\cdot v}=\frac{4-3}{2}=\frac12
$$

The numerator measures how far the starting point is from satisfying the plane equation. The denominator measures how fast the line closes this gap.

---

## Check

**Line.** The value $t=\frac12$ gives the same point in each coordinate:

$$
x=1+\frac12=\frac32\ \checkmark,\qquad y=2\cdot\frac12=1\ \checkmark,\qquad z=2-\frac12=\frac32\ \checkmark
$$

**Plane.**

$$
\frac32+1+\frac32=4\ \checkmark
$$

**Sign change.** The points of the line on the two sides of $Q$ lie on opposite sides of the plane. For $t=0$ and $t=1$:

$$
(1,0,2):\ 1+0+2=3\lt4,\qquad (2,2,1):\ 2+2+1=5\gt4\ \checkmark
$$

The value of $x+y+z$ passes from below $4$ to above $4$, so the line crosses the plane between these two points, at the midpoint value $t=\frac12$.
