# Problem 12. A Normal Vector to a Plane

## Exercise

### Exercise 12. A Normal Vector to a Plane
Given $A=(1,0,2)$, $B=(2,1,0)$, and $C=(0,3,1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

> **Why this exercise:** creates a direct bridge from vectors to the description of a plane.

---

## Answer

$$
\overrightarrow{AB}=(1,1,-2),\qquad \overrightarrow{AC}=(-1,3,-1),\qquad n=\overrightarrow{AB}\times\overrightarrow{AC}=(5,3,4)
$$

Both dot products vanish: $n\cdot\overrightarrow{AB}=0$ and $n\cdot\overrightarrow{AC}=0$.

---

## Steps

### Step 1. Two vectors in the plane

The points $A$, $B$, $C$ lie in the plane, so the vectors joining them lie in it as well:

$$
\overrightarrow{AB}=B-A=(1,1,-2),\qquad \overrightarrow{AC}=C-A=(-1,3,-1)
$$

### Step 2. Vector perpendicular to both

The cross product of two vectors is perpendicular to each of them:

$$
\begin{aligned}
\overrightarrow{AB}\times\overrightarrow{AC} &= (1\cdot(-1)-(-2)\cdot3,\ (-2)\cdot(-1)-1\cdot(-1),\ 1\cdot3-1\cdot(-1)) \\
 &= (-1+6,\ 2+1,\ 3+1) \\
 &= (5,3,4)
\end{aligned}
$$

Therefore $n=(5,3,4)$.

### Step 3. Check with dot products

$$
n\cdot\overrightarrow{AB}=5\cdot1+3\cdot1+4\cdot(-2)=5+3-8=0
$$

$$
n\cdot\overrightarrow{AC}=5\cdot(-1)+3\cdot3+4\cdot(-1)=-5+9-4=0
$$

---

## Why it works

**The three points determine a plane.** The result $n\neq0$ shows that $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are not parallel, so $A$, $B$, $C$ are not on one line and exactly one plane passes through them.

**Perpendicular to two directions means perpendicular to the plane.** Every vector in the plane is a combination $s\overrightarrow{AB}+t\overrightarrow{AC}$, and

$$
n\cdot\left(s\overrightarrow{AB}+t\overrightarrow{AC}\right)=s\,(n\cdot\overrightarrow{AB})+t\,(n\cdot\overrightarrow{AC})=0
$$

Checking two independent directions therefore covers the entire plane.

**Bridge to the description of a plane.** A point $X=(x,y,z)$ lies in the plane exactly when $\overrightarrow{AX}$ is perpendicular to $n$:

$$
5(x-1)+3y+4(z-2)=0\quad\Longleftrightarrow\quad 5x+3y+4z=13
$$

The normal vector is not unique: every nonzero multiple of $n$ describes the same plane, because only its direction matters.

---

## Check

All three points satisfy the plane equation obtained from $n$:

$$
A:\ 5+0+8=13\ \checkmark,\qquad B:\ 10+3+0=13\ \checkmark,\qquad C:\ 0+9+4=13\ \checkmark
$$

A different pair of in-plane vectors must give a parallel normal. With $\overrightarrow{BC}=(-2,2,1)$,

$$
\overrightarrow{AB}\times\overrightarrow{BC}=(1\cdot1-(-2)\cdot2,\ (-2)\cdot(-2)-1\cdot1,\ 1\cdot2-1\cdot(-2))=(5,3,4)\ \checkmark
$$
