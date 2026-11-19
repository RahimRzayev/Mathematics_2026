# Problem 8. A Square Root in a Function Limit

## Exercise

### Exercise 8. A Square Root in a Function Limit
Compute

$$
\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}
$$

by rationalizing the numerator. Compare the idea with Exercise 3 involving a sequence.

> **Why this exercise:** reinforces transferring the same algebraic technique between two types of limits.

---

## Answer

$$
\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}=\frac14
$$

| | Exercise 3 (sequence) | Exercise 8 (function) |
|---|---|---|
| Expression | $\sqrt{n^2+5n}-n$ | $\frac{\sqrt x-2}{x-4}$ |
| Indeterminate form | $\infty-\infty$ | $\frac00$ |
| Conjugate | $\sqrt{n^2+5n}+n$ | $\sqrt x+2$ |
| After multiplication | $\frac{5n}{\sqrt{n^2+5n}+n}$ | $\frac{1}{\sqrt x+2}$ |
| Final step | divide by $n$ | substitute $x=4$ |
| Result | $\frac52$ | $\frac14$ |

The idea is the same in both exercises: the identity $(a-b)(a+b)=a^2-b^2$ removes the square root from a difference that causes the difficulty.

---

## Steps

### Step 1. Try direct substitution

At $x=4$ the numerator equals $\sqrt4-2=0$ and the denominator equals $0$. The form is $\frac00$.

### Step 2. Multiply and divide by the conjugate

The conjugate of $\sqrt x-2$ is $\sqrt x+2$:

$$
\frac{\sqrt x-2}{x-4}=\frac{\left(\sqrt x-2\right)\left(\sqrt x+2\right)}{(x-4)\left(\sqrt x+2\right)}
$$

### Step 3. Simplify the numerator

By the difference of squares:

$$
\left(\sqrt x-2\right)\left(\sqrt x+2\right)=\left(\sqrt x\right)^2-2^2=x-4
$$

### Step 4. Cancel the common factor

For $x\neq4$:

$$
\frac{\sqrt x-2}{x-4}=\frac{x-4}{(x-4)\left(\sqrt x+2\right)}=\frac{1}{\sqrt x+2}
$$

### Step 5. Pass to the limit

The function $\sqrt x$ is continuous at $x=4$, so $\sqrt x\to2$:

$$
\lim_{x\to4}\frac{1}{\sqrt x+2}=\frac{1}{2+2}=\frac14
$$

---

## Why it works

**The hidden common factor.** The form $\frac00$ signals that the numerator and the denominator vanish for the same reason. The denominator can be written as

$$
x-4=\left(\sqrt x-2\right)\left(\sqrt x+2\right)
$$

so the numerator $\sqrt x-2$ is a factor of the denominator. Rationalizing makes this factor visible and allows it to be canceled. As in Exercise 7, the cancellation is valid because the limit uses only points with $x\neq4$.

**The conjugate is harmless.** The expression $\sqrt x-2$ tends to $0$ and causes the difficulty. Its conjugate $\sqrt x+2$ tends to $4$, a nonzero number, so it creates no new difficulty in the denominator.

**Comparison with Exercise 3.** In Exercise 3 the troublesome difference is $\sqrt{n^2+5n}-n$, a difference of two large quantities. Here it is $\sqrt x-2$, a difference of two nearly equal finite quantities. In both cases a direct evaluation loses the information, and in both cases the conjugate replaces the difference by an exact algebraic expression: $5n$ there, $x-4$ here. The technique depends only on the algebraic structure, a difference containing a square root. It does not depend on whether the variable is an integer going to infinity or a real number approaching a point.

**One difference.** After conjugation Exercise 3 still has the form $\frac{\infty}{\infty}$ and needs a division by $n$. Here the troublesome factor cancels completely and the limit follows by substitution.

---

## Check

**Values on both sides of $4$.**

| $x$ | $3.9$ | $3.99$ | $3.999$ | $4.001$ | $4.01$ | $4.1$ |
|---|---|---|---|---|---|---|
| $\frac{\sqrt x-2}{x-4}$ | $0.25158$ | $0.25016$ | $0.250016$ | $0.249984$ | $0.24984$ | $0.24846$ |

The values approach $0.25$ from above on the left and from below on the right ✓.

**The two forms agree at a point where both are easy to compute.** For $x=9$:

$$
\frac{\sqrt9-2}{9-4}=\frac15,\qquad \frac{1}{\sqrt9+2}=\frac15\ \checkmark
$$

**Direction of approach.** The simplified form $\frac{1}{\sqrt x+2}$ decreases as $x$ increases, so the values are larger than $\frac14$ for $x\lt4$ and smaller for $x\gt4$. This agrees with the table ✓.
