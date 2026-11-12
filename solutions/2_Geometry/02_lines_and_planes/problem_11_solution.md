# Problem 11. Plane Containing a Line and a Point

## Exercise

### Exercise 11. Plane Containing a Line and a Point
Find the equation of the plane containing

$$
(x,y,z)=(1,0,2)+t(1,1,-1)
$$

and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

> **Why this exercise:** requires independently constructing two linearly independent directions in the plane.

---

## Answer

$$
x+2y+3z=7
$$

The normal vector is $n=(1,2,3)$. The point $P$ satisfies the equation, and substituting the line gives $7=7$ for every $t$.

---

## Steps

### Step 1. First direction: the direction of the line

The plane contains the line, so it contains its direction vector and its point:

$$
v=(1,1,-1),\qquad A=(1,0,2)
$$

### Step 2. Second direction: from the line to the point

Both $A$ and $P$ lie in the plane, so the vector joining them lies in it:

$$
w=\overrightarrow{AP}=P-A=(0-1,\ 2-0,\ 1-2)=(-1,2,-1)
$$

### Step 3. The two directions are independent

If $w=kv$, the first components would give $k=-1$ and the second components would give $k=2$. The vectors are not parallel. Equivalently, $P$ does not lie on the line, so the plane is uniquely determined.

### Step 4. Normal vector

$$
\begin{aligned}
n=v\times w &= (1\cdot(-1)-(-1)\cdot2,\ (-1)\cdot(-1)-1\cdot(-1),\ 1\cdot2-1\cdot(-1)) \\
&= (-1+2,\ 1+1,\ 2+1) \\
&= (1,2,3)
\end{aligned}
$$

### Step 5. Plane equation

The plane passes through $A$ with normal $n$:

$$
1\cdot(x-1)+2\cdot y+3\cdot(z-2)=0\quad\Longrightarrow\quad x+2y+3z=7
$$

### Step 6. The point and the line lie in the plane

$$
P:\ 0+2\cdot2+3\cdot1=7\ \checkmark
$$

For a general point $(1+t,\ t,\ 2-t)$ of the line:

$$
(1+t)+2t+3(2-t)=1+t+2t+6-3t=7\ \checkmark
$$

The parameter cancels, so every point of the line satisfies the equation.

---

## Why it works

**The line supplies only one direction.** A plane needs two independent directions, and a line provides one. The second direction cannot be read from the data. It has to be constructed by joining a point of the line to the point $P$.

**Why independence is required.** If $P$ were on the line, $w$ would be parallel to $v$ and the cross product would be the zero vector. Infinitely many planes contain a given line, and a point on the line would not select one of them. A point off the line selects exactly one.

**Why the whole line lies in the plane.** Two conditions together place a line in a plane:

- one point of the line lies in the plane, here $A$,
- the direction of the line is perpendicular to the normal, here $n\cdot v=0$.

Checking the line therefore requires no infinite list of points. The cancellation of $t$ in Step 6 expresses the second condition: the coefficient of $t$ is $n\cdot v=1+2-3=0$.

---

## Check

The normal is perpendicular to both constructed directions:

$$
n\cdot v=1+2-3=0\ \checkmark,\qquad n\cdot w=-1+4-3=0\ \checkmark
$$

A different point of the line gives a parallel normal. For $t=1$ the point is $B=(2,1,1)$ and $\overrightarrow{BP}=(-2,1,0)$:

$$
v\times\overrightarrow{BP}=(1\cdot0-(-1)\cdot1,\ (-1)\cdot(-2)-1\cdot0,\ 1\cdot1-1\cdot(-2))=(1,2,3)\ \checkmark
$$

Three points of the plane that are not on one line satisfy the equation:

$$
A:\ 1+0+6=7\ \checkmark,\qquad B:\ 2+2+3=7\ \checkmark,\qquad P:\ 0+4+3=7\ \checkmark
$$
