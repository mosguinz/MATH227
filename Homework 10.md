---
export_on_save:
    html: true
puppeteer:
    format: "Letter"
    timeout: 3000
---

# Homework 10

**Mos Kullathon**
921425216

$$
    % Differentials d[something]/d[something]
    \gdef\diff#1#2{\frac{\mathrm{d}#1}{\mathrm{d}#2}}
    % Shortcut for dy/dx
    \gdef\dydx{\diff{y}{x}}
    % Differential letter "d" with a thin space before it
    \gdef\dd{\mathop{}\!\mathrm{d}}
    % Shortcut for not implies
    \gdef\nimplies{\;\;\;\not\nobreak\!\!\!\!\implies\;}
    % Shortcuts for extended brackets
    \gdef\({\left(} \gdef\){\right)}
    \gdef\[{\left[} \gdef\]{\right]}
    % Shortcut for real number symbol
    \gdef\R{\mathbb{R}}
    % More spacing between lines in arrays (override by using \[5em])
    \gdef\arraystretch{2.2em}
$$

## 1\. Determine whether the following series is convergent or divergent. We may use any tests available

### (i) $\sum_{n=1}^\infty \frac{1}{n^2 2^n}$

As a $p$-series where $p=2$, $\displaystyle\sum_{n=1}^\infty\frac{1}{n^2}$ converges. Since $\displaystyle\frac{1}{n^2}\ge\frac{1}{n^22^n}$ for $n\ge1$, by comparison test $\displaystyle\sum_{n=1}^\infty \frac{1}{n^22^n}$ converges.

### (ii) $\sum_{n=2}^\infty \frac{3n^3+2n^2+2}{n^4-1}$

Let $\displaystyle a_n=\frac{3n^3+2n^2+2}{n^4-1}$ and $\displaystyle b_n=\frac{1}{n}$.

Then,
$$
\frac{a_n}{b_n}
=\frac{n(3n^3+2n^2+2)}{n^4-1}
=\frac{3n^4+2n^3+2n}{n^4-1} \\
\therefore \lim_{n\to\infty}\frac{a_n}{b_n}
=\lim_{n\to\infty}\frac{3n^4+2n^3+2n}{n^4-1}=3.
$$

Since $\displaystyle\sum_{n=1}^\infty b_n = \sum_{n=1}^\infty\frac{1}{n}$ is a $p$-series such that $p=1$, $\displaystyle\sum_{n=1}^\infty b_n$ diverges. Consequently, by limit comparison test, $\displaystyle\sum_{n=1}^\infty a_n$ also diverges.

### (iii) $\sum_{n=1}^\infty \frac{n^{1/3}}{(n^{3/2}-1)^{1/2}}$

At $n=1$, the first term is undefined. Therefore, the sum does not exist.
$$
\frac{1^{1/3}}{(1^{3/2}-1)^{1/2}}=\frac{1}{0}
$$

### (iv) $\sum_{n=1}^\infty \frac{n^2\ln n}{n^5+2n-1}$

For sufficiently large $n$,
$$
\frac{n^2\ln n}{n^5+2n-1}\approx\frac{1}{n^3}.
$$

Since $\displaystyle\sum_{n=1}^\infty\frac{1}{n^3}$ is a $p$-series such that $p=3$, the series converges.

### (v) $\sum_{n=1}^\infty (-1)^{n^2}\frac{n+1}{n!}$

Let $\displaystyle a_n=(-1)^{n^2}\frac{n+1}{n!}$.

Then,
$$
a_{n+1}=\frac{(-1)^{(n+1)^2}(n+1)+1}{(n+1)!}
=\frac{(-1)^{n^2+2n+1}n+2}{(n+1)n!}.
$$

and
$$
\begin{align*}
    \left|\frac{a_{n+1}}{a_n}\right|
    &= \left|
        \frac{(-1)^{\cancel{n^2}+2n+1}n+2}
        {(n+1)\cancel{n!}}
        \cdot
        \frac{\cancel{n!}}{\cancel{(-1)^{n^2}}(n+1)}
    \right| \\
    &= \left|
        \frac{(-1)^{2n+1}(n+2)}{(n+1)^2}
    \right|
\end{align*}
\\
\therefore\lim_{n\to\infty} \left|\frac{a_{n+1}}{a_n}\right|=0<1
$$

By ratio test, the series converges absolutely.

### (vi) $\sum_{n=1}^\infty \frac{(n!)^3}{(3n)!}$

