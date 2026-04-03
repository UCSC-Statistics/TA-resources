Integration Techniques
================
Jibo Shen

In this section, we cover the two powerful techniques for solving
complex integrals: Substitution (for composite functions) and
Integration by Parts (for products).

## Integration by Substitution

This technique is the reverse of the Chain Rule. It allows you to
simplify an integral by changing variables.

**When to use:** Use this when you see a function $g(x)$ inside another
function, and the derivative $g'(x)$ is multiplied on the outside.

**Formula:** If $u = g(x)$, then $du = g'(x)dx$.

$$ \int f(g(x)) \cdot g'(x) \, dx = \int f(u) \, du $$

e.g.) To solve $\int 2x e^{x^2} \, dx$:

1.  Let $u = x^2 \rightarrow$ $du = 2x \, dx$

2.  Substitute: $\int e^u \, du = e^u$

3.  Back-substitute: $\int 2x e^{x^2} \, dx = e^{x^2} + C$

------------------------------------------------------------------------

## Integration by Parts

Integration by Parts is a technique used to integrate the product of two
functions.

### The Formula

The following formula transforms a difficult integral into an easier one
(hopefully).

$$ \int u \, dv = uv - \int v \, du $$

- $u$: The part you differentiate (aiming to simplify it).
- $dv$: The part you integrate (aiming to keep it manageable).

The general strategy is to identify a part that is easy to integrate,
and still manageable after integration.The other part should be
simplified after differentiation.

**Steps**

1.  choose $u$ (simplifies when differentiated) and $dv$ (easy to
    integrate).
2.  Compute $du$ and $v$.
3.  Apply $\int u\,dv = uv - \int v\,du$.

### Example: Polynomials and Exponentials

A very common pattern is the product of a polynomial and an exponential
function, such as $\int x^n e^{x} \, dx$.

**Strategy:** Always choose the polynomial ($x$ or $x^2$) to be $u$,
since their order goes down after differentiation.

#### Example 1 (Single Step)

Solve $\int x e^x \, dx$:

1.  Choose variables:

- Let $u = x \rightarrow$ $du = dx$
- Let $dv = e^x dx \rightarrow$ $v = e^x$

2.  Apply Formula:

$$ \int x e^x \, dx = xe^x - \int e^x \, dx $$

3.  Result:

$$ \int x e^x \, dx = xe^x - e^x $$

Note that we omit the integration constant $C$ here.

#### Example 2 (Repeated Steps)

If the polynomial has a higher power (like $x^2$), we just apply the
rule multiple times until the $x$ disappears.

Solve $\int x^2 e^x \, dx$:

1.  Round 1:

- Let $u = x^2 \rightarrow$ $du = 2x \, dx$
- Let $dv = e^x dx \rightarrow$  $v = e^x$
- Apply Formula:

$$ \int x^2 e^x \, dx = x^2 e^x - \int 2x e^x \, dx $$

2.  We then need to solve the remaining integral $\int 2x e^x \, dx$.
    From Example 1, we know $\int x e^x \, dx = xe^x - e^x$. We can
    substitute this back in.

3.  Final Calculation:

$$
\begin{aligned}
\int x^2 e^x \, dx &= x^2 e^x - 2(xe^x - e^x) \\
&= x^2 e^x - 2xe^x + 2e^x
\end{aligned}
$$
