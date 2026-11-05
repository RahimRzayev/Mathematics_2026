# Problem 1. Vector Operations and Their Meaning

## Exercise

### Exercise 1. Vector Operations and Their Meaning
For $u=(2,-1,3)$ and $v=(-1,4,2)$ compute

$$
u+v,\qquad u-v,\qquad 3u-2v.
$$

Then verify that $(u+v)-v=u$, and explain geometrically what adding two vectors means.

> **Why this exercise:** reinforces basic operations and immediately connects them with their geometric meaning.

---

## Answer

$$
u+v=(1,3,5),\qquad u-v=(3,-5,1),\qquad 3u-2v=(8,-11,5)
$$

The identity $(u+v)-v=u$ holds: $(1,3,5)-(-1,4,2)=(2,-1,3)$.

Adding two vectors means performing one displacement after the other. The sum is the total displacement from the start of the first vector to the end of the second.

---

## Steps

### Step 1. Mechanism

Vector operations are performed coordinate by coordinate:

$$
(a_1,a_2,a_3)+(b_1,b_2,b_3)=(a_1+b_1,\ a_2+b_2,\ a_3+b_3),\qquad c\ (a_1,a_2,a_3)=(ca_1,\ ca_2,\ ca_3)
$$

### Step 2. Sum

$$
u+v=(2+(-1),\ -1+4,\ 3+2)=(1,3,5)
$$

### Step 3. Difference

$$
u-v=(2-(-1),\ -1-4,\ 3-2)=(3,-5,1)
$$

### Step 4. Linear combination

The two scalar multiples are

$$
3u=(6,-3,9),\qquad 2v=(-2,8,4)
$$

Subtracting coordinate by coordinate gives

$$
3u-2v=(6-(-2),\ -3-8,\ 9-4)=(8,-11,5)
$$

### Step 5. The requested identity

$$
(u+v)-v=(1-(-1),\ 3-4,\ 5-2)=(2,-1,3)=u
$$

---

## Why it works

**Head-to-tail rule.** Place the tail of $v$ at the head of $u$. The vector from the tail of $u$ to the head of $v$ is $u+v$.

**Parallelogram rule.** Place $u$ and $v$ at a common point and complete the parallelogram. The diagonal starting at that point is $u+v$. Both orders of addition trace two sides of the same parallelogram, which explains $u+v=v+u$.

**Coordinates.** Each coordinate of a vector records the displacement along one axis. Displacements along the same axis add as numbers, so geometric addition is the same as coordinatewise addition.

**The identity.** Subtracting $v$ is the displacement $v$ taken in the opposite direction. Moving along $v$ and then back along $v$ returns to the head of $u$, so $(u+v)-v=u$.

---

## Check

Commutativity of addition gives an independent computation of the sum:

$$
v+u=(-1+2,\ 4-1,\ 2+3)=(1,3,5)=u+v\ \checkmark
$$

The combination $3u-2v$ can be rebuilt from the sum and difference, since $3u-2v=\frac12(u+v)+\frac52(u-v)$:

$$
\frac12(1,3,5)+\frac52(3,-5,1)=\left(\frac{1+15}{2},\ \frac{3-25}{2},\ \frac{5+5}{2}\right)=(8,-11,5)\ \checkmark
$$
