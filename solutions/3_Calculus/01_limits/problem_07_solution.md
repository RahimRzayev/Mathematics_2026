# Problem 7. Limit at a Point and Canceling a Factor

## Exercise

### Exercise 7. Limit at a Point and Canceling a Factor
Compute

$$
\lim_{x\to3}\frac{x^2-4x+3}{x-3}.
$$

Explain why the value of the function at $x=3$ is not needed to compute the limit.

> **Why this exercise:** separates the concept of a limit from the value of a function at a point.

---

## Answer

$$
\lim_{x\to3}\frac{x^2-4x+3}{x-3}=2
$$

The value at $x=3$ is not needed because the limit describes the values of the function at points near $3$ and different from $3$. The function is not defined at $x=3$ at all, and the limit still exists.

---

## Steps

### Step 1. Try direct substitution

At $x=3$ the numerator equals $9-12+3=0$ and the denominator equals $0$. The form is $\frac00$, so substitution gives no answer.

### Step 2. Factor the numerator

The numerator vanishes at $x=3$, so $x-3$ is one of its factors:

$$
x^2-4x+3=(x-1)(x-3)
$$

### Step 3. Cancel the common factor

For $x\neq3$ the factor $x-3$ is not zero and can be canceled:

$$
\frac{x^2-4x+3}{x-3}=\frac{(x-1)(x-3)}{x-3}=x-1
$$

### Step 4. Pass to the limit

$$
\lim_{x\to3}\frac{x^2-4x+3}{x-3}=\lim_{x\to3}(x-1)=3-1=2
$$

---

## Why it works

**The definition excludes the point itself.** The statement $\lim_{x\to3}f(x)=L$ means: for every $\varepsilon\gt0$ there is $\delta\gt0$ such that

$$
0\lt|x-3|\lt\delta\quad\Longrightarrow\quad|f(x)-L|\lt\varepsilon
$$

The condition $0\lt|x-3|$ removes the point $x=3$ from consideration. Whatever happens exactly at $x=3$ has no influence on the limit.

**Canceling is legitimate for the same reason.** The cancellation in Step 3 requires $x-3\neq0$. In a limit as $x\to3$ only points with $x\neq3$ are used, so the requirement is satisfied.

**Two functions that differ at one point.** Let $f(x)=\frac{x^2-4x+3}{x-3}$ and $g(x)=x-1$.

| | $f(x)$ | $g(x)$ |
|---|---|---|
| Domain | all real $x$ except $3$ | all real $x$ |
| Value at $x=3$ | not defined | $2$ |
| Values for $x\neq3$ | $x-1$ | $x-1$ |
| Limit as $x\to3$ | $2$ | $2$ |

The graph of $f$ is the line $y=x-1$ with the single point $(3,2)$ removed. The two functions agree at every point near $3$ other than $3$, so they have the same limit.

**Limit and value are separate notions.** If the function were given some value at $x=3$, for example $f(3)=10$, the limit would still be $2$. The limit states what the values approach. The value states what the function equals at the point. The two numbers may agree, may differ, or one of them may not exist.

---

## Check

**Factorization.**

$$
(x-1)(x-3)=x^2-3x-x+3=x^2-4x+3\ \checkmark
$$

**Values on both sides of $3$.**

| $x$ | $2.9$ | $2.99$ | $2.999$ | $3.001$ | $3.01$ | $3.1$ |
|---|---|---|---|---|---|---|
| $f(x)$ | $1.9$ | $1.99$ | $1.999$ | $2.001$ | $2.01$ | $2.1$ |

The values approach $2$ from both sides ✓.

**The definition.** For $x\neq3$,

$$
|f(x)-2|=|x-1-2|=|x-3|
$$

so the choice $\delta=\varepsilon$ satisfies the definition for every $\varepsilon\gt0$ ✓.
