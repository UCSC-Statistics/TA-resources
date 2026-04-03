First and Second Order Partial Derivatives
================
Jibo Shen

When we deal with bivariate functions, the concept of “slope” becomes
more nuanced. We cannot just say “the derivative” because the function
can change differently depending on which direction we move.

Instead, we use **Partial Derivatives**, which measure the rate of
change along one specific coordinate axis while holding all other
variables frozen.

------------------------------------------------------------------------

# First Order Partial Derivatives

The **Partial Derivative** **w.r.t** (with respect to) $x$ measures how
$f$ changes as $x$ varies, assuming $y$ remains fixed.

Notation: We use the “curly d” symbol $\partial$ (pronounced “partial”)
to distinguish it from the standard $d$.

- Partial w.r.t $x$: $\frac{\partial}{\partial x} f(x, y)$ or $f_x$
- Partial w.r.t $y$: $\frac{\partial}{\partial y} f(x, y)$ or $f_y$

Note: The abbreviation **w.r.t** stands for “with respect to”. It
emphasizes the variable is actually changing.

**Important Rule:** When calculating $\frac{\partial}{\partial x}$, you
must treat all other variables ($y, z$, etc.) exactly like
**constants**.

This implies that doing a partial derivative is essentially doing a
univariate derivative. Therefore, all the techniques we discussed in the
univariate case (Product Rule, Quotient Rule, Chain Rule) still apply.

## Example 1:

Let $f(x, y) = x^3 + 5y^2$. Find $\frac{\partial f}{\partial x}$.

Here, we are deriving w.r.t $x$.

- The first term $x^3$ becomes $3x^2$.
- The second term $5y^2$ does not contain $x$. Therefore, it is treated
  entirely as a constant. The derivative of a constant is $0$.

$$\frac{\partial f}{\partial x} = 3x^2 + 0 = 3x^2$$

## Example 2: The Product Rule (Partial)

Let $f(x, y) = x e^{xy}$. Find $\frac{\partial f}{\partial x}$.

Here, we are deriving w.r.t $x$. Since $x$ appears in two places
multiplied together (the $x$ in front and the $x$ inside the exponent),
we use the product rule. Note that $y$ is treated as a constant.

$$
\begin{aligned}
\frac{\partial}{\partial x} [x \cdot e^{xy}] &= \frac{\partial}{\partial x}(x) \cdot e^{xy} + x \cdot \frac{\partial}{\partial x}(e^{xy}) \\
&= 1 \cdot e^{xy} + x \cdot (e^{xy} \cdot y) \quad \text{(Chain rule: deriv of } xy \text{ w.r.t } x \text{ is } y) \\
&= e^{xy} + xy e^{xy}
\end{aligned}
$$

## Example 3: The Quotient Rule (Partial)

Let $f(x, y) = \frac{x}{y^2 + 1}$. Find $\frac{\partial f}{\partial y}$.

Here, we are deriving w.r.t $y$. The variable $y$ is in the denominator,
so we can use the quotient rule. We treat $x$ as a constant.

$$
\begin{aligned}
\text{Numerator } u = x &\rightarrow u' = 0 \quad (\text{deriv of constant is 0}) \\
\text{Denominator } v = y^2 + 1 &\rightarrow v' = 2y \\
\text{Apply Formula: } \frac{u'v - uv'}{v^2} &= \frac{(0)(y^2+1) - (x)(2y)}{(y^2+1)^2} \\
&= \frac{-2xy}{(y^2+1)^2}
\end{aligned}
$$

## Example 4: The Chain Rule (Partial)

Let $f(x, y) = (x^2 + y^2)^{10}$. Find $\frac{\partial f}{\partial x}$.

Here, we have an “inner” function ($x^2 + y^2$) inside an “outer”
function $( \dots )^{10}$. We use the chain rule.

$$
\begin{aligned}
\text{Outer deriv: } & 10(x^2 + y^2)^9 \\
\text{Inner deriv w.r.t } x: & \frac{\partial}{\partial x}(x^2 + y^2) = 2x + 0 = 2x \\
\text{Multiply them: } & 10(x^2 + y^2)^9 \cdot 2x \\
&= 20x(x^2 + y^2)^9
\end{aligned}
$$

**Caution**: One of the most common mistakes in multivariate calculus is
confusing variable and constants when differentiating. Always pause
before starting and ask yourself: “Which letter is the variable, and
which letters are just numbers?”

------------------------------------------------------------------------

# Second Order Partial Derivatives

Just as we can differentiate a function twice, we can take partial
derivatives of partial derivatives.

Since we have two variables, there are four possible second-order
derivatives:

1.  **$f_{xx}$**: Differentiate w.r.t $x$, then w.r.t $x$ again.
    $$\frac{\partial^2 f}{\partial x^2} = \frac{\partial}{\partial x} \left( \frac{\partial f}{\partial x} \right)$$

