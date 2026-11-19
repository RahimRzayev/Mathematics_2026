# Problem 11. An n-th Root

## Exercise

### Exercise 11. An n-th Root
Compute

$$
\lim_{n\to\infty}\sqrt[n]{5^n+2^n}.
$$

Explain which term dominates and why the transformation looks different from the case of a quotient of polynomials.

> **Why this exercise:** extends the idea of dominance to exponential expressions.

---

## Answer

$$
\lim_{n\to\infty}\sqrt[n]{5^n+2^n}=5
$$

The term $5^n$ dominates, because $\frac{2^n}{5^n}=\left(\frac25\right)^n\to0$.

The transformation differs from the polynomial case because there is no quotient to divide. The dominant term is factored out under the root, the root of $5^n$ gives exactly $5$, and the root of the remaining factor tends to $1$. The limit is the base of the dominant term, not a ratio of coefficients.

---

## Steps

### Step 1. Find the dominant term

The ratio of the two terms is

$$
\frac{2^n}{5^n}=\left(\frac25\right)^n\to0
$$

by Exercise 4, since $0\lt\frac25\lt1$. The term $2^n$ becomes negligible in comparison with $5^n$.

### Step 2. Factor out the dominant term

$$
5^n+2^n=5^n\left(1+\left(\frac25\right)^n\right)
$$

### Step 3. Take the root

The $n$-th root of a product is the product of the $n$-th roots, and $\sqrt[n]{5^n}=5$:

$$
\sqrt[n]{5^n+2^n}=5\cdot\sqrt[n]{1+\left(\frac25\right)^n}
$$

### Step 4. Bound the remaining factor

Since $0\lt\left(\frac25\right)^n\lt1$,

$$
1\lt1+\left(\frac25\right)^n\lt2
$$

Taking $n$-th roots and multiplying by $5$:

$$
5\lt\sqrt[n]{5^n+2^n}\lt5\cdot\sqrt[n]{2}
$$

### Step 5. The limit of $\sqrt[n]{2}$

By Bernoulli's inequality $\left(1+\frac1n\right)^n\ge1+n\cdot\frac1n=2$. Taking $n$-th roots:

$$
1\lt\sqrt[n]{2}\le1+\frac1n
$$

Both bounds tend to $1$, so $\sqrt[n]{2}\to1$ by the squeeze theorem.

### Step 6. Apply the squeeze theorem

The lower bound in Step 4 is the constant $5$, and the upper bound tends to $5\cdot1=5$. Therefore

$$
\lim_{n\to\infty}\sqrt[n]{5^n+2^n}=5
$$

---

## Why it works

**Dominance among exponentials.** For polynomials the term with the highest power dominates. For exponentials the term with the largest base dominates, and the dominance is much stronger: the ratio $\left(\frac25\right)^n$ falls below $0.0002$ already for $n=10$.

**Why the transformation looks different.** The idea is the same as in Exercise 1: isolate the dominant term and show that the rest has no influence. The form of the expression changes how this is done.

| | Quotient of polynomials | $n$-th root of a sum of powers |
|---|---|---|
| Operation that isolates the dominant term | divide numerator and denominator by $n^k$ | factor $5^n$ out under the root |
| What happens to the other terms | they tend to $0$ as terms of a sum | they form a factor that tends to $1$ |
| What the limit is | ratio of the leading coefficients | base of the dominant power |

**Why the limit cannot be taken inside the root directly.** The expression under the root tends to $+\infty$ and the exponent $\frac1n$ tends to $0$. This is the indeterminate form $\infty^0$. Factoring replaces it by the exact number $5$ multiplied by a factor of the form "bounded quantity to the power $\frac1n$", which tends to $1$.

**Coefficients do not matter.** The same argument shows that a constant coefficient has no effect. For example,

$$
\sqrt[n]{7\cdot5^n+2^n}=5\cdot\sqrt[n]{7+\left(\frac25\right)^n}\to5
$$

because the factor under the last root lies between $7$ and $8$, and $\sqrt[n]{7}\to1$ and $\sqrt[n]{8}\to1$. In a quotient of polynomials the coefficients decide the answer. Under an $n$-th root they disappear.

**General statement.** For positive numbers $a$ and $b$,

$$
\lim_{n\to\infty}\sqrt[n]{a^n+b^n}=\max(a,b)
$$

---

## Check

| $n$ | $1$ | $2$ | $3$ | $5$ | $10$ |
|---|---|---|---|---|---|
| $5^n+2^n$ | $7$ | $29$ | $133$ | $3157$ | $9\ 766\ 649$ |
| $\sqrt[n]{5^n+2^n}$ | $7$ | $\approx5.3852$ | $\approx5.1045$ | $\approx5.0102$ | $\approx5.00005$ |
| Upper bound $5\cdot\sqrt[n]{2}$ | $10$ | $\approx7.0711$ | $\approx6.2996$ | $\approx5.7435$ | $\approx5.3589$ |

Every value lies between $5$ and the upper bound, and the values decrease toward $5$ ✓.

**Speed of convergence.** The sequence reaches $5.00005$ at $n=10$, far below its upper bound. The bound in Step 4 is generous: the factor under the root is close to $1$, not close to $2$. The bound is still sufficient for the proof, because the squeeze theorem needs only that both bounds tend to $5$ ✓.
