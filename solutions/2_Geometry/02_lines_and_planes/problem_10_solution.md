# Problem 10. Projection of a Point onto a Plane

## Exercise

### Exercise 10. Projection of a Point onto a Plane
Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

> **Why this exercise:** combines the normal, intersection, and distance into the construction of a projection and reflection.

---

## Answer

- Projection: $Q=(1,0,2)$.
- Reflection: $P'=(0,-1,1)$.
- The midpoint of $PP'$ is $(1,0,2)=Q$, and $1+0+2=3$, so it lies on the plane.

---

## Steps

### Step 1. Line through $P$ along the normal

The projection is reached by moving from $P$ perpendicularly to the plane, which means along the normal $n=(1,1,1)$:

$$
X(t)=P+tn=(2+t,\ 1+t,\ 3+t)
$$

### Step 2. Intersection with the plane

$$
(2+t)+(1+t)+(3+t)=3\quad\Longrightarrow\quad 6+3t=3\quad\Longrightarrow\quad t=-1
$$

### Step 3. Projection

$$
Q=X(-1)=(2-1,\ 1-1,\ 3-1)=(1,0,2)
$$

### Step 4. Reflection

The reflection lies on the same normal line, at the same distance on the other side of the plane. The parameter value is doubled:

$$
P'=X(-2)=(2-2,\ 1-2,\ 3-2)=(0,-1,1)
$$

Equivalently, $P'=2Q-P=(2,0,4)-(2,1,3)=(0,-1,1)$.

### Step 5. Midpoint

$$
\frac{P+P'}{2}=\left(\frac{2+0}{2},\ \frac{1-1}{2},\ \frac{3+1}{2}\right)=(1,0,2)
$$

$$
1+0+2=3\ \checkmark
$$

The midpoint is the projection $Q$ and lies on the plane.

---

## Why it works

The construction uses three tools from this set in sequence.

**The normal gives the direction.** The orthogonal projection is the point of the plane for which $P-Q$ is perpendicular to the plane. The only direction perpendicular to the plane is $n$, so $Q$ lies on the line $P+tn$.

**The intersection gives the point.** The projection is the point where this normal line meets the plane. The equation has a unique solution because the direction of the line is $n$ itself and $n\cdot n=3\neq0$.

**The parameter gives the distance.** The value $t=-1$ means that the plane is reached after one step of $-n$. The distance from $P$ to the plane is

$$
\Vert P-Q\Vert=|t|\ \Vert n\Vert=\sqrt3
$$

**Reflection as a double step.** The reflection continues the same motion for an equal distance beyond the plane: $P'=P+2tn$. The projection $Q=P+tn$ is then exactly halfway between $P$ and $P'$, which is why the midpoint lies on the plane.

In closed form, for a plane $n\cdot X=d$:

$$
t=\frac{d-n\cdot P}{n\cdot n}=\frac{3-6}{3}=-1,\qquad Q=P+tn,\qquad P'=P+2tn
$$

---

## Check

The segment from $P$ to $Q$ is perpendicular to the plane, since it is a multiple of the normal:

$$
P-Q=(1,1,1)=n\ \checkmark
$$

The distance agrees with the point-to-plane formula:

$$
d=\frac{|2+1+3-3|}{\sqrt{1+1+1}}=\frac{3}{\sqrt3}=\sqrt3\ \checkmark
$$

The point and its reflection lie on opposite sides of the plane at equal distances. The expression $x+y+z-3$ takes opposite values at the two points:

$$
P:\ 2+1+3-3=3,\qquad P':\ 0-1+1-3=-3\ \checkmark
$$

Reflecting $P'$ returns $P$. For $P'$ the parameter is $t=\frac{3-0}{3}=1$, and

$$
P'+2n=(0,-1,1)+(2,2,2)=(2,1,3)=P\ \checkmark
$$
