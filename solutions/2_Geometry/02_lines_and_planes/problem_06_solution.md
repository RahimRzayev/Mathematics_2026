# Problem 6. Angle Between Planes

## Exercise

### Exercise 6. Angle Between Planes
Given

$$
\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.
$$

First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

> **Why this exercise:** focuses attention on one mechanism—using normals to analyze position and angle—without also introducing the construction of the intersection line.

---

## Answer

- Normal vectors: $n_1=(1,1,1)$ and $n_2=(1,-1,0)$.
- The planes are not parallel, because $n_1$ and $n_2$ are not multiples of each other.
- The angle between the planes is $90^\circ$, because $n_1\cdot n_2=0$. The planes are perpendicular.

---

## Steps

### Step 1. Read the normal vectors

The coefficients of $x$, $y$, $z$ in a plane equation are the components of a normal vector. The equation of $\Pi_2$ has no $z$ term, so its third component is $0$:

$$
n_1=(1,1,1),\qquad n_2=(1,-1,0)
$$

### Step 2. Test for parallelism

Two planes are parallel exactly when their normal vectors are parallel. If $n_1=kn_2$, the third components would give $1=k\cdot0$, which is impossible. The planes are not parallel, so they intersect along a line.

### Step 3. Dot product of the normals

$$
n_1\cdot n_2=1\cdot1+1\cdot(-1)+1\cdot0=0
$$

### Step 4. Angle

The angle between two planes is the acute or right angle between their normals:

$$
\cos\theta=\frac{|n_1\cdot n_2|}{\Vert n_1\Vert\ \Vert n_2\Vert}=\frac{0}{\sqrt3\cdot\sqrt2}=0
$$

$$
\theta=90^\circ
$$

---

## Why it works

**A plane has one perpendicular direction.** A plane contains infinitely many directions, so comparing directions inside two planes gives no single answer. Each plane has exactly one perpendicular direction, and that direction describes the tilt of the whole plane. Comparing two planes therefore reduces to comparing two vectors.

**Parallelism.** Parallel planes have the same tilt, so they have the same perpendicular direction. This holds exactly when the normals are multiples of each other.

**The angle.** The angle between two planes is measured in a cross-section perpendicular to their intersection line. In this cross-section each plane appears as a line and each normal appears as a vector perpendicular to its line. Rotating both lines by $90^\circ$ turns them into the two normals, and a common rotation does not change the angle between them. The angle between the planes is therefore the angle between the normals.

**The absolute value.** A normal can be replaced by its opposite without changing the plane. This replaces the angle between normals by its supplement. The absolute value selects the angle in $[0^\circ,90^\circ]$, so the answer does not depend on the choice of orientation.

**Position is not needed.** The constants $1$ and $2$ on the right sides were not used. They shift the planes without rotating them, so they affect the location of the intersection line but not the angle.

---

## Check

The normal $n_2$ satisfies the homogeneous equation of $\Pi_1$, which means that it lies along $\Pi_1$:

$$
1\cdot1+1\cdot(-1)+1\cdot0=0\ \checkmark
$$

The plane $\Pi_1$ contains a direction perpendicular to $\Pi_2$, which is the definition of perpendicular planes.

The result agrees with a familiar case. The plane $\Pi_2$ is vertical, since its equation does not involve $z$. The plane $\Pi_1$ is symmetric under exchanging $x$ and $y$, and $\Pi_2$ is parallel to the mirror plane $x=y$ of this symmetry. A plane parallel to a mirror plane of $\Pi_1$ meets $\Pi_1$ at a right angle ✓.

The lengths used in the formula are

$$
\Vert n_1\Vert=\sqrt{1+1+1}=\sqrt3,\qquad \Vert n_2\Vert=\sqrt{1+1+0}=\sqrt2
$$

Both are nonzero, so the quotient is defined and equals $0$ ✓.
