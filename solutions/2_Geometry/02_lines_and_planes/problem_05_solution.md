# Problem 5. Relative Position of Two Lines

## Exercise

### Exercise 5. Relative Position of Two Lines
Analyze the position of

$$
L_1:(x,y,z)=(1,1,0)+t(1,2,1),
$$

$$
L_2:(x,y,z)=(2,0,1)+s(0,1,-1).
$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

> **Why this exercise:** teaches how to distinguish qualitatively different relationships between lines in space.

---

## Answer

The lines are **skew**.

- They are not parallel: the direction vectors $(1,2,1)$ and $(0,1,-1)$ are not multiples of each other.
- They do not intersect: the system for a common point has no solution.

---

## Steps

### Step 1. Compare the directions

$$
v_1=(1,2,1),\qquad v_2=(0,1,-1)
$$

If $v_1=kv_2$, the first components would give $1=k\cdot0$, which is impossible. The directions are not parallel, so the lines are either intersecting or skew.

### Step 2. Set up the system for a common point

A common point requires parameter values $t$ and $s$ for which all three coordinates agree:

$$
\begin{cases}
1+t=2, \\
1+2t=s, \\
t=1-s.
\end{cases}
$$

### Step 3. Solve two equations

The first equation gives $t=1$. The second equation then gives

$$
s=1+2\cdot1=3
$$

### Step 4. Test the third equation

$$
t=1,\qquad 1-s=1-3=-2,\qquad 1\neq-2
$$

The third equation fails. No pair $(t,s)$ satisfies all three equations, so the lines have no common point.

### Step 5. Classify

The lines are not parallel and do not intersect. They are skew.

---

## Why it works

Two lines in space fall into exactly one of four cases, decided by two questions.

| Directions parallel? | Common point? | Classification |
|---|---|---|
| yes | yes | the same line |
| yes | no | parallel |
| no | yes | intersecting at one point |
| no | no | skew |

**Why three equations matter.** The system has three equations and only two unknowns. In the plane there would be two equations, and non-parallel lines would always meet. In space the third coordinate adds a condition that the values of $t$ and $s$ found from the first two equations usually do not satisfy. Skew lines exist only because of this extra dimension.

**What the failed equation means.** For $t=1$ and $s=3$ the two lines pass through points with equal $x$ and $y$ coordinates but different heights:

$$
L_1:\ (2,3,1),\qquad L_2:\ (2,3,-2)
$$

One line passes above the other without touching it.

---

## Check

The classification can be confirmed without solving the system. Two non-parallel lines lie in one plane, and therefore intersect, exactly when the vector joining them is perpendicular to $v_1\times v_2$.

$$
v_1\times v_2=(2\cdot(-1)-1\cdot1,\ 1\cdot0-1\cdot(-1),\ 1\cdot1-2\cdot0)=(-3,1,1)
$$

The vector joining the given points of the two lines is

$$
w=(2,0,1)-(1,1,0)=(1,-1,1)
$$

$$
w\cdot(v_1\times v_2)=1\cdot(-3)+(-1)\cdot1+1\cdot1=-3\neq0\ \checkmark
$$

The value is nonzero, so the lines do not lie in one plane and are skew.

The same quantities give the distance between the lines:

$$
d=\frac{|w\cdot(v_1\times v_2)|}{\Vert v_1\times v_2\Vert}=\frac{3}{\sqrt{9+1+1}}=\frac{3}{\sqrt{11}}\approx0.90
$$

The distance is positive, which agrees with the absence of a common point ✓.
