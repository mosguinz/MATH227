---
print_background: true
export_on_save:
    html: true
puppeteer:
    format: "Letter"
    timeout: 3000
---

# Homework 2

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

1. Evaluate the following indefinite integrals

    a. $\displaystyle\int\frac{1}{(5-3x)^2}\dd x$

    $$
    \begin{darray}{rcl}
        u = 5-3x & \implies & \dd u = -3\dd x
        \\
        & \iff & \dd x = -\frac{1}{3} \dd u
    \end{darray}
    \\
    \begin{align*}
        \therefore \int\frac{1}{(5-3x)^2}\dd x &= \int\frac{1}{u^2} \(-\frac{1}{3}\dd u\)
        \\
        &= -\frac{1}{3} \int u^{-2}\dd u
        \\
        &= -\frac{1}{3} \cdot \frac{u^{-1}}{-1} + c
        \\
        &= \frac{u^{-1}}{3} + c
        \\
        &= \frac{1}{3(5-3x)} + c
        \\
        &= \frac{1}{15-9x} + c
    \end{align*}
    $$

    b. $\displaystyle\int y(1-y^2)^{2/3}\dd y$

    $$
    \begin{darray}{rcl}
        u = 1-y^2 & \implies & \dd u = -2y\dd y
        \\
        & \iff & \dd y = \frac{1}{-2y}\dd u
    \end{darray}
    \\
    \begin{align*}
        \therefore \int y(1-y^2)^{2/3}\dd y &= \int yu^{2/3} \(\frac{1}{-2y}\dd u\)
        \\
        &= -\frac{1}{2}\int\cancel{y}u^{2/3}\(\cancel{\frac{1}{y}}\dd u\)
        \\
        &= -\frac{1}{2}\int u^{2/3} \dd u
        \\
        &= -\frac{1}{2} \(\frac{u^{5/3}}{5/3}\) + c
        \\
        &= -\frac{1}{2} \(\frac{3u^{5/3}}{5}\) + c
        \\
        &= -\frac{3u^{5/3}}{10} + c
        \\
        &= -\frac{3(1-y^2)^{5/3}}{10} + c
    \end{align*}
    $$

    c. $\displaystyle\int\tan^7 \frac{x}{2}\sec^2\frac{x}{2}\dd x$

    $$
    \begin{darray}{rcl}
        u = \tan\frac{x}{2} &\implies& \dd u = \frac{1}{2}\sec^2\frac{x}{2}\dd x
        \\
        & \iff & 2\dd u = \sec^2\frac{x}{2}\dd x
    \end{darray}
    \\
    \begin{align*}
        \therefore \int\tan^7\frac{x}{2}\sec^2\frac{x}{2}\dd x &=
        \int 2u^7\dd u
        \\
        &= 2\int u^7\dd u
        \\
        &= 2 \(\frac{u^8}{8}\) + c
        \\
        &= 2\(\frac{\tan^8\frac{x}{2}}{8}\) + c
        \\
        &= \frac{2}{8}\tan^8\(\frac{x}{2}\) + c
        \\
        &= \frac{1}{4}\tan^8\(\frac{x}{2}\) + c
    \end{align*}
    $$

    d. $\displaystyle\int t\sqrt{4+t}\dd t$

    $$
    \begin{darray}{rcl}
        u = 4+t &\implies& \dd u = \dd t
        \\
        & \iff & t = u-4
    \end{darray}
    \\
    \begin{align*}
        \therefore \int t\sqrt{4+t}\dd t &=
        \int (u-4) \sqrt{u} \dd u
        \\
        &= \int u^{1/2}(u-4) \dd u
        \\
        &= \int (u^{3/2} - 4u^{1/2}) \dd u
        \\
        &= \frac{u^{5/2}}{5/2} - \frac{4u^{3/2}}{3/2} + c
        \\
        &= \frac{2u^{5/2}}{5} - \frac{8u^{3/2}}{3} + c
        \\
        &= \frac{2(4+t)^{5/2}}{5} - \frac{8(4+t)^{3/2}}{3} + c
    \end{align*}
    $$

    e. $\displaystyle\int\frac{\ln\sqrt{t}}{t}\dd t$

    $$
    \begin{align*}
        \int\frac{\ln\sqrt{t}}{t}\dd t &= \int\frac{\ln t^{1/2}}{t} \dd t
        \\
        &= \int\frac{\frac{1}{2}\ln t}{t} \dd t
        \\
        &= \frac{1}{2}\int\frac{\ln t}{t} \dd t
    \end{align*}
    \\
    \begin{darray}{rcl}
        u = \ln t & \implies & \dd u = \frac{1}{t}\dd t
        \\
        & \iff & \dd t = t\dd u
    \end{darray}
    \\
    \begin{align*}
        \therefore \frac{1}{2}\int\frac{\ln t}{t}\dd t &= \frac{1}{2}\int\frac{u}{\cancel{t}}(\cancel{t}\dd u)
        \\
        &= \frac{1}{2}\int u \dd u
        \\
        &= \frac{1}{2} \(\frac{u^2}{2}\) + c
        \\
        &= \frac{1}{2} \(\frac{\ln^2 t}{2}\) + c
        \\
        &= \frac{\ln^2 t}{4} + c
    \end{align*}
    $$

    f. $\displaystyle\int(3x^2 + 2x) e^{x^3+x^2+1} \dd x$

    $$
    \begin{darray}{rcl}
        u = x^3 + x^2 + 1 & \implies & \dd u = (3x^2 + 2x) \dd x
    \end{darray}
    \\
    \begin{align*}
        \therefore \int(3x^2 + 2x) e^{x^3+x^2+1} \dd x &= \int e^u \dd u
        \\
        &= e^u + c
        \\
        &= e^{x^3+x^2+1} + c
    \end{align*}
    $$