Let $\displaystyle a_n=\frac{(n!)^3}{(3n)!}$.

Then,
$$
\begin{align*}
    a_{n+1}
    &=\frac{((n+1)!)^3}{(3(n+1))!} \\
    &=\frac{((n+1)!)^3}{(3n+3)!} \\
    &= \frac{((n+1)n!)^3}{(3n+3)(3n+2)(3n+1)(3n)!} \\
    &= \frac{(n+1)^3(n!)^3}{(3n+3)(3n+2)(3n+1)(3n)!}
\end{align*}
$$

and
$$
\begin{align*}
    \left|\frac{a_{n+1}}{a_n}\right|
    &= \left|
    \frac{(n+1)^3\cancel{(n!)^3}}
    {(3n+3)(3n+2)(3n+1)\cancel{(3n)!}}
    \cdot \frac{\cancel{(3n)!}}{\cancel{(n!)^3}}
    \right| \\
    &= \left|
    \frac{(n+1)^3}
    {(3n+3)(3n+2)(3n+1)}
    \right|
\end{align*}
\\
\therefore \lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|=\frac{1}{3^3}=\frac{1}{27}<1
$$

By ratio test, the series converges absolutely.

### (vii) $\sum_{n=1}^\infty (\frac{n}{3n+1})^n$

Let $\displaystyle a_n = \(\frac{n}{3n+1}\)^n$.

Then,
$$
|a_n|^{\frac{1}{n}}
=\left|\(\frac{n}{3n+1}\)^n\right|^\frac{1}{n}
=\left|\frac{n}{3n+1}\right|
=\frac{n}{3n+1},
\quad n\ge 1
$$

and
$$
\lim_{n\to\infty}|a_n|^\frac{1}{n}
= \lim_{n\to\infty}\frac{n}{3n+1}=\frac{1}{3}\\
\therefore \lim_{n\to\infty}|a_n|^\frac{1}{n}< 0.
$$

By root test, the series converges absolutely.

### (viii) $\sum_{n=2}^\infty \frac{(-1)^n}{\ln n}$

Let $\displaystyle a_n = \frac{1}{\ln n}$.

Since $\ln n$ is monotonically increasing, its reciprocal $\displaystyle a_n = \frac{1}{\ln n}$ must be monotonically decreasing.

Then,
$$
\lim_{n\to\infty}a_n
=\lim_{n\to\infty}\frac{1}{\ln n}
=0.
$$

By alternating series test, the series converge.

### (ix) $\sum_{n=2}^\infty (-1)^n\ln n$

$$
\lim_{n\to\infty}\ln n = \infty
$$

By divergence test, the series diverges.

## 2\. Find the radius of convergence and interval of convergence for the following power series

### (i) $\sum_{n=0}^\infty\frac{1}{n2^n}x^n$

$$
a_n=\frac{x^n}{n2^n},\quad
a_{n+1}=\frac{x^{n+1}}{(n+1)2^{n+1}}
\\
\begin{align*}
    \left|
        \frac{a_{n+1}}{a_n}
    \right|
    &= \left|
        \frac{x^{n+1}}{(n+1)2^{n+1}}
        \cdot\frac{n2^n}{x^n}
    \right| \\
    &= \left|
        \frac{xn}{2(n+1)}
    \right| \\
    &= |x|\frac{n}{2n+2},\quad n\ge0
\end{align*}
\\
% \frac{n}{2n+2}\to\frac{1}{2}
% \implies|x|\frac{n}{2n+2}\to L<1 \iff |x|<2 \\
% \therefore R=2
% \\
\therefore L=\lim_{n\to\infty}
\left| \frac{a_{n+1}}{a_n} \right| = \frac{|x|}{2}
\implies L <1 \iff |x|<2
$$

Since
$$
|x|<2\iff -2<x<2,
$$

by ratio test, the series converges absolutely for $-2<x<2$ centered at $x=0$.

$$
x=-2\implies
\sum_{n=0}^\infty\frac{1}{n2^n}(-2)^n
=\sum_{n=0}^\infty\frac{(-1)^n}{n}
$$

Since $\displaystyle\frac{1}{n}\to0$, by alternating series test, the series converges at $x=-2$.

$$
x=2\implies
\sum_{n=0}^\infty\frac{1}{n2^n}(2)^n
=\sum_{n=0}^\infty\frac{1}{n}
$$

At $x=2$, the series is a $p$-series such that $p=1$. Therefore, the series diverge at $x=2$.

As such:

