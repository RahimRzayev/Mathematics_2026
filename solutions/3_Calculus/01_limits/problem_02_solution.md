# Problem 2. Different Growth Rates

## Exercise

### Exercise 2. Different Growth Rates
Compute

$$
\lim_{n\to\infty}\frac{3n+1}{n^2+4},\qquad \lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}.
$$

Compare the two cases and formulate a general observation about the degrees of the polynomials in the numerator and denominator.

> **Why this exercise:** teaches how to compare growth rates and recognize qualitatively different cases.

---

## Answer

$$
\lim_{n\to\infty}\frac{3n+1}{n^2+4}=0,\qquad \lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}=+\infty
$$

The first sequence converges to $0$. The second sequence diverges to $+\infty$.

**General observation.** Let the numerator have degree $k$ with leading coefficient $a$, and the denominator have degree $m$ with leading coefficient $b$.

| Degrees | Limit of the quotient |
|---|---|
| $k\lt m$ | $0$ |
| $k=m$ | $\frac{a}{b}$ |
| $k\gt m$ | $+\infty$ if $\frac{a}{b}\gt0$, and $-\infty$ if $\frac{a}{b}\lt0$ |

---

## Steps

### Step 1. First limit: divide by $n^2$

The highest power in the denominator is $n^2$:

$$
\frac{3n+1}{n^2+4}=\frac{\frac3n+\frac1{n^2}}{1+\frac4{n^2}}
$$

### Step 2. First limit: pass to the limit

The numerator tends to $0$ and the denominator tends to $1$:

$$
\lim_{n\to\infty}\frac{3n+1}{n^2+4}=\frac{0+0}{1+0}=0
$$

### Step 3. Second limit: divide by $n^2$

The highest power in the denominator is again $n^2$:

$$
\frac{2n^3-n}{5n^2+1}=\frac{2n-\frac1n}{5+\frac1{n^2}}
$$

### Step 4. Second limit: pass to the limit

The numerator $2n-\frac1n$ grows without bound and the denominator tends to $5$, a positive number. The quotient grows without bound:

$$
\lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}=+\infty
$$

### Step 5. Compare the two cases

| | First sequence | Second sequence |
|---|---|---|
| Degree of the numerator | $1$ | $3$ |
| Degree of the denominator | $2$ | $2$ |
| Which part grows faster | denominator | numerator |
| Result | $0$ | $+\infty$ |

Together with Exercise 1, where the degrees are equal and the limit is the ratio of the leading coefficients, this gives the three cases of the general observation.

---

## Why it works

**One formula for all three cases.** Factoring the leading term out of each polynomial gives

$$
\frac{an^k+\dots}{bn^m+\dots}=\frac{a}{b}\cdot n^{k-m}\cdot\frac{1+\dots}{1+\dots}
$$

where the omitted terms in the last fraction are multiples of negative powers of $n$ and tend to $0$. The last fraction tends to $1$, so the behavior is decided by the factor $n^{k-m}$:

- for $k\lt m$ the exponent is negative and $n^{k-m}\to0$,
- for $k=m$ the factor equals $1$ and the limit is $\frac{a}{b}$,
- for $k\gt m$ the exponent is positive and $n^{k-m}\to+\infty$, with the sign of the result set by $\frac{a}{b}$.

**Applied to the two sequences.** For large $n$ the first quotient behaves like the quotient of its leading terms, and so does the second:

$$
\frac{3n}{n^2}=\frac3n\to0,\qquad \frac{2n^3}{5n^2}=\frac{2n}{5}\to+\infty
$$

**Growth rate, not size.** In the first sequence the numerator also grows without bound. The limit is $0$ because the denominator grows faster. A limit of a quotient compares rates of growth.

---

## Check

| $n$ | $10$ | $100$ | $1000$ |
|---|---|---|---|
| $\frac{3n+1}{n^2+4}$ | $\frac{31}{104}\approx0.2981$ | $\frac{301}{10004}\approx0.03009$ | $\frac{3001}{1000004}\approx0.003001$ |
| $\frac3n$ | $0.3$ | $0.03$ | $0.003$ |
| $\frac{2n^3-n}{5n^2+1}$ | $\frac{1990}{501}\approx3.972$ | $\approx39.997$ | $\approx399.9997$ |
| $\frac{2n}{5}$ | $4$ | $40$ | $400$ |

The first sequence follows $\frac3n$ and shrinks by a factor of about $10$ when $n$ grows $10$ times ✓. The second follows $\frac{2n}{5}$ and grows by a factor of about $10$ ✓.

**Bound for the second sequence.** For $n\ge1$ the inequalities $2n^3-n\ge n^3$ and $5n^2+1\le6n^2$ hold, so

$$
\frac{2n^3-n}{5n^2+1}\ge\frac{n^3}{6n^2}=\frac n6
$$

The right side exceeds every number for large $n$, which confirms the divergence to $+\infty$ ✓.
