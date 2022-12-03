---
print_background: true
export_on_save:
    html: true
puppeteer:
    format: "Letter"
    timeout: 3000
---

# Homework 6

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

**Mos Kullathon**
921425216

## 1\. Let $I_n = \int\sec^nx\dd x$. Derive the following reduction formula for $I_n$. $$I_n = \frac{\tan x\sec^{n-2}x}{n-1}+\frac{n-2}{n-1}I_{n-2}.$$

$$
\begin{align*}
    I_n &= \int\sec^nx\dd x
    \\
    &= \int\sec^{n-2}x\sec^nx\dd x
\end{align*}
\\
\begin{align*}
    u = \sec^{n-2}x &\implies& u' &= (n-2)\sec^{n-3}x\sec x\tan x
    \\
    &&&= (n-2)\sec^{n-2}x\tan x
    \\
    v' = \sec^2x &\implies& v &= \tan x
\end{align*}
\\
\begin{align*}
    I_n &= \int\sec^{n-2}x\sec^nx\dd x
    \\
    &= uv - \int vu'\dd x
    \\
    &= \tan x\sec^{n-2} (x) - (n-2)\int\sec^{n-2}x\tan^2x\dd x
    \\
    &= \tan x\sec^{n-2} (x) - (n-2)\int\sec^{n-2}x(\sec^2(x) - 1)\dd x
    \\
    &= \tan x\sec^{n-2} (x) - (n-2)\int\sec^n(x) - \sec^{n-2}\dd x
    \\
    &= \tan x\sec^{n-2} (x) - (n-2)
    \underbrace{\int\sec^n x\dd x}_{I_n}
    + (n-2)
    \underbrace{\int\sec^{n-2}x\dd x}_{I_{n-2}}
    \\
    &= \tan x\sec^{n-2} (x) - (n-2)I_n
    + (n-2)I_{n-2}
\end{align*}
\\
\begin{align*}
    I_n + (n-2)I_n &= \tan x\sec^{n-2}(x) + (n-2)I_{n-2}
    \\
    I_n(1+(n-2))&= \tan x\sec^{n-2}(x)+ (n-2)I_{n-2}
    \\
    I_n &= \frac{\tan x\sec^{n-2}(x)+ (n-2)I_{n-2}}{1+(n-2)}
    \\
    &= \frac{\tan x\sec^{n-2}(x)+ (n-2)I_{n-2}}{n-1}
    \\
    &= \frac{\tan x\sec^{n-2}x}{n-1} + \frac{n-2}{n-1}I_{n-2}
\end{align*}
$$


## 2\. Use the formula above to find $\int\sec^5x\dd x$.

$$
\begin{align*}
    I_5 &= \int\sec^5\dd x
    \\
    &= \frac{\tan x\sec^{5-2}x}{5-1}+\frac{5-2}{5-1}I_{5-2}
    \\
    &= \frac{\tan x\sec^{3}x}{4}+\frac{3}{4}I_{3}
    \\
    &= \frac{\tan x\sec^{3}x}{4}+\frac{3}{4}
    \(\frac{\tan x\sec^{3-2}x}{3-1}+\frac{3-2}{3-1}I_{3-2}\)
    \\
    &= \frac{\tan x\sec^{3}x}{4}+\frac{3}{4}
    \(\frac{\tan x\sec x}{2}+\frac{1}{2}I_{1}\)
    \\
    &= \frac{\tan x\sec^{3}x}{4}+\frac{3}{4}
    \(\frac{\tan x\sec x}{2}+\frac{1}{2}\int\sec x\dd x\)
    \\
    &= \frac{\tan x\sec^{3}x}{4}+\frac{3}{4}
    \(\frac{\tan x\sec x}{2}+\frac{1}{2}
    \ln|\tan(x) + \sec(x)|\) + C
    \\
    &= \frac{\tan x\sec^{3}x}{4}+\frac{3}{8}
    \(\tan x\sec x+\ln|\tan(x) + \sec(x)|\) + C
    \\
    &= \frac{1}{8}(2\tan x\sec^3 x +
    3(\tan x\sec x + \ln|\tan(x) + \sec (x)|)) + C
\end{align*}
$$

## Book section 3.1

Find the integral by using the simplest method. Not all problems require integration by parts.

### (23) $\displaystyle\int\sin(\ln2x)\dd x$

$$
\begin{darray}{cc}
    u = \ln 2x &\implies& \dd u = \frac{1}{x}\dd x
    \\
    &\iff& \dd x = x\dd u
    \\
    &\iff& e^u = 2x
    \\
    &\iff& x = \frac{e^u}{2}
\end{darray}
\\
\begin{align*}
    \int\sin(\ln2x)\dd x &= \int\sin(u)\frac{e^u}{2}\dd u
    \\
    &= \frac{1}{2}\int e^u\sin u\dd u
