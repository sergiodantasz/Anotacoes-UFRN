# Relações

Considere:

$$
A \times B = \{ (a, b) \mid a \in A \land b \in B \}
$$

Uma relação $R$ é qualquer subconjunto de $A \times B$.

# Funções

Uma função é uma relação em $A \times B$ onde cada elemento de $A$ aparece uma única vez.

$$
f : \{ (x, y) \mid y = f(a) \} \subseteq A \times B
$$

$$
f : A \to B
$$

# Injetividade

$f$ é injetiva se, e somente se:

$$
\displaylines{
(\forall x_1, x_2 \in A)[f(x_1) = f(x_2) \implies x_1 = x_2] \\
\text{ou} \\
(\forall x_1, x_2 \in A)[x_1 \neq x_2 \implies f(x_1) \neq f(x_2)]
}
$$

# Sobrejetividade

$f$ é sobrejetiva se, e somente se:

$$
(\forall y \in B)(\exists x \in A)[f(x) = y]
$$

# Bijetividade

$$
f \text{ é bijetiva} \iff f \text{ é injetiva} \land f \text{ é sobrejetiva}
$$

# Função Inversa

A inversa da função $f$, cuja notação é $f^{-1}$, quando existir, é dada por:

$$
f^{-1} = \{ (y, x) \mid f(x) = y \}
$$

# Exercícios

> Verifique se as funções abaixo são injetivas, sobrejetivas e possuem inversa.

## Ex. 1

> [!example] Função
> $f : \mathbb{R} \to \mathbb{R}$, com $f(x) = 2x + 1$.

**Injetividade:**

Sejam $x_1, x_2 \in \mathbb{R}$.

Suponha que $f(x_1) = f(x_2)$.

Calculamos:

$$
\begin{align}
f(x_1) = f(x_2) &\iff 2x_1 + 1 = 2x_2 + 1 \\
                &\iff 2x_1 = 2x_2 \\
                &\iff x_1 = x_2
\end{align}
$$

Logo $f$ é injetiva.

**Sobrejetividade:**

Seja $y \in \mathbb{R}$.

Tome $x = \frac{y - 1}{2} \in \mathbb{R}$.

Calculamos:

$$
\begin{align}
f(x) &= f\left(\frac{y - 1}{2}\right) \\
     &= 2\left( \frac{y - 1}{2} \right) + 1 \\
     &= y - 1 + 1 \\
     &= y
\end{align}
$$

Logo $f$ é sobrejetiva. 

**Inversa:**

Vamos encontrar $f^{-1}$. Trocando $x$ por $y$ e $y$ por $x$ na função original, temos $x = 2y + 1$.

Calculamos:

$$
\begin{align}
x = 2y + 1 &\iff x - 1 = 2y \\
           &\iff \frac{x - 1}{2} = y
\end{align}
$$

Logo $f^{-1}(x) = \frac{x - 1}{2}$.

Portanto, $f$ é bijetiva e possui inversa. $\blacksquare$

## Ex. 2

> [!example] Função
> $f : \mathbb{R} \to [4, \infty)$, com $f(x) = x^2 + 4$.

**Injetividade:**

Veja que:

$$
\displaylines{
f(-1) = (-1)^2 + 4 = 1 + 4 = 5 \\
\text{e} \\
f(1) = 1^2 + 4 = 1 + 4 = 5
}
$$

Como $f(-1) = f(1)$ e $-1 \neq 1$, logo $f$ não é injetiva.

**Sobrejetividade:**

Seja $y \in [4, \infty)$.

Tome $x = \sqrt{y - 4}$.

Calculamos:

$$
\begin{align}
f(x) &= f(\sqrt{y - 4}) \\
     &= (\sqrt{y - 4})^2 + 4 \\
     &= y - 4 + 4 \\
     &= y
\end{align}
$$

Logo $f$ é sobrejetiva.

**Inversa:**

Como $f$ não é bijetiva, então ela não possui inversa.

