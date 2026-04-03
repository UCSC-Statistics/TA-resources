Advanced Differentiation Rules
================
Jibo Shen

In this section, we move beyond simple functions to handle products,
ratios, composite functions.

------------------------------------------------------------------------

## The Product Rule

The Product Rule is used when differentiating the multiplication of two
distinct functions $f(x)$ and $g(x)$.

For $y = f(x) \cdot g(x)$:

$$
\frac{dy}{dx}= \frac{d}{dx} \Big[ f(x) \cdot g(x) \Big] = f'(x)g(x) + f(x)g'(x)
$$

e.g.) Differentiate $y = x^2 \cdot e^x$:

$$
\begin{aligned}
\text{Let } f(x) = x^2 &\rightarrow f'(x) = 2x \\
\text{Let } g(x) = e^x &\rightarrow g'(x) = e^x \\
\text{Apply formula: } \quad \frac{dy}{dx} &= (2x)(e^x) + (x^2)(e^x) \\
&= xe^x(2 + x)
\end{aligned}
$$

------------------------------------------------------------------------

## The Quotient Rule

The Quotient Rule is used when differentiating a ratio (division) of two
functions $f(x),\ g(x)$.

For $y = \frac{f(x)}{g(x)}$:

$$
\frac{dy}{dx}= \frac{d}{dx} \left[ \frac{f(x)}{g(x)} \right] = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2}
$$

e.g.) Differentiate $y = \frac{e^x}{x}$:

$$
\begin{aligned}
\text{Numerator: } f(x)=e^x &\rightarrow f'(x) = e^x \\
\text{Denominator: } g(x)= x &\rightarrow g'(x) = 1 \\
\text{Apply formula: } \quad \frac{dy}{dx} &= \frac{(e^x)(x) - (e^x)(1)}{x^2} \\
&= \frac{e^x(x-1)}{x^2}
\end{aligned}
$$

------------------------------------------------------------------------

## The Chain Rule

The Chain Rule allows us to differentiate **composite functions**
(functions inside other functions).

A composite function has the form $y = f(g(x))$, to differentiate:

$$
\frac{dy}{dx}= \frac{d}{dx} \Big[ f(g(x)) \Big] = f'(g(x)) \cdot g'(x)
$$

It is somehow like peeling an onion: You first take the derivative of
the outer function $f(x)$, leaving the inside $g(x)$ alone. Then
multiply by the derivative of the inner function $g'(x)$.

e.g.) Differentiate $y=(3x + 1)^5$:

$$
\begin{aligned}
\text{Outer: } (\dots)^5 &\rightarrow 5(\dots)^4 \\
\text{Inner: } 3x + 1 &\rightarrow 3 \\
\text{Result: } \quad \frac{dy}{dx} &= 5(3x+1)^4 \cdot 3 \\
&= 15(3x+1)^4
\end{aligned}
$$

e.g.) Differentiate $y = e^{x^2}$:

$$
\begin{aligned}
\text{Outer: } e^{(\dots)} &\rightarrow e^{(\dots)} \\
\text{Inner: } x^2 &\rightarrow 2x \\
\text{Result: } \quad \frac{dy}{dx} &= e^{x^2} \cdot 2x \\
&= 2x e^{x^2}
\end{aligned}
$$

------------------------------------------------------------------------

## L’Hôpital’s Rule

We put L’Hôpital’s Rule here, but it is not actually a rule to calculate
differentiations. L’Hôpital’s Rule is a technique for finding limits
that result in indeterminate forms:

If you try to evaluate a limit, $\lim_{x \to c} \frac{f(x)}{g(x)}$ and
you get $\frac{0}{0}$ or $\frac{\infty}{\infty}$. L’Hôpital’s Rule
enables us to evaluate the limit by differentiating the numerator and
denominator **separately**, then re-evaluate.

$$
\lim_{x \to c} \frac{f(x)}{g(x)} = \lim_{x \to c} \frac{f'(x)}{g'(x)}
$$

If the following **conditions** are met:

1.  Both $f(x)$ and $g(x)$ must be differentiable on an open interval
    around $c$ (except possibly at $c$ itself).
2.  The derivative of the denominator, $g'(x)$, must not be zero near
    $c$.
3.  The new limit, $\lim_{x \to c} \frac{f'(x)}{g'(x)}$ must exist (or
    equal $\pm \infty$).

e.g.) Find $\lim_{x \to 0} \frac{e^x - 1}{x}$:

$$
\begin{aligned}
\text{Check: } & \frac{e^0 - 1}{0} = \frac{0}{0} \quad (\text{Indeterminate}) \\
\text{Differentiate top: } & \frac{d}{dx}(e^x - 1) = e^x \\
\text{Differentiate bottom: } & \frac{d}{dx}(x) = 1 \\
\text{Re-evaluate: } & \lim_{x \to 0} \frac{e^x}{1} = \frac{e^0}{1} = 1
\end{aligned}
$$
