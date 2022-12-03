---
print_background: true
export_on_save:
    html: true
puppeteer:
    format: "Letter"
    timeout: 3000
---

# Homework 5

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

## 1\. Evaluate the following integrals

### (a) $\displaystyle\int x\cos(5x)\dd x$

$$
\begin{darray}{cc}
    u = x &\implies& u' = 1
    \\
    v' = \cos(5x) &\implies& v = \frac{1}{5}\sin(5x)
\end{darray}
\\
\begin{align*}
    \int x\cos(5x)\dd x &= uv - \int vu' \dd x
    \\
    &= \frac{x}{5}\sin(5x) - \int\frac{1}{5}\sin(5x)\dd x
    \\
    &= \frac{x}{5}\sin(5x) - \frac{1}{5}\int\sin(5x)\dd x
    \\
    &= \frac{x}{5}\sin(5x) - \frac{1}{5}\(-\frac{1}{5}\cos(5x)\) + c
    \\
    &= \frac{1}{5}\sin(5x) + \frac{1}{25}\cos(5x) + c
\end{align*}
$$

### (b) $\displaystyle\int_0^1 x^2e^{-x}\dd x$

$$
\begin{darray}{cc}
    u = x^2 &\implies& u' = 2x
    \\
    v' = e^{-x} &\implies& v = -e^{-x}
\end{darray}
\\
\begin{align*}
    \int_0^1 x^2 e^{-x}\dd x &= \bigg[uv\bigg]_0^1 - \int_0^1 vu' \dd x
    \\
    &= \bigg[-x^2e^{-x}\bigg]_0^1 - \int_0^1 -2xe^{-x} \dd x
    \\
    &= \bigg[-x^2e^{-x}\bigg]_0^1 + 2\int_0^1 xe^{-x} \dd x
\end{align*}
\\
\begin{darray}{cc}
    p = x &\implies& p' = 1
    \\
    q' = e^{-x} &\implies& q = -e^{-x}
\end{darray}
\\
\begin{align*}
    \int_0^1 xe^{-x}\dd x &= \bigg[pq\bigg]_0^1 - \int_0^1 qp' \dd x
    \\
    &= \bigg[-xe^{-x}\bigg]_0^1 - \int_0^1 -e^{-x}\dd x
    \\
    &= \bigg[-xe^{-x}\bigg]_0^1 + \bigg[-e^{-x}\bigg]_0^1
    \\
    &= -\frac{1}{e} - \frac{1}{e} + 1
    \\
    &= \frac{-2+e}{e}
\end{align*}
\\
\begin{align*}
    \therefore\int_0^1 x^2e^{-x}\dd x &=
    \bigg[-x^2e^{-x}\bigg]_0^1 + 2\(\frac{-2+e}{e}\)
    \\
    &= -\frac{1}{e} + \frac{-4+2e}{e}
    \\
    &= \frac{-5+2e}{e}
\end{align*}
$$

### (c\) $\displaystyle\int x(\ln x)^2\dd x$

$$
\begin{darray}{cc}
    u = (\ln x)^2 &\implies& u' = \frac{2}{x}\ln x
    \\
    v' = x &\implies& v = \frac{1}{2}x^2
\end{darray}
\\
\begin{align*}
    \int x(\ln x)^2 \dd x &= uv - \int vu'\dd x
    \\
    &= \frac{1}{2}x^2\ln^2 x - \int x\ln x \dd x
\end{align*}
\\
\begin{darray}{cc}
    p = \ln x &\implies& p' = \frac{1}{x}
    \\
    q' = x &\implies& q = \frac{1}{2}x^2
\end{darray}
\\
\begin{align*}
    \int x \ln x \dd x &= pq - \int qp'\dd x
    \\
    &= \frac{1}{2}x^2\ln x - \int\ \frac{1}{2}x\dd x
    \\
    &= \frac{1}{2}x^2\ln x - \frac{1}{4}x^2 + c
