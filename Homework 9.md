---
print_background: true
export_on_save:
    html: true
puppeteer:
    format: "Letter"
    timeout: 3000
---

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

# Homework 9

**Mos Kullathon**
921425216

Determine if the following series is convergent or divergent. You can use any tests you have learnt so far.

(a) $\sum_{n=1}^\infty \sin(n\frac{\pi}{2})$

$\displaystyle\lim_{n\to\infty}\sin\(n\frac{\pi}{2}\)$ does not exist. By divergence test, the series diverges.

(b) $\sum_{n=2}^\infty \frac{1}{n(\ln n)^2}$

Let $\displaystyle f(x) = \frac{1}{x\ln^2x}$.

Since $\displaystyle f(x)=\frac{1}{x\ln^2x}>0$ and $x\ln^2x$ is monotonically increasing for $x\ge2$, so its reciprocal $\displaystyle f(x) = \frac{1}{x\ln^2x}$ is decreasing for $x\ge2$.

By integral test:
$$
\int_2^\infty\frac{1}{x(\ln x)^2}\dd x
= \lim_{n\to\infty}\int_2^n \frac{1}{x(\ln x)^2}\dd x
\\
\begin{darray}{cc}
    u = \ln x &\implies& \dd u = \frac{1}{x}\dd x
    \\
    &\iff& \dd x = x\dd u
    \\
    x = 2 &\implies& u = \ln 2
    \\
    x = n &\implies& u = \ln n
\end{darray}
\\
\begin{align*}
    \lim_{n\to\infty}\int_{\ln2}^{\ln n} \frac{1}{x(\ln x)^2}\dd x
    &= \lim_{n\to\infty}\int_{\ln2}^{\ln n} \frac{x\dd u}{x u^2} \\
    &= \lim_{n\to\infty}\int_{\ln2}^{\ln n} u^{-2}\dd u \\
    &= \lim_{n\to\infty}\[-\frac{1}{u}\]_{\ln2}^{\ln n} \\
    &= \lim_{n\to\infty}-\frac{1}{\ln n} + \frac{1}{\ln 2}
    \\
    &= \frac{1}{\ln 2}
\end{align*}
$$

Since $\displaystyle\int_2^\infty\frac{1}{x(\ln x)^2}\dd x = \frac{1}{\ln 2} < \infty$, the series is convergent.

(c\) $\sum_{n=1}^\infty \frac{1}{n^{3/2}+1}$

Let $\displaystyle a_n = \frac{1}{n^{3/2}+1}$ and $\displaystyle b_n = \frac{1}{n^{3/2}}$.

Then,
$$
\frac{a_n}{b_n} = \frac{n^{3/2}}{n^{3/2}+1}. \\
\therefore \lim_{n\to\infty}\frac{a_n}{b_n}=1
$$

By limit comparison test, $\displaystyle\sum_{n=1}^\infty a_n$ and $\displaystyle\sum_{n=1}^\infty b_n$ will either converge or diverge together.

Let $\displaystyle f(x)=\frac{1}{x^{3/2}}$.

Since $\displaystyle f(x)>0$ and $\displaystyle f'(x)=-\frac{3}{2x^{5/2}} < 0$ for all $x\ge1$, we apply the integral test.


$$
\begin{align*}
    \int_1^\infty\frac{1}{x^{3/2}} \dd x
    &= \lim_{n\to\infty}\int_1^n x^{-3/2}\dd x \\
    &= \lim_{n\to\infty}\[\frac{x^{-1/2}}{-1/2}\]_1^n \\
    &= \lim_{n\to\infty}\[-\frac{2}{\sqrt{x}}\]_1^n \\
    &= \lim_{n\to\infty}-\frac{2}{\sqrt{n}} + 2 \\
    &= 2
\end{align*}
$$

By integral test, $\displaystyle \sum_{n=1}^\infty \frac{1}{n^{3/2}}$ is convergent. Subsequently, by the limit comparison test, the series $\displaystyle\sum_{n=1}^\infty \frac{1}{n^{3/2}+1}$ must also be convergent.

