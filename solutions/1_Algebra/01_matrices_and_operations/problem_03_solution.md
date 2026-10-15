# Problem 3. When Can Matrices Be Multiplied?

## Result

Sizes: $A$ is $2\times 3$, $B$ is $3\times 4$, $C$ is $4\times 2$, $D$ is $2\times 2$.

| Product | Defined? | Size of result |
|---|---|---|
| $AB$ | Yes | $2\times 4$ |
| $BA$ | No | — |
| $BC$ | Yes | $3\times 2$ |
| $CB$ | No | — |
| $AC$ | No | — |
| $CA$ | Yes | $4\times 3$ |
| $AD$ | No | — |
| $DA$ | Yes | $2\times 3$ |

## Main Steps

**The rule.** For a product $XY$ to exist, the number of **columns of $X$** must equal the number of **rows of $Y$**. If the sizes are $m\times n$ and $p\times q$, the product exists only when $n=p$, and then the result has size $m\times q$.

Write the sizes side by side and compare the inner numbers.

- $AB$: $A$ is $2\times 3$, $B$ is $3\times 4$. Inner numbers: $3$ and $3$. Equal, so $AB$ exists and has size $2\times 4$.
- $BA$: $B$ is $3\times 4$, $A$ is $2\times 3$. Inner numbers: $4$ and $2$. Not equal, so $BA$ is not defined.
- $BC$: $B$ is $3\times 4$, $C$ is $4\times 2$. Inner numbers: $4$ and $4$. Equal, so $BC$ exists and has size $3\times 2$.
- $CB$: $C$ is $4\times 2$, $B$ is $3\times 4$. Inner numbers: $2$ and $3$. Not equal, so $CB$ is not defined.
- $AC$: $A$ is $2\times 3$, $C$ is $4\times 2$. Inner numbers: $3$ and $4$. Not equal, so $AC$ is not defined.
- $CA$: $C$ is $4\times 2$, $A$ is $2\times 3$. Inner numbers: $2$ and $2$. Equal, so $CA$ exists and has size $4\times 3$.
- $AD$: $A$ is $2\times 3$, $D$ is $2\times 2$. Inner numbers: $3$ and $2$. Not equal, so $AD$ is not defined.
- $DA$: $D$ is $2\times 2$, $A$ is $2\times 3$. Inner numbers: $2$ and $2$. Equal, so $DA$ exists and has size $2\times 3$.

## Explanation

The product $XY$ is built from **rows of $X$** and **columns of $Y$**. Each entry of the result is a row times a column, which needs both to have the same length. That length is the inner number. The outer numbers tell you the size of the answer.

A helpful picture: the shapes must "fit together" in the middle, and the outside sizes remain as the result.

Notice that a product can exist in one order and not in the other. For example, $AB$ exists but $BA$ does not. So matrix multiplication is not only non-commutative; it may not even be possible to reverse the order.

## Verification

Use the rule "outer sizes give the answer" on the defined products. For $AB$, the outer sizes are $2$ and $4$, giving $2\times 4$. For $DA$, the outer sizes are $2$ and $3$, giving $2\times 3$. These match the table.
