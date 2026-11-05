# Problem 10. Triangle Area from Vectors

## Exercise

### Exercise 10. Triangle Area from Vectors
The points $A=(0,0,0)$, $B=(2,1,0)$, and $C=(1,3,2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac12$.

> **Why this exercise:** shows the interpretation of the length of the cross product as area.

---

## Answer

$$
\overrightarrow{AB}=(2,1,0),\qquad \overrightarrow{AC}=(1,3,2),\qquad \overrightarrow{AB}\times\overrightarrow{AC}=(2,-4,5)
$$

- Area of the parallelogram: $3\sqrt5$.
- Area of the triangle: $\frac{3\sqrt5}{2}\approx3.35$.

A diagonal cuts the parallelogram into two congruent triangles, which gives the factor $\frac12$.

---

## Steps

### Step 1. Side vectors

$$
\overrightarrow{AB}=B-A=(2,1,0),\qquad \overrightarrow{AC}=C-A=(1,3,2)
$$

### Step 2. Cross product

$$
\overrightarrow{AB}\times\overrightarrow{AC}=(1\cdot2-0\cdot3,\ 0\cdot1-2\cdot2,\ 2\cdot3-1\cdot1)=(2,-4,5)
$$

### Step 3. Area of the parallelogram

The area equals the length of the cross product:

$$
S_{\mathrm{par}}=\Vert\overrightarrow{AB}\times\overrightarrow{AC}\Vert=\sqrt{2^2+(-4)^2+5^2}=\sqrt{45}=3\sqrt5
$$

### Step 4. Area of the triangle

$$
S_{\mathrm{tri}}=\frac12\ S_{\mathrm{par}}=\frac{3\sqrt5}{2}
$$

---

## Why it works

**Length of the cross product as area.** For vectors $a$ and $b$ with angle $\theta$ between them,

$$
\Vert a\times b\Vert=\Vert a\Vert\ \Vert b\Vert\sin\theta
$$

A parallelogram with sides $a$ and $b$ has base $\Vert a\Vert$ and height $\Vert b\Vert\sin\theta$. The product of base and height is exactly the length of the cross product.

**The factor $\frac12$.** The parallelogram built on $\overrightarrow{AB}$ and $\overrightarrow{AC}$ has vertices $A$, $B$, $D$, $C$, where $D=B+C-A$. The diagonal $BC$ divides it into the triangles $ABC$ and $DCB$. These triangles have equal corresponding sides, so they are congruent and have equal areas. Each therefore occupies half of the parallelogram.

---

## Check

The cross product is perpendicular to both sides:

$$
(2,-4,5)\cdot(2,1,0)=4-4+0=0\ \checkmark,\qquad (2,-4,5)\cdot(1,3,2)=2-12+10=0\ \checkmark
$$

The area can also be computed without the cross product, from lengths and the dot product. With $\Vert\overrightarrow{AB}\Vert^2=5$, $\Vert\overrightarrow{AC}\Vert^2=14$, and $\overrightarrow{AB}\cdot\overrightarrow{AC}=5$,

$$
S_{\mathrm{par}}^2=\Vert\overrightarrow{AB}\Vert^2\Vert\overrightarrow{AC}\Vert^2-(\overrightarrow{AB}\cdot\overrightarrow{AC})^2=5\cdot14-5^2=45
$$

This agrees with $S_{\mathrm{par}}=\sqrt{45}=3\sqrt5$ ✓.
