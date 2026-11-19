# Problem 4. Powers and Oscillation

## Exercise

### Exercise 4. Powers and Oscillation
Analyze

$$
\left(\frac23\right)^n,\qquad \left(\frac32\right)^n,\qquad (-1)^n,\qquad \frac{(-1)^n}{n}.
$$

For each sequence, describe the type of behavior and justify your answer.

> **Why this exercise:** organizes the basic types of sequence behavior and shows that oscillation does not always rule out convergence.

---

## Answer

| Sequence | Type of behavior | Limit |
|---|---|---|
| $\left(\frac23\right)^n$ | positive, decreasing, bounded | converges to $0$ |
| $\left(\frac32\right)^n$ | positive, increasing, unbounded | diverges to $+\infty$ |
| $(-1)^n$ | bounded, oscillates between $-1$ and $1$ | no limit |
| $\frac{(-1)^n}{n}$ | bounded, oscillates in sign with shrinking amplitude | converges to $0$ |

---

## Steps

### Step 1. First terms

| $n$ | $1$ | $2$ | $3$ | $4$ | $5$ |
|---|---|---|---|---|---|
| $\left(\frac23\right)^n$ | $\frac23\approx0.667$ | $\frac49\approx0.444$ | $\frac8{27}\approx0.296$ | $\frac{16}{81}\approx0.198$ | $\frac{32}{243}\approx0.132$ |
| $\left(\frac32\right)^n$ | $1.5$ | $2.25$ | $3.375$ | $5.0625$ | $7.59375$ |
| $(-1)^n$ | $-1$ | $1$ | $-1$ | $1$ | $-1$ |
| $\frac{(-1)^n}{n}$ | $-1$ | $\frac12$ | $-\frac13$ | $\frac14$ | $-\frac15$ |

### Step 2. The sequence $\left(\frac32\right)^n$

Each term is the previous one multiplied by $\frac32\gt1$, so the sequence is increasing. By Bernoulli's inequality $(1+h)^n\ge1+nh$ for $h\gt0$:

$$
\left(\frac32\right)^n=\left(1+\frac12\right)^n\ge1+\frac n2
$$

The right side grows without bound, so

$$
\lim_{n\to\infty}\left(\frac32\right)^n=+\infty
$$

### Step 3. The sequence $\left(\frac23\right)^n$

Each term is the previous one multiplied by $\frac23\lt1$, so the sequence is decreasing and positive. It is the reciprocal of the sequence from Step 2:

$$
0\lt\left(\frac23\right)^n=\frac{1}{\left(\frac32\right)^n}\le\frac{1}{1+\frac n2}=\frac{2}{n+2}
$$

Both bounds tend to $0$. By the squeeze theorem

$$
\lim_{n\to\infty}\left(\frac23\right)^n=0
$$

### Step 4. The sequence $(-1)^n$

The terms with even and odd indices form two constant subsequences:

$$
a_{2k}=1\to1,\qquad a_{2k+1}=-1\to-1
$$

If a sequence converges, every subsequence converges to the same limit. Here two subsequences have different limits, so the sequence has no limit. It is bounded, since $|a_n|=1$, but it does not converge.

### Step 5. The sequence $\frac{(-1)^n}{n}$

The sign alternates, but the absolute value is $\frac1n$:

$$
-\frac1n\le\frac{(-1)^n}{n}\le\frac1n
$$

Both bounds tend to $0$. By the squeeze theorem

$$
\lim_{n\to\infty}\frac{(-1)^n}{n}=0
$$

---

## Why it works

**Bernoulli's inequality.** By the binomial theorem, for $h\gt0$,

$$
(1+h)^n=1+nh+\binom n2h^2+\dots+h^n\ge1+nh
$$

because all omitted terms are positive. Repeated multiplication by a number greater than $1$ grows at least as fast as a linear function, and a linear function is unbounded.

**The general geometric sequence $q^n$.** The first three sequences are cases of one family:

| Ratio $q$ | Behavior of $q^n$ |
|---|---|
| $q\gt1$ | diverges to $+\infty$ |
| $q=1$ | constant, limit $1$ |
| $-1\lt q\lt1$ | converges to $0$ |
| $q\le-1$ | no limit |

**Oscillation and convergence.** Convergence to $L$ means that for every $\varepsilon\gt0$ all terms from some index on satisfy $|a_n-L|\lt\varepsilon$. The definition does not require the terms to approach $L$ from one side.

- In $(-1)^n$ the distance between consecutive terms is always $2$. The terms cannot all stay within a small distance of one number.
- In $\frac{(-1)^n}{n}$ the terms jump from one side of $0$ to the other, but the size of the jumps tends to $0$. The terms stay within $\frac1n$ of the number $0$.

Oscillation rules out convergence only when its amplitude does not shrink to $0$.

---

## Check

**Bernoulli bounds for $n=10$.**

$$
\left(\frac32\right)^{10}\approx57.665\ge1+\frac{10}{2}=6\ \checkmark,\qquad \left(\frac23\right)^{10}\approx0.01734\le\frac{2}{12}\approx0.1667\ \checkmark
$$

**Later terms.** $\left(\frac23\right)^{20}\approx0.0003$ and $\left(\frac32\right)^{20}\approx3325$, in agreement with the limits $0$ and $+\infty$ ✓.

**The definition for $\frac{(-1)^n}{n}$.** For $\varepsilon=0.01$ every $n\gt100$ gives

$$
\left|\frac{(-1)^n}{n}-0\right|=\frac1n\lt0.01\ \checkmark
$$

In general, the index $N\ge\frac1\varepsilon$ works for any $\varepsilon\gt0$.

**The definition fails for $(-1)^n$.** Suppose the limit is $L$ and take $\varepsilon=\frac12$. From some index on, both the terms equal to $1$ and the terms equal to $-1$ must satisfy $|1-L|\lt\frac12$ and $|-1-L|\lt\frac12$. Then

$$
2=|1-(-1)|\le|1-L|+|L-(-1)|\lt\frac12+\frac12=1
$$

which is a contradiction. No number $L$ is the limit ✓.
