# Problem 2. A Line in Space

## Exercise

### Exercise 2. A Line in Space
Given

$$
L:(x,y,z)=(2,-1,3)+t(1,2,-2).
$$

State a point on the line and its direction vector, check whether $P=(4,3,-1)$ lies on $L$, and find the point corresponding to $t=-1$.

> **Why this exercise:** reinforces the interpretation of parametric form as “point + direction.”

---

## Answer

- Point on the line: $P_0=(2,-1,3)$, obtained for $t=0$.
- Direction vector: $v=(1,2,-2)$.
- The point $P=(4,3,-1)$ lies on $L$. It corresponds to $t=2$.
- The point for $t=-1$ is $(1,-3,5)$.

---

## Steps

### Step 1. Read the point and the direction

The equation has the form $P_0+tv$. The constant part is a point of the line and the coefficient of $t$ is its direction:

$$
P_0=(2,-1,3),\qquad v=(1,2,-2)
$$

### Step 2. Coordinate equations

$$
\begin{cases}
x=2+t, \\
y=-1+2t, \\
z=3-2t.
\end{cases}
$$

### Step 3. Test the point $P$

The point $P=(4,3,-1)$ lies on $L$ only if one value of $t$ satisfies all three equations. Each equation is solved separately:

$$
\begin{aligned}
2+t=4 &\quad\Longrightarrow\quad t=2 \\
-1+2t=3 &\quad\Longrightarrow\quad t=2 \\
3-2t=-1 &\quad\Longrightarrow\quad t=2
\end{aligned}
$$

All three equations give the same value $t=2$, so $P$ lies on $L$.

### Step 4. The point for $t=-1$

$$
(2,-1,3)+(-1)\cdot(1,2,-2)=(2-1,\ -1-2,\ 3+2)=(1,-3,5)
$$

---

## Why it works

The parametric form reads as "point + direction": the line starts at $P_0$ and each unit of $t$ adds one copy of $v$. Positive values of $t$ move along $v$, negative values move against it.

**The membership test.** A single parameter controls all three coordinates at once. A point lies on the line only when the three coordinate equations agree on one value of $t$. If two equations gave different values, the point would lie off the line. Here all three agree.

**Equivalent form of the test.** The point $P$ lies on $L$ exactly when $P-P_0$ is a multiple of $v$:

$$
P-P_0=(4-2,\ 3+1,\ -1-3)=(2,4,-4)=2\ (1,2,-2)=2v
$$

The multiplier is the parameter value $t=2$.

---

## Check

The value $t=2$ rebuilds the point $P$:

$$
(2,-1,3)+2\ (1,2,-2)=(2+2,\ -1+4,\ 3-4)=(4,3,-1)=P\ \checkmark
$$

The point for $t=-1$ differs from $P_0$ by exactly $-v$:

$$
(1,-3,5)-(2,-1,3)=(-1,-2,2)=-v\ \checkmark
$$

The points for $t=-1$, $t=0$, and $t=2$ are $(1,-3,5)$, $(2,-1,3)$, and $(4,3,-1)$. The step from the first to the second is $v$ and the step from the second to the third is $2v$, as the parameter values require ✓.
