# Problem 2. Powers, Roots, and the Domain

## Exercise

### Problem 2. Powers, Roots, and the Domain
For

$$
f(x)=2\sqrt{x}-\frac{3}{x^2}+x^{3/2}
$$

1. rewrite the function using powers,
2. determine the domain,
3. compute the derivative,
4. compare the domain of the function with the domain of its derivative.

> **Why this problem:** it teaches how to rewrite different forms so that the power rule can be applied and how to keep track of the domain.

---

## Answer

1. Power form:

$$
f(x)=2x^{1/2}-3x^{-2}+x^{3/2}
$$

2. Domain of $f$: $x\gt0$, that is, the interval $(0,\infty)$.

3. Derivative:

$$
f'(x)=x^{-1/2}+6x^{-3}+\frac32x^{1/2}=\frac1{\sqrt x}+\frac6{x^3}+\frac32\sqrt x
$$

4. The derivative is defined for $x\gt0$, so the two domains coincide: both are $(0,\infty)$. Term by term the picture is different: the derivative of $2\sqrt x$ loses the point $x=0$, but that point is already excluded from the domain of $f$ by the term $-\frac3{x^2}$.

---

## Sketch

![Graph of f on the interval (0,3.5], increasing, with the y-axis as vertical asymptote](figures/problem_02_domain.png)

The graph exists only to the right of the $y$-axis. Near $x=0$ the term $-\frac3{x^2}$ dominates and the values fall to $-\infty$, so the $y$-axis, drawn red dashed, is a vertical asymptote. The curve crosses the $x$-axis at $(1,0)$ and increases on the whole domain, in agreement with $f'(x)\gt0$. The two axes use different units.

---

## Steps

### Step 1. Rewrite with powers

The two identities used are

$$
\sqrt x=x^{1/2},\qquad \frac1{x^n}=x^{-n}
$$

Therefore

$$
f(x)=2x^{1/2}-3x^{-2}+x^{3/2}
$$

### Step 2. Domain

Each term imposes its own condition:

| Term | Condition | Allowed $x$ |
|---|---|---|
| $2\sqrt x$ | square root of a real number needs $x\ge0$ | $[0,\infty)$ |
| $-\frac3{x^2}$ | denominator must not vanish | $x\neq0$ |
| $x^{3/2}=\left(\sqrt x\right)^3$ | square root again | $[0,\infty)$ |

The domain of $f$ is the intersection of the three sets:

$$
D(f)=[0,\infty)\cap\left((-\infty,0)\cup(0,\infty)\right)=(0,\infty)
$$

### Step 3. Differentiate

In power form every term is $c\ x^r$, and the power rule $\left(x^r\right)'=rx^{r-1}$ holds for every real exponent $r$ (for $x\gt0$):

| Term | Rule | Derivative |
|---|---|---|
| $2x^{1/2}$ | $2\cdot\frac12x^{-1/2}$ | $x^{-1/2}$ |
| $-3x^{-2}$ | $-3\cdot(-2)x^{-3}$ | $6x^{-3}$ |
| $x^{3/2}$ | $\frac32x^{1/2}$ | $\frac32x^{1/2}$ |

$$
f'(x)=x^{-1/2}+6x^{-3}+\frac32x^{1/2}=\frac1{\sqrt x}+\frac6{x^3}+\frac32\sqrt x
$$

### Step 4. Domain of the derivative

| Term of $f'(x)$ | Condition | Allowed $x$ |
|---|---|---|
| $\frac1{\sqrt x}$ | $x\ge0$ and $\sqrt x\neq0$ | $(0,\infty)$ |
| $\frac6{x^3}$ | $x\neq0$ | $x\neq0$ |
| $\frac32\sqrt x$ | $x\ge0$ | $[0,\infty)$ |

The intersection is $(0,\infty)$, so

$$
D(f')=(0,\infty)=D(f)
$$

### Step 5. Comparison

The derivative never exists at points outside $D(f)$: a derivative at $x_0$ requires the value $f(x_0)$. So in general $D(f')\subseteq D(f)$, and the only question is whether the derivative loses points of $D(f)$.

| Term | Domain of the term | Domain of its derivative | Point lost |
|---|---|---|---|
| $2\sqrt x$ | $[0,\infty)$ | $(0,\infty)$ | $x=0$ |
| $-\frac3{x^2}$ | $x\neq0$ | $x\neq0$ | none |
| $x^{3/2}$ | $[0,\infty)$ | $[0,\infty)$, one-sided at $0$ | none |

The only point that could be lost is $x=0$, and $x=0$ is not in $D(f)$. For this function nothing is lost: $D(f')=D(f)$.

---

## Why it works

**Why rewrite with powers.** The power rule is stated for $x^r$. Roots and reciprocals are powers in disguise, and after rewriting, the whole function is a sum of constant multiples of powers. Linearity of the derivative then reduces the work to three applications of one rule, with no quotient rule for $\frac3{x^2}$ and no separate formula for $\sqrt x$.

**Why the domain has to be tracked separately.** The power form hides the conditions. The expression $x^{1/2}$ looks harmless, but it still means $\sqrt x$ and needs $x\ge0$. The expression $x^{-2}$ still means $\frac1{x^2}$ and needs $x\neq0$. The power rule for a non-integer exponent is valid only where the power is defined by a root, here for $x\gt0$.

**Why a derivative can lose a point.** For $g(x)=\sqrt x$ at $x_0=0$ the difference quotient is

$$
\frac{\sqrt h-0}h=\frac1{\sqrt h}\to\infty\quad(h\to0^+)
$$

so $g$ is defined at $0$ but has no derivative there: the tangent at the origin is vertical. For $x^{3/2}$ the quotient is $\frac{h^{3/2}}h=\sqrt h\to0$, so the one-sided derivative at $0$ exists and equals $0$. Exponents below $1$ produce a vertical tangent at the endpoint, exponents above $1$ do not.

**Sign of the derivative.** All three terms of $f'(x)$ are positive for $x\gt0$, so $f'(x)\gt0$ on the whole domain and $f$ is increasing on $(0,\infty)$.

---

## Check

**Difference quotients.** $f'(1)=1+6+\frac32=8.5$ and $f'(4)=\frac12+\frac6{64}+3=3.59375$.

| $h$ | $\frac{f(1+h)-f(1)}h$ | $\frac{f(4+h)-f(4)}h$ |
|---|---|---|
| $0.01$ | $8.4124$ | $3.59496$ |
| $0.001$ | $8.4911$ | $3.59387$ |

The quotients approach $8.5$ and $3.59375$ ✓.

**Values used in the sketch.**

$$
f(1)=2-3+1=0,\qquad f(4)=4-\frac3{16}+8=11.8125\ \checkmark
$$

**Behavior at the edge of the domain.** For $x=0.01$: $f(0.01)=0.2-30\ 000+0.001\approx-29\ 999.8$, so the values fall without bound as $x\to0^+$ ✓.
