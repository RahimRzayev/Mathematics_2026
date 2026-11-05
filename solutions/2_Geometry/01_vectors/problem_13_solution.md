# Problem 13. Do Four Points Lie in One Plane?

## Exercise

### Exercise 13. Do Four Points Lie in One Plane?
Given

$$
A=(0,0,0),\qquad B=(1,2,0),\qquad C=(0,1,1),\qquad D=(2,5,1).
$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $n=\overrightarrow{AB}\times\overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD}\cdot n=0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A,B,C$, and justify the criterion.

> **Why this exercise:** combines the known cross and dot products into a geometric criterion needed for planes, without introducing a separate concept used only once.

---

## Answer

$$
n=(2,-1,1),\qquad \overrightarrow{AD}=(2,5,1),\qquad \overrightarrow{AD}\cdot n=0
$$

The point $D$ lies in the plane determined by $A,B,C$, so the four points are coplanar.

---

## Steps

### Step 1. Vectors from $A$

$$
\overrightarrow{AB}=B-A=(1,2,0),\qquad \overrightarrow{AC}=C-A=(0,1,1)
$$

### Step 2. Normal vector

$$
n=\overrightarrow{AB}\times\overrightarrow{AC}=(2\cdot1-0\cdot1,\ 0\cdot0-1\cdot1,\ 1\cdot1-2\cdot0)=(2,-1,1)
$$

Since $n\neq0$, the points $A,B,C$ are not on one line and determine a unique plane.

### Step 3. Test the fourth point

$$
\overrightarrow{AD}=D-A=(2,5,1)
$$

$$
\overrightarrow{AD}\cdot n=2\cdot2+5\cdot(-1)+1\cdot1=4-5+1=0
$$

### Step 4. Conclusion

The dot product equals $0$, so $\overrightarrow{AD}$ is perpendicular to $n$ and $D$ lies in the plane through $A,B,C$.

---

## Why it works

The criterion states that, for $n\neq0$, the point $D$ lies in the plane through $A,B,C$ exactly when $\overrightarrow{AD}\cdot n=0$. It has two directions.

**If $D$ is in the plane, the dot product is $0$.** In this case $\overrightarrow{AD}$ lies in the plane, so it can be written as $s\overrightarrow{AB}+t\overrightarrow{AC}$. The vector $n$ is perpendicular to both $\overrightarrow{AB}$ and $\overrightarrow{AC}$, so

$$
\overrightarrow{AD}\cdot n=s\ (\overrightarrow{AB}\cdot n)+t\ (\overrightarrow{AC}\cdot n)=0
$$

**If the dot product is $0$, $D$ is in the plane.** All vectors perpendicular to $n$ form a plane through the origin in $\mathbb R^3$. The independent vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ already span this plane, so $\overrightarrow{AD}$ is a combination of them. Hence $D=A+s\overrightarrow{AB}+t\overrightarrow{AC}$ lies in the plane through $A,B,C$.

Geometrically, $\overrightarrow{AD}\cdot n$ measures how far $D$ is displaced from the plane along the normal direction. A value of $0$ means there is no displacement.

---

## Check

The dot-product test states that $\overrightarrow{AD}$ is a combination of $\overrightarrow{AB}$ and $\overrightarrow{AC}$. This combination can be found directly. The first coordinate requires $s=2$ and the third requires $t=1$:

$$
2\overrightarrow{AB}+\overrightarrow{AC}=2(1,2,0)+(0,1,1)=(2,5,1)=\overrightarrow{AD}\ \checkmark
$$

The vector $n$ is perpendicular to both sides:

$$
n\cdot\overrightarrow{AB}=2-2+0=0\ \checkmark,\qquad n\cdot\overrightarrow{AC}=0-1+1=0\ \checkmark
$$