\end{align*}
\\
\begin{align*}
    \therefore \int x(\ln x)^2\dd x
    &= \frac{1}{2}x^2\ln^2x - \frac{1}{2}x^2\ln x + \frac{1}{4}x^2 + c
    \\
    &= \frac{1}{4}x^2 (2\ln^2(x) - 2\ln(x) + 1) + c
\end{align*}
$$

### (d) $\displaystyle\int x \csc^2 x\dd x$

$$
\begin{darray}{cc}
    u = x &\implies& u' = 1
    \\
    v' = \csc^2x &\implies& v = -\cot x
\end{darray}
\\
\begin{align*}
    \int x \csc^2x\dd x &= uv - \int vu'\dd x
    \\
    &= -x\cot(x)- \int-\cot x\dd x
    \\
    &= -x\cot(x)+ \ln|\sin x| + c
\end{align*}
$$

### (e) $\displaystyle\int_0^{\pi/4} e^x\cos(2x)\dd x$

$$
\begin{darray}{cc}
    u = \cos(2x) &\implies& u' = -2\sin(2x)
    \\
    v' = e^x &\implies& v = e^x
\end{darray}
\\
\begin{align*}
    \int e^x\cos(2x)\dd x &= uv - \int vu'\dd x
    \\
    &= e^x\cos(2x) - \int -2e^x\sin(2x) \dd x
    \\
    &= e^x\cos(2x) + 2\int e^x\sin(2x)\dd x
\end{align*}
\\
\begin{darray}{cc}
    p = \sin(2x) &\implies& p' = 2\cos(2x)
    \\
    q' = e^x &\implies& q = e^x
\end{darray}
\\
\begin{align*}
    \int e^x\sin(2x)\dd x &= pq - \int qp' \dd x
    \\
    &= e^x\sin(2x) - \int2e^x\cos(2x)
    \\
    &= e^x\sin(2x) -2 \int e^x\cos(2x)
\end{align*}
\\
\begin{align*}
    \int e^x\cos(2x)\dd x
    &= e^x\cos(2x) + 2 \(e^x\sin(2x) -2 \int e^x\cos(2x)\)
    \\
    &= e^x\cos(2x) + 2e^x\sin(2x) - 4\int e^x\cos(2x)
    \\
    5 \int e^x\cos(2x)\dd x &= e^x\cos(2x) + 2e^x\sin(2x)
    \\
    \int e^x\cos(2x)\dd x &= \frac{1}{5}(e^x\cos(2x) + 2e^x\sin(2x)) + c
\end{align*}
\\
\begin{align*}
    \therefore \int_0^{\pi/4} e^x\cos(2x)\dd x
    &= \[\frac{1}{5}(e^x\cos(2x) + 2e^x\sin(2x))\]_0^{\pi/4}
    \\
    &= \frac{1}{5}(2e^{\pi/4}-1)
\end{align*}
$$

### (f) $\displaystyle\int_0^\pi e^{\cos t} \sin(2t)\dd t$ (Recall $\sin(2t)=2\sin t\cos t$)

$$
\begin{darray}{cc}
    u = \cos t &\implies& \dd u = -\sin t\dd t
    \\
    &\iff& \dd t = \frac{1}{-\sin t}\dd u
    \\
    t = 0 &\implies& u = \cos 0 = 1
    \\
    t = \pi &\implies& u = \cos\pi = -1
\end{darray}
\\
\begin{align*}
    \int_0^\pi e^{\cos t}\sin(2t)\dd t
    &= 2 \int_1^{-1} e^{\cos t}\sin t\cos t \dd t
    \\
    &= 2\int_1^{-1} ue^u\cancel{\sin t} \(\frac{1}{\cancel{-\sin t}}\)\dd u
    \\
    &= -2\int_1^{-1} ue^u\dd u
    \\
    &= 2\int_{-1}^1 ue^u\dd u
