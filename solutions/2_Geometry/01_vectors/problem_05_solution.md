# Problem 5. Angle Between Vectors

## Exercise

### Exercise 5. Angle Between Vectors
Given $u=(1,1,0)$ and $v=(1,0,1)$:

1. Use the sign of $u\cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

> **Why this exercise:** teaches how to extract qualitative information first and only then perform the exact calculation.

---

## Answer

- Prediction: $u\cdot v=1\gt0$, so the angle is acute.
- Exact value: $\theta=\frac{\pi}{3}=60^\circ$.
- Comparison: $60^\circ\lt90^\circ$, so the prediction is correct.

---

## Steps

### Step 1. Prediction from the sign

$$
u\cdot v=1\cdot1+1\cdot0+0\cdot1=1>0
$$

A positive dot product means an acute angle.

### Step 2. Lengths of the vectors

$$
\Vert u\Vert=\sqrt{1^2+1^2+0^2}=\sqrt2,\qquad \Vert v\Vert=\sqrt{1^2+0^2+1^2}=\sqrt2
$$

### Step 3. Cosine of the angle

$$
\cos\theta=\frac{u\cdot v}{\Vert u\Vert\ \Vert v\Vert}=\frac{1}{\sqrt2\cdot\sqrt2}=\frac12
$$

### Step 4. The angle

The angle between vectors lies in $[0,\pi]$, and on this interval the cosine takes the value $\frac12$ only once:

$$
\theta=\arccos\frac12=\frac{\pi}{3}=60^\circ
$$

### Step 5. Comparison

The computed angle satisfies $0^\circ\lt60^\circ\lt90^\circ$. It is acute, in agreement with the prediction from Step 1.

---

## Why it works

The formula $u\cdot v=\Vert u\Vert\ \Vert v\Vert\cos\theta$ contains two positive lengths, so the sign of $u\cdot v$ equals the sign of $\cos\theta$. On $[0,\pi]$ the sign of the cosine determines the type of angle:

| Sign of $u\cdot v$ | Sign of $\cos\theta$ | Type of angle |
|---|---|---|
| positive | positive | acute, $\theta\lt90^\circ$ |
| zero | zero | right, $\theta=90^\circ$ |
| negative | negative | obtuse, $\theta\gt90^\circ$ |

The sign requires only the dot product, while the exact angle also requires the lengths. The cheaper calculation therefore gives a useful prediction and a check on the final result.

---

## Check

The value $60^\circ$ can be confirmed geometrically. Take the two vectors as sides of a triangle, with third side

$$
u-v=(0,1,-1),\qquad \Vert u-v\Vert=\sqrt2
$$

All three sides have length $\sqrt2$, so the triangle is equilateral and each of its angles equals $60^\circ$ ✓.
