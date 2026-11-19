# Problem 3. A Square Root and Removing an Indeterminate Form

## Exercise

### Exercise 3. A Square Root and Removing an Indeterminate Form
Compute

$$
\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right).
$$

Use the conjugate expression and explain why this transformation removes the difficulty.

> **Why this exercise:** introduces conjugation as a deliberate technique for removing an indeterminate form.

---

## Answer

$$
\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right)=\frac52
$$

The conjugate turns the difference of two large, nearly equal quantities into a quotient. The subtraction is carried out exactly by the identity $(a-b)(a+b)=a^2-b^2$: the terms $n^2$ cancel and $5n$ remains. The new denominator is a sum, in which nothing cancels.

---

## Steps

### Step 1. Identify the form

Both $\sqrt{n^2+5n}$ and $n$ grow without bound, so the expression has the indeterminate form $\infty-\infty$.

### Step 2. Multiply and divide by the conjugate

The conjugate of $\sqrt{n^2+5n}-n$ is $\sqrt{n^2+5n}+n$:

$$
\sqrt{n^2+5n}-n=\frac{\left(\sqrt{n^2+5n}-n\right)\left(\sqrt{n^2+5n}+n\right)}{\sqrt{n^2+5n}+n}
$$

### Step 3. Simplify the numerator

By the difference of squares:

$$
\left(\sqrt{n^2+5n}\right)^2-n^2=n^2+5n-n^2=5n
$$

Therefore

$$
\sqrt{n^2+5n}-n=\frac{5n}{\sqrt{n^2+5n}+n}
$$

### Step 4. Divide by $n$

The new expression has the form $\frac{\infty}{\infty}$, which is handled as in Exercise 1. Since $n\gt0$,

$$
\frac{\sqrt{n^2+5n}}{n}=\sqrt{\frac{n^2+5n}{n^2}}=\sqrt{1+\frac5n}
$$

and

$$
\frac{5n}{\sqrt{n^2+5n}+n}=\frac{5}{\sqrt{1+\frac5n}+1}
$$

### Step 5. Pass to the limit

Since $\frac5n\to0$, the root tends to $\sqrt1=1$:

$$
\lim_{n\to\infty}\frac{5}{\sqrt{1+\frac5n}+1}=\frac{5}{1+1}=\frac52
$$

---

## Why it works

**Why $\infty-\infty$ is indeterminate.** The difference of two quantities that both grow without bound can behave in any way:

$$
(n+1)-n\to1,\qquad n^2-n\to+\infty,\qquad n-n^2\to-\infty
$$

The form alone gives no information. The result depends on how closely the two quantities follow each other.

**What the conjugate does.** The difficulty is a subtraction of two large numbers that are almost equal. The identity $(a-b)(a+b)=a^2-b^2$ removes the square root from the difference, and the subtraction $n^2+5n-n^2$ is then performed exactly. What is left is a quotient whose denominator is a sum of two positive terms. A sum of positive terms cannot cancel, so the standard method of dividing by $n$ applies.

**Why the answer is $\frac52$.** Completing the square gives

$$
\left(n+\frac52\right)^2=n^2+5n+\frac{25}{4}
$$

The number $n^2+5n$ is slightly less than $\left(n+\frac52\right)^2$, so $\sqrt{n^2+5n}$ is slightly less than $n+\frac52$. Subtracting $n$ leaves a value slightly less than $\frac52$.

**A wrong shortcut.** The following reasoning is incorrect: the term $5n$ is small compared with $n^2$, so $\sqrt{n^2+5n}$ can be replaced by $\sqrt{n^2}=n$, and the limit is $0$. Dropping $5n$ under the root changes the root by about $\frac52$. This change is negligible in a quotient, but it is the whole answer in a difference.

---

## Check

**Numerical values.**

| $n$ | $1$ | $4$ | $10$ | $100$ | $1000$ | $10\ 000$ |
|---|---|---|---|---|---|---|
| $\sqrt{n^2+5n}-n$ | $\sqrt6-1\approx1.4495$ | $\sqrt{36}-4=2$ | $\approx2.2474$ | $\approx2.4695$ | $\approx2.49688$ | $\approx2.499688$ |

The values increase toward $2.5$ ✓.

**Upper bound.** From $n^2+5n\lt\left(n+\frac52\right)^2$ it follows that

$$
\sqrt{n^2+5n}-n\lt\frac52
$$

for every $n$. All values in the table are below $2.5$ ✓.

**The two forms agree.** For $n=4$ the transformed expression gives

$$
\frac{5\cdot4}{\sqrt{36}+4}=\frac{20}{10}=2
$$

which equals the value $\sqrt{36}-4=2$ of the original expression ✓.