\end{align*}
\\
\begin{darray}{cc}
    p = u &\implies& p' = 1
    \\
    q' = e^u &\implies& q = e^u
\end{darray}
\\
\begin{align*}
    \int_{-1}^1 ue^u\dd u
    &= \bigg[pq\bigg]_{-1}^1 - \int qp' \dd u
    \\
    &= \bigg[ue^u\bigg]_{-1}^1 - \int e^u \dd u
    \\
    &= \bigg[ue^u\bigg]_{-1}^1 - \bigg[e^u\bigg]_{-1}^1
    \\
    &= e + \frac{1}{e} - e + \frac{1}{e}
    \\
    &= \frac{2}{e}
    \\
\end{align*}
\\
\begin{align*}
    \therefore \int_0^\pi e^{\cos t}\sin(2t)\dd t
    &= 2 \int_1^{-1} e^{\cos t}\sin t\cos t \dd t
    \\
    &= 2 \cdot\frac{2}{e}
    \\
    &= \frac{4}{e}
\end{align*}
$$

## 2\. Show that the reduction formula for $\displaystyle I_n = \int(\ln x)^n \dd x$ is $$I_n = x (\ln x)^n - nI_{n-1}$$

$$
\begin{darray}{cc}
    u = (\ln x)^n &\implies& u' = \frac{n}{x}(\ln x)^{n-1}
    \\
    v' = 1 &\implies& v = x
\end{darray}
\\
\begin{align*}
    I_n =
    \int (\ln x)^n &= uv - \int vu'\dd x
    \\
    &= x(\ln x)^n - \int\frac{n\cancel{x}}{\cancel{x}}(\ln x)^{n-1}
    \\
    &= x(\ln x)^n - n\underbrace{\int (\ln x)^{n-1}}_{I_{n-1}}
    \\
    &= x(\ln x)^n - nI_{n-1}
\end{align*}
$$

## Book Section 3.3:

### (135) $\displaystyle\int\frac{\dd x}{\sqrt{x^2-a^2}}\dd x$

$$
\int\frac{\dd x}{\sqrt{x^2-a^2}}\dd x = \int\frac{1}{\sqrt{x^2-a^2}}\dd x
\\
\begin{darray}{cc}
    x = a\sec\theta &\implies& \dd x = a\sec\theta\tan\theta\dd\theta
    \\
    &\iff& \theta = \sec^{-1}\(\frac{x}{a}\)
\end{darray}
\\
\begin{align*}
    \int\frac{1}{\sqrt{x^2-a^2}}\dd x
    &= \int\frac{1}{\sqrt{a^2\sec^2\theta - a^2}}
    (a\sec\theta\tan\theta\dd\theta)
    \\
    &= \int\frac{1}{\sqrt{a^2(\sec^2\theta - 1)}}
    (a\sec\theta\tan\theta\dd\theta)
    \\
    &= \int\frac{1}{\sqrt{a^2\tan^2\theta}}
    (a\sec\theta\tan\theta\dd\theta)
    \\
    &= \int\frac{1}{\cancel{a\tan\theta}}
    (\cancel{a}\sec\theta\cancel{\tan\theta}\dd\theta)
    \\
    &= \int\sec\theta\dd\theta
    \\
    &= \ln|\tan\theta + \sec\theta| + c
    \\
    &= \ln\left|\tan\(\sec^{-1}\(\frac{x}{a}\)\) + \sec\(\sec^{-1}\(\frac{x}{a}\)\)\right| + c
    \\
    &= \ln\left|\tan\(\sec^{-1}\(\frac{x}{a}\)\) + \frac{x}{a}\right| + c
    \\
    &= \ln|\frac{x}{a}\sqrt{1-\frac{1}{\frac{x^2}{a^2}}} + \frac{x}{a}| + c
    \\
    &= \ln\left|\frac{x}{a}\sqrt{\frac{x^2}{x^2} - \frac{a^2}{x^2}} + \frac{x}{a}\right| + c
    \\
    &= \ln\left|\frac{x}{a}\sqrt{\(\frac{1}{x^2}\)x^2-a^2} + \frac{x}{a}\right| + c
    \\
    &= \ln\left|\frac{1}{a}\sqrt{x^2-a^2} + \frac{x}{a}\right| + c
    \\
    &= \ln\left|\frac{1}{a}(\sqrt{x^2-a^2} + x) \right| + c
    \\
    &= \ln\left|\frac{1}{a}\right| + \ln|\sqrt{x^2-a^2} + x| + c
    \\
    &= \ln|\sqrt{x^2-a^2} + x| + c