2. Evaluate the following definite integrals

    a. $\displaystyle\int_0^1 (3t-1)^{50} \dd t$

    $$
    \begin{darray}{rcl}
        u = 3t - 1 & \implies & \dd u = 3\dd t
        \\
        & \iff & \dd t = \frac{1}{3}\dd u
        \\
        t = 0 & \implies & u = 3(0)-1 = -1
        \\
        t = 1 & \implies & u = 3(1)-1 = 2
    \end{darray}
    \\
    \begin{align*}
        \therefore \int_0^1(3t-1)^{50}\dd t &=
        \int_{-1}^2 \frac{1}{3}u^{50}\dd u
        \\
        &= \frac{1}{3}\bigg[\frac{u^{51}}{51}\bigg]_{-1}^2
        \\
        &= \frac{1}{3}\(\frac{2^{51}}{51} - \frac{-1^{51}}{51}\)
        \\
        &= \frac{1}{3} \(\frac{2^{51} + 1}{51}\)
        \\
        &= \frac{250199979298361}{17}
    \end{align*}
    $$

    b. $\displaystyle\int_0^{\pi/3} (1+e^{\sin x})\cos x \dd x$

    $$
    \begin{darray}{rcl}
        u = \sin x & \implies & \dd u = \cos x \dd x
        \\
        x = 0 &\implies& u = \sin0=0
        \\
        x = \frac{\pi}{3} &\implies& u = \sin\frac{\pi}{3} = \frac{\sqrt{3}}{2}
    \end{darray}
    \\
    \begin{align*}
        \therefore \int_0^{\pi/3} (1+e^{\sin x})\cos x \dd x &=
        \int_0^{\frac{\sqrt{3}}{2}} (1+e^u) \dd u
        \\
        &= \bigg[u + e^u\bigg]_0^{\frac{\sqrt{3}}{2}}
        \\
        &= \frac{\sqrt{3}}{2} + e^{\frac{\sqrt{3}}{2}} - 0 - e^0
        \\
        &= \frac{\sqrt{3}}{2} + e^{\frac{\sqrt{3}}{2}} - 1
    \end{align*}
    $$

    c. $\displaystyle\int_1^e \frac{(\ln x)^2}{x} \dd x$

    $$
    \begin{darray}{rcl}
        u = \ln x & \implies & \dd u = \frac{1}{x}\dd x
        \\
        x = 1 & \implies & u = \ln 1 = 0
        \\
        x = e & \implies & u = \ln e = 1
    \end{darray}
    \\
    \begin{align*}
        \therefore \int_1^e\frac{(\ln x)^2}{x} \dd x &=
        \int_0^1 u^2 \dd u
        \\
        &= \bigg[\frac{u^3}{3}\bigg]_0^1
        \\
        &= \frac{1^3}{3} - \frac{0^3}{3}
        \\
        &= \frac{1}{3}
    \end{align*}
    $$

    d. $\displaystyle\int_\pi^{\pi/2} \frac{\cos x}{\sin^4 x} \dd x$

    $$
    \begin{darray}{rcl}
        u = \sin x &\implies& \dd u = \cos x \dd x
        \\
        x = \pi &\implies& u = \sin\pi = 0
        \\
        x = \frac{\pi}{2} &\implies& u = \sin\frac{\pi}{2} = 1
    \end{darray}
    \\
    \begin{align*}
        \therefore \int_\pi^{\pi/2}\frac{\cos x}{\sin^4 x}\dd x &=
        \int_0^1 \frac{1}{u^4}\dd u
        \\
        &= \int_0^1 u^{-4}\dd u
        \\
        &= \bigg[\frac{u^{-3}}{-3}\bigg]_0^1
        \\
        &= \frac{1}{-3(1^3)}-\frac{1}{-3(0^3)}
        \\
        &= -\frac{1}{3} + \frac{1}{0}
        \\
        &= \text{DNE}
    \end{align*}
    $$

