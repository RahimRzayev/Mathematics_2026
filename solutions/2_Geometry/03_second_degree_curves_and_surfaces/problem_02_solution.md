# Problem 2. Circle by Completing the Square

## Exercise

### Exercise 2. Circle by Completing the Square
Reduce

$$
x^2+y^2-6x+4y-3=0
$$

to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

> **Why this exercise:** practices completing the square as a transition from a general equation to the geometry of the object.

---

## Answer

$$
(x-3)^2+(y+2)^2=16
$$

- Center: $(3,-2)$.
- Radius: $4$.
- Two points of the circle: $(7,-2)$ and $(3,2)$. Both satisfy the general form and the canonical form.

---

## Steps

### Step 1. Group the terms by variable

$$
(x^2-6x)+(y^2+4y)=3
$$

### Step 2. Complete the square in $x$

Half of the coefficient $-6$ is $-3$, and $(-3)^2=9$:

$$
x^2-6x=(x-3)^2-9
$$

### Step 3. Complete the square in $y$

Half of the coefficient $4$ is $2$, and $2^2=4$:

$$
y^2+4y=(y+2)^2-4
$$

### Step 4. Substitute and collect the constants

$$
\begin{aligned}
(x-3)^2-9+(y+2)^2-4 &= 3 \\
(x-3)^2+(y+2)^2 &= 16
\end{aligned}
$$

### Step 5. Read the center and the radius

Comparing with $(x-x_0)^2+(y-y_0)^2=r^2$:

$$
(x_0,y_0)=(3,-2),\qquad r=\sqrt{16}=4
$$

### Step 6. Two simple points

Moving from the center by the radius along each axis gives

$$
(3+4,\ -2)=(7,-2),\qquad (3,\ -2+4)=(3,2)
$$

### Step 7. Substitute into both forms

Point $(7,-2)$:

$$
\begin{aligned}
49+4-42-8-3 &= 0\ \checkmark \\
(7-3)^2+(-2+2)^2 &= 16+0=16\ \checkmark
\end{aligned}
$$

Point $(3,2)$:

$$
\begin{aligned}
9+4-18+8-3 &= 0\ \checkmark \\
(3-3)^2+(2+2)^2 &= 0+16=16\ \checkmark
\end{aligned}
$$

---

## Why it works

**The general form hides the geometry.** The equation $x^2+y^2-6x+4y-3=0$ is correct but shows neither the center nor the radius. The canonical form states the definition of a circle directly: the squared distance from $(x,y)$ to the center equals $r^2$.

**Completing the square is a shift of the origin.** The linear terms $-6x$ and $4y$ appear because the center is not at the origin. The identity

$$
x^2+px=\left(x+\frac{p}{2}\right)^2-\frac{p^2}{4}
$$

absorbs each linear term into a shifted square. In the new coordinates $u=x-3$ and $v=y+2$ the equation is $u^2+v^2=16$, a circle centered at the origin.

**The sign of the right side matters.** After completing the squares the right side must be positive for a circle to exist. Here it is $16$. A value of $0$ would give a single point, and a negative value would give no real points.

**Signs of the center.** The center is read with opposite signs from the brackets: $(x-3)$ gives $x_0=3$, and $(y+2)=(y-(-2))$ gives $y_0=-2$.

---

## Check

Expanding the canonical form returns the general form:

$$
(x-3)^2+(y+2)^2-16=x^2-6x+9+y^2+4y+4-16=x^2+y^2-6x+4y-3\ \checkmark
$$

The center and radius agree with the general formulas. For $x^2+y^2+Dx+Ey+F=0$ the center is $\left(-\frac{D}{2},-\frac{E}{2}\right)$ and $r^2=\frac{D^2}{4}+\frac{E^2}{4}-F$:

$$
\left(-\frac{-6}{2},\ -\frac42\right)=(3,-2)\ \checkmark,\qquad r^2=9+4+3=16\ \checkmark
$$

The two opposite points also lie on the circle. For $(-1,-2)$ and $(3,-6)$:

$$
1+4+6-8-3=0\ \checkmark,\qquad 9+36-18-24-3=0\ \checkmark
$$
