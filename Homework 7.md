---
print_background: true
export_on_save:
    html: true
puppeteer:
    format: "Letter"
    timeout: 3000
---

# Homework 7

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
    \gdef\arraystretch{2em}
$$

**Mos Kullathon**
921425216

## Section 3.4

Express the rational function as a sum or difference of two simpler rational expressions.

### (183) $\displaystyle\frac{x^2+1}{x(x+1)(x+2)}$

$$
\begin{align*}
    \frac{x^2+1}{x(x+1)(x+2)} &= \frac{A}{x} + \frac{B}{x+1} + \frac{C}{x+2};\quad A,B,C\in\R
    \\
    x^2 + 1 &= A(x+1)(x+2) + Bx(x+2) + Cx(x+1)
\end{align*}
$$

Let $x=0$.

$$
    0^2 + 1 = A(0+1)(0+2) \\
    1 = 2A \\
    \therefore A = \frac{1}{2}
$$

Let $x = -1$.

$$
    (-1)^2 + 1 =  B(-1)(-1+2) \\
    2 = -B \\
    \therefore B = -2
$$

Let $x = -2$.

$$
    (-2)^2 + 1 = C(-2)(-2+1) \\
    5 = 2C \\
    \therefore C = \frac{5}{2}
$$

$$
    \therefore \frac{x^2+1}{x(x+1)(x+2)} = \frac{1}{2x}
    -\frac{2}{x+1}
    +\frac{5}{2(x+2)}
$$

### (185) $\displaystyle\frac{3x+1}{x^2}$

$$
\begin{align*}
    \frac{3x+1}{x^2} &= \frac{A}{x} + \frac{B}{x^2};\quad A,B\in\R
    \\
    3x+1 &= Ax + B
\end{align*}
$$

By comparing coefficients, $A = 3, B= 1$.

$$
\therefore\frac{3x+1}{x^2} = \frac{3}{x} + \frac{1}{x^2}
$$

### (187) $\displaystyle\frac{2x^4}{x^2-2x}$

$$
\gdef\longdiv#1#2{
    \mathstrut#1\kern.25em\smash{\raisebox.3ex\hbox{)\kern.1em}}
    \mkern-8mu\overline{\enspace\mathstrut#2}
    }
\def\arraystretch{1em}
\begin{array}{l}
    \phantom{x^2-2x\;\;\;} 2x^2+4x+8 \\
    \longdiv{x^2-2x}{2x^4} \\
    \phantom{x^2-2x\;\;\;} \underline{2x^4-4x^3} \\
    \phantom{x^2-2x\;\;\;2x^4-} 4x^3 \\
    \phantom{x^2-2x\;\;\;2x^4-} \underline{4x^3-8x^2} \\
    \phantom{x^2-2x\;\;\;2x^4-4x^3-} 8x^2 \\
    \phantom{x^2-2x\;\;\;2x^4-4x^3-} \underline{8x^2-16x} \\
    \phantom{x^2-2x\;\;\;2x^4-4x^3-8x^2-} 16x \\
\end{array}
$$

$$
\begin{align*}
    \therefore \frac{2x^4}{x^2-2x} &=
    2x^2+4x+8+\frac{16x}{x^2-2x} \\
    &= 2x^2+4x+8+\frac{16x}{x(x-2)} \\
    &= 2x^2+4x+8+\frac{16}{x-2}
\end{align*}
$$

### (189) $\displaystyle\frac{1}{x^2(x-1)}$

$$
\begin{align*}
    \frac{1}{x^2(x-1)} &= \frac{A}{x} + \frac{B}{x^2} + \frac{C}{x-1};\quad A,B,C\in\R
    \\
    1 &= Ax(x-1) + B(x-1) + Cx^2
\end{align*}
$$

Let $x=0$.

$$
1 = B(0-1) \\
1 = -B \\
\therefore B = -1
$$

Let $x=1$.

$$
1 = C(1^2) \\
\therefore C = 1
$$

Let $x=2$ and substitute $B=-1, C=1$.

$$
1 = A(2)(2-1) -(2-1) + (2^2) \\
1 = 2A-1+4 \\
\therefore A = -1
$$