3. Suppose that $\displaystyle\int_0^a xe^{-x^2}\dd x = \frac{1}{3}$. Find $a$.

$$
\begin{darray}{rcl}
    u = -x^2 &\implies& \dd u =-2x\dd x
    \\
    &\iff& \dd x = \frac{1}{-2x}\dd u = -\frac{1}{2}\cdot\frac{1}{x}\dd u
    \\
    x = 0 &\implies& u = -0^2 = 0
    \\
    x = a &\implies& u = -a^2
\end{darray}
\\
\begin{align*}
    \therefore \int_0^a xe^{-x^2}\dd x &=
    \int_0^{-a^2} xe^u \dd x \(-\frac{1}{2}\cdot\frac{1}{x}\dd u\)
    \\
    &= -\frac{1}{2}\int_0^{-a^2} e^u\dd u
    \\
    &= -\frac{1}{2}\bigg[e^u\bigg]_0^{-a^2}
    \\
    &= -\frac{1}{2}\(e^{-a^2}-e^0\)
    \\
    &= -\frac{1}{2}e^{-a^2} + \frac{1}{2}
    \\
    &= \frac{1}{3}
    \\
    -\frac{1}{2}e^{-a^2} + \frac{1}{2} &= \frac{1}{3}
    \\
    -\frac{1}{2e^{a^2}} &= \frac{1}{3} - \frac{1}{2}
    \\
    -\frac{1}{2e^{a^2}} &= -\frac{1}{6}
    \\
    2e^{a^2} &= 6
    \\
    e^{a^2} &= 3
    \\
    a^2 &= \ln 3
    \\
    a &= \pm\sqrt{\ln 3}
\end{align*}
$$

4. Find $\displaystyle\int\cot x\dd x$ and $\displaystyle\int\csc x \dd x$.

$$
\begin{align*}
    \int \cot x \dd x &= \int\frac{1}{\tan x}\dd x
    \\
    &= \int\frac{\cos x}{\sin x}\dd x
\end{align*}
\\
\begin{darray}{rcl}
    u = \sin x &\implies& \dd u = \cos x \dd x
\end{darray}
\\
\begin{align*}
    \therefore \int\frac{\cos x}{\sin x}\dd x &= \int \frac{1}{u}\dd u
    \\
    &= \int u^{-1}\dd u
    \\
    &= \ln(u) + c
    \\
    &= \ln(\sin x) + c
\end{align*}
\\
\\
\begin{align*}
    \int \csc x \dd x &= \int\frac{\csc x(\cot x + \csc x)}{\cot x + \csc x}\dd x
    \\
    &= \int\frac{\csc(x)\cot(x) + \csc^2 x}{\cot x + \csc x}\dd x
    \\
