# Problem 5. The Classical Limit Leading to the Number $e$

## Exercise

### Exercise 5. The Classical Limit Leading to the Number $e$
Compute

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^n.
$$

Calculate several values for increasing $n$ and compare the observed behavior with the value of the limit. Explain why a few values do not constitute a proof.

> **Why this exercise:** connects a central limit with intuition based on concrete terms of a sequence.

---

## Answer

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^n=e\approx2.71828
$$

The sequence is increasing and bounded above by $3$, so it converges. Its limit is the definition of the number $e$.

| $n$ | $1$ | $2$ | $5$ | $10$ | $100$ | $1000$ | $10\ 000$ | $100\ 000$ |
|---|---|---|---|---|---|---|---|---|
| $\left(1+\frac1n\right)^n$ | $2$ | $2.25$ | $2.48832$ | $2.59374$ | $2.70481$ | $2.71692$ | $2.71815$ | $2.71827$ |

The values increase and settle near $2.718$, in agreement with the limit. A few values are not a proof, because a finite table says nothing about the infinitely many terms that were not computed.

---

## Steps

### Step 1. Identify the form

The base $1+\frac1n$ tends to $1$ and the exponent $n$ grows without bound. This is the indeterminate form $1^\infty$. Two tempting arguments give different answers, and both are wrong:

- "the base tends to $1$, and $1^n=1$, so the limit is $1$",
- "the base is greater than $1$ and the exponent grows, so the limit is $+\infty$".

The base and the exponent change at the same time, and the result depends on the balance between them.

### Step 2. Compute several values

$$
\left(1+\frac11\right)^1=2,\qquad \left(1+\frac12\right)^2=\frac94=2.25,\qquad \left(1+\frac15\right)^5=1.2^5=2.48832
$$

Further values are collected in the table in the Answer section.

### Step 3. Describe the observed behavior

- The values increase.
- The increases become smaller: from $n=1000$ to $n=10\ 000$ the value changes by about $0.0012$.
- The values appear to stay below $2.72$.

The observation suggests a limit close to $2.718$.

### Step 4. Expand by the binomial theorem

$$
\left(1+\frac1n\right)^n=\sum_{k=0}^{n}\binom nk\frac{1}{n^k}
$$

For $k\ge2$ the term with index $k$ can be rewritten as

$$
\binom nk\frac{1}{n^k}=\frac{n(n-1)\cdots(n-k+1)}{k!\cdot n^k}=\frac{1}{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}{n}\right)
$$

so that

$$
\left(1+\frac1n\right)^n=1+1+\sum_{k=2}^{n}\frac{1}{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}{n}\right)
$$

### Step 5. The sequence is increasing

When $n$ is replaced by $n+1$, every factor $1-\frac jn$ is replaced by the larger factor $1-\frac j{n+1}$, so every term of the sum increases. One additional positive term also appears. Therefore

$$
\left(1+\frac1n\right)^n\lt\left(1+\frac1{n+1}\right)^{n+1}
$$

### Step 6. The sequence is bounded above

Every factor $1-\frac jn$ is less than $1$, so the term with index $k$ is at most $\frac1{k!}$. Since $k!\ge2^{k-1}$,

$$
\left(1+\frac1n\right)^n\le1+1+\frac12+\frac14+\dots+\frac1{2^{n-1}}\lt1+2=3
$$

### Step 7. Conclusion

An increasing sequence that is bounded above converges. The sequence therefore has a limit, and this limit is denoted by $e$. The first term gives the lower bound $2$, and Step 6 gives the upper bound $3$:

$$
2\lt e\le3,\qquad e=2.718281828\dots
$$

---

## Why it works

**Two effects in balance.** The base approaches $1$, which pulls the power toward $1$. The exponent grows, which pushes the power up. The increase of the base above $1$ is $\frac1n$ and the number of multiplications is $n$, and the product of these two quantities is exactly $1$. This balance gives a finite limit greater than $1$.

**Why a few values do not constitute a proof.**

*Finitely many terms.* A table contains finitely many terms. A limit is a statement about all terms with sufficiently large index. No finite list covers them.

*The same table from a different sequence.* Let

$$
b_n=\left(1+\frac1n\right)^n+\frac{n}{10^{12}}
$$

For every $n$ in the table the added term is at most $10^{-7}$, so the table of $b_n$, rounded to five decimal places, looks the same as the table above. But $b_n$ grows without bound. The table cannot distinguish a convergent sequence from a divergent one.

*The limit is not identified.* The value $2.71827$ for $n=100\ 000$ is consistent with a limit of $2.7183$, of $2.71828$, or of $2.718281828\dots$

*Shrinking increases are not enough.* An increasing sequence with shrinking increases need not converge. The sums $1+\frac12+\frac13+\dots+\frac1n$ increase by smaller and smaller amounts and still grow without bound.

The argument in Steps 4 to 6 is a proof because it applies to every $n$ at once.

---

## Check

**Bounds.** Every value in the table lies between $2$ and $3$ ✓, and the values increase with $n$ ✓, as proved in Steps 5 and 6.

**Distance from the limit.**

| $n$ | $100$ | $1000$ | $10\ 000$ |
|---|---|---|---|
| $e-\left(1+\frac1n\right)^n$ | $\approx0.0135$ | $\approx0.00136$ | $\approx0.000136$ |

The distance falls about $10$ times when $n$ grows $10$ times. The convergence is real but slow: $n=10\ 000$ gives only three correct decimal places.

**The inequality $k!\ge2^{k-1}$.** For $k=1,2,3,4$ the values are $1\ge1$, $2\ge2$, $6\ge4$, $24\ge8$ ✓. Each further step multiplies the left side by $k\ge2$ and the right side by $2$, so the inequality is preserved.

**The geometric sum.**

$$
1+\frac12+\frac14+\dots+\frac1{2^{n-1}}=2-\frac1{2^{n-1}}\lt2\ \checkmark
$$
