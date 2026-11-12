# Problem 12. Recognizing a Surface from Cross-Sections

## Exercise

### Exercise 12. Recognizing a Surface from Cross-Sections
A certain surface has the following properties:
- the cross-section $z=0$ is a point,
- for $z\gt0$, the cross-sections $z=\mathrm{const}$ are circles with increasing radius,
- vertical cross-sections through the $Oz$ axis are parabolas.

Propose a simple equation for such a surface and justify your choice.

> **Why this exercise:** reverses the usual reasoning: from geometry to an equation.

---

## Answer

$$
z=x^2+y^2
$$

This surface is a paraboloid of revolution. It satisfies all three properties:

- $z=0$ gives $x^2+y^2=0$, which is the single point $(0,0,0)$,
- $z=c\gt0$ gives the circle $x^2+y^2=c$ of radius $\sqrt{c}$, which increases with $c$,
- every vertical plane through the $Oz$ axis cuts the surface in a parabola $z=r^2$.

The answer is not unique: any equation $z=a(x^2+y^2)$ with $a\gt0$ has the same properties.

---

## Steps

### Step 1. Use the circles

The horizontal sections are circles centered on the $Oz$ axis. A circle of radius $r$ at height $z$ has the equation $x^2+y^2=r^2$. The surface is therefore described by

$$
x^2+y^2=r(z)^2
$$

where $r(z)$ is the radius at height $z$. The equation depends on $x$ and $y$ only through $x^2+y^2$.

### Step 2. Use the parabolas

The vertical plane $y=0$ contains the $Oz$ axis. In this plane the section must be a parabola with its vertex at the origin, and the simplest one is

$$
z=x^2
$$

On this curve the distance from the axis is $|x|$, so the radius and the height are related by $z=r^2$.

### Step 3. Combine

Replacing $r^2$ by $x^2+y^2$:

$$
z=x^2+y^2
$$

### Step 4. Verify the first property

$$
z=0:\ x^2+y^2=0\quad\Longrightarrow\quad x=0,\ y=0
$$

The section is one point.

### Step 5. Verify the second property

$$
z=c\gt0:\ x^2+y^2=c
$$

The section is a circle of radius $\sqrt{c}$. The radius increases with height: $c=1$ gives $1$, $c=4$ gives $2$, $c=9$ gives $3$.

### Step 6. Verify the third property

A vertical plane through the $Oz$ axis contains the points

$$
x=r\cos\varphi,\qquad y=r\sin\varphi
$$

where the angle $\varphi$ is fixed and $r$ is the signed distance from the axis. Substituting:

$$
z=r^2\cos^2\varphi+r^2\sin^2\varphi=r^2
$$

The section is the parabola $z=r^2$ for every angle $\varphi$, not only for the coordinate planes.

---

## Why it works

**Each property determines one feature of the equation.**

- Circular horizontal sections centered on the axis mean rotational symmetry, so $x$ and $y$ enter only through $x^2+y^2$.
- Parabolic vertical sections mean that the height is proportional to the square of the distance from the axis.
- The point at $z=0$ places the vertex at the origin, so there is no constant term.

**Similar surfaces that fail one property.** Comparing with close candidates shows that all three conditions are needed.

| Surface | $z=0$ | Sections $z=c\gt0$ | Vertical sections | Verdict |
|---|---|---|---|---|
| $z=x^2+y^2$ | point | circles, radius $\sqrt{c}$ | parabolas | fits |
| $z^2=x^2+y^2$ | point | circles, radius $c$ | pairs of straight lines | fails the third property |
| $z=x^2+y^2+1$ | empty | circles for $c\gt1$ | parabolas | fails the first property |
| $z=x^2+4y^2$ | point | ellipses | parabolas | fails the second property |
| $z=x^2-y^2$ | two lines | hyperbolas | parabolas or lines | fails the first and second |

The cone $z^2=x^2+y^2$ is the closest alternative. It also starts from a point and has growing circles, but its radius grows in proportion to the height and its vertical sections are straight lines. The parabolic sections distinguish the paraboloid from the cone.

**Freedom in the answer.** The properties describe the shape but not the scale. The equation $z=a(x^2+y^2)$ with any $a\gt0$ gives circles of radius $\sqrt{c/a}$ and parabolas $z=ar^2$. The choice $a=1$ is the simplest.

---

## Check

A vertical plane that is not a coordinate plane gives a parabola. In the plane $y=x$, the points are $(t,t,z)$ and the surface gives

$$
z=t^2+t^2=2t^2
$$

The distance from the axis is $r=\sqrt2\ |t|$, so $z=r^2$, the same parabola as in the plane $y=0$ ✓.

Three points at the same height are at the same distance from the axis. At height $z=4$:

$$
(2,0,4):\ 4+0=4\ \checkmark,\qquad (0,-2,4):\ 0+4=4\ \checkmark,\qquad \left(\sqrt2,\sqrt2,4\right):\ 2+2=4\ \checkmark
$$

There are no points below the plane $z=0$. For $z=-1$ the equation $x^2+y^2=-1$ has no real solution, so the surface lies entirely in $z\ge0$ and the point at $z=0$ is its lowest point ✓.
