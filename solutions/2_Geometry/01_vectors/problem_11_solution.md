# Problem 11. Decomposition into Parallel and Perpendicular Components

## Exercise

### Exercise 11. Decomposition into Parallel and Perpendicular Components
Decompose $u=(3,4)$ into components parallel and perpendicular to $v=(1,2)$. Check

$$
u=u_{\parallel}+u_{\perp},\qquad u_{\perp}\cdot v=0.
$$

Explain why these are two independent checks of correctness.

> **Why this exercise:** deepens the idea of projection through construction and verification.

---

## Answer

$$
u_{\parallel}=\left(\frac{11}{5},\frac{22}{5}\right),\qquad u_{\perp}=\left(\frac45,-\frac25\right)
$$

Both checks hold. They are independent because each one can pass while the other fails: the first tests whether the parts add up to $u$, and the second tests whether the remainder has the correct direction.

---

## Steps

### Step 1. Parallel component

The parallel component is the projection of $u$ onto $v$:

$$
u_{\parallel}=\mathrm{proj}_v\,u=\frac{u\cdot v}{v\cdot v}\,v
$$

The two dot products are

$$
u\cdot v=3\cdot1+4\cdot2=11,\qquad v\cdot v=1^2+2^2=5
$$

Therefore

$$
u_{\parallel}=\frac{11}{5}(1,2)=\left(\frac{11}{5},\frac{22}{5}\right)
$$

### Step 2. Perpendicular component

$$
u_{\perp}=u-u_{\parallel}=\left(\frac{15}{5}-\frac{11}{5},\ \frac{20}{5}-\frac{22}{5}\right)=\left(\frac45,-\frac25\right)
$$

### Step 3. First check: the sum

$$
u_{\parallel}+u_{\perp}=\left(\frac{11+4}{5},\ \frac{22-2}{5}\right)=\left(\frac{15}{5},\frac{20}{5}\right)=(3,4)=u
$$

### Step 4. Second check: perpendicularity

$$
u_{\perp}\cdot v=\frac45\cdot1+\left(-\frac25\right)\cdot2=\frac45-\frac45=0
$$

---

## Why it works

A correct decomposition must satisfy three conditions:

1. the parts add up to $u$,
2. $u_{\parallel}$ is a multiple of $v$,
3. $u_{\perp}$ is perpendicular to $v$.

These conditions determine the decomposition uniquely. The two requested checks test different conditions, and a wrong answer can pass either one alone.

**The sum passes, perpendicularity fails.** Take the incorrect multiple $u_{\parallel}=2v=(2,4)$, which gives $u_{\perp}=(1,0)$. Then

$$
(2,4)+(1,0)=(3,4)=u,\qquad (1,0)\cdot(1,2)=1\neq0
$$

The sum cannot detect this error, because any vector plus "$u$ minus that vector" equals $u$.

**Perpendicularity passes, the sum fails.** Take the correct $u_{\parallel}$ with the incorrect remainder $u_{\perp}=(2,-1)$. Then

$$
(2,-1)\cdot(1,2)=0,\qquad \left(\frac{11}{5},\frac{22}{5}\right)+(2,-1)=\left(\frac{21}{5},\frac{17}{5}\right)\neq u
$$

The direction is correct but the length is wrong, and the dot product cannot detect this error.

---

## Check

The components are the legs of a right triangle with hypotenuse $u$, so the Pythagorean theorem gives a third check:

$$
\|u_{\parallel}\|^2+\|u_{\perp}\|^2=\frac{121+484}{25}+\frac{16+4}{25}=\frac{625}{25}=25=\|u\|^2\ \checkmark
$$

The component $u_{\parallel}$ is a multiple of $v$, since its coordinates have the same ratio as those of $v$:

$$
\frac{22/5}{11/5}=2=\frac21\ \checkmark
$$
