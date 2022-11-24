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
$$

# Homework 8

**Mos Kullathon**
921425216

1\. Find the following limits

a. $\lim_{n\to\infty}\frac{(-1)^{n^3}}{n}$

By squeeze theorem:
$$
\lim_{n\to\infty}-\frac{1}{n} \le
\lim_{n\to\infty}\frac{(-1)^{n^3}}{n} \le
\lim_{n\to\infty}\frac{1}{n} \\
0 \le
\lim_{n\to\infty}\frac{(-1)^{n^3}}{n} \le
0 \\
\therefore \lim_{n\to\infty}\frac{(-1)^{n^3}}{n}=0.
$$


b. $\lim_{n\to\infty}\frac{n^2+1}{n+100}$

$$
\deg(n^2+1) > \deg(n+100)
\\
\therefore \lim_{n\to\infty}\frac{n^2+1}{n+100} = \infty
$$

c. $\lim_{n\to\infty}(\frac{1}{5e})^n$

$$
\lim_{n\to\infty}\(\frac{1}{5e}\)^n
= \lim_{n\to\infty}\frac{1^n}{5e^n}
= \frac{\displaystyle\lim_{n\to\infty}1^n}{\displaystyle\lim_{n\to\infty}5e^n}
= 0
$$

d. $\lim_{n\to\infty}\frac{n^{100}}{e^{0.01n}}$

The polynomial $n^{100}$ grows slower than the exponential $e^{0.01n}$.

$$
\therefore \lim_{n\to\infty}\frac{n^{100}}{e^{0.01n}} = 0
$$

e. $\lim_{n\to\infty}(1+\frac{1}{n})(2+\frac{\cos n}{3n^2})$

$$
\begin{align*}
    &\lim_{n\to\infty}\(1+\frac{1}{n}\)
    \(2+\frac{\cos n}{3n^2}\)
    \\
    &= \underbrace{\lim_{n\to\infty}\(1+\frac{1}{n}\)}
    _{1}
    \lim_{n\to\infty}\(2+\frac{\cos n}{3n^2}\) \\
    &=
    \lim_{n\to\infty}2+
    \lim_{n\to\infty}\frac{\cos n}{3n^2}
\end{align*}
$$

By squeeze theorem:
$$
    \lim_{n\to\infty}-\frac{1}{3n^2} \leq
    \lim_{n\to\infty}\frac{\cos n}{3n^2} \leq
    \lim_{n\to\infty}\frac{1}{3n^2} \\
    0 \leq
    \lim_{n\to\infty}\frac{\cos n}{3n^2} \leq
    0 \\
    \therefore  \lim_{n\to\infty}\frac{\cos n}{3n^2}=0.
$$

As such,
$$
\begin{align*}
    &\lim_{n\to\infty}\(1+\frac{1}{n}\)
    \(2+\frac{\cos n}{3n^2}\)
    \\
    &=
    \lim_{n\to\infty}2+0 \\
    &= 2.
\end{align*}
$$

f. $\lim_{n\to\infty}\frac{\ln\sqrt{n+1}}{n^2}$

$$
\begin{align*}
    \lim_{n\to\infty}\frac{\ln\sqrt{n+1}}{n^2}
    &= \lim_{n\to\infty}\frac{\frac{1}{2}\ln(n+1)}{n^2} \\
    &= \lim_{n\to\infty}\frac{\frac{1}{2(n+1)}}{2n} \\
    &= \lim_{n\to\infty}\frac{1}{4n(n+1)} \\
    &= 0
\end{align*}
$$

g. $\lim_{n\to\infty}\frac{n!}{n^n}$

$n^n$ grows faster than $n!$.
$$
\therefore\lim_{n\to\infty}\frac{n!}{n^n} =0
$$

h. $\lim_{n\to\infty}2^{1/n}$

$$
\lim_{n\to\infty}2^{1/n} = 2^{\lim_{n\to\infty}1/n} = 2^0 = 1
$$

i. $\lim_{n\to\infty}2^{n/(n^2+1)}$

$$
\lim_{n\to\infty}2^{n/(n^2+1)} = 2^{\lim_{n\to\infty}n/(n^2+1)}
=2^0=1
$$

j. $\lim_{n\to\infty}n^{1/n}$

$$
    \lim_{n\to\infty}n^{1/n}
    = \lim_{n\to\infty} e^{\frac{1}{n}\ln n}
    = e^{\lim_{n\to\infty}\frac{\ln n}{n}}
    = e^0
    = 1
$$

k. $\lim_{n\to\infty}(-1)^n \tan\frac{n}{n^5-1}$

