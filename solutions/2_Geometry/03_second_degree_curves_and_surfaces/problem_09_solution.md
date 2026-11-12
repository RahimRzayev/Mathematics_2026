# Problem 9. Ellipsoid and Its Cross-Sections

## Exercise

### Exercise 9. Ellipsoid and Its Cross-Sections
Consider

$$
\frac{x^2}{9}+\frac{y^2}{4}+\frac{z^2}{16}=1.
$$

Give the semiaxis lengths, describe the cross-section $z=0$, and explain how the cross-sections $z=c$ change for $|c|\lt4$.

> **Why this exercise:** teaches how to understand a 3D surface through a family of simpler 2D cross-sections.

---

## Answer

- Semiaxes: $3$ along $x$, $2$ along $y$, and $4$ along $z$.
- The cross-section $z=0$ is the ellipse $\frac{x^2}{9}+\frac{y^2}{4}=1$ with semiaxes $3$ and $2$.
- For $|c|\lt4$ the cross-section $z=c$ is an ellipse with the following semiaxes along $x$ and along $y$:

$$
3\sqrt{1-\frac{c^2}{16}},\qquad 2\sqrt{1-\frac{c^2}{16}}
$$

All these ellipses have the same proportions $3:2$. They are largest at $c=0$ and shrink as $|c|$ grows, down to a single point at $c=\pm4$.

---

## Steps

### Step 1. Semiaxes

$$
\frac{x^2}{3^2}+\frac{y^2}{2^2}+\frac{z^2}{4^2}=1
$$

Setting two variables to zero gives the points where the surface meets each axis:

$$
(\pm3,0,0),\qquad (0,\pm2,0),\qquad (0,0,\pm4)
$$

The semiaxes are $3$, $2$, and $4$.

### Step 2. Cross-section $z=0$

$$
\frac{x^2}{9}+\frac{y^2}{4}=1
$$

This is an ellipse in the plane $z=0$, centered at the origin, with semiaxis $3$ along $x$ and semiaxis $2$ along $y$.

### Step 3. Cross-section $z=c$

Substituting $z=c$ and moving the constant term to the right:

$$
\frac{x^2}{9}+\frac{y^2}{4}=1-\frac{c^2}{16}
$$

Let $k=1-\frac{c^2}{16}$. For $|c|\lt4$ the value $k$ is positive and at most $1$.

### Step 4. Canonical form of the cross-section

Dividing by $k$:

$$
\frac{x^2}{9k}+\frac{y^2}{4k}=1
$$

This is an ellipse in the plane $z=c$, centered on the $z$-axis. Its semiaxes along $x$ and along $y$ are

$$
3\sqrt{k},\qquad 2\sqrt{k}
$$

### Step 5. How the cross-sections change

| $c$ | $k$ | Semiaxis along $x$ | Semiaxis along $y$ |
|---|---|---|---|
| $0$ | $1$ | $3$ | $2$ |
| $\pm2$ | $\frac34$ | $\approx2.60$ | $\approx1.73$ |
| $\pm3$ | $\frac{7}{16}$ | $\approx1.98$ | $\approx1.32$ |
| $\pm3.9$ | $\approx0.05$ | $\approx0.67$ | $\approx0.44$ |

As $|c|$ grows from $0$ toward $4$, the factor $\sqrt{k}$ decreases from $1$ toward $0$. Both semiaxes are multiplied by the same factor, so the ellipse shrinks without changing its proportions.

---

## Why it works

**A surface as a stack of curves.** A horizontal plane $z=c$ fixes one variable, and the equation of the surface becomes an equation in $x$ and $y$ only, which is a plane curve. The surface is the union of these curves placed at their heights. Reading the curves one by one reconstructs the shape without a three-dimensional picture.

**Why the sections shrink.** The three nonnegative terms must add up to $1$. The term $\frac{c^2}{16}$ uses part of this total, and only $k=1-\frac{c^2}{16}$ remains for $x$ and $y$. The higher the plane, the less remains, and the smaller the ellipse.

**Why the proportions stay constant.** The height changes only the right side $k$, not the denominators $9$ and $4$. Every section is the central ellipse scaled by $\sqrt{k}$, and the ratio of its semiaxes is always $3:2$.

**The limiting cases.** At $c=\pm4$ the value $k=0$ gives $\frac{x^2}{9}+\frac{y^2}{4}=0$, which holds only for $x=y=0$: the section is the single point $(0,0,\pm4)$. For $|c|\gt4$ the value $k$ is negative and there is no section. The surface is therefore bounded between the planes $z=-4$ and $z=4$.

**The shrinking is slow near the middle and fast near the ends.** The factor $\sqrt{1-\frac{c^2}{16}}$ is the height of a semicircle as a function of $c$. It changes little near $c=0$ and drops steeply near $c=\pm4$. This gives the rounded, closed shape of the ellipsoid.

---

## Check

The axis points satisfy the equation:

$$
(3,0,0):\ \frac99=1\ \checkmark,\qquad (0,2,0):\ \frac44=1\ \checkmark,\qquad (0,0,4):\ \frac{16}{16}=1\ \checkmark
$$

A point of the section $c=2$ lies on the surface. The section has semiaxis $3\sqrt{\frac34}$ along $x$, so the point $\left(\frac{3\sqrt3}{2},0,2\right)$ should satisfy the equation:

$$
\frac{27/4}{9}+0+\frac{4}{16}=\frac34+\frac14=1\ \checkmark
$$

The other cross-sections follow the same rule. The plane $x=0$ gives the ellipse $\frac{y^2}{4}+\frac{z^2}{16}=1$ with semiaxes $2$ and $4$, and the plane $y=0$ gives $\frac{x^2}{9}+\frac{z^2}{16}=1$ with semiaxes $3$ and $4$. Each uses two of the three semiaxes found in Step 1 ✓.
