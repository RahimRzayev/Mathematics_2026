# Problem 6. From a Sequence to a Function — Limit at Infinity

## Exercise

### Exercise 6. From a Sequence to a Function — Limit at Infinity
Compute

$$
\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}.
$$

Compare the method with Exercise 1. Explain what changes when moving from $n$ to a real variable $x$, and what stays the same.

> **Why this exercise:** deliberately transfers a technique from sequence limits to function limits.

---

## Answer

$$
\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}=\frac35
$$

| | Exercise 1 (sequence) | Exercise 6 (function) |
|---|---|---|
| Variable | $n=1,2,3,\dots$ | every real $x$ in the domain |
| Form | $\frac{\infty}{\infty}$ | $\frac{\infty}{\infty}$ |
| Method | divide by $n^2$ | divide by $x^2$ |
| Result | ratio of leading coefficients, $\frac42=2$ | ratio of leading coefficients, $\frac35$ |

**What stays the same:** the indeterminate form, the division by the highest power, the vanishing of the lower-order terms, and the arithmetic of limits.

**What changes:** the variable runs through all real numbers and not only through integers. The definition of the limit must hold for every real $x$ beyond some bound, the function must be defined on an interval reaching to infinity, and the limit as $x\to-\infty$ becomes a separate meaningful question.

---

## Steps

### Step 1. Identify the form

The numerator and the denominator both grow without bound as $x\to\infty$. The form is $\frac{\infty}{\infty}$, as in Exercise 1.

### Step 2. Divide by $x^2$

For $x\neq0$:

$$
\frac{3x^2-x+1}{5x^2+4x-2}=\frac{3-\frac1x+\frac1{x^2}}{5+\frac4x-\frac2{x^2}}
$$

### Step 3. Limits of the separate terms

$$
\lim_{x\to\infty}\frac1x=0,\qquad \lim_{x\to\infty}\frac1{x^2}=0
$$

### Step 4. Arithmetic of limits

The numerator tends to $3$ and the denominator tends to $5\neq0$:

$$
\lim_{x\to\infty}\frac{3-\frac1x+\frac1{x^2}}{5+\frac4x-\frac2{x^2}}=\frac{3-0+0}{5+0-0}=\frac35
$$

### Step 5. Check that the function is defined for large $x$

The denominator vanishes where $5x^2+4x-2=0$:

$$
x=\frac{-4\pm\sqrt{16+40}}{10}=\frac{-2\pm\sqrt{14}}{5},\qquad x\approx0.348\quad\mathrm{or}\quad x\approx-1.148
$$

For $x\gt1$ the denominator is positive, so the function is defined on the whole interval $(1,\infty)$ and the limit at infinity makes sense.

---

## Why it works

**The algebra does not depend on the kind of variable.** Dividing by $x^2$ and using $\frac1x\to0$ are valid for real $x$ exactly as for integer $n$. The dominant terms $3x^2$ and $5x^2$ decide the result in the same way.

**The definition is more demanding.** The two definitions differ in the set of arguments that must be controlled:

- sequence: for every $\varepsilon\gt0$ there is $N$ such that $|a_n-L|\lt\varepsilon$ for all integers $n\gt N$,
- function: for every $\varepsilon\gt0$ there is $M$ such that $|f(x)-L|\lt\varepsilon$ for all real $x\gt M$.

The function limit controls all the points between the integers as well.

**A function limit implies the sequence limit, but not conversely.** If $f(x)\to L$ as $x\to\infty$, then the sequence $a_n=f(n)$ also tends to $L$, because the integers are among the real numbers. Here this gives

$$
\lim_{n\to\infty}\frac{3n^2-n+1}{5n^2+4n-2}=\frac35
$$

The converse fails in general. For $f(x)=\sin(\pi x)$ every integer gives $f(n)=0$, so the sequence $f(n)$ converges to $0$. The function has no limit as $x\to\infty$, because it keeps taking the values $1$ and $-1$ between the integers.

**The second direction.** A sequence has only one direction, $n\to\infty$. A function of a real variable can also be studied as $x\to-\infty$. The same computation gives

$$
\lim_{x\to-\infty}\frac{3x^2-x+1}{5x^2+4x-2}=\frac35
$$

because $\frac1x\to0$ in both directions.

---

## Check

**Numerical values, including a non-integer argument.**

| $x$ | $10$ | $10.5$ | $100$ | $1000$ |
|---|---|---|---|---|
| $f(x)$ | $\frac{291}{538}\approx0.5409$ | $\frac{321.25}{591.25}\approx0.5433$ | $\frac{29901}{50398}\approx0.5933$ | $\approx0.5993$ |

| $x$ | $-10$ | $-100$ | $-1000$ |
|---|---|---|---|
| $f(x)$ | $\frac{311}{458}\approx0.6790$ | $\frac{30101}{49598}\approx0.6069$ | $\approx0.6007$ |

The values approach $0.6$ in both directions ✓.

**Exact distance from the limit.**

$$
f(x)-\frac35=\frac{5\left(3x^2-x+1\right)-3\left(5x^2+4x-2\right)}{5\left(5x^2+4x-2\right)}=\frac{-17x+11}{5\left(5x^2+4x-2\right)}
$$

The numerator has degree $1$ and the denominator has degree $2$, so the difference tends to $0$ ✓. For large positive $x$ the difference is negative and for large negative $x$ it is positive. This agrees with the tables: the values approach $0.6$ from below on the right and from above on the left ✓.
