# Problem 9. Cross Product as a Perpendicular Direction

## Exercise

### Exercise 9. Cross Product as a Perpendicular Direction
For $u=(1,2,0)$ and $v=(0,1,3)$ compute $u\times v$. Use dot products to check perpendicularity to both vectors, compute $v\times u$, and compare the results.

> **Why this exercise:** teaches the geometric meaning of the cross product and the effect of changing the order of its arguments.

---

## Answer

$$
u\times v=(6,-3,1),\qquad v\times u=(-6,3,-1)=-(u\times v)
$$

The vector $u\times v$ is perpendicular to both $u$ and $v$. Reversing the order keeps the line and the length, and reverses the orientation.

---

## Steps

### Step 1. Coordinate formula

For $u=(u_1,u_2,u_3)$ and $v=(v_1,v_2,v_3)$,

$$
u\times v=(u_2v_3-u_3v_2,\ u_3v_1-u_1v_3,\ u_1v_2-u_2v_1)
$$

### Step 2. Compute $u\times v$

$$
\begin{aligned}
u_2v_3-u_3v_2 &= 2\cdot3-0\cdot1=6 \\
u_3v_1-u_1v_3 &= 0\cdot0-1\cdot3=-3 \\
u_1v_2-u_2v_1 &= 1\cdot1-2\cdot0=1
\end{aligned}
$$

Therefore $u\times v=(6,-3,1)$.

### Step 3. Check perpendicularity

$$
(u\times v)\cdot u=6\cdot1+(-3)\cdot2+1\cdot0=6-6+0=0
$$

$$
(u\times v)\cdot v=6\cdot0+(-3)\cdot1+1\cdot3=0-3+3=0
$$

### Step 4. Compute $v\times u$

$$
\begin{aligned}
v_2u_3-v_3u_2 &= 1\cdot0-3\cdot2=-6 \\
v_3u_1-v_1u_3 &= 3\cdot1-0\cdot0=3 \\
v_1u_2-v_2u_1 &= 0\cdot2-1\cdot1=-1
\end{aligned}
$$

Therefore $v\times u=(-6,3,-1)$.

### Step 5. Compare

Each coordinate of $v\times u$ is the negative of the corresponding coordinate of $u\times v$, so

$$
v\times u=-(u\times v)
$$

---

## Why it works

**Perpendicularity.** Expanding the dot product with the coordinate formula makes all terms cancel in pairs:

$$
(u\times v)\cdot u=(u_2v_3-u_3v_2)u_1+(u_3v_1-u_1v_3)u_2+(u_1v_2-u_2v_1)u_3=0
$$

The same cancellation occurs for $v$.

**Order of the arguments.** Exchanging $u$ and $v$ swaps the two products in every coordinate of the formula, which changes the sign of every coordinate.

**Geometric meaning.** Since $u$ and $v$ are not parallel, they span a plane, and only one line through the origin is perpendicular to that plane. Both $u\times v$ and $v\times u$ lie on this line and have equal length. They point to opposite sides of the plane, as described by the right-hand rule.

---

## Check

The length of $u\times v$ must agree with the identity $\Vert u\times v\Vert^2=\Vert u\Vert^2\Vert v\Vert^2-(u\cdot v)^2$. The left-hand side is

$$
\Vert u\times v\Vert^2=36+9+1=46
$$

With $\Vert u\Vert^2=5$, $\Vert v\Vert^2=10$, and $u\cdot v=2$, the right-hand side is

$$
5\cdot10-2^2=50-4=46\ \checkmark
$$

The reversed product is also perpendicular to both vectors, since it is a multiple of $u\times v$:

$$
(v\times u)\cdot u=-6+6+0=0\ \checkmark,\qquad (v\times u)\cdot v=0+3-3=0\ \checkmark
$$
