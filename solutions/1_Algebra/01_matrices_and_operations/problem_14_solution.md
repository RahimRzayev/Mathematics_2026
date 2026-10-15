# Problem 14. Rotation Matrices

## Exercise

### Exercise 14. Rotation Matrices
The matrix for a rotation through an angle $\theta$ is

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta \\
\end{pmatrix}.
$$

Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that

$$
R(\alpha)R(\beta)=R(\alpha+\beta).
$$

Explain the result geometrically.

> **Why this exercise:** shows the consistency between matrix algebra and the geometry of composing rotations.

---

## Answer

$$
R(\alpha)R(\beta)=R(\alpha+\beta)
$$

Rotating by $\beta$ and then by $\alpha$ is the same as one rotation by $\alpha+\beta$.

---

## Steps

### Step 1. Multiply the matrices

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta & -(\cos\alpha\sin\beta+\sin\alpha\cos\beta) \\
\sin\alpha\cos\beta+\cos\alpha\sin\beta & \cos\alpha\cos\beta-\sin\alpha\sin\beta \\
\end{pmatrix}
$$

| Entry | Computation |
|---|---|
| $(1,1)$ | $\cos\alpha\cos\beta+(-\sin\alpha)\sin\beta$ |
| $(1,2)$ | $\cos\alpha(-\sin\beta)+(-\sin\alpha)\cos\beta$ |
| $(2,1)$ | $\sin\alpha\cos\beta+\cos\alpha\sin\beta$ |
| $(2,2)$ | $\sin\alpha(-\sin\beta)+\cos\alpha\cos\beta$ |

### Step 2. Apply the angle-sum formulas

$$
\cos(\alpha+\beta)=\cos\alpha\cos\beta-\sin\alpha\sin\beta,\qquad
\sin(\alpha+\beta)=\sin\alpha\cos\beta+\cos\alpha\sin\beta
$$

Substitute into Step 1:

| Entry | Becomes |
|---|---|
| $(1,1)$ | $\cos(\alpha+\beta)$ |
| $(1,2)$ | $-\sin(\alpha+\beta)$ |
| $(2,1)$ | $\sin(\alpha+\beta)$ |
| $(2,2)$ | $\cos(\alpha+\beta)$ |

### Step 3. Conclude

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\
\sin(\alpha+\beta) & \cos(\alpha+\beta) \\
\end{pmatrix}
=R(\alpha+\beta)
$$

---

## Why it works

$R(\theta)$ turns every point of the plane around the origin by $\theta$, counterclockwise.

Multiplying matrices means applying one transformation after another. So $R(\alpha)R(\beta)$ turns by $\beta$, then by $\alpha$. The total turn is $\alpha+\beta$. The algebra and the geometry agree.

**Consequence:** rotations commute, because $\alpha+\beta=\beta+\alpha$. This is special to rotations. The general matrices from Problem 4 do not commute.

---

## Check

Take $\alpha=\beta=90^\circ$. Then

$$
R(90^\circ)=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
$$

and its square is

$$
\begin{pmatrix}
-1 & 0 \\
0 & -1 \\
\end{pmatrix}
$$

This is $R(180^\circ)$, since $\cos 180^\circ=-1$ and $\sin 180^\circ=0$. ✓
