# Problem 13. Closest Point on a Plane

## Exercise

### Exercise 13. Closest Point on a Plane
Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

> **Why this exercise:** combines projection, distance, and the normal direction in one problem.

---

## Answer

- Closest point: $Q=\left(\frac{28}{9},\ \frac29,\ \frac29\right)$.
- Distance: $\Vert P-Q\Vert=\frac13$.
- Perpendicularity: $Q-P=\frac19\ (1,2,2)=\frac19\ n$, a multiple of the normal vector.

---

## Steps

### Step 1. Line through $P$ along the normal

The closest point is the orthogonal projection of $P$ onto the plane. It lies on the line through $P$ with direction $n=(1,2,2)$:

$$
X(t)=P+tn=(3+t,\ 2t,\ 2t)
$$

### Step 2. Intersection with the plane

$$
(3+t)+2\cdot2t+2\cdot2t=4\quad\Longrightarrow\quad 3+9t=4\quad\Longrightarrow\quad t=\frac19
$$

### Step 3. Closest point

$$
Q=X\left(\frac19\right)=\left(3+\frac19,\ \frac29,\ \frac29\right)=\left(\frac{28}{9},\ \frac29,\ \frac29\right)
$$

### Step 4. Distance

$$
Q-P=\frac19\ (1,2,2),\qquad \Vert n\Vert=\sqrt{1+4+4}=3
$$

$$
\Vert Q-P\Vert=\frac19\cdot3=\frac13
$$

### Step 5. Perpendicularity

The segment from $P$ to $Q$ is the vector $\frac19 n$. It is parallel to the normal, so it is perpendicular to the plane.

---

## Why it works

**The closest point is the projection.** Let $X$ be any point of the plane. The vector $X-Q$ joins two points of the plane, so it lies in the plane and is perpendicular to $Q-P$, which is parallel to $n$. Since

$$
X-P=(Q-P)+(X-Q)
$$

the Pythagorean theorem gives

$$
\Vert X-P\Vert^2=\Vert Q-P\Vert^2+\Vert X-Q\Vert^2\ge\Vert Q-P\Vert^2
$$

Equality holds only when $X=Q$. The projection is therefore the unique closest point, and every other point of the plane is strictly farther from $P$.

**The three ideas in one construction.**

- Normal direction: it gives the only direction in which the shortest segment can run.
- Projection: the intersection of the normal line with the plane gives the closest point.
- Distance: the parameter gives the length of the segment, $|t|\ \Vert n\Vert$.

**Size of the answer.** The point $P$ almost satisfies the equation: $3+0+0=3$, compared with $4$. The gap of $1$ divided by $\Vert n\Vert=3$ gives the small distance $\frac13$.

---

## Check

The point $Q$ lies on the plane:

$$
\frac{28}{9}+2\cdot\frac29+2\cdot\frac29=\frac{28+4+4}{9}=4\ \checkmark
$$

The distance agrees with the point-to-plane formula:

$$
d=\frac{|3+0+0-4|}{\sqrt{1+4+4}}=\frac13\ \checkmark
$$

The segment is perpendicular to two independent directions lying in the plane. The vectors $a=(2,-1,0)$ and $b=(0,1,-1)$ satisfy $n\cdot a=0$ and $n\cdot b=0$, so they lie in the plane, and

$$
(Q-P)\cdot a=\frac19\ (2-2+0)=0\ \checkmark,\qquad (Q-P)\cdot b=\frac19\ (0+2-2)=0\ \checkmark
$$

Another point of the plane is farther away. For $X=(4,0,0)$, which satisfies $4+0+0=4$,

$$
\Vert X-P\Vert=1\gt\frac13\ \checkmark
$$
