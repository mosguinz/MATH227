---
print_background: true
export_on_save:
    html: true
puppeteer:
    format: "Letter"
    timeout: 3000
---

# Homework 4

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

## 1\. In lecture, we found the volume of a donut by revolving the cricles $$(x-(R-r))^2 + y^2 = r^2$$ along the $y$-axis where $R>r$.

### (a) Derive the integral formula for the volume of the donut. (It was covered in lass, but please rewrite it on your own)

First, we solve for $x$ to get an expression in terms of $y$.

$$
    (x-(R-r))^2 + y^2 = r^2
    \\
    (x-(R-r))^2 = r^2 - y^2
    \\
    x - (R-r) = \pm\sqrt{r^2-y^2}
    \\
    x = (R-r) \pm\sqrt{r^2-y^2}
$$

We can then split the expression for $x$ to produce two semicicles, where the positive square root component will produce the right side of the circle, and the negative component for the left side.

$$
f_L(y) = (R-r) -\sqrt{r^2-y^2}
\\
f_R(y) = (R-r) +\sqrt{r^2-y^2}
$$

Revolving the right-hand component ($f_R(y)$) around the x-axis would give us the outside shape of the donut. Similarly, revolving the left-hand component ($f_L(y)$) around the x-axis would produce the inside portion (the hole) of the donut.

As such, the volume of the donut $V$ would be the volume produced by revolving the outside minus the inside.

$$
\begin{align*}
    V &= \pi\int_{-r}^r f_R(y)^2 - f_L(y)^2 \dd y
    \\
    &= \pi\int_{-r}^r\((R-r) + \sqrt{r^2-y^2}\)^2 - \((R-r) -\sqrt{r^2-y^2}\)^2 \dd y
\end{align*}
$$

Let $A = R-r$ and $B = \sqrt{r^2-y^2}$. Then,
$$
\begin{align*}
    &\((R-r) + \sqrt{r^2-y^2}\)^2 - \((R-r) -\sqrt{r^2-y^2}\)^2
    \\
    &= (A+B)^2 - (A-B)^2
    \\
    &= (\cancel{A^2+B^2}+2AB) - (\cancel{A^2+B^2}-2AB)
    \\
    &= 2AB - (-2AB)
    \\
    &= 4AB
    \\
    &= 4(R-r)\sqrt{r^2-y^2}.
\end{align*}
$$

And so, we have that:

$$
\begin{align*}
    V &= \pi\int_{-r}^r\((R-r) + \sqrt{r^2-y^2}\)^2 - \((R-r) -\sqrt{r^2-y^2}\)^2 \dd y
    \\
    &= \pi\int_{-r}^r 4(R-r)\sqrt{r^2-y^2} \dd y
    \\
    &= 4\pi(R-r) \int_{-r}^r\sqrt{r^2-y^2}\dd y.
\end{align*}
$$

### (b) Compute the integral and find the volume of the donut. (Substitute $y = r\sin\theta$)

With the integrand being in form $\sqrt{r^2-y^2}$, we can use trigonometic substitution.

Let $y = r\sin\theta$.

$$
\begin{darray}{cc}
    y = r\sin\theta &\implies& \dd y = r\cos\theta\dd\theta
    \\
    y = r\sin\theta = -r &\implies& \theta = \sin^{-1}(-1) = -\frac{\pi}{2}
    \\
    y = r\sin\theta = r &\implies& \theta = \sin^{-1}(1) = \frac{\pi}{2}
\end{darray}
\\
\begin{align*}
    \therefore \int_{-r}^r \sqrt{r^2-y^2}\dd y
    &= \int_{-\pi/2}^{\pi/2}
    \sqrt{r^2-r^2\sin^2\theta}\cdot r\cos\theta\dd\theta
    \\
    &= \int_{-\pi/2}^{\pi/2}
    \sqrt{r^2(1-\sin^2\theta)}\cdot r\cos\theta\dd\theta
    \\
    &= \int_{-\pi/2}^{\pi/2}
    \sqrt{r^2\cos^2\theta}\cdot r\cos\theta\dd\theta
    \\
    &= \int_{-\pi/2}^{\pi/2}
    r\cos\theta\cdot r\cos\theta\dd\theta
    \\
    &= \int_{-\pi/2}^{\pi/2}
    r^2\cos^2\theta \dd\theta
    \\
    &= r^2\int_{-\pi/2}^{\pi/2}
    \cos^2\theta\dd\theta
    \\
    &= r^2\int_{-\pi/2}^{\pi/2}
    \frac{1+\cos2\theta}{2}\dd\theta
    \\
    &= \frac{r^2}{2}\int_{-\pi/2}^{\pi/2}
    1+\cos2\theta\dd\theta
    \\
    &= \frac{r^2}{2}\[\theta+\frac{\sin2\theta}{2}\]_{-\pi/2}^{\pi/2}
    \\
    &= \frac{r^2}{2}\(\frac{\pi}{2}+\cancel{\frac{\sin\pi}{2}} + \frac{\pi}{2}-\cancel{\frac{\sin(-\pi)}{2}}\)
    \\
    &= \frac{\pi r^2}{2}
