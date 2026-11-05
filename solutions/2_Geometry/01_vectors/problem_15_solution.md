# Problem 15. Comparing Directions Using the Cosine of the Angle

## Exercise

### Exercise 15. Comparing Directions Using the Cosine of the Angle
Given

$$
a=(1,2,1),\qquad b=(2,4,2),\qquad c=(2,0,3).
$$

For each pair, compute

$$
\frac{u\cdot v}{\Vert u\Vert\ \Vert v\Vert}.
$$

Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

> **Why this exercise:** reinforces the connection between the dot product and angle, and the distinction between direction and length.

---

## Answer

| Pair | Cosine | Angle |
|---|---|---|
| $a,b$ | $1$ | $0^\circ$ |
| $a,c$ | $\frac{5}{\sqrt{78}}\approx0.566$ | $\approx55.5^\circ$ |
| $b,c$ | $\frac{5}{\sqrt{78}}\approx0.566$ | $\approx55.5^\circ$ |

Order by increasing angle: first the pair $a,b$, then the pairs $a,c$ and $b,c$, which are tied.

For $a$ and $b$ the value is $1$ because $b=2a$. The two vectors have different lengths but the same direction and orientation, and the formula divides out the lengths.

---

## Steps

### Step 1. Lengths

$$
\Vert a\Vert=\sqrt{1+4+1}=\sqrt6,\qquad \Vert b\Vert=\sqrt{4+16+4}=\sqrt{24}=2\sqrt6,\qquad \Vert c\Vert=\sqrt{4+0+9}=\sqrt{13}
$$

### Step 2. Pair $a,b$

$$
a\cdot b=2+8+2=12,\qquad \frac{a\cdot b}{\Vert a\Vert\ \Vert b\Vert}=\frac{12}{\sqrt6\cdot2\sqrt6}=\frac{12}{12}=1
$$

### Step 3. Pair $a,c$

$$
a\cdot c=2+0+3=5,\qquad \frac{a\cdot c}{\Vert a\Vert\ \Vert c\Vert}=\frac{5}{\sqrt6\ \sqrt{13}}=\frac{5}{\sqrt{78}}
$$

### Step 4. Pair $b,c$

$$
b\cdot c=4+0+6=10,\qquad \frac{b\cdot c}{\Vert b\Vert\ \Vert c\Vert}=\frac{10}{2\sqrt6\ \sqrt{13}}=\frac{5}{\sqrt{78}}
$$

### Step 5. Order the pairs

On $[0,\pi]$ the cosine is strictly decreasing, so a larger cosine means a smaller angle. Since

$$
1>\frac{5}{\sqrt{78}}\approx0.566
$$

the pair $a,b$ has the smallest angle, and the pairs $a,c$ and $b,c$ share a larger angle:

$$
\theta_{ab}=0^\circ,\qquad \theta_{ac}=\theta_{bc}=\arccos\frac{5}{\sqrt{78}}\approx55.5^\circ
$$

---

## Why it works

**Length does not affect the value.** Dividing each vector by its length turns the expression into the dot product of two unit vectors:

$$
\frac{u\cdot v}{\Vert u\Vert\ \Vert v\Vert}=\frac{u}{\Vert u\Vert}\cdot\frac{v}{\Vert v\Vert}
$$

The value therefore depends only on directions and orientations.

**The value for $a$ and $b$.** Since $b=2a$, both vectors normalize to the same unit vector $e$, and

$$
\frac{a\cdot b}{\Vert a\Vert\ \Vert b\Vert}=e\cdot e=\Vert e\Vert^2=1
$$

The value $1$ means the angle is $0^\circ$. This does not mean the vectors are equal, since $\Vert b\Vert=2\Vert a\Vert$.

**The tie.** Since $b=2a$, the vectors $a$ and $b$ have the same direction, so each forms the same angle with $c$. Numerically, the factor $2$ doubles both the dot product and the denominator, and the two factors cancel.

---

## Check

The tie follows directly from $b=2a$, without separate calculation:

$$
\frac{b\cdot c}{\Vert b\Vert\ \Vert c\Vert}=\frac{2\ (a\cdot c)}{2\ \Vert a\Vert\ \Vert c\Vert}=\frac{a\cdot c}{\Vert a\Vert\ \Vert c\Vert}\ \checkmark
$$

All values lie in the required range $[-1,1]$, as the Cauchy-Schwarz inequality requires:

$$
\frac{5}{\sqrt{78}}\approx0.566\in[-1,1]\ \checkmark
$$

The positive sign of $a\cdot c=5$ predicts an acute angle, which agrees with $55.5^\circ$ ✓.
