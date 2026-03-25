# Introdução

A sequência pode ser representada por $\{a_n\}$ ou $a_n$. Seus elementos são representados por $a_0, a_1, a_2, \ldots, a_n$.

> O primeiro elemento pode ser $a_0$ ou $a_1$, isso deve ser explicitado.

# Fórmula Fechada

É a representação da sequência usando uma fórmula geral.

Por exemplo, $a_n = 2^n \cdot 3$, para $n \geq 0$.

# Fórmula Recursiva

Uma sequência possui a forma recursiva quando o termo geral é calculado a partir de casos base bem definidos.

Por exemplo, $a_0 = 5$ e $a_n = 3 \cdot a_{n - 1}$, para $n \geq 1$.

> A fórmula recursiva pode ser utilizada para construir a fórmula fechada.

## Sequência de Fibonacci

$$
1, 1, 2, 3, 5, 8, 13, 21, \ldots
$$

É dada por:

- $f_0 = 1$;
- $f_1 = 1$;
- $f_n = f_{n - 1} + f_{n - 2}$, para $n \geq 2$.

A sequência de Fibonacci é expressa pela fórmula:

$$
f_n = \frac{1}{\sqrt{5}} \cdot \left[ \left( \frac{1 + \sqrt{5}}{2} \right)^n - \left( \frac{1 - \sqrt{5}}{2} \right)^n \right] = \frac{\phi^n - \psi^n}{\sqrt{5}}, \psi = 1 - \phi
$$

## Fatorial

$$
n! = n \cdot (n - 1) \cdot (n - 2) \cdot \ldots \cdot 2 \cdot 1
$$

É dada por:

- $a_1 = 1$;
- $a_n = n \cdot a_{n - 1}$, para $n \geq 2$.

# Função de Ackermann

$$
A(m, n) = \begin{cases}
  n + 1, \quad& \text{se } m = 0 \\
  A(m - 1, 1), \quad& \text{se } m > 0 \text{ e } n = 0 \\
  A(m - 1, A(m, n - 1)), \quad& \text{se } m > 0 \text{ e } n > 0 \\
\end{cases}
$$

Com $m$ e $n$ números não negativos.