\end{align*}
$$

Finally, we substitute the result of this integral into our expression for volume.

$$
\begin{align*}
    V &= 4\pi(R-r)\int_{-r}^r\sqrt{r^2-y^2}\dd y
    \\
    &= 4\pi(R-r)\frac{\pi r^2}{2}
    \\
    &= 2\pi^2r^2(R-r)
\end{align*}
$$

## 2\. Find the volume of the solid of revolution by rotating the region bounded by $y = 2x^2, y = 8$ and the $y$-axis.

> **Question open to interpretation**
> Axis of revolution not specified. Assuming revolution around the y-axis.

$$
y = 2x^2 \implies x = \pm\sqrt{\frac{y}{2}}
$$

Since the region is bounded by the y-axis, we only consider the positive component.
$$
x = \sqrt{\frac{y}{2}}
$$

And at $x=0$, $y=0$. So, the integral for the volume $V$ is
$$
\begin{align*}
    V &= \pi\int_0^8 \(\sqrt{\frac{y}{2}}\)^2\dd y
    \\
    &= \pi \int_0^8 \frac{y}{2}\dd y
    \\
    &= \pi \[\frac{y^2}{4}\]_0^8
    \\
    &= 16\pi.
\end{align*}
$$


## Long Question 1

In Figure 1, the region $R$ is enclosed by the parabola $y = 4 − (x − 3)^2$ and the line segment $AC$ where $A, C$ are the points $(1, 0)$ and $(5, 0)$ respectively. $B$ is the vertec ofthe parabola.

### (a) (i) Write down the coordinates of $B$.

$$
\begin{darray}{cc}
    y = 4 - (x-3)^2  &\implies& \frac{\dd y}{\dd x} = -2(x - 3)
    \\
    -2(x - 3) = 0 &\implies& x = 3
    \\
    x = 3 &\implies& y = 4-(3-3)^2 = 4
\end{darray}
\\
\therefore B = (3, 4)
$$

### (ii) Write down the equation of the curve $AB$ and $BC$ as a function of $x = f(y)$.

$$
y = 4-(x-3)^2
\\
y-4 = -(x-3)^2
\\
-y+4 = (x-3)^2
\\
\pm\sqrt{-y+4} = x - 3
\\
x = 3\pm\sqrt{-y+4}
\\
\begin{align*}
    \therefore f_{AB}(y) &= 3 - \sqrt{4-y}
    \\
    f_{BC}(y) &= 3 + \sqrt{4-y}
\end{align*}
$$

A jelly ring in the shape of solid of revolution of the region $R$ is revolved the $y$-axis as shown in Figure 2. The jelly ring contains two layers and we let $h$ be the height of the lower layer.

### (b) (i) Show that the volume of the lower layer of the jelly ring is $$8\pi(8-(4-h)^{3/2})$$

Similar to question one, revolving the right-hand side ($f_{BC}(y)$) will produce the volume of the entire jelly. Revolving the left-hand side ($f_{AB}(y)$) will produce the volume of the hole.

As such, the volume of the lower portion of the jelly ring $V_\text{lower}$ would be the volume produced by revolving the outside minus the inside from $0$ to height $h$.

$$
\begin{align*}
    V_\text{lower} &= \pi \int_0^h f_{BC}(y)^2-f_{AB}(y)^2 \dd y
    \\
    &= \pi\int_0^h (3 + \sqrt{4-y})^2 - (3 - \sqrt{4-y})^2 \dd y
\end{align*}
$$