\end{align*}
\\
\begin{darray}{cc}
    p = \sin u &\implies& p' = \cos u
    \\
    q' = e^u &\implies& q = e^u
\end{darray}
\\
\begin{align*}
    \int e^u\sin u\dd u &= pq - \int qp'\dd u
    \\
    &= e^u\sin u - \int e^u\cos u \dd u
\end{align*}
\\
\begin{darray}{cc}
    r = \cos u &\implies& r' = -\sin u
    \\
    s' = e^u &\implies& s = e^u
\end{darray}
\\
\begin{align*}
    \int e^u\cos u\dd u &= rs - \int sr'\dd u
    \\
    &= e^u\cos u + \int e^u\sin u\dd u
\end{align*}
\\
\begin{align*}
    \therefore \int e^u\sin u\dd u
    &= e^u \sin u - \int e^u\cos\dd u
    \\
    &= e^u \sin u - e^u\cos u - \int e^u\sin u \dd u
    \\
    2\int e^u\sin u\dd u &= e^u\sin u - e^u\cos u + C
    \\
    \int e^u\sin u\dd u &= \frac{1}{2}(e^u\sin u - e^u\cos u) + C
\end{align*}
\\
\begin{align*}
    \therefore
    \int\sin(\ln2x)\dd x &= \frac{1}{2}\int e^u\sin u\dd u
    \\
    &= \frac{1}{4}(e^u\sin u - e^u\cos u) + C
    \\
    &= \frac{1}{4}(2x\sin(\ln2x) - 2x\cos(\ln2x)) + C
    \\
    &= \frac{1}{2}x(\sin(\ln2x) - \cos(\ln2x)) + C
\end{align*}
$$

### (25) $\displaystyle\int(\ln x)^2\dd x$

$$
\begin{darray}{cc}
    u = \ln^2 x &\implies& u' = \frac{2\ln x}{x}
    \\
    v' = 1 &\implies& v = x
\end{darray}
\\
\begin{align*}
    \int(\ln x)^2\dd x &= uv - \int vu'\dd x
    \\
    &= x\ln^2 x - \int\frac{2\cancel{x}\ln x}{\cancel{x}}\dd x
    \\
    &= x\ln^2 x - 2\int\ln x\dd x
\end{align*}
\\
\begin{darray}{cc}
    p = \ln x &\implies& p' = \frac{1}{x}
    \\
    q' = 1 &\implies& q = x
\end{darray}
\\
\begin{align*}
    \int\ln x\dd x &= pq - \int qp'\dd x
    \\
    &= x\ln x - \int\frac{x}{x}\dd x
    \\
    &= x\ln x - x + C
\end{align*}
\\
\begin{align*}
    \int(\ln x)^2\dd x &= x\ln^2x - 2\int\ln x\dd x
    \\
    &= x\ln^2(x) - 2(x\ln(x) - x) + C
    \\
    &= x\ln^2(x) - 2x\ln(x) + 2x + C
    \\
    &= x(\ln^2(x) - 2\ln(x) + 2) + C
\end{align*}
$$

### (28) $\displaystyle\int\sin^{-1}x\dd x$

$$
\begin{darray}{cc}
    u = \sin^{-1}x &\implies& u' = \frac{1}{\sqrt{1-x^2}}
    \\
    v' = 1 &\implies& v = x
\end{darray}
\\
\begin{align*}
    \int\sin^{-1}\dd x &= uv - \int vu'\dd x
    \\
    &= x\sin^{-1}(x) - \int \frac{x}{\sqrt{1-x^2}}\dd x
\end{align*}
\\
\begin{darray}{cc}
    p = 1-x^2 &\implies& \dd p = -2x\dd x
    \\
    &\iff& \dd x = -\frac{1}{2x}\dd p
\end{darray}
\\
\begin{align*}
    \int\frac{x}{\sqrt{1-x^2}}\dd x
    &= \int\frac{\cancel{x}}{\sqrt{p}}\(-\frac{1}{2\cancel{x}}\dd p\)
    \\
    &= -\frac{1}{2}\int\frac{1}{\sqrt{p}}\dd p
    \\
    &= -\frac{1}{2}\int p^{-1/2}\dd p
    \\
    &= -\frac{1}{2}\cdot\frac{p^{1/2}}{1/2} + C
    \\
    &= -\sqrt{p} + C
    \\
    &= -\sqrt{1-x^2} + C
\end{align*}
\\
\begin{align*}
    \therefore \int\sin^{-1}\dd x
    &= x\sin^{-1}(x) - \int\frac{x}{\sqrt{1-x^2}}\dd x
    \\
    &= x\sin^{-1}(x) - (-\sqrt{1-x^2}) + C
    \\
    &= \sqrt{1-x^2} + x\sin^{-1}(x) + C