(d) $\sum_{n=1}^\infty \frac{\sqrt{n}}{(n+1)^2}$

Let $\displaystyle a_n = \frac{\sqrt{n}}{(n+1)^2} = \frac{n^{1/2}}{n^2+2n+1}$ and $\displaystyle b_n = \frac{1}{n^{3/2}}$.

Then,
$$
\frac{a_n}{b_n} = \frac{n^2}{n^2+2n+1}. \\
\therefore \lim_{n\to\infty}\frac{a_n}{b_n}=1
$$

Since $\displaystyle b_n = \frac{1}{n^{3/2}}$ is nonnegative and decreasing, we apply the integral test.

From (c\), we concluded that $\displaystyle \sum_{n=1}^\infty\frac{1}{n^{3/2}}$ is convergent by integral test. Subsequently, by the limit comparison test, the series $\displaystyle\sum_{n=1}^\infty \frac{\sqrt{n}}{(n+1)^2}$ must also be convergent.

(e) $\sum_{n=2}^\infty \frac{(\ln n)^2}{n}$

Since
$$
\ln n = 1 \iff n =e,
$$

and
$$
\frac{\dd}{\dd n}\ln n = \frac{1}{n} > 0, \forall n>3
$$

we have that
$$
\ln n > 1 ,\forall n>3.
$$

As such, for all values $n>3$:
$$
\ln n > 1 \\
\iff \ln^2n > 1 \\
\iff \frac{\ln^2 n}{n} > \frac{1}{n}.
$$

Since $\displaystyle\sum_{n=2}^\infty\frac{1}{n}$ is divergent, by comparison test $\displaystyle\sum_{n=2}^\infty\frac{(\ln n)^2}{n}$ must also be divergent.

(f) $\sum_{n=1}^\infty \frac{n^2}{(n^2+10)^2}$

Let $\displaystyle a_n = \frac{n^2}{(n^2+10)^2} = \frac{n^2}{n^4 +20n^2 + 100}$ and $\displaystyle b_n =\frac{1}{n^2}$.

Then,
$$
\frac{a_n}{b_n} = \frac{n^4}{n^4+20n^2+100} \\
\therefore\lim_{n\to\infty}\frac{a_n}{b_n} = 1
$$

Since $\displaystyle \sum_{n=1}^\infty \frac{1}{n^2}$ converges, then by limit comparison $\displaystyle \sum_{n=1}^\infty \frac{n^2}{(n^2+10)^2}$ also converges.

(g) $\sum_{n=1}^\infty \frac{n\ln n}{n^3+2}$

For sufficiently large $n$,
$$
\frac{n\ln n}{n^3+2}\approx\frac{n}{n^3+2}
$$

Let $\displaystyle a_n = \frac{n}{n^3+2}$ and $\displaystyle b_n = \frac{n^\epsilon}{n^2}=\frac{1}{n^{2-\epsilon}}$ for some small $\epsilon>0$.

Then,
$$
\frac{a_n}{b_n} = \frac{n^{3-\epsilon}}{n^3+2} \\
\therefore \lim_{n\to\infty}\frac{a_n}{b_n}=0
$$

For small values of $\epsilon>0$, the series $\displaystyle\sum_{n=1}^\infty\frac{1}{n^{2-\epsilon}}$ converges. As such, by limit comparison test $\displaystyle\sum_{n=1}^\infty \frac{n\ln n}{n^3+2}$ converges.

(h) $\sum_{n=2}^\infty \frac{1}{n^2(\ln n)^2}$

$$
\ln e = 1 \implies \ln n > 1 ,\forall n>3
$$

So for $n>3$:
$$
\ln n > 1 \\
\iff \ln^2 n > 1 \\
\iff n^2\ln^2n > n^2 \\
\iff \frac{1}{n^2\ln^2n} < \frac{1}{n^2}
$$

Since $\displaystyle\sum_{n=2}^\infty\frac{1}{n^2}$ converges, by comparison test $\displaystyle\sum_{n=2}^\infty\frac{1}{n^2(\ln n)^2}$ also converges.


