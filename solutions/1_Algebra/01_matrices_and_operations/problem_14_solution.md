# Problem 14. Rotation Matrices

## Result

$$
R(\alpha)R(\beta)=R(\alpha+\beta)
$$

Rotating by $\beta$ and then by $\alpha$ is the same as rotating once by $\alpha+\beta$.

## Main Steps

**Multiply the matrices.** Rows of $R(\alpha)$ are $(\cos\alpha,\,-\sin\alpha)$ and $(\sin\alpha,\,\cos\alpha)$. Columns of $R(\beta)$ are $(\cos\beta,\,\sin\beta)^T$ and $(-\sin\beta,\,\cos\beta)^T$.

- Entry $(1,1)$: $\cos\alpha\cos\beta+(-\sin\alpha)\sin\beta=\cos\alpha\cos\beta-\sin\alpha\sin\beta$.
- Entry $(1,2)$: $\cos\alpha(-\sin\beta)+(-\sin\alpha)\cos\beta=-\cos\alpha\sin\beta-\sin\alpha\cos\beta$.
- Entry $(2,1)$: $\sin\alpha\cos\beta+\cos\alpha\sin\beta$.
- Entry $(2,2)$: $\sin\alpha(-\sin\beta)+\cos\alpha\cos\beta=\cos\alpha\cos\beta-\sin\alpha\sin\beta$.

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta & -(\cos\alpha\sin\beta+\sin\alpha\cos\beta) \\
\sin\alpha\cos\beta+\cos\alpha\sin\beta & \cos\alpha\cos\beta-\sin\alpha\sin\beta \\
\end{pmatrix}
$$

**Use the angle-sum formulas.** Recall

$$
\cos(\alpha+\beta)=\cos\alpha\cos\beta-\sin\alpha\sin\beta,\qquad
\sin(\alpha+\beta)=\sin\alpha\cos\beta+\cos\alpha\sin\beta
$$

Substitute these into the matrix:

- Entry $(1,1)$ is $\cos(\alpha+\beta)$.
- Entry $(1,2)$ is $-\sin(\alpha+\beta)$.
- Entry $(2,1)$ is $\sin(\alpha+\beta)$.
- Entry $(2,2)$ is $\cos(\alpha+\beta)$.

So

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\
\sin(\alpha+\beta) & \cos(\alpha+\beta) \\
\end{pmatrix}
=R(\alpha+\beta)
$$

## Explanation

Geometrically, $R(\theta)$ turns every point in the plane around the origin by the angle $\theta$, counterclockwise.

Multiplying matrices means applying one transformation after another. So $R(\alpha)R(\beta)$ first turns by $\beta$ and then by $\alpha$. The total turn is $\alpha+\beta$, which is exactly what $R(\alpha+\beta)$ does. The matrix algebra and the geometry agree.

A consequence: rotations commute. $R(\alpha)R(\beta)=R(\beta)R(\alpha)$, because $\alpha+\beta=\beta+\alpha$. This is special to rotations; the general matrices from Problem 4 do not commute.

## Verification

Take $\alpha=\beta=90^\circ$. Then $R(90^\circ)$ has rows $(0,\,-1)$ and $(1,\,0)$. Squaring it gives rows $(-1,\,0)$ and $(0,\,-1)$, which is $R(180^\circ)$, since $\cos180^\circ=-1$ and $\sin180^\circ=0$. The result is consistent.
