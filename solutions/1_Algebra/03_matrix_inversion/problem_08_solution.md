# Problem 8. Inverse of a Transformation

## Exercise

### Exercise 8. Inverse of a Transformation
The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

> **Why this exercise:** gives the inverse the interpretation of undoing a transformation.

---

## Answer

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 2 \\
\end{pmatrix}
$$

| Map | Horizontal direction | Vertical direction |
|---|---|---|
| $S$ | stretch by $2$ | shrink by $\frac12$ |
| $S^{-1}$ | shrink by $\frac12$ | stretch by $2$ |

$S^{-1}$ performs the opposite scaling in each direction and returns every point to where it started.

---

## Steps

### Step 1. Invert a diagonal matrix

A diagonal matrix scales each coordinate separately. To undo it, divide each coordinate by the same factor:

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac{1}{1/2} \\
\end{pmatrix}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 2 \\
\end{pmatrix}
$$

### Step 2. Confirm with the definition

$$
SS^{-1}=
\begin{pmatrix}
2\cdot\frac12 & 0 \\
0 & \frac12\cdot 2 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=I
$$

### Step 3. Describe the geometry

- $S$ sends $(x,\ y)$ to $\left(2x,\ \frac12 y\right)$: the plane is stretched horizontally and squashed vertically.
- $S^{-1}$ sends $(x,\ y)$ to $\left(\frac12 x,\ 2y\right)$: it squashes horizontally and stretches vertically, exactly reversing $S$.

A unit square becomes a $2\times\frac12$ rectangle under $S$. Then $S^{-1}$ turns that rectangle back into the unit square.

---

## Why it works

An inverse transformation is defined by "apply the map, then apply the inverse, and nothing has changed":

$$
S^{-1}(Sv)=v\quad\mathrm{for\ every}\ v
$$

Scaling by $k$ along an axis is undone by scaling by $\frac1k$ along the same axis. Because the two axes do not interact in a diagonal matrix, each one is undone independently.

Note also $\det S=2\cdot\frac12=1$: $S$ preserves area. The inverse has $\det S^{-1}=1$ as well.

---

## Check

Take $v=(1,\ 1)$.

$$
Sv=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
\frac12 \\
\end{pmatrix}
$$

$$
S^{-1}(Sv)=
\begin{pmatrix}
\frac12 & 0 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
\frac12 \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}=v
$$

The vector returns to its starting position. ✓