## Section 5.5

State whether each of the following series converges absolutely, conditionally, or not at all.

(251) $\displaystyle \sum_{n=1}^\infty (-1)^{n+1}\frac{\sqrt{n}+1}{\sqrt{n}+3}$

Let $\displaystyle a_n = \frac{\sqrt{n}+1}{\sqrt{n}+3}$.

$$
\lim_{n\to\infty}a_n = \frac{\sqrt{n}+1}{\sqrt{n}+3}
= 1 \neq 0
$$

By divergence test, the series diverges.

(252) $\displaystyle \sum_{n=1}^\infty (-1)^{n+1}\frac{1}{\sqrt{n+3}}$

Let $\displaystyle a_n = \frac{1}{\sqrt{n+3}}$.

Since $\sqrt{n+3}$ is monotonically increasing, its reciprocal $\displaystyle a_n=\frac{1}{\sqrt{n+3}}$ must subsequently be decreasing.

And
$$
\lim_{n\to\infty}a_n
=\lim_{n\to\infty}\frac{1}{\sqrt{n+3}} = 0.
$$

By alternating series test, $\displaystyle \sum_{n=1}^\infty (-1)^{n+1}\frac{1}{\sqrt{n+3}}$ is convergent.

**Testing for absolute convergence**

$$
\sum_{n=1}^\infty \left|(-1)^{n+1}\frac{1}{\sqrt{n+3}}\right|
= \sum_{n=1}^\infty \frac{1}{\sqrt{n+3}}
$$

Let $\displaystyle f(x) = \frac{1}{\sqrt{x+3}}$.

We note that $f(x) >0$ and $f'(x)<0$ for $x\in[1,\infty)$.

$$
\begin{align*}
    \int_1^\infty\frac{1}{\sqrt{x+3}}\dd x
    &= \lim_{n\to\infty}\int_1^n(x+3)^{-1/2}\dd x \\
    &= \lim_{n\to\infty}\[2\sqrt{x+3}\]_1^n \\
    &= \lim_{n\to\infty} 2\sqrt{n+3}-4 \\
    &= \infty
\end{align*}
$$

By integral test, we find that the sum of the absolute values of the terms do not converge.

As such, we conclude that $\displaystyle \sum_{n=1}^\infty (-1)^{n+1}\frac{1}{\sqrt{n+3}}$ exhibits conditional convergence.

(260) $\displaystyle \sum_{n=1}^\infty (-1)^{n+1}\sin^2(1/n)$

Since $\displaystyle\sin x\le x$ for $x>0$. Then, where $a_n=\sin^2(1/n)$, we have that $0\le a_{n+1}\le a_n$ for $n\ge1$.

$$
\lim_{n\to\infty}\sin^2(1/n)
=\sin^2\(\lim_{n\to\infty}\frac{1}{n}\)
=\sin^20=0
$$

By alternating series test, the series is convergent.

**Testing for absolute convergence**

$$
\sum_{n=1}^\infty\left|(-1)^{n+1}\sin^2(1/n)\right|
=\sum_{n=1}^\infty \sin^2(1/n)
$$

For $n>0$:
$$
\sin n \le n \\
\iff \sin\frac{1}{n} \le \frac{1}{n} \\
\iff \sin^2\frac{1}{n} \le \frac{1}{n^2}
$$

Since $\displaystyle\sum_{n=1}^\infty\frac{1}{n^2}$ converges, by comparison test $\displaystyle\sum_{n=1}^\infty\sin^2\frac{1}{n}$ also converges. As such, we conclude that $\displaystyle\sum_{n=1}^\infty(-1)^{n+1}\sin^2(1/n)$ exhibits absolute convergence.

(261) $\displaystyle \sum_{n=1}^\infty (-1)^{n+1}\cos^2(1/n)$

$$
\lim_{n\to\infty}\cos^2(1/n)
=\cos^2\(\lim_{n\to\infty}\frac{1}{n}\)
=\cos^20
=1\neq0
$$

By divergence test, the series is divergent.