\end{align*}
$$


### (36) $\displaystyle\int x\sec^2x\dd x$

$$
\begin{darray}{cc}
    u = x &\implies& u' = 1
    \\
    v' = \sec^2x &\implies& v = \tan x
\end{darray}
\\
\begin{align*}
    \int x\sec^2x\dd x &= uv - \int vu'\dd x
    \\
    &= x\tan x - \int\tan x \dd x
    \\
    &= x\tan x - \int\frac{\sin x}{\cos x}\dd x
\end{align*}
\\
\begin{darray}{cc}
    p = \cos x &\implies& \dd p = -\sin x\dd x
    \\
    &\iff& \dd x = \frac{\dd p}{-\sin x}
\end{darray}
\\
\begin{align*}
    \int\frac{\sin x}{\cos x}\dd x
    &= \int\frac{\cancel{\sin x}}{p}\cdot\frac{\dd p}
    {-\cancel{\sin x}}
    \\
    &= -\int\frac{1}{p}\dd p
    \\
    &= -\ln(p) + C
    \\
    &= -\ln(\cos x) + C
\end{align*}
\\
\begin{align*}
    \therefore \int x\sec^2x\dd x
    &= x\tan x - \int\frac{\sin x}{\cos x}\dd x
    \\
    &= x\tan x - (-\ln(\cos x)) + C
    \\
    &= x\tan x + \ln(\cos x) + C
\end{align*}
$$

Derive the following formulas using the technique of integration by parts. Assume that n is a positive integer. These formulas are called reduction formulas because the exponent in the x term has been reduced by one in each case. The second integral is simpler than the original integral.

### (49) $\displaystyle\int x^n\cos x\dd x = x^n\sin x - n\int x^{n-1}\sin x\dd x$

$$
\begin{darray}{cc}
    u = x^n &\implies& u' = nx^{n-1}
    \\
    v' = \cos x &\implies& v = \sin x
\end{darray}
\\
\begin{align*}
    \int x^n\cos x\dd x &= uv - \int vu'\dd x
    \\
    &= x^n\sin x - \int nx^{n-1}\sin x\dd x
    \\
    &= x^n\sin x -n\int x^{n-1}\sin x\dd x
\end{align*}
$$

### (65) Find the area of the region enclosed by the curve $y=x\cos x$ and the *x*-axis for $\frac{11\pi}{2}\leq x\leq \frac{13\pi}{2}$.  (Express the answer in exact form.)

Since $x\cos x \ge 0$ for all $x\in[\frac{11\pi}{2}, \frac{13\pi}{2}]$, the area $A$ between the curve $y=x\cos x$ and the x-axis is

$$
\int_{11\pi/2}^{13\pi/2} x\cos x\dd x.
$$

$$
\begin{darray}{cc}
    u = x &\implies& u' = 1
    \\
    v' = \cos x &\implies& v = \sin x
\end{darray}
\\
\begin{align*}
    \int_{11\pi/2}^{13\pi/2} x\cos x\dd x
    &= \bigg[x\sin x\bigg]_{11\pi/2}^{13\pi/2}
    - \int_{11\pi/2}^{13\pi/2} \sin x\dd x
    \\
    &= \bigg[x\sin x\bigg]_{11\pi/2}^{13\pi/2}
    - \bigg[-\cos x\bigg]_{11\pi/2}^{13\pi/2}
    \\
    &= \frac{13\pi}{2}-\frac{11\pi}{2}(-1) - 0
    \\
    &= 12\pi
\end{align*}
$$

### (66) Find the volume of the solid generated by revolving the region bounded by the curve $y=\ln x$, the x-axis, and the vertical line $x=e^2$ about the *x*-axis. (Express the answer in exact form.)

Since $y=\ln x$ is increasing and $\ln x = 0 \implies x = 1$, and the region is bounded by $x=e^2$, we have that the volume $V$ of the solid generated by revolving the region around the x-axis is

$$
\begin{align*}
    V &= \pi \int_1^{e^2} \ln^2(x) - 0^2\dd x
    \\
    &= \pi \int_1^{e^2} \ln^2(x)\dd x
\end{align*}
$$

From (25), we found $\int\ln^2 x\dd x$.

$$
\int \ln^2 x \dd x = x(\ln^2(x) - 2\ln(x) + 2) + C
$$

Therefore:

$$
\begin{align*}
    V &= \pi \int_1^{e^2} \ln^2 x\dd x
    \\
    &= \pi \bigg[x(\ln^2(x) - 2\ln(x) + 2)\bigg]_1^{e^2}
    \\
    &= \pi (e^2(4-4+2)- (2))
    \\
    &= \pi(2e^2 - 2)
    \\
    &= 2\pi(e^2 - 1).
\end{align*}
$$