2.  **$f_{yy}$**: Differentiate w.r.t $y$, then w.r.t $y$ again.
    $$\frac{\partial^2 f}{\partial y^2} = \frac{\partial}{\partial y} \left( \frac{\partial f}{\partial y} \right)$$

3.  **$f_{xy}$ (Mixed)**: Differentiate w.r.t $x$ first, then w.r.t $y$.
    $$\frac{\partial^2 f}{\partial x \partial y} = \frac{\partial}{\partial y} \left( \frac{\partial f}{\partial x} \right)$$

4.  **$f_{yx}$ (Mixed)**: Differentiate w.r.t $y$ first, then w.r.t $x$.
    $$\frac{\partial^2 f}{\partial y \partial x} = \frac{\partial}{\partial x} \left( \frac{\partial f}{\partial y} \right)$$

## Example 1

Let $f(x, y) = x^3 y^2$.

**Step 1**: First Order

- $f_x = 3x^2 y^2$
- $f_y = x^3 (2y) = 2x^3 y$

**Step 2**: Second Order

- **$f_{xx}$**: Differentiate $f_x$ ($3x^2 y^2$) w.r.t $x$:
  $$3(2x)y^2 = 6xy^2$$
- **$f_{yy}$**: Differentiate $f_y$ ($2x^3 y$) w.r.t $y$:
  $$2x^3(1) = 2x^3$$
- **$f_{xy}$**: Differentiate $f_x$ ($3x^2 y^2$) w.r.t $y$:
  $$3x^2(2y) = 6x^2y$$
- **$f_{yx}$**: Differentiate $f_y$ ($2x^3 y$) w.r.t $x$:
  $$2(3x^2)y = 6x^2y$$

**Symmetry:** Notice in the example above that $f_{xy} = f_{yx}$. This
is not a coincidence. For almost all functions used in this course, the
order of differentiation does not matter.

$$\frac{\partial^2 f}{\partial x \partial y} = \frac{\partial^2 f}{\partial y \partial x}$$

**Self-Check Tip:** This symmetry is a fantastic way to check your work.
If you calculate $f_{xy}$ and $f_{yx}$ separately and get different
answers, you know for sure that you made a mistake in one of them!

## Example 2

Let $f(x, y) = x \sin(xy)$. This is trickier because the variables are
mixed inside the sine function.

**Step 1**: First Order Derivatives

- Find $f_x$: We differentiate w.r.t $x$. Notice that $x$ appears
  *twice* (once outside, once inside). We must use the Product Rule and
  Chain Rule.

$$
    \begin{aligned}
    f_x &= \frac{\partial}{\partial x}(x) \cdot \sin(xy) + x \cdot \frac{\partial}{\partial x}(\sin(xy)) \\
    &= (1) \cdot \sin(xy) + x \cdot (\cos(xy) \cdot y) \quad (\text{Chain rule: deriv of } xy \text{ is } y) \\
    &= \sin(xy) + xy \cos(xy)
    \end{aligned}
$$

- Find $f_y$: We differentiate w.r.t $y$. Here, the $x$ outside is just
  a constant coefficient. We only need the Chain Rule.

$$
    \begin{aligned}
    f_y &= x \cdot \frac{\partial}{\partial y}(\sin(xy)) \\
    &= x \cdot (\cos(xy) \cdot x) \quad (\text{Chain rule: deriv of } xy \text{ is } x) \\
    &= x^2 \cos(xy)
    \end{aligned}
$$

**Step 2**: Second Order Derivatives (Mixed)

Now, let’s calculate the mixed partial $f_{xy}$ (taking the derivative
of $f_x$ w.r.t $y$). We look at our result for
$f_x = \sin(xy) + xy \cos(xy)$ and differentiate w.r.t $y$.

- Term 1 $\sin(xy)$: Derivative is $\cos(xy) \cdot x$.
- Term 2 $xy \cos(xy)$: We treat $x$ as a constant coefficient, so we
  are differentiating $x [y \cos(xy)]$. This requires the Product Rule.

$$
    \begin{aligned}
    \frac{\partial}{\partial y} [\sin(xy)] &= x \cos(xy) \\
    \frac{\partial}{\partial y} [xy \cos(xy)] &= x \left[ (1)\cos(xy) + y(-\sin(xy) \cdot x) \right] \\
    &= x \cos(xy) - x^2 y \sin(xy)
    \end{aligned}
$$

Combining them:

$$
    \begin{aligned}
    f_{xy} &= x \cos(xy) + [x \cos(xy) - x^2 y \sin(xy)] \\
    &= 2x \cos(xy) - x^2 y \sin(xy)
    \end{aligned}
$$

**Note:** Try differentiating $f_y = x^2 \cos(xy)$ w.r.t $x$, you will
get the exact same result!
