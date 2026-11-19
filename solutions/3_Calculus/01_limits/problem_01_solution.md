# Problem 1. Dominant Terms in a Sequence

## Exercise

### Exercise 1. Dominant Terms in a Sequence
Compute

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.
$$

Explain why the highest-degree terms determine the result.

> **Why this exercise:** introduces the idea of a dominant term and teaches how to simplify the behavior of expressions for large arguments.

---

## Answer

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}=2
$$

The highest-degree terms determine the result because, after $n^2$ is factored out of the numerator and the denominator, every other term becomes a multiple of $\frac1n$ or $\frac1{n^2}$ and tends to $0$. Only the coefficients $4$ and $2$ remain, and $\frac42=2$.

---

## Steps

### Step 1. Identify the form

The numerator and the denominator both grow without bound, so the expression has the indeterminate form $\frac{\infty}{\infty}$. The limit cannot be read off directly.

### Step 2. Divide by the highest power of $n$

The highest power in the denominator is $n^2$. Dividing the numerator and the denominator by $n^2$ does not change the fraction:

$$
\frac{4n^2-3n+1}{2n^2+5n-7}=\frac{4-\frac3n+\frac1{n^2}}{2+\frac5n-\frac7{n^2}}
$$

### Step 3. Limits of the separate terms

$$
\lim_{n\to\infty}\frac3n=0,\qquad \lim_{n\to\infty}\frac1{n^2}=0,\qquad \lim_{n\to\infty}\frac5n=0,\qquad \lim_{n\to\infty}\frac7{n^2}=0
$$

### Step 4. Arithmetic of limits

The numerator tends to $4$ and the denominator tends to $2\neq0$, so the limit of the quotient is the quotient of the limits:

$$
\lim_{n\to\infty}\frac{4-\frac3n+\frac1{n^2}}{2+\frac5n-\frac7{n^2}}=\frac{4-0+0}{2+0-0}=2
$$

---

## Why it works

**The dominant term.** Factoring the highest power out of each polynomial gives

$$
4n^2-3n+1=4n^2\left(1-\frac{3}{4n}+\frac{1}{4n^2}\right),\qquad 2n^2+5n-7=2n^2\left(1+\frac{5}{2n}-\frac{7}{2n^2}\right)
$$

Both brackets tend to $1$. For large $n$ the numerator behaves like $4n^2$ and the denominator like $2n^2$, and

$$
\frac{4n^2}{2n^2}=2
$$

The terms $-3n+1$ and $5n-7$ are not small by themselves. They are small in comparison with $n^2$, and this is the only thing that matters in a quotient.

**Sizes for a concrete $n$.** For $n=1000$:

| Term | $4n^2$ | $3n$ | $1$ |
|---|---|---|---|
| Value | $4\ 000\ 000$ | $3000$ | $1$ |

The term $3n$ is less than $0.1$ percent of $4n^2$, and the share decreases further as $n$ grows.

**Why the division is needed.** The rule "limit of a quotient equals quotient of limits" requires finite limits and a nonzero limit of the denominator. Before the division neither the numerator nor the denominator has a finite limit. After the division both have finite limits, $4$ and $2$, and the rule applies.

---

## Check

**Numerical values.**

| $n$ | $10$ | $100$ | $1000$ | $10\ 000$ |
|---|---|---|---|---|
| $a_n$ | $\frac{371}{243}\approx1.5267$ | $\frac{39701}{20493}\approx1.9373$ | $\frac{3997001}{2004993}\approx1.9935$ | $\approx1.99935$ |

The values approach $2$ ✓.

**Exact distance from the limit.**

$$
a_n-2=\frac{4n^2-3n+1-2\left(2n^2+5n-7\right)}{2n^2+5n-7}=\frac{-13n+15}{2n^2+5n-7}
$$

The numerator has degree $1$ and the denominator has degree $2$, so the difference tends to $0$ ✓. For $n\ge2$ the difference is negative, which agrees with the table: the terms approach $2$ from below. For $n=10$ the formula gives $\frac{-115}{243}\approx-0.4733$, and $1.5267-2=-0.4733$ ✓.

**Remark on $n=1$.** The denominator factors as $2n^2+5n-7=(2n+7)(n-1)$, so the term $a_1$ is not defined. This does not affect the limit, which depends only on the terms with large $n$.
