#calc2

convert rectangular points to coordinates in polar form;
	$x = rcos(\theta), y = rsin(\theta), \frac{y}{x}=tan(\theta), r^2=x^2+y^2$
graph polar equations and find the interval for one complete rotation through the graph;
find all points of intersection of polar graphs;
	just do it like normal
	also check poles (pole is $r=0$)
find arc length in polar form;
$$
r=f(\theta)
$$
$$
s=\int_\alpha^\beta{\sqrt{f(\theta)^2+f^\prime(\theta)^2}d\theta}
$$
find eccentricity and state which conic when you’re given an equation in polar form;
	foci are $c$ away from major axis (along $a$)
	Hyperbola $e=c/a$ $c^2=a^2+b^2$    $vertices=a$
	asymptotes: $y=k\pm \frac{a}{b}(x-h)$
	$$
	\frac{(x-h)^2}{a^2}-\frac{(y-k)^2}{b^2}=1
	$$
	Ellipse $e=c/a$ $c^2=a^2-b^2$
	$$
	\frac{(x-h)^2}{a^2}+\frac{(y-k)^2}{b^2}=1
	$$
	Parabola
	$$
		(x-h)^2=4p(y-k)
	$$
	Polar: 
	Hyperbola e > 1, Ellipse e < 1, Parabola e = 1
	$$
	r=\frac{ed}{1\pm ecos(\theta)}
	$$
find area of an ellipse; $area=\pi a b$
	$\frac{1}{2}\int_\alpha^\beta{[f(\theta)]^2d\theta}$
find volume of a solid of revolution, and this could be from chapter 7 as well;
usually $r(x) = x$
$$
V=\pi\int_a^b{[axis-R(x)]^2-[axis-r(x)]^2dx}
$$
$$
V=2\pi\int_a^b{(x-axis)f(x)dx}
$$
$$
SA=2\pi \int_a^b{(f(x) orxdependingonrevolvearoundxory,respectively)\sqrt{1+[f^\prime(x)]^2}dx}
$$
a few problems for finding integrals, which could include integration by parts and tabular, as well as using tables for integration;
$$\int{udv} = uv - \int{vdu}$$

| S   | u     | n              |
| --- | ----- | -------------- |
| +   | du⇘   | $\int{v}dv$    |
| -   | ddu⇘  | $\iint{v}dv$   |
| +   | dddu⇘ | $\iiint{v}dv$  |
| -   | 0     | $\iiiint{v}dv$ |

and divergence and convergence problems, so make sure you have that table as well