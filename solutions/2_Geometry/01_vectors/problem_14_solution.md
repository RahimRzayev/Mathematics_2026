# Problem 14. Closest Point on a Line

## Exercise

### Exercise 14. Closest Point on a Line
Given a point $P=(4,1)$ and a line through the origin with direction $v=(1,2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

> **Why this exercise:** shows projection as a complete solution to a minimum-distance problem.

---

## Answer

- Closest point: $Q=\left(\frac65,\frac{12}{5}\right)$.
- Distance: $\Vert P-Q\Vert=\frac{7}{\sqrt5}=\frac{7\sqrt5}{5}\approx3.13$.
- Perpendicularity: $(P-Q)\cdot v=0$.

---

## Steps

### Step 1. Treat $P$ as a vector

The line passes through the origin, so the point $P$ corresponds to the vector $\overrightarrow{OP}=(4,1)$. The closest point is the projection of this vector onto $v$:

$$
Q=\mathrm{proj}_v\ P=\frac{P\cdot v}{v\cdot v}\ v
$$

### Step 2. The two dot products

$$
P\cdot v=4\cdot1+1\cdot2=6,\qquad v\cdot v=1^2+2^2=5
$$

### Step 3. Closest point

$$
Q=\frac65\ (1,2)=\left(\frac65,\frac{12}{5}\right)
$$

### Step 4. Vector from $Q$ to $P$

$$
P-Q=\left(\frac{20}{5}-\frac65,\ \frac55-\frac{12}{5}\right)=\left(\frac{14}{5},-\frac75\right)
$$

### Step 5. Distance

$$
\Vert P-Q\Vert=\sqrt{\frac{196}{25}+\frac{49}{25}}=\sqrt{\frac{245}{25}}=\frac{7\sqrt5}{5}=\frac{7}{\sqrt5}
$$

### Step 6. Perpendicularity

The appropriate vector is $P-Q$, which joins the closest point to $P$:

$$
(P-Q)\cdot v=\frac{14}{5}\cdot1+\left(-\frac75\right)\cdot2=\frac{14}{5}-\frac{14}{5}=0
$$

---

## Why it works

The projection gives the minimum distance, not only a candidate for it. Let $X$ be any point on the line. Both $Q$ and $X$ are multiples of $v$, so $Q-X$ is parallel to $v$ and is perpendicular to $P-Q$. Since

$$
P-X=(P-Q)+(Q-X)
$$

the Pythagorean theorem gives

$$
\Vert P-X\Vert^2=\Vert P-Q\Vert^2+\Vert Q-X\Vert^2\ge\Vert P-Q\Vert^2
$$

Equality holds only when $X=Q$. Therefore $Q$ is the unique closest point, and every other point on the line is strictly farther from $P$.

Geometrically, the shortest segment from a point to a line is the perpendicular segment. Any other segment is the hypotenuse of a right triangle whose leg is the perpendicular segment.

---

## Check

The point $Q$ lies on the line, since $Q=\frac65v$ ✓.

The distance agrees with the point-to-line formula. The line has the equation $2x-y=0$, so

$$
d=\frac{|2\cdot4-1|}{\sqrt{2^2+(-1)^2}}=\frac{7}{\sqrt5}\ \checkmark
$$

A nearby point on the line is farther away. For $X=v=(1,2)$, the distance satisfies

$$
\Vert P-X\Vert^2=3^2+(-1)^2=10>\frac{49}{5}=\Vert P-Q\Vert^2\ \checkmark
$$
