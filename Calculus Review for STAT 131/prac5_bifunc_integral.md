Practice Problems: Double Integrals
================

1.  Consider the region $D$ in the first quadrant bounded by
    $y = \sqrt{x}$ and $y = x^2$.

    1)  Set up the double integral $\iint_D xy \, dx \, dy$ integrating
        with respect to $y$ first ($dy \, dx$). Evaluate the integral.
    2)  Set up the integral with respect to $x$ first ($dx \, dy$).
        Evaluate the integral; it should be the same as your previous
        answer.

2.  Evaluate the following integral by first sketching the region and
    reversing the order of integration (since $\int \sin(x^2) dx$ has no
    elementary antiderivative): $$
    \int_0^1 \int_y^1 \sin(x^2) \, dx \, dy
    $$

3.  Evaluate the double integral $$
    \iint_{0 < y < 3x < 3} (2x - y) \, dx \, dy.
    $$ *Draw a graph in the $x$-$y$ plane and indicate the integration
    region.*

4.  Let $$
    f(x, y) = \begin{cases} 
    2x^2y, & 0 < x < 2 \text{ and } 0 < y < 1, \\
    0, & \text{otherwise}.
    \end{cases}
    $$

    1)  For any given $0 < x < 2$, evaluate $\int_0^1 f(x, y) \, dy$.
    2)  For any given $0 < y < 1$, evaluate $\int_0^2 f(x, y) \, dx$.
    3)  Evaluate $\int_0^1 \int_0^2 y \times f(x, y) \, dx \, dy$.
    4)  Evaluate $\iint_{x+y<1} f(x, y) \, dx \, dy$. (*Draw the
        region.*)

5.  Let $$
    f(x, y) = \begin{cases} 
    \frac{1}{4\pi}, & x^2 + y^2 \le 4, \\
    0, & \text{otherwise}.
    \end{cases}
    $$ Evaluate $\iint_{x^2+y^2 \le 4} f(x, y) \, dx \, dy$.

6.  Let $$
    f(x, y) = \begin{cases} 
    \frac{e^{-2x/y}e^{-y}}{y}, & 0 < x \text{ and } 0 < y, \\
    0, & \text{otherwise}.
    \end{cases}
    $$ For any given $y > 0$, evaluate $\int_0^y f(x, y) \, dx$.

7.  Let $b > 0$. Compute the integral: $$
    \int_0^\infty x e^{-bx} \, dx.
    $$ *(Hint: Use integration by parts with $u = x$ and
    $dv = e^{-bx} dx$).*

8.  Evaluate the following integrals:

    1)  $\int_0^\infty \int_0^\infty e^{-(2x+3y)} \, dx \, dy$.
    2)  $\int_0^\infty \int_0^\infty x e^{-(2x+3y)} \, dx \, dy$.
        *(Hint: You can use the result from Question 7.)*

9.  Let $$
    f(x, y) = \begin{cases} 
    (x+y)e^{-2y}, & 0 < x < y \text{ and } 0 < y < \infty, \\
    0, & \text{otherwise}.
    \end{cases}
    $$

    1)  For any given $0 < y < \infty$, evaluate
        $\int_0^y f(x, y) \, dx$, and use this to evaluate the integral
        $\int_0^\infty \int_0^\infty f(x,y) \, dx \, dy$.
    2)  For any given $0 < x < \infty$, evaluate
        $\int_x^\infty f(x, y) \, dy$, and use this to evaluate the
        integral $\int_0^\infty \int_0^\infty f(x,y) \, dx \, dy$.
