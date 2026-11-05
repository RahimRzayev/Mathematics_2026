# Problem 2. Distance as the Length of a Vector

## Exercise

### Exercise 2. Distance as the Length of a Vector
The points are $A=(1,2,3)$ and $B=(4,-2,6)$.

1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

> **Why this exercise:** shows that the point-distance formula comes directly from the length of a difference vector.

---

## Answer

$$
\overrightarrow{AB}=(3,-4,3),\qquad \|\overrightarrow{AB}\|=d(A,B)=\sqrt{34}\approx 5.83
$$

Both calculations agree because the coordinates of $\overrightarrow{AB}$ are exactly the coordinate differences that appear in the distance formula.

---

## Steps

### Step 1. Construct the vector

The vector from $A$ to $B$ is the endpoint minus the starting point:

$$
\overrightarrow{AB}=B-A=(4-1,\ -2-2,\ 6-3)=(3,-4,3)
$$

### Step 2. Length of the vector

$$
\|\overrightarrow{AB}\|=\sqrt{3^2+(-4)^2+3^2}=\sqrt{9+16+9}=\sqrt{34}
$$

### Step 3. Coordinate distance formula

$$
d(A,B)=\sqrt{(x_B-x_A)^2+(y_B-y_A)^2+(z_B-z_A)^2}
$$

Substituting the coordinates of the points gives

$$
d(A,B)=\sqrt{(4-1)^2+(-2-2)^2+(6-3)^2}=\sqrt{9+16+9}=\sqrt{34}
$$

---

## Why it works

For general points $A$ and $B$, the vector $\overrightarrow{AB}$ has coordinates

$$
\overrightarrow{AB}=(x_B-x_A,\ y_B-y_A,\ z_B-z_A)
$$

Substituting these coordinates into the length formula produces the distance formula term by term:

$$
\|\overrightarrow{AB}\|=\sqrt{(x_B-x_A)^2+(y_B-y_A)^2+(z_B-z_A)^2}=d(A,B)
$$

The two calculations are therefore one formula written in two ways. The distance between two points is the length of the displacement that carries one point to the other.

Geometrically, the numbers $3$, $4$, $3$ are the edge lengths of a box with $A$ and $B$ at opposite corners. Applying the Pythagorean theorem twice gives the box diagonal $\sqrt{3^2+4^2+3^2}$.

---

## Check

Moving from $A$ along $\overrightarrow{AB}$ must end at $B$:

$$
A+\overrightarrow{AB}=(1+3,\ 2-4,\ 3+3)=(4,-2,6)=B\ \checkmark
$$

Distance does not depend on the order of the points. The reversed vector is $\overrightarrow{BA}=(-3,4,-3)$, and

$$
\|\overrightarrow{BA}\|=\sqrt{9+16+9}=\sqrt{34}\ \checkmark
$$
