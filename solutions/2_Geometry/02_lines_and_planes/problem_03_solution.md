# Problem 3. Plane Through a Point with a Given Normal Vector

## Exercise

### Exercise 3. Plane Through a Point with a Given Normal Vector
Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

> **Why this exercise:** shows the basic construction of a plane from a point and a normal vector.

---

## Answer

$$
2x+y-z+3=0
$$

Equivalently, $2x+y-z=-3$. The point $P$ satisfies it: $2\cdot1+(-2)-3+3=0$.

The normal vector fixes the orientation of the plane: its components are the coefficients of $x$, $y$, $z$. The point $P$ fixes the position of the plane, which determines the constant term.

---

## Steps

### Step 1. Condition for a point of the plane

A point $X=(x,y,z)$ lies in the plane exactly when the vector from $P$ to $X$ is perpendicular to $n$:

$$
n\cdot(X-P)=0
$$

### Step 2. Write the condition in coordinates

$$
X-P=(x-1,\ y+2,\ z-3)
$$

$$
2(x-1)+1\cdot(y+2)+(-1)\cdot(z-3)=0
$$

### Step 3. Simplify

$$
\begin{aligned}
2x-2+y+2-z+3 &= 0 \\
2x+y-z+3 &= 0
\end{aligned}
$$

### Step 4. Substitute $P$

$$
2\cdot1+(-2)-3+3=2-2-3+3=0\ \checkmark
$$

---

## Why it works

**The normal vector sets the orientation.** A plane contains infinitely many directions, so no single direction vector describes it. There is only one direction perpendicular to the plane, and the normal vector records it. Every vector lying in the plane is perpendicular to $n$.

**The point sets the position.** All planes with normal $n=(2,1,-1)$ have the form $2x+y-z=d$ and are parallel to each other. The value of $d$ selects one of them. Requiring the plane to pass through $P$ gives

$$
d=n\cdot P=2\cdot1+1\cdot(-2)+(-1)\cdot3=-3
$$

**Reading the equation.** In the equation $2x+y-z+3=0$ the coefficients $(2,1,-1)$ are the components of $n$. A normal vector can therefore be read directly from any plane equation.

The normal vector is not unique. Any nonzero multiple gives the same plane, for example $-4x-2y+2z-6=0$.

---

## Check

Another point of the plane gives a vector perpendicular to $n$. The point $Q=(0,0,3)$ satisfies the equation, since $0+0-3+3=0$, and

$$
\overrightarrow{PQ}=(-1,2,0),\qquad n\cdot\overrightarrow{PQ}=2\cdot(-1)+1\cdot2+(-1)\cdot0=0\ \checkmark
$$

Moving from $P$ along the normal leaves the plane. The point $P+n=(3,-1,2)$ gives

$$
2\cdot3+(-1)-2+3=6\neq0\ \checkmark
$$

The value $6$ equals $n\cdot n=4+1+1$, as expected for a step of exactly one normal vector away from the plane.
