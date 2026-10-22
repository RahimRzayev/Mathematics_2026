# Problem 9. Area and the Determinant

## Exercise

### Exercise 9. Area and the Determinant
The vectors

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

> **Why this exercise:** gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.

---

## Answer

| Order | Determinant | Area |
|---|---|---|
| $(u,\ v)$ | $11$ | $11$ |
| $(v,\ u)$ | $-11$ | $11$ |

Reversing the order **flips the sign** of the determinant. The **area stays** $11$.

---

## Steps

### Step 1. Put the vectors as columns

$$
\det(u,\ v)=\det
\begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}=3\cdot 4-1\cdot 1=11
$$

### Step 2. Area is the absolute value

$$
\mathrm{Area}=\left|\det(u,\ v)\right|=11
$$

### Step 3. Reverse the order

Swap the two columns:

$$
\det(v,\ u)=\det
\begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix}=1\cdot 1-3\cdot 4=-11
$$

Area: $\left|-11\right|=11$. Unchanged.

---

## Why it works

The determinant of two vectors in the plane is a **signed area**:

- **Size** $\left|\det\right|$: the area of the parallelogram.
- **Sign**: the orientation of the pair.
  - Positive: turning from the first vector to the second is **counterclockwise**.
  - Negative: the turn is **clockwise**.

Here $u=(3,\ 1)$ points almost along the $x$-axis, and $v=(1,\ 4)$ points steeply up. Turning from $u$ to $v$ is counterclockwise, so $\det(u,\ v)>0$.

Swapping the vectors is a column swap, so the sign flips. The parallelogram itself is the same shape, so its area does not change.

---

## Check

Compute the area without determinants. The parallelogram has vertices

$$
(0,\ 0),\quad(3,\ 1),\quad(4,\ 5),\quad(1,\ 4)
$$

It fits inside the box $[0,4]\times[0,5]$ of area $20$. The four corner triangles outside it have areas

$$
\frac{3\cdot 1}{2}+\frac{1\cdot 4}{2}+\frac{3\cdot 1}{2}+\frac{1\cdot 4}{2}=1.5+2+1.5+2=7
$$

and the two leftover corner squares, each $1\times 1$, add $2$. Area $=20-7-2=11$. ✓
