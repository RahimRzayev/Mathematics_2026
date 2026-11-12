# Problem 1. Line Through Two Points

## Exercise

### Exercise 1. Line Through Two Points
Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

> **Why this exercise:** teaches how to move between equivalent descriptions of a line and connect them with the appropriate vectors.

---

## Answer

- Direction vector: $v=\overrightarrow{AB}=(3,-3)$, or the shorter parallel vector $(1,-1)$.
- Parametric form: $(x,y)=(1,2)+t(3,-3)$.
- Normal vector: $n=(1,1)$.
- General form: $x+y-3=0$.

Both points satisfy the general equation: $1+2-3=0$ and $4+(-1)-3=0$.

---

## Steps

### Step 1. Direction vector

The line passes through $A$ and $B$, so the vector joining them points along the line:

$$
v=\overrightarrow{AB}=B-A=(4-1,\ -1-2)=(3,-3)
$$

### Step 2. Parametric form

A point of the line is the starting point $A$ plus a multiple of the direction vector:

$$
(x,y)=(1,2)+t(3,-3),\qquad t\in\mathbb{R}
$$

In coordinates:

$$
\begin{cases}
x=1+3t, \\
y=2-3t.
\end{cases}
$$

### Step 3. Normal vector

A normal vector is perpendicular to the direction vector. For $v=(3,-3)$ the vector $n=(1,1)$ works, because

$$
n\cdot v=1\cdot3+1\cdot(-3)=0
$$

### Step 4. General form

A point $X=(x,y)$ lies on the line exactly when $\overrightarrow{AX}$ is perpendicular to $n$:

$$
n\cdot(X-A)=0\quad\Longrightarrow\quad 1\cdot(x-1)+1\cdot(y-2)=0\quad\Longrightarrow\quad x+y-3=0
$$

### Step 5. Substituting both points

$$
A:\ 1+2-3=0\ \checkmark,\qquad B:\ 4+(-1)-3=0\ \checkmark
$$

---

## Why it works

The two forms describe the same set of points in two different ways.

**Parametric form generates the points.** Each value of $t$ produces one point: the line is traced by starting at $A$ and moving along $v$. The direction vector is visible as the coefficient of $t$.

**General form tests the points.** The equation $x+y-3=0$ does not produce points. It decides whether a given point belongs to the line. The normal vector is visible as the coefficients of $x$ and $y$.

**The two vectors are linked by perpendicularity.** In the plane, a direction $(a,b)$ always has the normal $(-b,a)$ or any multiple of it. For $(3,-3)$ this gives $(3,3)$, which is parallel to $(1,1)$.

Neither vector is unique. Any nonzero multiple of $v$ is a direction vector and any nonzero multiple of $n$ is a normal vector, because only the direction matters.

---

## Check

Eliminating the parameter gives the general form again. Adding the two coordinate equations removes $t$:

$$
x+y=(1+3t)+(2-3t)=3\ \checkmark
$$

The parametric form reaches both points:

$$
t=0:\ (1,2)=A\ \checkmark,\qquad t=1:\ (1+3,\ 2-3)=(4,-1)=B\ \checkmark
$$

The slope agrees in both forms. From the points, the slope is $\frac{-1-2}{4-1}=-1$. From $x+y-3=0$, the line is $y=-x+3$, which also has slope $-1$ ✓.