By squeeze theorem:
$$
    \lim_{n\to\infty}-1\cdot
    \tan\frac{n}{n^5-1}
    \leq \lim_{n\to\infty}(-1)^n\tan\frac{n}{n^5-1}
    \leq \lim_{n\to\infty}1\cdot\tan\frac{n}{n^5-1}
    \\
    -1(0) \leq\lim_{n\to\infty}(-1)^n\tan\frac{n}{n^5-1}\leq 1(0)
    \\
    0\leq\lim_{n\to\infty}(-1)^n\tan\frac{n}{n^5-1}\leq 0 \\
    \therefore
    \lim_{n\to\infty}(-1)^n\tan\frac{n}{n^5-1} = 0.
$$

2\. Evaluate the following infinite series

(i) $\sum_{n=1}^\infty(\frac{2}{5})^n$

The common ratio $r$ is
$$
    r=\frac{\(\frac{2}{5}\)^2}{\frac{2}{5}}
    =\frac{\(\frac{2}{5}\)^3}{\(\frac{2}{5}\)^2}
    =\frac{\(\frac{2}{5}\)^n}{\(\frac{2}{5}\)^{n-1}}
    =\frac{2}{5}.
$$
Since $|r|<1$, the series converges.

Where the initial term $a=\frac{2}{5}$, using the geometric sum formula yields:

$$
\begin{align*}
    \sum_{n=1}^\infty\(\frac{2}{5}\)^n&= \frac{\frac{2}{5}}{1-\frac{2}{5}} \\
    &= \frac{2}{3}
\end{align*}
$$

(ii) $\sum_{n=2}^\infty(-1)^n\frac{5}{7^n}$

The common ratio $r$ is
$$
    r=\frac{\frac{5(-1)^3}{7^3}}{\frac{5(-1)^2}{7^2}}
    =\frac{\frac{5(-1)^4}{7^4}}{\frac{5(-1)^3}{7^3}}
    =\frac{\frac{5(-1)^n}{7^n}}{\frac{5(-1)^{n-1}}{7^{n-1}}}
    =-\frac{1}{7}.
$$

Since $|r|<1$, the series converges.

Where the initial term $a=\frac{5(-1)^2}{7^2}=\frac{5}{49}$, using the geometric sum formula yields:

$$
\begin{align*}
    \sum_{n=2}^\infty(-1)^n\frac{5}{7^n}
    &= \frac{\frac{5}{49}}{1+\frac{1}{7}} \\
    &= \frac{5}{56}
\end{align*}
$$


(iii) $4 + \frac{3}{10} + \frac{3}{10^2} + \frac{3}{10^3} + \cdots$

$$
\begin{align*}
    &4 + \frac{3}{10} + \frac{3}{10^2} + \frac{3}{10^3} + \cdots \\
    &= 4 + \sum_{n=1}^\infty\frac{3}{10^n}
\end{align*}
$$

For $\displaystyle\sum_{n=1}^\infty\frac{3}{10^n}$:

The common ratio $r$ is
$$
    r=\frac{\frac{3}{10^2}}{\frac{3}{10}}
    =\frac{\frac{3}{10^3}}{\frac{3}{10^2}}
    =\frac{\frac{3}{10^n}}{\frac{3}{10^{n-1}}}
    =\frac{1}{10}
$$

Since $|r|<1$, the series converges.

Where the initial term $a=\frac{3}{10}$, using the geometric sum formula yields:
$$
\begin{align*}
    \sum_{n=1}^\infty\frac{3}{10^n}
    &= \frac{\frac{3}{10}}{1-\frac{1}{10}} \\
    &= \frac{1}{3}. \\
    \therefore 4+\sum_{n=1}^\infty\frac{3}{10^n}
    &= 4+\frac{1}{3} \\
    &= \frac{13}{3}
\end{align*}
$$

(iv) $\sum_{n=1}^\infty(\ln2)^n,\quad\sum_{n=1}^\infty(\ln3)^n$ (Be careful of the convergence)

For $\displaystyle\sum_{n=1}^\infty(\ln2)^n$:

The common ratio $r$ is
$$
    r=\frac{\ln^22}{\ln2}=\frac{\ln^32}{\ln^22}
    =\frac{\ln^n2}{\ln^{n-1}2} = \ln2 \approx 0.69.
$$

Since $|r|<1$, the series converges.

Where the initial term $a=\ln2$, using the geometric sum formula yields:
$$
\begin{align*}
    \sum_{n=1}^\infty(\ln2)^n
    &= \frac{\ln2}{1-\ln2} \approx 2.26.
\end{align*}
$$

For $\displaystyle\sum_{n=1}^\infty(\ln3)^n$:

The common ratio $r$ is
$$
    r=\frac{\ln^23}{\ln2}=\frac{\ln^33}{\ln^23}
    =\frac{\ln^n3}{\ln^{n-1}3} = \ln3 \approx 1.10.
$$

Since $|r|>1$, the series diverges.
