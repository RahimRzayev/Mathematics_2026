# Problem 7. Classifying a Second-Degree Equation

## Exercise

### Exercise 7. Classifying a Second-Degree Equation
Determine the type of object described by:

1. $4x^2+9y^2=36$,
2. $x^2-y^2=1$,
3. $x^2-4y=0$,
4. $x^2+y^2+1=0$.

In the last case, explain why there are no real points.

> **Why this exercise:** develops quick recognition of the curve type and checking whether real solutions exist.

---

## Answer

| Equation | Object | Canonical form |
|---|---|---|
| $4x^2+9y^2=36$ | ellipse | $\frac{x^2}{9}+\frac{y^2}{4}=1$ |
| $x^2-y^2=1$ | hyperbola | $\frac{x^2}{1}-\frac{y^2}{1}=1$ |
| $x^2-4y=0$ | parabola | $x^2=4y$ |
| $x^2+y^2+1=0$ | empty set | $x^2+y^2=-1$ |

The last equation has no real points because $x^2+y^2\ge0$ for all real $x$ and $y$, so the left side is at least $1$ and can never equal $0$.

---

## Steps

### Step 1. Equation $4x^2+9y^2=36$

Both squares have positive coefficients and the right side is positive. Dividing by $36$:

$$
\frac{x^2}{9}+\frac{y^2}{4}=1
$$

This is an ellipse with center $(0,0)$ and semiaxes $3$ along $x$ and $2$ along $y$. The coefficients $4$ and $9$ are different, so it is not a circle.

### Step 2. Equation $x^2-y^2=1$

The squares have opposite signs and the right side is nonzero. This is a hyperbola with $a=b=1$.

- Vertices: $y=0$ gives $x=\pm1$, so $(\pm1,0)$.
- Asymptotes: $x^2-y^2=0$ gives $y=\pm x$.
- The branches open to the left and to the right, because $x^2=1+y^2\ge1$.

### Step 3. Equation $x^2-4y=0$

Only $x$ is squared, and $y$ appears to the first power:

$$
x^2=4y\quad\Longleftrightarrow\quad y=\frac{x^2}{4}
$$

This is a parabola with vertex $(0,0)$ and axis of symmetry $x=0$. It opens upward, because $4y=x^2\ge0$.

### Step 4. Equation $x^2+y^2+1=0$

Both squares have positive coefficients, as for a circle, but moving the constant to the right gives

$$
x^2+y^2=-1
$$

The right side would have to be the square of a radius, and it is negative. No real point satisfies the equation. The set of solutions is empty.

---

## Why it works

**A quick test from the squared terms.** For an equation $Ax^2+Cy^2+\ldots=0$ without an $xy$ term, the product $AC$ gives the candidate type:

| Product $AC$ | Squares | Candidate type |
|---|---|---|
| positive | same sign | ellipse or circle |
| negative | opposite signs | hyperbola |
| zero | one square missing | parabola |

The four equations give $AC=36$, $AC=-1$, $AC=0$, and $AC=1$.

**The test gives only a candidate.** The squared terms determine what the curve would be if it existed. The constant term decides whether it exists. Equations 1 and 4 both have two positive squares, but only the first has real points.

**Why equation 4 has no real points.** For real numbers every square is nonnegative:

$$
x^2\ge0,\qquad y^2\ge0\quad\Longrightarrow\quad x^2+y^2+1\ge1\gt0
$$

The left side is never smaller than $1$, so it cannot be $0$. The equation $x^2+y^2=r^2$ describes a circle only when $r^2\gt0$. For $r^2=0$ it describes one point, and for $r^2\lt0$ it describes nothing.

**Why existence is not a problem for the other types.** A hyperbola and a parabola always have real points when the equation has this form. In $x^2-y^2=1$ one square can compensate the other, and in $x^2=4y$ the first-power variable can take any nonnegative value.

---

## Check

One point of each real curve is substituted into the original equation.

$$
(3,0):\ 4\cdot9+9\cdot0=36\ \checkmark,\qquad (0,2):\ 4\cdot0+9\cdot4=36\ \checkmark
$$

$$
(1,0):\ 1-0=1\ \checkmark,\qquad \left(\sqrt2,1\right):\ 2-1=1\ \checkmark
$$

$$
(2,1):\ 4-4\cdot1=0\ \checkmark,\qquad (-4,4):\ 16-4\cdot4=0\ \checkmark
$$

For equation 4, the smallest value of the left side is reached at the origin and is still positive:

$$
(0,0):\ 0+0+1=1\neq0\ \checkmark
$$
