# Problem 6. Projection and Perpendicular Component

## Exercise

### Exercise 6. Projection and Perpendicular Component
Find the projection of $u=(4,2)$ onto the direction $v=(1,1)$. Then compute

$$
r=u-\mathrm{proj}_v\,u
$$

and verify that $r\cdot v=0$. Explain this result geometrically.

> **Why this exercise:** shows projection as a decomposition into parallel and perpendicular components.

---

## Answer

$$
\mathrm{proj}_v\,u=(3,3),\qquad r=(1,-1),\qquad r\cdot v=0
$$

The vector $u$ splits into a part $(3,3)$ along the line of $v$ and a part $r=(1,-1)$ perpendicular to that line.

---

## Steps

### Step 1. Projection formula

$$
\mathrm{proj}_v\,u=\frac{u\cdot v}{v\cdot v}\,v
$$

### Step 2. The two dot products

$$
u\cdot v=4\cdot1+2\cdot1=6,\qquad v\cdot v=1\cdot1+1\cdot1=2
$$

### Step 3. Projection

$$
\mathrm{proj}_v\,u=\frac62\,(1,1)=3\,(1,1)=(3,3)
$$

### Step 4. Remainder

$$
r=u-\mathrm{proj}_v\,u=(4,2)-(3,3)=(1,-1)
$$

### Step 5. Perpendicularity

$$
r\cdot v=(1,-1)\cdot(1,1)=1-1=0
$$

---

## Why it works

The projection is the multiple $cv$ for which the remainder $u-cv$ is perpendicular to $v$. This condition determines $c$:

$$
(u-cv)\cdot v=0\quad\Longrightarrow\quad u\cdot v-c\,(v\cdot v)=0\quad\Longrightarrow\quad c=\frac{u\cdot v}{v\cdot v}
$$

The equation $r\cdot v=0$ is therefore built into the projection formula.

Geometrically, a perpendicular dropped from the head of $u$ onto the line of $v$ forms a right triangle:

- the hypotenuse is $u$,
- the leg along the line is $\mathrm{proj}_v\,u$,
- the leg perpendicular to the line is $r$.

The result $r\cdot v=0$ states that nothing in $r$ points along $v$: all of the component of $u$ in the direction of $v$ has been removed.

---

## Check

The two parts rebuild the original vector:

$$
\mathrm{proj}_v\,u+r=(3,3)+(1,-1)=(4,2)=u\ \checkmark
$$

The right triangle satisfies the Pythagorean theorem:

$$
\|\mathrm{proj}_v\,u\|^2+\|r\|^2=18+2=20=\|u\|^2\ \checkmark
$$