* the radius of convergence is $2$
* the interval of convergence is $[-2,2)$.

### (ii) $\sum_{n=0}^\infty\frac{(x-1)^n}{\sqrt{n}}$

$$
a_n=\frac{(x-1)^n}{\sqrt{n}},\quad
a_{n+1}=\frac{(x-1)^{n+1}}{\sqrt{n+1}}
\\
\begin{align*}
    \left|\frac{a_{n+1}}{a_n}\right|
    &= \left|
        \frac{(x-1)^{n+1}}{\sqrt{n+1}}
        \cdot\frac{\sqrt{n}}{(x-1)^n}
    \right| \\
    &= \left|
        \frac{\sqrt{n}(x-1)}{\sqrt{n+1}}
    \right| \\
    &= |x-1|\frac{\sqrt{n}}{\sqrt{n+1}},\quad n\ge0
\end{align*}
\\
\therefore L=\lim_{n\to\infty}
\left|\frac{a_{n+1}}{a_n}\right|=|x-1|
\implies L<1 \iff |x-1|<1 \\
$$

Since
$$
|x-1|<1
\iff -1<x-1<1
\iff 0<x<2,
$$

by ratio test, the series converges absolutely for $0<x<2$ centered at $x=1$.

$$
x=0\implies\sum_{n=0}^\infty\frac{(0-1)^n}{\sqrt{n}}
=\sum_{n=0}^\infty\frac{(-1)^n}{\sqrt{n}}
$$

Since $\displaystyle\frac{1}{\sqrt{n}}\to0$, by alternating series test, the series converges at $x=0$.

$$
x=2\implies\sum_{n=0}^\infty\frac{(2-1)^n}{\sqrt{n}}
=\sum_{n=0}^\infty\frac{1^n}{\sqrt{n}}
=\sum_{n=0}^\infty\frac{1}{n^{1/2}}
$$

At $x=2$, the series is a $p$-series such that $\displaystyle p=\frac{1}{2}$. Therefore, the series diverges at $x=2$.

As such:

* the radius of convergence is $1$
* the interval of convergence is $[0,2)$.

### (iii) $\sum_{n=2}^\infty \frac{1}{n\ln n}x^n$

$$
a_n=\frac{x^n}{n\ln n},\quad
a_{n+1}=\frac{x^{n+1}}{(n+1)\ln(n+1)} \\
\begin{align*}
    \left|\frac{a_{n+1}}{a_n}\right|
    &= \left|
        \frac{x^{n+1}}{(n+1)\ln(n+1)}\cdot
        \frac{n\ln n}{x^n}
    \right| \\
    &= \left|
        \frac{nx\ln n}{(n+1)\ln(n+1)}
    \right|
\end{align*}
\\
\begin{align*}
    \therefore L =
    \lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|
    &= \lim_{n\to\infty}\left|
        \frac{nx\ln n}{(n+1)\ln(n+1)}
    \right| \\
    &= \lim_{n\to\infty}
    \left| \frac{nx}{n+1} \right|
    \cdot\lim_{n\to\infty}
    \left|\frac{\ln n}{\ln(n+1)}\right| \\
    &= |x| \cdot \lim_{n\to\infty}
    \left|\frac{\frac{1}{n}}{\frac{1}{n+1}}\right| \\
    &= |x| \\
    \implies L <1 &\iff |x| <1
\end{align*}
$$

Since
$$
|x|<1\iff-1<x<1,
$$

by ratio test, the series converges absolutely for $-1<x<1$.

$$
x=-1\implies
\sum_{n=2}^\infty \frac{1}{n\ln n}(-1)^n
$$

Since $\displaystyle\frac{1}{n\ln n}\to0$, by alternating series test, the series converge at $x=-1$.

$$
x=1\implies
\sum_{n=2}^\infty \frac{1}{n\ln n}(1)^n
=\sum_{n=2}^\infty \frac{1}{n\ln n}
$$

Let $\displaystyle g(x)=\frac{1}{x\ln x}$. Since $g'(x)<0$ for $x\ge2$, we apply the integral test.

$$
\begin{darray}{cc}
    u=\ln x &\implies& \dd u=\frac{1}{x}\dd x \\
    &\iff&\dd x = x\dd u \\
    x=2 &\implies& u = \ln 2 \\
    x=n &\implies& u = \ln n
