# Problem 12. Intersection Line of Two Planes

## Exercise

### Exercise 12. Intersection Line of Two Planes
Find a parametric equation of the line that is the intersection of

$$
x+y+z=3,\qquad x-y+z=1.
$$

Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

> **Why this exercise:** shows the equivalence of the algebraic and geometric approaches to constructing an intersection line.

---

## Answer

$$
(x,y,z)=(2,1,0)+t(-1,0,1)
$$

- Direction from the system: $(-1,0,1)$.
- Direction from the cross product: $n_1\times n_2=(2,0,-2)$.

The two vectors are parallel, since $(2,0,-2)=-2\ (-1,0,1)$. They describe the same line.

---

## Steps

### Step 1. Solve the system

$$
\begin{cases}
x+y+z=3, \\
x-y+z=1.
\end{cases}
$$

Subtracting the second equation from the first removes $x$ and $z$:

$$
2y=2\quad\Longrightarrow\quad y=1
$$

Substituting $y=1$ into the first equation:

$$
x+z=2
$$

### Step 2. Introduce a parameter

There are two equations and three unknowns, so one unknown is free. Setting $z=t$ gives

$$
x=2-t,\qquad y=1,\qquad z=t
$$

### Step 3. Parametric equation and first direction

$$
(x,y,z)=(2,1,0)+t(-1,0,1)
$$

The direction vector obtained from the system is

$$
v=(-1,0,1)
$$

### Step 4. Direction from the cross product

The normal vectors are $n_1=(1,1,1)$ and $n_2=(1,-1,1)$:

$$
\begin{aligned}
n_1\times n_2 &= (1\cdot1-1\cdot(-1),\ 1\cdot1-1\cdot1,\ 1\cdot(-1)-1\cdot1) \\
&= (2,\ 0,\ -2)
\end{aligned}
$$

### Step 5. Compare

$$
(2,0,-2)=-2\ (-1,0,1)=-2v
$$

The two vectors are multiples of each other. They have the same direction line, with opposite orientation and different lengths.

---

## Why it works

**Algebraic approach.** Solving the system finds all points that satisfy both equations at once. The solution set of two independent equations in three unknowns has one free parameter, which is a line. The free variable becomes the parameter, and its coefficients form the direction vector.

**Geometric approach.** The intersection line lies in both planes. A vector lying in a plane is perpendicular to the normal of that plane. The direction of the line is therefore perpendicular to both $n_1$ and $n_2$, and the cross product gives exactly such a vector.

**Why they agree.** Both approaches impose the same two conditions. Moving along the line by $v$ must keep both equations satisfied, which means

$$
n_1\cdot v=0,\qquad n_2\cdot v=0
$$

This is the homogeneous version of the system. In space, the vectors perpendicular to two non-parallel vectors form a single line, so any two answers must be multiples of each other.

**What each approach provides.** The cross product gives only the direction. A point of the line still has to come from the system. The system gives both the point and the direction.

A different choice of free variable or parameter changes the point and rescales the direction, but the line is the same.

---

## Check

The direction is perpendicular to both normals:

$$
n_1\cdot v=-1+0+1=0\ \checkmark,\qquad n_2\cdot v=-1-0+1=0\ \checkmark
$$

The point $(2,1,0)$ lies in both planes:

$$
2+1+0=3\ \checkmark,\qquad 2-1+0=1\ \checkmark
$$

A general point $(2-t,\ 1,\ t)$ of the line satisfies both equations for every $t$:

$$
(2-t)+1+t=3\ \checkmark,\qquad (2-t)-1+t=1\ \checkmark
$$

The normals are not parallel, since $n_1\times n_2\neq0$. The planes are therefore not parallel and their intersection is a line, as assumed ✓.