$$
\therefore\frac{1}{x^2(x-1)} = -\frac{1}{x}-\frac{1}{x^2}+\frac{1}{x-1}
$$

### (192) $\displaystyle\frac{1}{x^4-1} = \frac{1}{(x+1)(x-1)(x^2+1)}$

$$
\begin{align*}
    \frac{1}{(x+1)(x-1)(x^2+1)} &= \frac{A}{x+1}+\frac{B}{x-1}+\frac{C}{x^2+1};\quad A,B,C\in\R
    \\
    1 &= A(x-1)(x^2+1) + B(x+1)(x^2+1) + C(x+1)(x-1)
\end{align*}
$$

Let $x=-1$.

$$
1 = A(-1-1)(-1^2+1) \\
1 = -4A \\
\therefore A =-\frac{1}{4}
$$

Let $x=1$.

$$
1 = B(1+1)(1^2+1) \\
1 = 4B \\
\therefore B = \frac{1}{4}
$$

Let $x=0$ and substitute $A=-\frac{1}{4},B=\frac{1}{4}$.

$$
1 = A(0-1)(0^2+1) + B(0+1)(0^2+1) + C(0+1)(0-1) \\
1 = -A+B-C \\
1 = \frac{1}{4}+\frac{1}{4}-C \\
\frac{1}{2} = -C \\
\therefore C = -\frac{1}{2}
$$

$$
\begin{align*}
    \therefore \frac{1}{x^4-1}
    &= \frac{1}{(x+1)(x-1)(x^2+1)} \\
    &= -\frac{1}{4(x+1)} + \frac{1}{4(x-1)} - \frac{1}{2(x^2 + 1)}
\end{align*}
$$

## Section 3.7

Determine whether the improper integrals converge or diverge. If possible, determine the value of the integrals that converge.

### (359) $\displaystyle\int_{-\infty}^\infty\frac{1}{x^2+1}\dd x$

$$
    \int_{-\infty}^\infty\frac{1}{x^2+1}\dd x
    = \int_{-\infty}^0\frac{1}{x^2+1}\dd x
    + \int_{0}^\infty\frac{1}{x^2+1}\dd x
$$

$$
\begin{align*}
    \int_{-\infty}^0\frac{1}{x^2+1}\dd x
    &= \lim_{n\to-\infty}\int_{n}^0\frac{1}{x^2+1}\dd x \\
    &= \lim_{n\to-\infty}\bigg[\tan^{-1}x\bigg]_n^0 \\
    &= \lim_{n\to-\infty}-\tan^{-1}n \\
    &= \frac{\pi}{2} \\
    \int_{0}^\infty\frac{1}{x^2+1}\dd x
    &= \lim_{n\to\infty}\int_0^n\frac{1}{x^2+1}\dd x \\
    &= \lim_{n\to\infty}\bigg[\tan^{-1}x\bigg]_0^n \\
    &= \lim_{n\to\infty}\tan^{-1}n \\
    &= \frac{\pi}{2}
\end{align*}
\\
\begin{align*}
    \therefore
    \int_{-\infty}^\infty\frac{1}{x^2+1}\dd x
    &= \int_{-\infty}^0\frac{1}{x^2+1}\dd x
    + \int_{0}^\infty\frac{1}{x^2+1}\dd x \\
    &= \frac{\pi}{2} + \frac{\pi}{2} \\
    &= \pi
\end{align*}
$$

### (362) $\displaystyle\int_0^\infty e^{-x}\dd x$

$$
\begin{align*}
    \int_0^\infty e^{-x}\dd x
    &= \lim_{n\to\infty} \int_0^n e^{-x}\dd x \\
    &= \lim_{n\to\infty} \bigg[-e^{-x}\bigg]_0^n \\
    &= \lim_{n\to\infty} -e^{-n}-(-e^0) \\
    &= \lim_{n\to\infty} -\frac{1}{e^n} + \lim_{n\to\infty} 1 \\
    &= 0+1 \\
    &= 1
\end{align*}
$$

### (365) $\displaystyle\int_0^1\frac{\dd x}{\sqrt[3]{x}}$

