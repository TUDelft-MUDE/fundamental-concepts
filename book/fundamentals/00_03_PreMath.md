$\newcommand{\pderAt}[3]{\frac{\partial #1}{\partial #2}(#3)}$
$\newcommand{\dderAt}[3]{\frac{\mathrm{d} #1}{\mathrm{d} #2}(#3)}$

(PM_taylor)=
# Taylor series

## Taylor's theorem for approximating functions of 1 variable

Taylor’s theorem can be used to approximate a function $f(x)$ with the so called $p$-th order Taylor polynomial:

$$
f(x) \approx f(x_0) + \dderAt{f}{x}{x_0}\cdot(x-x_0) + \frac{1}{2!}\dderAt{^2f}{x^2}{x_0}\cdot(x-x_0)^2  + \ldots + \frac{1}{p!} \dderAt{^pf}{x^p}{x_0}\cdot(x-x_0)^p = P_k(x)
$$

where $\dderAt{f}{x}{x_0}$ signifies the derivative of $f$ with respect to $x$ evaluated at $x_0$. For the Taylor approximation to be valid, it is required that the function $f: \mathbb{R}\mapsto \mathbb{R}$ is $p$-times differentiable at the point $x_0 \in \mathbb{R}$.

The approximation error is equal to 

$$
R_p(x) = f(x)- P_k (x) 
$$

and $R_p(x)$ is called the remainder term. In the vicinity of $x_0$ the error is of the order $O(x^{p+1})$ 

:::{card} Example

A linear approximation (also called linearization) of $f(x) = \cos(x)$ at $x=x_0$ is obtained by the first-order Taylor polynomial as:

$$
f(x) \approx \cos x_0 + \dderAt{\cos x}{x}{x_0}\cdot (x-x_0) = \cos x_0 – \sin x_0 \cdot(x-x_0)
$$

So far, this is for an approximation around an arbitrary point. In general $x_0$ is not a variable but a given point around which we seek to approximate $f$. For example, the first order Taylor approximation of $\cos(x)$ around $x_0=0$ is:

$$
f(x) \approx \cos(0) - sin(0)\cdot(x-0) = 1
$$

Here the dependence on $x$ disappears because the first derivative of $\cos(x)$ is zero at $x=0$. The first order Taylor approximation of $\cos(x)$ at $x_0=\frac12\pi$ is given as:

$$
f(x) \approx -x+\frac12\pi
$$

:::

## First-order Taylor polynomial for linearizing a function of $n$ variables

For linearizing non-linear functions of $\mathbf{x} = (x_1, x_2, \ldots, x_n)$ being a vector with length $n$, the same principles can be applied. Partial derivatives now need to be taken with respect to each of the variables in $\mathbf{x}$, each evaluated at the same point $\mathbf{x}_0=(x_{0,1},x_{0,2},\ldots,x_{0,n})$. The first-order Taylor approximation is then given by:

$$
f(\mathbf{x}) \approx f(\mathbf{x}_0)  + \pderAt{f}{x_1}{\mathbf{x}_0} \cdot (x_1-x_{0,1})+ \pderAt{f}{x_2}{\mathbf{x}_0}\cdot (x_2-x_{0,2}) + \ldots + \pderAt{f}{x_n}{\mathbf{x}_0}\cdot (x_n-x_{0,n}) f(x_0) \Delta x_0
$$

:::{card} Exercise

Find a linear approximation of the function $f(x,y)=x^2+xy$ around $(x,y)=(1,1)$. Note that, by definition, the result should be a function that is linear in both $x$ and $y$, i.e. of the form $f(x,y) \approx ax+by+c$ where $a$, $b$ and $c$ are constants.


 ```{admonition} Solution
:class: tip, dropdown
A linear approximation of the function $f(x,y) = x^2+xy$ around $(x,y)=(x_0,y_0)$ is given as:

$$
f(x,y) \approx f(0,0) + \pderAt{f}{x}{x_0,y_0}\cdot(x-x_0) + \pderAt{f}{y}{x_0,y_0}\cdot(y-y_0) = (2x_0+y_0)\cdot(x-x_0) + x_0\cdot(y-y_0)
$$ 

For an approximation around $(x_0,y_0) = (1,1)$ we get:

$$
f(x,y) \approx (2+1)\cdot(x-1) + 1\cdot(y-1) = 3x+y-4
$$
```

:::


