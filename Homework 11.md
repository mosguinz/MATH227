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


# Homework 11

**Mos Kullathon**
921425216

## 1.

### (a) Find $\frac{\dd y}{\dd x}$ and $\frac{\dd^2y}{\dd x^2}$ for the following parametrized curve:

#### (i) $x=\sec t, y=\tan t$

#### (ii) $x=2t^2, y=t^4$

### (b) For (i) above, find the equation of the tangent line at $\frac{\pi }{4}$

> ## 2. Find the arc length of the curve $x=t^3, y=\frac{3t^2}{2}$ when $0\le t\le\sqrt{3}$.

> ## 3.

> ### (a) Use Desmos to draw the graph $x(t)=\cos t, y(t)=\sin(3t)$ for $\pi\le t\le\pi$.

> ### (b) Find the area of the bounded region.

> ### (c\) Find the volume of solid of revolution by revloving the curve along the y-axis.

> ### (d) Write down the arc length integral of this curve from $t=0$ to $t=\pi/2$.

> ## 4. Convert the following points into polar coordinates:

> ### (a) $(-4,4)$

> ### (b) $(3,3\sqrt{3})$

> ### (c\) $(\sqrt{3}, -1)$

> ### (d) $(-6,0)$

> ## 5. Consider the polar equation $r=2+\cos(2\theta)$.

> ### (a) Use Desmos to sketch the picture.

> ### (b) Find the slope of the tangent line at $\theta=\pi/4$.

> ### (c\) Find the area of the bounded region of the graph.

> ## 6. Consider the polar equation $r=\theta^2$.

> ### (a) Use Desmos to sketch the picture for $0\le\theta\le4\pi$.

> ### (b) Find the slope of the tangent line at $\theta=3\pi/4$.

> ### (c\) Find the arc length of the curve for $0\le\theta\le4\pi$.
