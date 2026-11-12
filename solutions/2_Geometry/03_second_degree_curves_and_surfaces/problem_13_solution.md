# Problem 13. Intersection of a Sphere and a Plane

## Exercise

### Exercise 13. Intersection of a Sphere and a Plane
Given the sphere

$$
x^2+y^2+z^2=25
$$

and the plane $z=3$, find the equation of the intersection curve and its radius. Then describe what happens for $z=c$ depending on $c$.

> **Why this exercise:** connects a surface equation with the geometry of its intersection.

---

## Answer

The intersection with the plane $z=3$ is the circle

$$
x^2+y^2=16,\qquad z=3
$$

with center $(0,0,3)$ and radius $4$.

For a general plane $z=c$:

| Value of $c$ | Intersection |
|---|---|
| $\lvert c\rvert\lt5$ | circle with center $(0,0,c)$ and radius $\sqrt{25-c^2}$ |
| $\lvert c\rvert=5$ | one point, $(0,0,5)$ or $(0,0,-5)$ |
| $\lvert c\rvert\gt5$ | empty |

---

## Steps

### Step 1. Substitute the plane into the sphere

$$
x^2+y^2+3^2=25\quad\Longrightarrow\quad x^2+y^2=16
$$

### Step 2. Describe the curve

The curve consists of the points that satisfy both conditions:

$$
\begin{cases}
x^2+y^2=16, \\
z=3.
\end{cases}
$$

It is a circle lying in the plane $z=3$. Its center is $(0,0,3)$, the point of the plane on the $z$-axis, and its radius is $\sqrt{16}=4$.

### Step 3. General plane $z=c$

$$
x^2+y^2=25-c^2
$$

The left side is nonnegative, so the right side decides what the intersection is.

### Step 4. Three cases

- $25-c^2\gt0$, which means $|c|\lt5$: a circle of radius $\sqrt{25-c^2}$.
- $25-c^2=0$, which means $c=\pm5$: only $x=y=0$ is possible, so the intersection is a single point. The plane touches the sphere.
- $25-c^2\lt0$, which means $|c|\gt5$: no real solution. The plane misses the sphere.

### Step 5. How the radius changes

| $c$ | $0$ | $\pm3$ | $\pm4$ | $\pm4.9$ | $\pm5$ |
|---|---|---|---|---|---|
| radius | $5$ | $4$ | $3$ | $\approx0.99$ | $0$ |

The largest circle is at $c=0$, where the plane passes through the center of the sphere. The radius decreases as the plane moves away from the center.

---

## Why it works

**An intersection is a system of two equations.** A point of the intersection curve must satisfy the equation of the sphere and the equation of the plane at the same time. Substituting $z=3$ uses the second equation to simplify the first. The single equation $x^2+y^2=16$ alone would describe a cylinder in space. Together with $z=3$ it describes a circle.

**A right triangle explains the radius.** Let $O$ be the center of the sphere, $C=(0,0,c)$ the center of the section, and $P$ any point of the section. The segment $OC$ is perpendicular to the plane, so the triangle $OCP$ has a right angle at $C$:

$$
|OC|^2+|CP|^2=|OP|^2\quad\Longrightarrow\quad c^2+r^2=25
$$

The distance $|OC|=|c|$ is the distance from the center to the plane, $|CP|=r$ is the radius of the section, and $|OP|=5$ is the radius of the sphere. For $c=3$ this is the triangle with sides $3$, $4$, $5$.

**The three cases as a comparison of distances.** The distance from the center of the sphere to the plane $z=c$ is $|c|$.

- Distance smaller than the radius: the plane cuts the sphere in a circle.
- Distance equal to the radius: the plane is tangent to the sphere.
- Distance greater than the radius: the plane and the sphere have no common point.

**The radius does not decrease evenly.** From $c=0$ to $c=3$ the radius falls only from $5$ to $4$. From $c=4$ to $c=5$ it falls from $3$ to $0$. The sections change slowly near the middle of the sphere and quickly near the top and bottom, which is the same behavior as for the ellipsoid in Exercise 9.

---

## Check

A point of the circle satisfies both equations. For $(4,0,3)$:

$$
16+0+9=25\ \checkmark,\qquad z=3\ \checkmark
$$

A point not on the coordinate planes also works. For $\left(\frac{12}{5},\frac{16}{5},3\right)$:

$$
\frac{144}{25}+\frac{256}{25}+9=16+9=25\ \checkmark
$$

Every point of the circle is at distance $4$ from its center $(0,0,3)$. For the same point:

$$
\sqrt{\left(\frac{12}{5}\right)^2+\left(\frac{16}{5}\right)^2+0^2}=\sqrt{16}=4\ \checkmark
$$

The tangent case gives exactly one point. For $c=5$:

$$
x^2+y^2=0\quad\Longrightarrow\quad (0,0,5),\qquad 0+0+25=25\ \checkmark
$$

The empty case is confirmed for $c=6$, where $x^2+y^2=25-36=-11$ has no real solution ✓.
