# Problem 12. Exponential Function Limit

## Exercise

### Exercise 12. Exponential Function Limit
Compute

$$
\lim_{x\to0}(1+3x)^{1/x}.
$$

Connect the result with the limit from Exercise 5 and show the appropriate transformation.

> **Why this exercise:** teaches how to recognize the classical pattern after a transformation.

---

## Answer

$$
\lim_{x\to0}(1+3x)^{1/x}=e^3\approx20.0855
$$

The transformation is the substitution $t=3x$, which rewrites the expression as the cube of the classical pattern:

$$
(1+3x)^{1/x}=\left((1+t)^{1/t}\right)^3
$$

The connection with Exercise 5: the limit $\left(1+\frac1n\right)^n\to e$ is the pattern $(1+t)^{1/t}$ with $t=\frac1n$.

---

## Steps

### Step 1. Identify the form

As $x\to0$ the base $1+3x$ tends to $1$ and the exponent $\frac1x$ is unbounded. This is the indeterminate form $1^\infty$, the same as in Exercise 5.

### Step 2. Write the limit from Exercise 5 in function form

Exercise 5 gives

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^n=e
$$

With $t=\frac1n$ the expression becomes $(1+t)^{1/t}$, and $n\to\infty$ corresponds to $t\to0$. The corresponding limit for a real variable is the standard result

$$
\lim_{t\to0}(1+t)^{1/t}=e
$$

### Step 3. Substitute $t=3x$

Then $x=\frac t3$, so $\frac1x=\frac3t$, and $x\to0$ exactly when $t\to0$:

$$
(1+3x)^{1/x}=(1+t)^{3/t}
$$

### Step 4. Separate the pattern

By the rule $u^{ab}=\left(u^a\right)^b$:

$$
(1+t)^{3/t}=\left((1+t)^{1/t}\right)^3
$$

### Step 5. Pass to the limit

The inner expression tends to $e$, and the function $u\mapsto u^3$ is continuous:

$$
\lim_{x\to0}(1+3x)^{1/x}=\left(\lim_{t\to0}(1+t)^{1/t}\right)^3=e^3
$$

---

## Why it works

**Recognizing the pattern.** The classical limit has the shape

$$
\left(1+\mathrm{small}\right)^{1/\mathrm{small}}\to e
$$

where the same small quantity appears in the base and, inverted, in the exponent. In $(1+3x)^{1/x}$ the small quantity in the base is $3x$, but the exponent is $\frac1x$ and not $\frac1{3x}$. The exponent is $3$ times larger than the pattern requires:

$$
\frac1x=3\cdot\frac1{3x}
$$

The factor $3$ becomes the power of $e$.

**From the sequence to the function.** Exercise 5 uses only the arguments $t=\frac1n$. The function limit in Step 2 covers every real $t$ near $0$. The passage is justified by a squeeze: for a real $y$ with $n\le y\lt n+1$,

$$
\left(1+\frac1{n+1}\right)^n\le\left(1+\frac1y\right)^y\le\left(1+\frac1n\right)^{n+1}
$$

Both bounds tend to $e$, because each differs from a term of the sequence in Exercise 5 by a factor that tends to $1$. This gives the limit for $t=\frac1y\to0^+$. The case $t\to0^-$ reduces to it by an algebraic substitution.

**Both sides of $0$.** The limit is two-sided. For $x\gt0$ the base is slightly above $1$ and the exponent is large and positive. For $x\lt0$ the base is slightly below $1$ and the exponent is large and negative. Both cases give the same limit. The expression is defined when $1+3x\gt0$, which means $x\gt-\frac13$ and $x\neq0$.

**General statement.** The same substitution $t=kx$ gives, for every constant $k\neq0$,

$$
\lim_{x\to0}(1+kx)^{1/x}=e^k
$$

In sequence form, with $x=\frac1n$:

$$
\lim_{n\to\infty}\left(1+\frac3n\right)^n=e^3
$$

---

## Check

**Values on both sides of $0$.**

| $x$ | $-0.01$ | $-0.001$ | $-0.0001$ | $0.0001$ | $0.001$ | $0.01$ |
|---|---|---|---|---|---|---|
| $(1+3x)^{1/x}$ | $21.0294$ | $20.1763$ | $20.0946$ | $20.0765$ | $19.9955$ | $19.2186$ |

The values approach $e^3\approx20.0855$ from above on the left and from below on the right ✓.

**The value of $e^3$.**

$$
e^3\approx2.71828^3\approx20.0855\ \checkmark
$$

**The exponent rule.** For $x=0.01$ the two forms give the same number:

$$
1.03^{100}\approx19.2186,\qquad \left(1.03^{1/0.03}\right)^3\approx2.6786^3\approx19.2186\ \checkmark
$$