Portanto, $f$ é sobrejetiva. Por não ser injetiva, então $f$ não possui inversa. $\blacksquare$

## Ex. 3

> [!example] Função
> $f : \mathbb{N}^* \to \mathbb{Z}$, com $f(x) = \begin{cases} -\frac{x}{2}, &\text{se } x \text{ é par} \\ \frac{x - 1}{2}, &\text{se } x \text{ é ímpar} \end{cases}$.

**Injetividade:**

Sejam $x_1, x_2 \in \mathbb{N}^*$.

**Caso $x_1$ e $x_2$ são pares:**

Suponha que $f(x_1) = f(x_2)$.

Calculamos:

$$
\begin{align}
f(x_1) = f(x_2) &\iff -\frac{x_1}{2} = -\frac{x_2}{2} \\
                &\iff \frac{x_1}{2} = \frac{x_2}{2} \\
                &\iff x_1 = x_2
\end{align}
$$

Assim, temos que $f$ é injetiva.

**Caso $x_1$ e $x_2$ são ímpares:**

Suponha que $f(x_1) = f(x_2)$.

Calculamos:

$$
\begin{align}
f(x_1) = f(x_2) &\iff \frac{x_1 - 1}{2} = \frac{x_2 - 1}{2} \\
                &\iff x_1 - 1 = x_2 - 1 \\
                &\iff x_1 = x_2
\end{align}
$$

Logo $f$ é injetiva.

**Caso $x_1$ é par e $x_2$ é ímpar:**

Suponha que $x_1 \neq x_2$. Vamos mostrar que $f(x_1) \neq f(x_2)$.

Suponha, por contradição, que $f(x_1) = f(x_2)$.

Note que:

$$
-\frac{x_1}{2} = \frac{x_2 - 1}{2} \iff -x_1 = x_2 - 1
$$

Como $-x_1 < 0$ e $x_2 - 1 \geq 0$, chegamos a um absurdo. Logo $f(x_1) \neq f(x_2)$.

Assim, $f$ é injetiva.

**Caso $x_1$ é ímpar e $x_2$ é par:**

*Análogo ao caso anterior.*

**Sobrejetividade:**

Seja $y \in \mathbb{Z}$.

**Caso $x$ é par:**

Tome $x = -2y$.

Calculamos:

$$
\begin{align}
f(x) &= f(-2y) \\
     &= -\left(\frac{-2y}{2}\right) \\
     &= y
\end{align}
$$

Logo $f$ é sobrejetiva.

**Caso $x$ é ímpar:**

Tome $x = 2y + 1$.

Calculamos:

$$
\begin{align}
f(x) &= f(2y + 1) \\
     &= \frac{(2y + 1) - 1}{2} \\
     &= \frac{2y}{2} \\
     &= y
\end{align}
$$

Logo $f$ é sobrejetiva.

**Inversa:**

Vamos encontrar $f^{-1}$.

**Caso $x$ é par:**

Trocando $x$ e $y$, temos $x = -\frac{y}{2}$. Calculamos:

$$
\begin{align}
x = -\frac{y}{2} &\iff 2x = -y \\
                 &\iff y = -2x
\end{align}
$$

Logo $f^{-1}(x) = -2x$, para $x < 0$.

**Caso $x$ é ímpar:**

Trocando $x$ e $y$, temos $x = \frac{y - 1}{2}$. Calculamos:

$$
\begin{align}
x = \frac{y - 1}{2} &\iff 2x = y - 1 \\
                    &\iff y = 2x + 1
\end{align}
$$

Logo $f^{-1}(x) = 2x + 1$, para $x \geq 0$.

Sendo assim, a inversa de $f$ é dada por:

$$
f^{-1}(x) = \begin{cases}
  -2x,    &\text{se } x < 0 \\
  2x + 1, &\text{se } x \geq 0
\end{cases}
$$

Portanto, $f$ é bijetiva e possui inversa. $\blacksquare$
