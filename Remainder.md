#calc2/series/alternating
Remainder: $R_N$ is remainder when approximating an infinite, converging series by computing the summation using a finite $n$
$|S-S_N|=|R_N| \leq a_{n+1}$
For precision go one more than desired number of decimal places
Ex: 
Precision desired: 2 places. Sum: 
$$
\sum_{n=1}^\infty \frac{(-1)^n}{n^2}
$$
Take just the right part of that remainder equation. Because of that abs, your sign doesn't matter
$$
|R_N| \leq \frac{1}{(n+1)^2}
$$
$R_N=\frac{1}{10^{2+1}}$ because of desired precision
$$
0.001 \leq \frac{1}{(n + 1)^2}
$$
$$
1000 \leq (n+1)^2
$$
$$
30.6 \leq n
$$
always round up
$$
n \geq 31
$$

Find error in already calculated summation by $|S - S_N|=R_N$
Ex:
$$
\sum_{n=1}^\infty \frac{(-1)^{n+1}}{n^4}
$$
Finding the interval is ridiculously obvious, you imbecile, why are you even bothering to ask me?

interval is
$S_N \pm R_N$