\end{darray}
\\
\begin{align*}
    \lim_{n\to\infty}\int_2^n\frac{1}{x\ln x}\dd x
    &= \lim_{n\to\infty}\int_{\ln 2}^{\ln n}
    \frac{x\dd u}{xu} \\
    &= \lim_{n\to\infty}
    \bigg[\ln u\bigg]_{\ln 2}^{\ln n} \\
    &= \lim_{n\to\infty}\ln(\ln n)-\ln(\ln 2) \\
    &= \infty
\end{align*}
$$

By integral test, the series diverge at $x=1$.

As such:

* the radius of convergence is $1$
* the interval of convergence is $[-1,1)$.

### (iv) $\sum_{n=2}^\infty (2+\frac{1}{n})^n x^n$

$$
a_n = \(2+\frac{1}{n}\)^n x^n
\\
\begin{align*}
    |a_n|^\frac{1}{n}
    &= \left|
        \(2+\frac{1}{n}\) x
    \right|
\end{align*}
\\
\therefore L=\lim_{n\to\infty}|a_n|^\frac{1}{n}
= |2x| \implies L < 1 \iff |2x|<1
$$

Since
$$
|2x|<1
\iff |x| < \frac{1}{2}
\iff -\frac{1}{2}<x<\frac{1}{2},
$$

by root test, the series converges absolutely for $\displaystyle-\frac{1}{2}<x<\frac{1}{2}$ centered at $x=0$.

$$
x=-\frac{1}{2}\implies
\sum_{n=2}^\infty \(2+\frac{1}{n}\)^n \(-\frac{1}{2}\)^n
\\
a_n=\(2+\frac{1}{n}\)^n \(-\frac{1}{2}\)^n \\
|a_n|^\frac{1}{n} =
\left|
\(2+\frac{1}{n}\) \(-\frac{1}{2}\)
\right|
$$

Since $|a_n|^\frac{1}{n}\to-1$, by root test, the series converges at $\displaystyle x=-\frac{1}{2}$.

$$
x=\frac{1}{2}\implies
\sum_{n=2}^\infty \(2+\frac{1}{n}\)^n \(\frac{1}{2}\)^n
\\
\begin{align*}
    \lim_{n\to\infty}\(2+\frac{1}{n}\)^n \(\frac{1}{2}\)^n
    &= \lim_{n\to\infty}
    \(\(2+\frac{1}{n}\) \(\frac{1}{2}\)\)^n \\
    &= \lim_{n\to\infty}
    \(1+\frac{1}{2n}\)^n \\
    &= \lim_{n\to\infty}
    e^{n\ln\(1+\frac{1}{2n}\) } \\
    &= \lim_{n\to\infty}
    \exp\frac{\ln\(1+\frac{1}{2n}\) }{1/n} \\
    &= \exp\lim_{n\to\infty}
    \frac{\frac{1}{1+\frac{1}{2n}}\cdot
    -\frac{1}{2n^2}}{-\frac{1}{n^2}} \\
    &= \exp\lim_{n\to\infty}
    \frac{1}{1+\frac{1}{2n}}\cdot\frac{1}{2} \\
    &= \exp\frac{1}{2} \\
    &= \sqrt{e} \quad\approx 1.64872
\end{align*}
$$

Since $\displaystyle\(2+\frac{1}{n}\)^n \(\frac{1}{2}\)^n\to\sqrt{e}$, by divergence test, the series diverge at $\displaystyle x=\frac{1}{2}$.

As such:

* the radius of convergence is $\displaystyle\frac{1}{2}$
* the interval of convergence is $\displaystyle\[-\frac{1}{2},\frac{1}{2}\)$.

## 3\. Section 6.1

In the following exercises, given that $\displaystyle\frac{1}{1-x}=\sum_{n=0}^\infty x^n$ with convergence in $(−1,1)$,  find the power series for each function with the given center *a*, and identify its interval of convergence.

### (35) $f(x)=\frac{x}{1-x^2}; a=0$

$$
\begin{align*}
    f(x) &= \frac{x}{1-x^2} \\
    &= \sum_{n=0}^\infty x(x^2)^n,\quad |x^2|<1 \\
    &= \sum_{n=0}^\infty x^{2n+1},\quad |x|<1
\end{align*}
$$

Since
$$
|x|<1\iff-1<x<1,
$$

$f(x)$ converges within $-1<x<1$.

Then,
$$
f(-1) = \sum_{n=0}^\infty(-1)^{2n+1}
$$

Since $\displaystyle\lim_{n\to\infty} (-1)^{2n+1}$ does not exist, $f(-1)$ diverges by divergence test.

