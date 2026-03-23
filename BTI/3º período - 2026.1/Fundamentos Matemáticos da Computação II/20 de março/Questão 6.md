**Injetividade:**

Sejam $x_1, x_2 \in \mathbb{R}$ tais que $f(x_1) = f(x_2)$.

Calculamos:

$$
\begin{align}
f(x_1) = f(x_2)
             &\implies \frac{x_1}{3} + \frac{3}{2} = \frac{x_2}{3} + \frac{3}{2} \\
             &\implies \frac{x_1}{3} = \frac{x_2}{3} \\
             &\implies x_1 = x_2
\end{align}
$$

Logo $f$ é injetiva.

**Sobrejetividade:**

Seja $y \in \mathbb{R}$.

Tome $x = 3\left( y - \frac{3}{2} \right)$.

Calculamos:

$$
\begin{align}
f(x) &= f\left(3\left( y - \frac{3}{2} \right)\right) \\
     &= \frac{3\left( y - \frac{3}{2} \right)}{3} + \frac{3}{2} \\
     &= y - \frac{3}{2} + \frac{3}{2} \\
     &= y
\end{align}
$$

Logo $f$ é sobrejetiva.

**Inversa:**

Como $f$ é bijetiva, vamos encontrar sua inversa.

Calculamos:

$$
\begin{align}
f(x) = \frac{x}{3} + \frac{3}{2} &\iff f(x) - \frac{3}{2} = \frac{x}{3} \\
                              &\iff x = 3\left(f(x) - \frac{3}{2}\right)
\end{align}
$$

Após a troca de variáveis teremos:

$$
f^{-1}(y) = 3\left(y - \frac{3}{2}\right)
$$

Logo a inversa de $f$ é dada por $f^{-1}(y) = 3\left(y - \frac{3}{2}\right)$.