Let $A = 3$ and $B = \sqrt{4-y}$. Then,
$$
\begin{align*}
    &(3 + \sqrt{4-y})^2 - (3 - \sqrt{4-y})^2
    \\
    &= (A+B)^2 - (A-B)^2
    \\
    &= 4AB
    \\
    &= 12\sqrt{4-y}.
\end{align*}
$$

And so, we have that:
$$
\begin{align*}
    V_\text{lower} &= \pi\int_0^h (3 + \sqrt{4-y})^2 - (3 - \sqrt{4-y})^2 \dd y
    \\
    &= \pi\int_0^h 12\sqrt{4-y} \dd y
    \\
    &= 12\pi\int_0^h \sqrt{4-y} \dd y
    \\
    &= 12\pi\int_0^h (4-y)^{1/2} \dd y
    \\
    &= 12\pi\[-\frac{2(4-y)^{3/2}}{3}\]_0^h
    \\
    &= 12\pi \(-\frac{2(4-h)^{3/2}}{3} + \frac{2(4-0)^{3/2}}{3}\)
    \\
    &= 12\pi \(-\frac{2(4-h)^{3/2}}{3} + \frac{16}{3}\)
    \\
    &= 12\pi \(\frac{1}{3}\)(-2(4-h)^{3/2} + 16)
    \\
    &= 12\pi \(\frac{1}{3}\)(2)(-(4-h)^{3/2} + 8)
    \\
    &= 8\pi(-(4-h)^{3/2} + 8)
    \\
    &= 8\pi(8-(4-h)^{3/2})
\end{align*}
$$

which matches the provided expression for volume.


### (ii) If the upper and the lower layers have the same volume, find the value of $h$. (You leave your answer of $h$ in three decimal places).

Since the integral found for the lower portion is valid for the entire jelly ring, we simply need to change its bound to reflect the upper portion.
$$
\begin{align*}
    V_\text{upper} &= \pi\int_h^4 12\sqrt{4-y}\dd y
    \\
    &= 12\pi\int_h^4 \sqrt{4-y}\dd y
    \\
    &= 12\pi\[-\frac{2(4-y)^{3/2}}{3}\]_h^4
    \\
    &= 12\pi \(-\cancel{\frac{2(4-4)^{3/2}}{3}} + \frac{2(4-h)^{3/2}}{3}\)
    \\
    &= \frac{24\pi(4-h)^{3/2}}{3}
    \\
    &= 8\pi (4-h)^{3/2}
\end{align*}
$$

Since $V_\text{upper} = V_\text{lower}$, we can then solve for $h$.
$$
\begin{align*}
    V_\text{upper} &= V_\text{lower}
    \\
    \cancel{8\pi} (4-h)^{3/2} &= \cancel{8\pi}(8-(4-h)^{3/2})
    \\
    \sqrt{(4-h)^3} &= 8-\sqrt{(4-h)^3}
    \\
    2\sqrt{(4-h)^3} &= 8
    \\
    \sqrt{(4-h)^3} &= 4
    \\
    (4-h)^3 &= 16
    \\
    4-h &= \sqrt[3]{16}
    \\
    h &= -2\sqrt[3]{2} + 4
    \\
    &\approx 1.480
\end{align*}
$$

### (c\) If milk is poured into the center of the jelly ring until it is fully filled. Find the volume of the milk required.

Revolving $f_{AB}(y)$ around the y-axis produces the volume of the hole. So, its volume is also the volume of the milk.

$$
\begin{align*}
    V_\text{milk} &= \pi\int_0^4 f_{AB}(y)^2 \dd y
    \\
    &= \pi\int_0^4 (3-\sqrt{4-y})^2 \dd y
    \\
    &= \pi\int_0^4 (9+(4-y) - 6\sqrt{4-y}) \dd y
    \\
    &= \pi\int_0^4 \(13 - y - 6(4-y)^{1/2}\) \dd y
    \\
    &= \pi\[13y - \frac{y^2}{2} + \frac{12(4-y)^{3/2}}{3}\]_0^4
    \\
    &= \pi\[13y - \frac{y^2}{2} + 4(4-y)^{3/2}\]_0^4
    \\
    &= \pi\(13(4) - \frac{16}{2} - 4(4)^{3/2}\)
    \\
    &= 12\pi
\end{align*}
$$

