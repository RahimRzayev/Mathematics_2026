# Problem 9. Distances

## Exercise

### Exercise 9. Distances
Compute:

1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

> **Why this exercise:** organizes two similar formulas through one geometric idea.

---

## Answer

1. Distance from $P$ to the line: $\frac85=1.6$.
2. Distance from $Q$ to the plane: $\frac53\approx1.67$.

Both formulas are one formula: substitute the point into the left side of the equation, take the absolute value, and divide by the length of the normal vector.

---

## Steps

### Step 1. Formula for a point and a line in the plane

For the line $ax+by+c=0$ and the point $(x_0,y_0)$:

$$
d=\frac{|ax_0+by_0+c|}{\sqrt{a^2+b^2}}
$$

### Step 2. Distance from $P$ to the line

$$
d=\frac{|3\cdot2+4\cdot3-10|}{\sqrt{3^2+4^2}}=\frac{|6+12-10|}{\sqrt{25}}=\frac85
$$

### Step 3. Formula for a point and a plane in space

For the plane $ax+by+cz+e=0$ and the point $(x_0,y_0,z_0)$:

$$
d=\frac{|ax_0+by_0+cz_0+e|}{\sqrt{a^2+b^2+c^2}}
$$

### Step 4. Distance from $Q$ to the plane

$$
d=\frac{|2\cdot2-2\cdot(-1)+3-4|}{\sqrt{2^2+(-2)^2+1^2}}=\frac{|4+2+3-4|}{\sqrt9}=\frac53
$$

---

## Why it works

**One formula in vector form.** A line in the plane and a plane in space are both described by one linear equation $n\cdot X+c=0$, where $n$ is a normal vector. For the line $n=(3,4)$, for the plane $n=(2,-2,1)$. Both distance formulas are

$$
d=\frac{|n\cdot X_0+c|}{\Vert n\Vert}
$$

The only difference is the number of coordinates.

**Why the normal direction appears.** The shortest path from a point to a line or a plane is perpendicular to it, so it runs along $n$. Let $A$ be any point of the line or plane, so that $n\cdot A+c=0$. The distance is the length of the projection of $X_0-A$ onto the normal direction:

$$
d=\frac{|n\cdot(X_0-A)|}{\Vert n\Vert}=\frac{|n\cdot X_0-n\cdot A|}{\Vert n\Vert}=\frac{|n\cdot X_0+c|}{\Vert n\Vert}
$$

The point $A$ disappears from the result. Only the component of $X_0-A$ along the normal counts. The component along the line or plane does not change the distance.

**Meaning of the two parts.**

- The numerator is the value of the equation at the point. It is zero on the line or plane and grows in proportion to the distance from it.
- The denominator removes the dependence on the scale of the equation. Multiplying the equation by a constant multiplies the numerator and $\Vert n\Vert$ by the same factor.

**Why a line in the plane behaves like a plane in space.** Each is described by a single equation and has exactly one perpendicular direction. A line in space has no single normal direction, so this formula does not apply to it.

---

## Check

Each distance is recomputed from the foot of the perpendicular, the point reached by moving from the given point along the normal.

**Line.** The value of the equation at $P$ is $8$ and $\Vert n\Vert^2=25$, so the foot is

$$
F=P-\frac{8}{25}\ (3,4)=\left(2-\frac{24}{25},\ 3-\frac{32}{25}\right)=\left(\frac{26}{25},\ \frac{43}{25}\right)
$$

$$
3\cdot\frac{26}{25}+4\cdot\frac{43}{25}-10=\frac{78+172}{25}-10=0\ \checkmark
$$

$$
\Vert P-F\Vert=\frac{8}{25}\ \Vert(3,4)\Vert=\frac{8}{25}\cdot5=\frac85\ \checkmark
$$

**Plane.** The value of the equation at $Q$ is $5$ and $\Vert n\Vert^2=9$, so the foot is

$$
G=Q-\frac59\ (2,-2,1)=\left(2-\frac{10}{9},\ -1+\frac{10}{9},\ 3-\frac59\right)=\left(\frac89,\ \frac19,\ \frac{22}{9}\right)
$$

$$
2\cdot\frac89-2\cdot\frac19+\frac{22}{9}-4=\frac{16-2+22}{9}-4=0\ \checkmark
$$

$$
\Vert Q-G\Vert=\frac59\ \Vert(2,-2,1)\Vert=\frac59\cdot3=\frac53\ \checkmark
$$
