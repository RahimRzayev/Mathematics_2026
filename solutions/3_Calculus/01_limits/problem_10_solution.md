# Problem 10. Continuity of a Piecewise Function

## Exercise

### Exercise 10. Continuity of a Piecewise Function
Find $a$ so that

$$
f(x)=
\begin{cases}
ax+1,&x<2, \\
x^2-1,&x\ge2
\end{cases}
$$

is continuous at $x=2$. Explicitly compare the left-hand limit, right-hand limit, and function value.

> **Why this exercise:** organizes the definition of continuity as agreement among three quantities.

---

## Answer

$$
a=1
$$

| Quantity | Formula used | Value |
|---|---|---|
| Left-hand limit $\lim_{x\to2^-}f(x)$ | $ax+1$ | $2a+1$ |
| Right-hand limit $\lim_{x\to2^+}f(x)$ | $x^2-1$ | $3$ |
| Function value $f(2)$ | $x^2-1$ | $3$ |

The three quantities agree exactly when $2a+1=3$, which gives $a=1$.

---

## Steps

### Step 1. Left-hand limit

For $x\lt2$ the function is given by $ax+1$, a polynomial:

$$
\lim_{x\to2^-}f(x)=\lim_{x\to2^-}(ax+1)=2a+1
$$

### Step 2. Right-hand limit

For $x\gt2$ the function is given by $x^2-1$:

$$
\lim_{x\to2^+}f(x)=\lim_{x\to2^+}\left(x^2-1\right)=4-1=3
$$

### Step 3. Function value

The point $x=2$ belongs to the second branch, because the condition there is $x\ge2$:

$$
f(2)=2^2-1=3
$$

### Step 4. Compare the three quantities

Continuity at $x=2$ requires

$$
\lim_{x\to2^-}f(x)=\lim_{x\to2^+}f(x)=f(2)
$$

The right-hand limit and the function value are both $3$ for every $a$. The remaining condition is

$$
2a+1=3\quad\Longrightarrow\quad a=1
$$

### Step 5. The resulting function

$$
f(x)=
\begin{cases}
x+1, & x\lt2, \\
x^2-1, & x\ge2
\end{cases}
$$

---

## Why it works

**Continuity as agreement of three quantities.** A function is continuous at a point $x_0$ when

$$
\lim_{x\to x_0}f(x)=f(x_0)
$$

This single equation contains three requirements:

1. the value $f(x_0)$ is defined,
2. the two-sided limit exists, which means that the left-hand and right-hand limits are equal,
3. the limit equals the value.

**Why only one condition on $a$ appears.** The point $x=2$ and all points to its right are described by the same polynomial $x^2-1$. A polynomial is continuous, so the right-hand limit automatically equals the value. The parameter $a$ enters only through the left branch, and the left branch must arrive at the same height $3$.

**Meaning on the graph.** The left branch is a line through the point $(0,1)$ with slope $a$. It ends at height $2a+1$ above $x=2$. The right branch starts at the point $(2,3)$. Changing $a$ rotates the line about $(0,1)$, and $a=1$ is the only slope for which the end of the line meets the start of the parabola.

**What happens for other values of $a$.** For $a\neq1$ the one-sided limits are different, the two-sided limit does not exist, and the graph has a jump of size

$$
|(2a+1)-3|=2|a-1|
$$

For example, $a=0$ gives a left-hand limit of $1$ and a jump of size $2$.

**Continuity elsewhere.** Each branch is a polynomial, so $f$ is continuous at every point other than $2$ for any $a$. With $a=1$ the function is continuous on the whole real line.

---

## Check

**Values near $x=2$ for $a=1$.**

| $x$ | $1.9$ | $1.99$ | $1.999$ | $2$ | $2.001$ | $2.01$ | $2.1$ |
|---|---|---|---|---|---|---|---|
| Branch | $x+1$ | $x+1$ | $x+1$ | $x^2-1$ | $x^2-1$ | $x^2-1$ | $x^2-1$ |
| $f(x)$ | $2.9$ | $2.99$ | $2.999$ | $3$ | $3.004001$ | $3.0401$ | $3.41$ |

The values on both sides approach $3$, which is the value at $x=2$ ✓.

**A value of $a$ that fails.** For $a=0$ the left branch is the constant $1$:

| $x$ | $1.9$ | $1.99$ | $1.999$ | $2$ |
|---|---|---|---|---|
| $f(x)$ | $1$ | $1$ | $1$ | $3$ |

The left-hand limit is $1\neq3$, so the function is not continuous at $x=2$ ✓.

**Substitution of the answer.**

$$
2a+1=2\cdot1+1=3=f(2)\ \checkmark
$$