$$
\begin{align*}
    \int_0^1\frac{\dd x}{\sqrt[3]{x}}
    &= \lim_{n\to0}\int_n^1x^{-\frac{1}{3}}\dd x \\
    &= \lim_{n\to0}\bigg[\frac{x^\frac{2}{3}}{2/3}\bigg]_n^1 \\
    &= \lim_{n\to0}\bigg[\frac{3x^{2/3}}{2}\bigg]_n^1 \\
    &= \lim_{n\to0}\frac{3(1)^{2/3}}{2} - \frac{3n^{2/3}}{2} \\
    &= \frac{3}{2}
\end{align*}
$$

Evaluate the integrals. If the integral diverges, answer “diverges.”

### (374) $\displaystyle\int_1^\infty\frac{\dd x}{x^e}$

$$
\begin{align*}
    \int_1^\infty\frac{\dd x}{x^e}
    &= \lim_{n\to\infty} \int_1^n x^{-e} \dd x \\
    &= \lim_{n\to\infty} \bigg[\frac{x^{1-e}}{1-e}\bigg]_1^n \\
    &= \lim_{n\to\infty} \frac{n^{1-e}}{1-e}
        - \frac{1^{1-e}}{1-e}\\
    &= \lim_{n\to\infty} \frac{1}{1-e(n^{e-1})}
        - \frac{1^{1-e}}{1-e}\\
    &= 0 - \frac{1}{1-e} \\
    &= \frac{1}{e-1}
\end{align*}
$$

### (375) $\displaystyle\int_0^1\frac{\dd x}{x^\pi}$

$$
\begin{align*}
    \int_0^1\frac{\dd x}{x^\pi} &=
    \lim_{n\to0}\int_n^1 x^{-\pi} \dd x\\
    &= \lim_{n\to0}\bigg[\frac{x^{1-\pi}}{1-\pi}\bigg]_n^1 \\
    &= \lim_{n\to0}\frac{1}{1-\pi} - \frac{0^{1-\pi}}{1-\pi} \\
    &= \infty
\end{align*}
$$


Therefore, $\displaystyle\int_0^1\frac{\dd x}{x^\pi}$ diverges.

### (382) $\displaystyle\int_0^\infty xe^{-x}\dd x$

$$
\int_0^\infty xe^{-x}\dd x =
\lim_{n\to\infty}\int_0^n xe^{-x}\dd x
\\
\begin{darray}{cc}
    u = x \implies u' = 1 \\
    v' = e^{-x} \implies v = -e^{-x}
\end{darray}
\\
\begin{align*}
    \int_0^n xe^{-x}\dd x &=
    \bigg[uv\bigg]_0^n - \int_0^n vu'\dd x \\
    &=  \bigg[-xe^{-x}\bigg]_0^n + \int_0^n e^{-x}\dd x \\
    &= -ne^{-n} + \bigg[-e^{-x}\bigg]_0^n \\
    &= -ne^{-n} -e^{-n} + 1 \\
    &= -\frac{n}{e^n} - \frac{1}{e^n} + 1
\end{align*}
$$

By L’Hôpital’s:

$$
\lim_{n\to\infty}-\frac{n}{e^n}
= \lim_{n\to\infty}-\frac{1}{e^n}
= 0.
$$

$$
\begin{align*}
    \therefore \int_0^\infty xe^{-x}\dd x
    &= \lim_{n\to\infty} -\frac{n}{e^n} - \frac{1}{e^n} + 1 \\
    &= -0-0+1 \\
    &= 1
\end{align*}
$$

### (394) Find the area of the region in the first quadrant between the curve $y=e^{-6x}$ and the *x*-axis.

$$
\begin{align*}
    A &= \int_0^\infty e^{-6x}\dd x \\
    &= \lim_{n\to\infty}\int_0^n e^{-6x}\dd x \\
    &= \lim_{n\to\infty}\bigg[-\frac{e^{-6x}}{6}\bigg]_0^n \\
    &= \lim_{n\to\infty} -\frac{e^{-6n}}{6} + \frac{1}{6} \\
    &= -0+\frac{1}{6} \\
    &= \frac{1}{6}
\end{align*}
$$
