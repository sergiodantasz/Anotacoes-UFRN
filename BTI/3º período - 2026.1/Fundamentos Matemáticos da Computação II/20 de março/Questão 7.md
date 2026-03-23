**Injetividade:**

Note que $f(-1) = (-1)^2 + 2 = 1 + 2 = 3$. Veja também que $f(1) = 4 - 1^2 = 4 - 1 = 3$. Como $f(-1) = f(1)$ e $-1 \neq 1$, logo $f$ não é injetiva.

**Sobrejetividade:**

Seja $y \in \mathbb{R}$.

**Caso $y \geq 3$:**

Tome $x = -\sqrt{y - 2}$.

Calculamos:

$$
\begin{align}
f(x) &= f\left(-\sqrt{y - 2}\right) \\
     &= \left(-\sqrt{y - 2}\right)^2 + 2 \\
     &= y - 2 + 2 \\
     &= y
\end{align}
$$

Logo $f$ é sobrejetiva.

**Caso $y < 3$:**

Tome $x = \sqrt{4 - y}$.

Calculamos:

$$
\begin{align}
f(x) &= f\left(\sqrt{4 - y}\right) \\
     &= 4 - \left(\sqrt{4 - y}\right)^2 \\
     &= 4 - (4 - y) \\
     &= 4 - 4 + y \\
     &= y
\end{align}
$$

Logo $f$ é sobrejetiva.

**Inversa:**

Como $f$ não é sobrejetiva, logo ela não possui inversa.