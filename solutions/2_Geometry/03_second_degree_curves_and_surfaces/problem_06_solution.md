# Problem 6. Shifted Ellipse

## Exercise

### Exercise 6. Shifted Ellipse
Reduce

$$
4x^2+9y^2-16x+18y-11=0
$$

to canonical form. Give the center and semiaxis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

> **Why this exercise:** reinforces completing the square and recognizing a shift of the coordinate system.

---

## Answer

$$
\frac{(x-2)^2}{9}+\frac{(y+1)^2}{4}=1
$$

- Center: $(2,-1)$.
- Semiaxes: $3$ along the $x$-direction and $2$ along the $y$-direction.
- Substituting the center into the left-hand side gives $-36$. This is consistent with the form $4(x-2)^2+9(y+1)^2-36=0$, in which both squares vanish at the center and only the constant $-36$ remains.

---

## Steps

### Step 1. Group the terms and factor out the coefficients of the squares

$$
4(x^2-4x)+9(y^2+2y)=11
$$

### Step 2. Complete the squares inside the brackets

$$
x^2-4x=(x-2)^2-4,\qquad y^2+2y=(y+1)^2-1
$$

### Step 3. Substitute

The subtracted numbers are multiplied by the factors in front of the brackets:

$$
\begin{aligned}
4\left((x-2)^2-4\right)+9\left((y+1)^2-1\right) &= 11 \\
4(x-2)^2-16+9(y+1)^2-9 &= 11 \\
4(x-2)^2+9(y+1)^2 &= 36
\end{aligned}
$$

### Step 4. Divide by the right side

$$
\frac{4(x-2)^2}{36}+\frac{9(y+1)^2}{36}=1\quad\Longrightarrow\quad \frac{(x-2)^2}{9}+\frac{(y+1)^2}{4}=1
$$

### Step 5. Read the center and the semiaxes

Comparing with $\frac{(x-x_0)^2}{a^2}+\frac{(y-y_0)^2}{b^2}=1$:

$$
(x_0,y_0)=(2,-1),\qquad a=\sqrt9=3,\qquad b=\sqrt4=2
$$

### Step 6. Substitute the center into the left-hand side

$$
4\cdot2^2+9\cdot(-1)^2-16\cdot2+18\cdot(-1)-11=16+9-32-18-11=-36
$$

### Step 7. Compare with the form obtained

Step 3 shows that the left-hand side equals

$$
4(x-2)^2+9(y+1)^2-36
$$

At the center both squares are $0$, so the value must be $-36$. The direct substitution gives the same number, which confirms the center and the constant $36$.

---

## Why it works

**A shift of the coordinate system.** With the new coordinates $u=x-2$ and $v=y+1$ the equation becomes

$$
\frac{u^2}{9}+\frac{v^2}{4}=1
$$

This is an ellipse centered at the origin of the $(u,v)$ system. The origin $u=0$, $v=0$ corresponds to $x=2$, $y=-1$. The curve is the standard ellipse moved by $2$ to the right and by $1$ down. The shift changes the position only. The shape and the semiaxes stay the same.

**Why the coefficients are factored out first.** The identity $x^2+px=\left(x+\frac{p}{2}\right)^2-\frac{p^2}{4}$ requires the coefficient of $x^2$ to be $1$. Factoring out $4$ and $9$ prepares each bracket. The constants $-4$ and $-1$ then leave the brackets multiplied by $4$ and $9$, which gives $-16$ and $-9$.

**Meaning of the value at the center.** The left-hand side is a function of the point. It is $0$ on the ellipse, negative inside, and positive outside. The center is the point where both squares vanish, so the function takes its smallest value there, $-36$. The size of this value is the right side of the form $4(x-2)^2+9(y+1)^2=36$. A positive number on the right is the condition for the ellipse to exist.

---

## Check

Expanding the form from Step 3 returns the original equation:

$$
4(x^2-4x+4)+9(y^2+2y+1)-36=4x^2-16x+16+9y^2+18y+9-36=4x^2+9y^2-16x+18y-11\ \checkmark
$$

The four endpoints of the axes lie on the curve. They are obtained by moving from the center by $3$ horizontally or by $2$ vertically:

$$
(5,-1):\ 100+9-80-18-11=0\ \checkmark
$$

$$
(-1,-1):\ 4+9+16-18-11=0\ \checkmark
$$

$$
(2,1):\ 16+9-32+18-11=0\ \checkmark
$$

$$
(2,-3):\ 16+81-32-54-11=0\ \checkmark
$$

A point outside the ellipse gives a positive value. For $(6,-1)$:

$$
144+9-96-18-11=28\gt0\ \checkmark
$$