\end{align*}
$$


### (140) $\displaystyle\int\frac{\dd x}{(1+x^2)^2}$

$$
\int\frac{\dd x}{(1+x^2)^2} = \int\frac{1}{(1+x^2)^2}\dd x
\\
\begin{darray}{cc}
    x = \tan\theta &\implies& \dd x = \sec^2\theta\dd\theta
    \\
    &\iff& \theta = \tan^{-1}x
    \\
    &\iff& \sin\theta = \frac{x}{\sqrt{1+x^2}}
    \\
    &\iff& \cos\theta = \frac{1}{\sqrt{1+x^2}}
\end{darray}
\\
\begin{align*}
    \int\frac{1}{(1+x^2)^2}\dd x &=
    \int\frac{1}{(1 + \tan^2\theta)^2}
    (\sec^2\theta\dd\theta)
    \\
    &= \int\frac{1}{\sec^4\theta}(\sec^2\dd\theta)
    \\
    &= \int\frac{1}{\sec^2\theta}\dd\theta
    \\
    &= \int\cos^2\theta\dd\theta
    \\
    &= \int\frac{1}{2}(\cos(2\theta) + 1)\dd\theta
    \\
    &= \frac{1}{2}\int\cos(2\theta) + 1 \dd\theta
    \\
    &= \frac{1}{2}\(\theta + \frac{1}{2}\sin2\theta\) + c
    \\
    &= \frac{1}{2}\(\theta+\frac{1}{2}2\sin\theta\cos\theta\) + c
    \\
    &= \frac{1}{2}(\theta + \sin\theta\cos\theta) + c
    \\
    &= \frac{1}{2} \(\tan^{-1}(x) + \frac{x}{1+x^2}\) + c
\end{align*}
$$


### (142) $\displaystyle\int\frac{\sqrt{x^2-25}}{x}\dd x$

$$
\begin{darray}{cc}
    r^2 = 25 &\implies& r = 5
    \\
    x = r\sec\theta &\implies&
    \dd x = r\sec\theta\tan\theta\dd\theta
    \\
    &\iff& \theta = \sec^{-1}\(\frac{x}{r}\)
    \\
    &\iff& \sec\theta = \frac{x}{r}
    \\
    &\iff& \tan\theta = \frac{\sqrt{x^2 - r^2}}{r}
\end{darray}
\\
\begin{align*}
    \int\frac{\sqrt{x^2-25}}{x}\dd x
    &= \int\frac{\sqrt{r^2\sec^2\theta - r^2}}{r\sec\theta}
    (r\sec\theta\tan\theta\dd\theta)
    \\
    &= \int\frac{\sqrt{r^2(\sec^2\theta - 1)}}{r\sec\theta}
    (r\sec\theta\tan\theta\dd\theta)
    \\
    &= \int\frac{\sqrt{r^2\tan^2\theta}}{r\sec\theta}
    (r\sec\theta\tan\theta\dd\theta)
    \\
    &= \int\frac{r\tan\theta}{\cancel{r\sec}\theta}
    (\cancel{r\sec}\theta\tan\theta\dd\theta)
    \\
    &= r\int\tan^2\theta\dd\theta
    \\
    &= r\int\frac{\sin^2\theta}{\cos^2\theta}\dd\theta
    \\
    &= r\int\frac{1-\cos^2\theta}{\cos^2\theta}\dd\theta
    \\
    &= r\int\frac{1}{\cos^2\theta} - 1 \dd\theta
    \\
    &= r\int\sec^2(\theta) - 1 \dd\theta
    \\
    &= r(\tan(\theta)-\theta) + c
    \\
    &= r\(\frac{\sqrt{x^2 - r^2}}{r} - \sec^{-1}\(\frac{x}{r}\)\) + c
    \\
    &= \sqrt{x^2 - r^2} - r\sec^{-1}\(\frac{x}{r}\) + c
    \\
    &= \sqrt{x^2 - 25} - 5\sec^{-1}\(\frac{x}{5}\) + c
