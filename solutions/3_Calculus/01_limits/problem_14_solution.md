# Problem 14. A $0/0$ Limit with Trigonometry

## Exercise

### Exercise 14. A $0/0$ Limit with Trigonometry
Compute

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}.
$$

Justify the result without using l'Hôpital's rule, using a trigonometric identity and the fundamental limit.

> **Why this exercise:** requires combining two known tools in one argument.

---

## Answer

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}=\frac12
$$

The two tools are the half-angle identity $1-\cos x=2\sin^2\frac x2$ and the fundamental limit $\frac{\sin t}{t}\to1$:

$$
\frac{1-\cos x}{x^2}=\frac12\left(\frac{\sin\frac x2}{\frac x2}\right)^2\to\frac12\cdot1^2
$$

---

## Steps

### Step 1. Identify the form

At $x=0$ the numerator equals $1-\cos0=0$ and the denominator equals $0$. The form is $\frac00$.

### Step 2. Apply the trigonometric identity

The double-angle formula $\cos2t=1-2\sin^2t$ with $t=\frac x2$ gives

$$
1-\cos x=2\sin^2\frac x2
$$

Therefore

$$
\frac{1-\cos x}{x^2}=\frac{2\sin^2\frac x2}{x^2}
$$

### Step 3. Match the denominator to the argument of the sine

The argument of the sine is $\frac x2$, so the denominator is rewritten through $\frac x2$:

$$
x^2=4\left(\frac x2\right)^2
$$

Then

$$
\frac{2\sin^2\frac x2}{x^2}=\frac{2\sin^2\frac x2}{4\left(\frac x2\right)^2}=\frac12\left(\frac{\sin\frac x2}{\frac x2}\right)^2
$$

### Step 4. Apply the fundamental limit

Let $t=\frac x2$. Then $t\to0$ exactly when $x\to0$, and $t\neq0$ for $x\neq0$:

$$
\lim_{x\to0}\frac{\sin\frac x2}{\frac x2}=\lim_{t\to0}\frac{\sin t}{t}=1
$$

### Step 5. Pass to the limit

The limit of a square is the square of the limit:

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}=\frac12\cdot1^2=\frac12
$$

---

## Why it works

**The role of each tool.** The numerator $1-\cos x$ is a difference of two nearly equal quantities, and no factor of $x$ is visible in it. The identity converts this difference into a product, $2\sin\frac x2\cdot\sin\frac x2$. Each sine factor can then be paired with one factor $\frac x2$ from the denominator, and each pair is the fundamental limit. Neither tool is sufficient alone: the identity does not evaluate the limit, and the fundamental limit cannot be applied to a cosine.

**Why the denominator is $x^2$.** The numerator contains two sine factors, each of the same order as $x$, so $1-\cos x$ is of the same order as $x^2$. Dividing by $x^2$ gives a finite nonzero limit. With a different power the result is different. For example,

$$
\lim_{x\to0}\frac{1-\cos x}{x}=\lim_{x\to0}x\cdot\frac{1-\cos x}{x^2}=0\cdot\frac12=0
$$

**Interpretation.** The result states that $1-\cos x$ is close to $\frac{x^2}{2}$ for small $x$, or that $\cos x$ is close to $1-\frac{x^2}{2}$. Near $0$ the graph of the cosine is approximated by a parabola opening downward.

**A second derivation.** Multiplying the numerator and the denominator by $1+\cos x$ and using $1-\cos^2x=\sin^2x$:

$$
\frac{1-\cos x}{x^2}=\frac{1-\cos^2x}{x^2(1+\cos x)}=\left(\frac{\sin x}{x}\right)^2\cdot\frac{1}{1+\cos x}
$$

The first factor tends to $1^2=1$ and the second to $\frac{1}{1+1}=\frac12$. The limit is again $\frac12$. This is the conjugate technique of Exercises 3 and 8 applied to a trigonometric difference.

---

## Check

**Numerical values, with $x$ in radians.**

| $x$ | $1$ | $0.5$ | $0.1$ | $0.01$ |
|---|---|---|---|---|
| $\frac{1-\cos x}{x^2}$ | $0.45970$ | $0.48967$ | $0.499583$ | $0.4999958$ |

The values approach $0.5$ ✓.

**Negative arguments.** Since $\cos(-x)=\cos x$ and $(-x)^2=x^2$, the expression is an even function. The values for $x=-0.1$ and $x=-0.01$ are the same as for $0.1$ and $0.01$, so the left-hand and right-hand limits agree ✓.

**The identity.** For $x=1$:

$$
1-\cos1\approx1-0.540302=0.459698,\qquad 2\sin^2\frac12\approx2\cdot0.479426^2\approx0.459698\ \checkmark
$$

**The two derivations agree.** Both give $\frac12$ ✓.
