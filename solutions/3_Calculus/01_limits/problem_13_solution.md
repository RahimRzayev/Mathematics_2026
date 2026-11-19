# Problem 13. Fundamental Trigonometric Limit

## Exercise

### Exercise 13. Fundamental Trigonometric Limit
Using

$$
\lim_{x\to0}\frac{\sin x}{x}=1,
$$

compute

$$
\lim_{x\to0}\frac{\sin5x}{x},\qquad \lim_{x\to0}\frac{\sin2x}{\sin3x}.
$$

In each case, show how you reduce the expression to the fundamental limit.

> **Why this exercise:** teaches how to reduce new limits to one known pattern.

---

## Answer

$$
\lim_{x\to0}\frac{\sin5x}{x}=5,\qquad \lim_{x\to0}\frac{\sin2x}{\sin3x}=\frac23
$$

**Reductions.**

$$
\frac{\sin5x}{x}=5\cdot\frac{\sin5x}{5x},\qquad \frac{\sin2x}{\sin3x}=\frac23\cdot\frac{\sin2x}{2x}\cdot\frac{3x}{\sin3x}
$$

Every fraction of the form $\frac{\sin u}{u}$ with $u\to0$ tends to $1$.

---

## Steps

### Step 1. First limit: identify the mismatch

Both $\sin5x$ and $x$ tend to $0$, so the form is $\frac00$. The fundamental limit requires the argument of the sine and the denominator to be the same expression. Here the argument is $5x$ and the denominator is $x$.

### Step 2. First limit: create the matching denominator

Multiplying and dividing by $5$:

$$
\frac{\sin5x}{x}=5\cdot\frac{\sin5x}{5x}
$$

### Step 3. First limit: substitute and pass to the limit

Let $t=5x$. Then $t\to0$ exactly when $x\to0$, and $t\neq0$ for $x\neq0$:

$$
\lim_{x\to0}\frac{\sin5x}{x}=5\cdot\lim_{t\to0}\frac{\sin t}{t}=5\cdot1=5
$$

### Step 4. Second limit: give each sine its own argument

The form is again $\frac00$. For $x\neq0$ the numerator is multiplied and divided by $2x$, and the denominator by $3x$:

$$
\frac{\sin2x}{\sin3x}=\frac{\frac{\sin2x}{2x}\cdot2x}{\frac{\sin3x}{3x}\cdot3x}
$$

### Step 5. Second limit: cancel $x$

$$
\frac{\sin2x}{\sin3x}=\frac23\cdot\frac{\frac{\sin2x}{2x}}{\frac{\sin3x}{3x}}
$$

### Step 6. Second limit: pass to the limit

With $t=2x$ in the numerator and $s=3x$ in the denominator, both fractions tend to $1$. The limit of the denominator is $1\neq0$, so the quotient rule applies:

$$
\lim_{x\to0}\frac{\sin2x}{\sin3x}=\frac23\cdot\frac11=\frac23
$$

---

## Why it works

**The pattern.** The fundamental limit is a statement about the shape

$$
\frac{\sin u}{u}\to1\qquad\mathrm{as}\quad u\to0
$$

The quantity $u$ may be any expression that tends to $0$ and is different from $0$ near the limit point. The argument of the sine and the denominator must be exactly the same. Each reduction above inserts the missing factor to restore this match and compensates for it outside the fraction.

**Why the substitution is allowed.** For $t=5x$ the condition $x\to0$ with $x\neq0$ is equivalent to $t\to0$ with $t\neq0$. The limit in $t$ is therefore the fundamental limit itself.

**Why the denominators are not zero.** In the second limit the expression requires $\sin3x\neq0$. For $0\lt|x|\lt\frac\pi3$ the number $3x$ lies strictly between $-\pi$ and $\pi$ and is not $0$, so $\sin3x\neq0$. The expression is defined at every point near $0$ other than $0$.

**Interpretation.** For small $u$ the fundamental limit says that $\sin u$ and $u$ are nearly equal in the sense that their ratio is close to $1$. Then $\sin5x$ is close to $5x$, and $\frac{\sin2x}{\sin3x}$ is close to $\frac{2x}{3x}=\frac23$. The steps above turn this informal description into a computation.

**Two invalid shortcuts.** The symbol $\sin$ cannot be canceled, and the coefficient cannot be moved out of the sine: $\sin5x\neq5\sin x$. The equality $\frac{\sin2x}{\sin3x}=\frac23$ does not hold for any particular $x\neq0$ near $0$. It holds only in the limit.

**General statement.** For constants $a$ and $b$ with $b\neq0$,

$$
\lim_{x\to0}\frac{\sin ax}{bx}=\frac ab,\qquad \lim_{x\to0}\frac{\sin ax}{\sin bx}=\frac ab
$$

---

## Check

**Numerical values, with $x$ in radians.**

| $x$ | $0.1$ | $0.01$ | $0.001$ |
|---|---|---|---|
| $\frac{\sin5x}{x}$ | $4.7943$ | $4.99792$ | $4.999979$ |
| $\frac{\sin2x}{\sin3x}$ | $0.67227$ | $0.666722$ | $0.66666722$ |

The first row approaches $5$ and the second approaches $\frac23\approx0.66666667$ ✓.

**Negative arguments.** Both expressions are even functions of $x$:

$$
\frac{\sin(-5x)}{-x}=\frac{-\sin5x}{-x}=\frac{\sin5x}{x},\qquad \frac{\sin(-2x)}{\sin(-3x)}=\frac{-\sin2x}{-\sin3x}=\frac{\sin2x}{\sin3x}
$$

The values at $-0.1$, $-0.01$, $-0.001$ are the same as in the table, so the limits from the left and from the right agree ✓.

**The reductions are identities.** For $x=0.1$:

$$
5\cdot\frac{\sin0.5}{0.5}\approx5\cdot0.95885=4.7943\ \checkmark
$$