$$
f(1) = \sum_{n=0}^\infty1^{2n+1} \\
$$

Since $\displaystyle\lim_{n\to\infty}1^{2n+1}=1$, $f(1)$ diverges by divergence test.

As such,
$$
f(x)
=\frac{x}{1-x^2}
=\sum_{n=0}^\infty x^{2n+1},\quad x\in(-1,1).
$$

### (37) $f(x)=\frac{x^2}{1+x^2}; a=0$

$$
\begin{align*}
    f(x) &= \frac{x^2}{1+x^2} \\
    &= \frac{x^2}{1-(-x^2)} \\
    &= \sum_{n=0}^\infty x^2(-x^2)^n,
    \quad\left|-x^2\right|<1 \\
    &= \sum_{n=0}^\infty(-1)^n x^{2n+2},
    \quad|x|<1
\end{align*}
$$

Since
$$
|x|<1\iff-1<x<1,
$$

$f(x)$ converges within $-1<x<1$.

Then,
$$
f(-1)=\sum_{n=0}^\infty(-1)^n (-1)^{2n+2}
=\sum_{n=0}^\infty(-1)^{3n+2}
$$

Since $\displaystyle\lim_{n\to\infty}(-1)^{3n+2}$ does not exist, $f(-1)$ diverges by divergence test.

$$
f(1)=\sum_{n=0}^\infty(-1)^n (1)^{2n+2}
=\sum_{n=0}^\infty(-1)^n
$$

Since $\displaystyle\lim_{n\to\infty}(-1)^n$ does not exist, $f(1)$ diverges by divergence test.

As such,
$$
f(x)=\frac{x^2}{1+x^2}
=\sum_{n=0}^\infty(-1)^n x^{2n+2},
\quad x\in(-1,1)
$$

### (39) $f(x)=\frac{1}{1-2x}; a=0$

$$
\begin{align*}
    f(x) &= \frac{1}{1-2x} \\
    &= \sum_{n=0}^\infty(2x)^n,
    \quad\left|2x\right|<1 \\
    &= \sum_{n=0}^\infty2^n x^n,
    \quad|x|<\frac{1}{2}
\end{align*}
$$

Since
$$
|x|<\frac{1}{2}\iff-\frac{1}{2}<x<\frac{1}{2},
$$

$f(x)$ converges within $\displaystyle-\frac{1}{2}<x<\frac{1}{2}$.

Then,
$$
f\(-\frac{1}{2}\)
=\sum_{n=0}^\infty 2^n\(-\frac{1}{2}\)^n
=\sum_{n=0}^\infty (-1)^n
$$

Since $\displaystyle\lim_{n\to\infty}(-1)^n$ does not exist, $f\(-\frac{1}{2}\)$ diverges by divergence test.

$$
f\(\frac{1}{2}\)
=\sum_{n=0}^\infty2^n\(\frac{1}{2}\)^n
=\sum_{n=0}^\infty 1
$$

Since $\displaystyle\lim_{n\to\infty}1=1$, $f(1)$ diverges by divergence test.

As such,
$$
f(x)=\frac{1}{1-2x}=\sum_{n=0}^\infty2^n x^n,
\quad x\in\(-\frac{1}{2},\frac{1}{2}\)
$$

### (41) $f(x)=\frac{x^2}{1-4x^2}; a=0$

$$
\begin{align*}
    f(x) &= \frac{x^2}{1-4x^2} \\
    &= \sum_{n=0}^\infty x^2(4x^2)^n,\quad |4x^2|<1 \\
    &= \sum_{n=0}^\infty x^24^nx^{2n},\quad |x^2|<\frac{1}{4} \\
    &= \sum_{n=0}^\infty 4^nx^{2n+2},\quad |x|<\frac{1}{2}
\end{align*}
$$

Since
$$
|x|<\frac{1}{2}\iff-\frac{1}{2}<x<\frac{1}{2},
$$

$f(x)$ converges within $\displaystyle-\frac{1}{2}<x<\frac{1}{2}$.

Then,
$$
f\(-\frac{1}{2}\)=\sum_{n=0}^\infty 4^n
\(-\frac{1}{2}\)^{2n+2}.
$$

Since $\displaystyle\lim_{n\to\infty}4^n\(-\frac{1}{2}\)^{2n+2}$ does not exist, by divergence test $\displaystyle f\(-\frac{1}{2}\)$ diverges.

$$
f\(\frac{1}{2}\)=\sum_{n=0}^\infty 4^n
\(\frac{1}{2}\)^{2n+2}
$$

