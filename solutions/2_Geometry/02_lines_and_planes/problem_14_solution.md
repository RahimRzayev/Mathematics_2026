# Problem 14. Contrast: Intersection and Parallelism

## Exercise

### Exercise 14. Contrast: Intersection and Parallelism
From the point $P=(0,0,1)$, two lines are drawn with direction vectors

$$
v_1=(2,1,-1),\qquad v_2=(2,1,0).
$$

For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

> **Why this exercise:** compares two very similar data sets that lead to different outcomes and forces recognition of the geometric condition before calculation.

---

## Answer

- The line with direction $v_1$ **intersects** the plane at the point $(2,1,0)$, for $t=1$.
- The line with direction $v_2$ is **parallel** to the plane and has no common point with it. Every point of this line has $z=1$.

Parallelism is recognized from the third component of $v_2$: it is $0$, so $v_2\cdot n=0$, and the starting point $P$ is not in the plane.

---

## Steps

### Step 1. Normal vector of the plane

The plane $z=0$ is $0\cdot x+0\cdot y+1\cdot z=0$, so

$$
n=(0,0,1)
$$

For any vector $v$, the dot product $v\cdot n$ is the third component of $v$.

### Step 2. Test both directions before calculating

$$
v_1\cdot n=-1\neq0,\qquad v_2\cdot n=0
$$

The first line crosses the plane at one point. The second line runs along the plane: it is either parallel to it or contained in it.

### Step 3. First line: intersection point

$$
X(t)=P+tv_1=(2t,\ t,\ 1-t)
$$

The condition $z=0$ gives

$$
1-t=0\quad\Longrightarrow\quad t=1
$$

$$
X(1)=(2,1,0)
$$

### Step 4. Second line: parallel or contained

The starting point $P=(0,0,1)$ has $z=1\neq0$, so it does not lie in the plane. A line that runs along the plane and has a point outside it has no point in it. The second line is parallel to the plane.

---

## Why it works

**The two data sets differ in one number.** The vectors $v_1$ and $v_2$ share their first two components. Only the third component differs, and it is the only component that matters for the plane $z=0$, because it is the component along the normal.

**Recognizing parallelism without an equation.** The third component of a direction vector is the rate at which the height $z$ changes along the line.

- For $v_1$ the rate is $-1$. The height decreases from $1$ and reaches $0$ after one step.
- For $v_2$ the rate is $0$. The height never changes.

The second line starts at height $1$ and stays there, so it can never reach height $0$. No equation needs to be solved.

**What the equation would show.** Substituting the second line $(2s,\ s,\ 1)$ into $z=0$ gives

$$
1=0
$$

The parameter does not appear and the statement is false, so there is no solution. This agrees with the geometric conclusion.

**The first two components.** The components $(2,1)$ decide where the first line lands in the plane, but not whether it lands. The second line moves in the same horizontal direction, directly above the path of the first, at constant height.

---

## Check

The intersection point satisfies both descriptions:

$$
P+1\cdot v_1=(0,0,1)+(2,1,-1)=(2,1,0),\qquad z=0\ \checkmark
$$

The first line changes sides of the plane at this point. For $t=0$ the height is $1$ and for $t=2$ the height is $-1$ ✓.

The second line stays at distance $1$ from the plane. Each of its points $(2s,\ s,\ 1)$ gives

$$
d=\frac{|1|}{\Vert n\Vert}=1\ \checkmark
$$

A constant nonzero distance confirms a parallel line with no common point.

The second line is parallel to the shadow of the first line in the plane. The projection of the first line onto $z=0$ is $(2t,\ t,\ 0)$, with direction $(2,1,0)=v_2$ ✓.