\end{align*}
$$


### (153) $\displaystyle\int_{-1}^1 (1-x^2)^{3/2}\dd x$

$$
\int_{-1}^1 (1-x^2)^{3/2}\dd x =
\int_{-1}^1 \sqrt{(1-x^2)^3}\dd x
\\
\begin{darray}{cc}
    x = \sin\theta &\implies& \dd x= \cos\theta\dd\theta
    \\
    &\iff& \theta = \sin^{-1}(x)
    \\
    x = \sin\theta = -1 &\implies& \theta = -\frac{\pi}{2}
    \\
    x = \sin\theta = 1 &\implies& \theta = \frac{\pi}{2}
\end{darray}
\\
\begin{align*}
    \int_{-1}^1\sqrt{(1-x^2)^3}\dd x
    &= \int_{-\pi/2}^{\pi/2}\sqrt{(1-\sin^2\theta)^3}
    \cdot(\cos\theta\dd\theta)
    \\
    &= \int_{-\pi/2}^{\pi/2}\sqrt{(\cos^2\theta)^3}
    \cdot(\cos\theta\dd\theta)
    \\
    &= \int_{-\pi/2}^{\pi/2}\sqrt{(\cos^2\theta)^2\cos^2\theta}
    \cdot(\cos\theta\dd\theta)
    \\
    &= \int_{-\pi/2}^{\pi/2}\cos^2\theta\cos\theta
    \cdot(\cos\theta\dd\theta)
    \\
    &= \int_{-\pi/2}^{\pi/2}\cos^2\theta\cos^2\theta\dd\theta
    \\
    &= \int_{-\pi/2}^{\pi/2}\frac{1}{2}(\cos(2\theta)+1)\cdot\frac{1}{2}(\cos(2\theta)+1)\dd\theta
    \\
    &= \frac{1}{4}\int_{-\pi/2}^{\pi/2}(\cos(2\theta)+1)^2\dd\theta
    \\
    &= \frac{1}{4}\int_{-\pi/2}^{\pi/2}\cos^2(2\theta) + 1 + 2\cos(2\theta)\dd\theta
    \\
    &= \frac{1}{4}\int_{-\pi/2}^{\pi/2}\frac{1}{2}(\cos(4\theta) + 1) + 1 + 2\cos(2\theta)\dd\theta
    \\
    &= \frac{1}{4}\int_{-\pi/2}^{\pi/2}\frac{1}{2}\cos(4\theta) + \frac{1}{2}
    + 1 + 2\cos(2\theta)\dd\theta
    \\
    &= \frac{1}{4}\int_{-\pi/2}^{\pi/2}\frac{1}{2}(\cos(4\theta) + 1 + 2 + 4\cos(2\theta))\dd\theta
    \\
    &= \frac{1}{8}\int_{-\pi/2}^{\pi/2}(\cos(4\theta)+4\cos(2\theta)+3)\dd\theta
    \\
    &= \frac{1}{8}\[\frac{\sin(4\theta)}{4}+4\sin(2\theta)+3\theta\]_{-\pi/2}^{\pi/2}
    \\
    &= \frac{1}{8}\(\frac{3}{2}\pi - \(-\frac{3}{2}\pi\)\)
    \\
    &= \frac{3}{8}\pi
\end{align*}
$$