\end{align*}
\\
\begin{darray}{rcrl}
    u = \cot x + \csc x &\implies& \dd u &= (-\csc^2(x) - \csc(x)\cot(x))\dd x
    \\
    &\iff& -\dd u &= (\csc^2(x)+\csc(x)\cot(x) )\dd x
\end{darray}
\\
\begin{align*}
    \therefore \int\csc x\dd x
    &= \int\frac{-\dd u}{u}
    \\
    &= \int -\frac{1}{u}\dd u
    \\
    &= -\int u^{-1}\dd u
    \\
    &= -\ln(u) + c
    \\
    &= -\ln(\cot x + \csc x) + c
\end{align*}
$$

5. Section 1.6: 351, 353, 357.

    351\. $\displaystyle\int x \csc(x^2)\dd x$

    $$
    \begin{darray}{rcl}
        u = x^2 &\implies& \dd u = 2x\dd x
        \\
        &\iff& \dd x = \frac{1}{2x}\dd u
    \end{darray}
    \\
    \begin{align*}
        \therefore \int x\csc(x^2)\dd x &=
        \int \cancel{x}\csc(u)\(\frac{1}{2\cancel{x}}\dd u\)
        \\
        &= \frac{1}{2} \int \csc u \dd u
    \end{align*}
    $$

    > From (4):
    > $$
    > \int\csc x\dd x = -\ln(\cot x + \csc x) + c
    > $$

    $$
    \begin{align*}
        \iff \frac{1}{2}\int\csc u \dd u &= \frac{1}{2}(-\ln(\cot u + \csc u)) + c
        \\
        &= -\frac{1}{2}\ln |\cot x^2 + \csc x^2| + c
    \end{align*}
    $$

    353\. $\displaystyle\int \ln(\csc x)\cot x \dd x$

    $$
    \begin{darray}{rcl}
        u = \ln(\csc x) &\implies& \dd u = \frac{-\cancel{\csc x} \cot x}{\cancel{\csc x}}\dd x
        \\
        &\iff& \dd x = -\frac{1}{\cot x}\dd u
    \end{darray}
    \\
    \begin{align*}
        \therefore\int\ln(\csc x)\cot x \dd x &=
        \int -u \dd u
        \\
        &= -\int u \dd u
        \\
        &= -\frac{u^2}{2} + c
        \\
        &= -\frac{\ln^2(\csc x)}{2} + c
    \end{align*}
    $$

    357\. $\displaystyle\int_0^{\pi/3}\frac{\sin x - \cos x}{\sin x + \cos x}\dd x$

    $$
    \begin{darray}{rcrl}
        u = \sin x + \cos x &\implies& \dd u &= (\cos x - \sin x)\dd x
        \\
        &\iff& -\dd u &= (-\cos x + \sin x)\dd x
        \\
        &&&= (\sin x -\cos x) \dd x
    \end{darray}
    \\
    \begin{darray}{rcll}
        x = 0 &\implies& u = \sin 0 + \cos 0 &= 1
        \\
        x = \frac{\pi}{3} &\implies& u = \sin \frac{\pi}{3} + \cos \frac{\pi}{3} &= \frac{1+\sqrt{3}}{2}
    \end{darray}
    \\
    \begin{align*}
        \therefore\int_1^{\pi/3}\frac{\sin x - \cos x}{\sin x + \cos x}\dd x
        &= \int_1^\frac{1+\sqrt{3}}{2} \frac{-\dd u}{u}
        \\
        &= \int_1^\frac{1+\sqrt{3}}{2} -\frac{1}{u}\dd u
        \\
        &= -\int_1^\frac{1+\sqrt{3}}{2} u^{-1} \dd u
        \\
        &= -\bigg[\ln u\bigg]_1^\frac{1+\sqrt{3}}{2}
        \\
        &= -\(\ln\frac{1+\sqrt{3}}{2} - \ln 1\)
        \\
        &= -\ln\frac{1+\sqrt{3}}{2}
        \\
        &= \ln(\sqrt{3}-1)
    \end{align*}
    $$
