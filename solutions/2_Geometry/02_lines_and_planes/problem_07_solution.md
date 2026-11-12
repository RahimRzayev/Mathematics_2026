# Problem 7. A Line Relative to a Plane

## Exercise

### Exercise 7. A Line Relative to a Plane
For

$$
L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,
$$

determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

> **Why this exercise:** builds a universal test for the relative position of a line and a plane.

---

## Answer

The line **lies in the plane**.

- $v\cdot n=0$, so the line does not cross the plane at a single point.
- The point $(1,1,0)$ of the line satisfies the plane equation, so the line is not merely parallel to the plane: it is contained in it.

---

## Steps

### Step 1. Direction vector and normal vector

$$
v=(1,-1,0),\qquad n=(1,1,1)
$$

### Step 2. Dot product

$$
v\cdot n=1\cdot1+(-1)\cdot1+0\cdot1=0
$$

The direction of the line is perpendicular to the normal, so the line runs along the plane. Two cases remain: parallel with no common point, or contained in the plane.

### Step 3. Test one point of the line

The point $P_0=(1,1,0)$ corresponds to $t=0$:

$$
1+1+0=2\ \checkmark
$$

The point lies in the plane.

### Step 4. Conclusion

The line has one point in the plane and its direction runs along the plane. Every point of the line therefore lies in the plane.

---

## Why it works

**The role of $v\cdot n$.** Substituting the line $P_0+tv$ into the plane equation $n\cdot X=d$ gives one equation for $t$:

$$
n\cdot P_0+t\ (v\cdot n)=d
$$

The dot product $v\cdot n$ is the coefficient of $t$. It measures how fast the line moves across the plane.

- If $v\cdot n\neq0$, the equation has exactly one solution. The line crosses the plane at one point.
- If $v\cdot n=0$, the parameter $t$ disappears. Moving along the line does not change the value of $n\cdot X$, so the line stays at a constant level relative to the plane.

**The second test.** When $v\cdot n=0$, the equation reduces to $n\cdot P_0=d$, a statement without $t$. It is either true for every $t$ or false for every $t$:

- true: the line lies in the plane,
- false: the line is parallel to the plane and has no common point with it.

Here $n\cdot P_0=2=d$, so the statement is true.

Geometrically, $v\cdot n=0$ means that the direction of the line has no component along the normal. The line never moves toward the plane or away from it.

---

## Check

Substituting the whole line into the plane equation gives an identity:

$$
(1+t)+(1-t)+0=2\ \checkmark
$$

The parameter cancels and the equation holds for every $t$.

A second point of the line confirms the result. For $t=1$ the point is $(2,0,0)$, and

$$
2+0+0=2\ \checkmark
$$

Two different points of the line lie in the plane, so the whole line does.
