# Problem 15. Complete Classification of a Line Relative to a Plane

## Exercise

### Exercise 15. Complete Classification of a Line Relative to a Plane
Let

$$
L:p+tv,\qquad \Pi:n\cdot x=d.
$$

State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

> **Why this exercise:** requires formulating a general mathematical criterion instead of carrying out one isolated calculation.

---

## Answer

| Case | Condition on the direction | Condition on the point |
|---|---|---|
| One intersection point | $n\cdot v\neq0$ | none |
| Parallel, no common points | $n\cdot v=0$ | $n\cdot p\neq d$ |
| Line contained in the plane | $n\cdot v=0$ | $n\cdot p=d$ |

In the first case the intersection point corresponds to

$$
t=\frac{d-n\cdot p}{n\cdot v}
$$

Examples for the plane $x+y+z=3$, with $n=(1,1,1)$ and $d=3$:

| Line | $n\cdot v$ | $n\cdot p$ | Result |
|---|---|---|---|
| $(0,0,0)+t(1,1,1)$ | $3$ | $0$ | one point, $(1,1,1)$ |
| $(0,0,0)+t(1,-1,0)$ | $0$ | $0$ | parallel, no common points |
| $(1,1,1)+t(1,-1,0)$ | $0$ | $3$ | contained in the plane |

---

## Steps

### Step 1. Substitute the line into the plane equation

A point $p+tv$ of the line lies in the plane exactly when

$$
n\cdot(p+tv)=d
$$

### Step 2. Reduce to one linear equation for $t$

The dot product is linear, so

$$
n\cdot p+t\ (n\cdot v)=d\quad\Longrightarrow\quad (n\cdot v)\ t=d-n\cdot p
$$

This is an equation of the form $at=b$ with

$$
a=n\cdot v,\qquad b=d-n\cdot p
$$

### Step 3. Classify the solutions of $at=b$

- If $a\neq0$, there is exactly one solution, $t=\frac{b}{a}$.
- If $a=0$ and $b\neq0$, the equation reads $0=b$ and has no solution.
- If $a=0$ and $b=0$, the equation reads $0=0$ and every $t$ is a solution.

### Step 4. Translate into geometry

- $n\cdot v\neq0$: exactly one point of the line lies in the plane. The line intersects the plane.
- $n\cdot v=0$ and $n\cdot p\neq d$: no point of the line lies in the plane. The line is parallel to the plane.
- $n\cdot v=0$ and $n\cdot p=d$: every point of the line lies in the plane. The line is contained in the plane.

### Step 5. Example of one intersection point

Line $(0,0,0)+t(1,1,1)$:

$$
n\cdot v=1+1+1=3\neq0,\qquad t=\frac{3-0}{3}=1
$$

The intersection point is $(1,1,1)$.

### Step 6. Example of a parallel line

Line $(0,0,0)+t(1,-1,0)$:

$$
n\cdot v=1-1+0=0,\qquad n\cdot p=0\neq3
$$

Substituting the line gives $t-t+0=3$, which is $0=3$. There is no common point.

### Step 7. Example of a contained line

Line $(1,1,1)+t(1,-1,0)$:

$$
n\cdot v=1-1+0=0,\qquad n\cdot p=1+1+1=3=d
$$

Substituting the line gives $(1+t)+(1-t)+1=3$, which is $3=3$ for every $t$.

---

## Why it works

**The classification is complete.** Every pair of numbers $a$, $b$ belongs to exactly one of the three cases in Step 3. No fourth case exists and no two cases overlap. A line and a plane can therefore never share exactly two points or any other finite number of points greater than one.

**Meaning of $n\cdot v$.** The value $n\cdot x$ measures the level of a point $x$ relative to the plane, and the plane is the level $d$. Along the line, this level changes at the constant rate $n\cdot v$ per unit of $t$.

- A nonzero rate means that the level passes through every value exactly once, including $d$.
- A zero rate means that the level stays at its starting value $n\cdot p$.

**Meaning of $n\cdot p$.** When the level is constant, the starting point decides everything. If the starting level equals $d$, the line stays in the plane. If it differs from $d$, the line never reaches the plane.

**Order of the tests.** The direction is tested first and the point second. The point test is needed only when $n\cdot v=0$. In the first case the position of $p$ changes where the intersection occurs, but not whether it occurs.

**The examples differ in one element.** The second and third lines have the same direction and differ only in the starting point. The first and second lines have the same starting point and differ only in direction. Each change switches exactly one condition of the criterion.

---

## Check

**First example.** The point $(1,1,1)$ lies on the line for $t=1$ and in the plane:

$$
1+1+1=3\ \checkmark
$$

**Second example.** Every point $(t,\ -t,\ 0)$ of the line is at the same nonzero distance from the plane:

$$
\frac{|t-t+0-3|}{\sqrt3}=\frac{3}{\sqrt3}=\sqrt3\ \checkmark
$$

**Third example.** Two different points of the line, for $t=0$ and $t=1$, lie in the plane:

$$
(1,1,1):\ 1+1+1=3\ \checkmark,\qquad (2,0,1):\ 2+0+1=3\ \checkmark
$$

**Agreement with the earlier exercises of this set.**

- Exercise 7: $n\cdot v=0$ and $n\cdot p=2=d$, so the line is contained in the plane ✓.
- Exercise 8: $n\cdot v=2\neq0$, so there is one intersection point, with $t=\frac{4-3}{2}=\frac12$ ✓.
- Exercise 14, second line: $n\cdot v=0$ and $n\cdot p=1\neq0=d$, so the line is parallel to the plane ✓.