Since
$$
\begin{align*}
    \lim_{n\to\infty}4^n\(\frac{1}{2}\)^{2n+2}
    &= \lim_{n\to\infty}\frac{4^n}{2^{2n+2}} \\
    &= \lim_{n\to\infty}\frac{4^n}{2^{2n}\cdot2^2} \\
    &= \lim_{n\to\infty}\frac{4^n}{(2^2)^n\cdot2^2} \\
    &= \lim_{n\to\infty}\frac{1}{4} \\
    &= \frac{1}{4}
\end{align*}
$$

by divergence test $\displaystyle f\(\frac{1}{2}\)$ diverges.

As such,
$$
f(x)=\frac{x^2}{1-4x^2}
=\sum_{n=0}^\infty 4^nx^{2n+2},
\quad x\in\(-\frac{1}{2},\frac{1}{2}\)
$$

## 4\. Find

### (i) The Taylor polynomial of degree 3 of $f(x)=x^{2/3}$ at $x=8$

$$
\begin{align*}
    f(x)=x^{2/3}
    &\implies f'(x)=\frac{2}{3}x^{-1/3} \\
    &\implies f''(x)=-\frac{2}{9}x^{-4/3} \\
    &\implies f'''(x)=\frac{8}{27}x^{-7/3} \\
\end{align*}
\\
\begin{darray}{cll}
    f(8) &= 8^{2/3} &= 4\\
    f'(8) &= \frac{2}{3}\cdot 8^{-1/3}  &= \frac{1}{3}\\
    f''(8) &= -\frac{2}{9}\cdot 8^{-4/3} &= -\frac{1}{72}\\
    f'''(8) &= \frac{8}{27}\cdot 8^{-7/3} &= \frac{1}{432}\\
\end{darray}
\\
\begin{align*}
    \therefore\sum_{n=0}^3\frac{f^{(n)}(x)}{n!}(x-8)^n
    &= f(8) + f'(8)(x-8)
    +\frac{f''(8)(x-8)^2}{2!}
    +\frac{f''(8)(x-8)^3}{3!} \\
    &= 4
    +\frac{x-8}{3}
    -\frac{(x-8)^2}{72\cdot2!}
    +\frac{(x-8)^3}{432\cdot3!} \\
    &= 4
    +\frac{x-8}{3}
    -\frac{(x-8)^2}{144}
    +\frac{(x-8)^3}{2592}
\end{align*}
$$

### (ii) The Taylor polynomial of degree 2 of $f(x)=\sec x$ at $x=0$

$$
\begin{align*}
    f(x)=\sec x
    &\implies f'(x) = \sec x\tan x \\
    &\implies f''(x) = (\sec x\tan^2 x) + \sec^3x \\
\end{align*}
\\
\begin{darray}{cll}
    f(0) &= \sec 0 &= 1\\
    f'(0) &= \sec 0\tan 0 &= 0\\
    f''(0) &= (\sec 0\tan^2 0) + \sec^30 &= 1\\
\end{darray}
\\
\begin{align*}
    \therefore\sum_{n=0}^2\frac{f^{(n)}(x)}{n!}(x-0)^n
    &= f(0) + f'(0)x
    +\frac{f''(0)x^2}{2!} \\
    &= 1 + 0x + \frac{x^2}{2!} \\
    &= 1 + \frac{x^2}{2}
\end{align*}
$$

## 5\. Find the Taylor series expansion of the following functions using the formula $$\frac{1}{1-x}=\sum_{n=0}^\infty x^n$$

Identify their interval of convergence. You may need to use differentiation and integration of the Taylor series.

### (i) $\frac{1}{2+3x}$

$$
\begin{align*}
    \frac{1}{2+3x} &= \frac{1}{2+3(x-1)+3} \\
    &= \frac{1}{5+3(x-1)} \\
    &= \frac{1}{5}\cdot\frac{1}{1+3(x-1)} \\
    &= \frac{1}{5}\cdot\frac{1}{1-(-3(x-1))} \\
    &= \sum_{n=0}^\infty\frac{1}{5}(-3(x-1))^n
    ,\quad \left|-3(x-1)\right|<1 \\
    &= \sum_{n=0}^\infty\frac{1}{5}(-3)^n(x-1)^n
    ,\quad \left|x-1\right|<\frac{1}{3} \\
\end{align*}
$$

> ### (ii) $\frac{1}{(1-2x)^2}$

> ### (iii) $\ln(1+x)$
