# Problem 8. Sphere

## Exercise

### Exercise 8. Sphere
Reduce

$$
x^2+y^2+z^2-4x+2y-6z-2=0
$$

to canonical form. Find the center and radius. Give two points on the sphere and check them in the equation.

> **Why this exercise:** transfers the technique known from circles from two dimensions to three.

---

## Answer

$$
(x-2)^2+(y+1)^2+(z-3)^2=16
$$

- Center: $(2,-1,3)$.
- Radius: $4$.
- Two points of the sphere: $(6,-1,3)$ and $(2,-1,7)$.

---

## Steps

### Step 1. Group the terms by variable

$$
(x^2-4x)+(y^2+2y)+(z^2-6z)=2
$$

### Step 2. Complete the square in each variable

$$
x^2-4x=(x-2)^2-4,\qquad y^2+2y=(y+1)^2-1,\qquad z^2-6z=(z-3)^2-9
$$

### Step 3. Substitute and collect the constants

$$
\begin{aligned}
(x-2)^2-4+(y+1)^2-1+(z-3)^2-9 &= 2 \\
(x-2)^2+(y+1)^2+(z-3)^2 &= 16
\end{aligned}
$$

### Step 4. Read the center and the radius

Comparing with $(x-x_0)^2+(y-y_0)^2+(z-z_0)^2=r^2$:

$$
(x_0,y_0,z_0)=(2,-1,3),\qquad r=\sqrt{16}=4
$$

### Step 5. Two points of the sphere

Moving from the center by the radius along the $x$-axis and along the $z$-axis gives

$$
(2+4,\ -1,\ 3)=(6,-1,3),\qquad (2,\ -1,\ 3+4)=(2,-1,7)
$$

### Step 6. Check the points in the original equation

Point $(6,-1,3)$:

$$
36+1+9-24-2-18-2=46-46=0\ \checkmark
$$

Point $(2,-1,7)$:

$$
4+1+49-8-2-42-2=54-54=0\ \checkmark
$$

---

## Why it works

**The same technique with one more variable.** For a circle, two squares are completed. For a sphere, three. Each variable is handled separately, because the equation contains no products such as $xy$ or $xz$. The linear terms $-4x$, $2y$, $-6z$ show that the center is shifted from the origin along each axis.

**Meaning of the canonical form.** The left side is the squared distance from the point $(x,y,z)$ to the center $(2,-1,3)$. The equation states that this distance equals $4$. This is the definition of a sphere, in the same way as $(x-x_0)^2+(y-y_0)^2=r^2$ is the definition of a circle.

**How to recognize a sphere in general form.** Three conditions hold in the original equation:

- all three squares are present with equal coefficients,
- there are no mixed products,
- after completing the squares, the right side is positive.

Here the right side is $2+4+1+9=16$. A value of $0$ would give one point, and a negative value would give no real points.

**Connection with circles.** Every plane that cuts the sphere does so in a circle. For example, the horizontal plane $z=3$ through the center gives $(x-2)^2+(y+1)^2=16$, a circle of radius $4$ in that plane.

---

## Check

Both points satisfy the canonical form:

$$
(6,-1,3):\ 4^2+0+0=16\ \checkmark,\qquad (2,-1,7):\ 0+0+4^2=16\ \checkmark
$$

Expanding the canonical form returns the original equation:

$$
x^2-4x+4+y^2+2y+1+z^2-6z+9-16=x^2+y^2+z^2-4x+2y-6z-2\ \checkmark
$$

A point that does not lie on a line through the center parallel to an axis confirms the result. The point $(2,3,3)$ is at distance $4$ from the center in the $y$-direction, and

$$
4+9+9-8+6-18-2=0\ \checkmark
$$

The center itself is not on the sphere. Substituting $(2,-1,3)$ into the left side gives

$$
4+1+9-8-2-18-2=-16
$$

which is $-r^2$, as the canonical form requires ✓.
