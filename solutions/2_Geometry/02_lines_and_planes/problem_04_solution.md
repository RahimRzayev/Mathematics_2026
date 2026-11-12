# Problem 4. Plane Through Three Points

## Exercise

### Exercise 4. Plane Through Three Points
Find the equation of the plane through

$$
A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).
$$

First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

> **Why this exercise:** connects earlier vector tools with constructing the equation of a plane.

---

## Answer

$$
\overrightarrow{AB}=(-1,1,0),\qquad \overrightarrow{AC}=(-1,0,1),\qquad n=\overrightarrow{AB}\times\overrightarrow{AC}=(1,1,1)
$$

The plane is

$$
x+y+z=1
$$

All three points satisfy it.

---

## Steps

### Step 1. Two vectors in the plane

The points $A$, $B$, $C$ lie in the plane, so the vectors joining them lie in it as well:

$$
\overrightarrow{AB}=B-A=(-1,1,0),\qquad \overrightarrow{AC}=C-A=(-1,0,1)
$$

### Step 2. Normal vector from the cross product

The cross product is perpendicular to both vectors, so it is perpendicular to the plane:

$$
\begin{aligned}
\overrightarrow{AB}\times\overrightarrow{AC} &= (1\cdot1-0\cdot0,\ 0\cdot(-1)-(-1)\cdot1,\ (-1)\cdot0-1\cdot(-1)) \\
&= (1,\ 1,\ 1)
\end{aligned}
$$

Therefore $n=(1,1,1)$.

### Step 3. Plane equation

The plane passes through $A$ and has normal $n$:

$$
n\cdot(X-A)=0\quad\Longrightarrow\quad 1\cdot(x-1)+1\cdot y+1\cdot z=0\quad\Longrightarrow\quad x+y+z=1
$$

### Step 4. Check on all three points

$$
A:\ 1+0+0=1\ \checkmark,\qquad B:\ 0+1+0=1\ \checkmark,\qquad C:\ 0+0+1=1\ \checkmark
$$

---

## Why it works

**Three points give two directions.** A plane equation needs a normal vector, and the points do not provide one directly. They provide two directions lying in the plane. The cross product converts two in-plane directions into the one direction perpendicular to both.

**The points are not on one line.** The result $n\neq0$ shows that $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are not parallel. The three points therefore determine exactly one plane.

**Perpendicular to two directions means perpendicular to the plane.** Every vector in the plane is a combination $s\overrightarrow{AB}+t\overrightarrow{AC}$, and its dot product with $n$ is $s\cdot0+t\cdot0=0$.

**Intercept form.** The points $A$, $B$, $C$ are the points where the plane crosses the three coordinate axes, each at distance $1$ from the origin. A plane with axis intercepts $a$, $b$, $c$ has the equation $\frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1$, which here gives $x+y+z=1$ directly.

---

## Check

The normal is perpendicular to both in-plane vectors:

$$
n\cdot\overrightarrow{AB}=-1+1+0=0\ \checkmark,\qquad n\cdot\overrightarrow{AC}=-1+0+1=0\ \checkmark
$$

A different pair of in-plane vectors gives the same normal. With $\overrightarrow{BC}=(0,-1,1)$,

$$
\overrightarrow{AB}\times\overrightarrow{BC}=(1\cdot1-0\cdot(-1),\ 0\cdot0-(-1)\cdot1,\ (-1)\cdot(-1)-1\cdot0)=(1,1,1)\ \checkmark
$$

Using $B$ instead of $A$ as the base point gives the same equation:

$$
1\cdot x+1\cdot(y-1)+1\cdot z=0\quad\Longrightarrow\quad x+y+z=1\ \checkmark
$$
