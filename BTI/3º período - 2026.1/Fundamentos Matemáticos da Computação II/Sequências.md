# Introdução

Sequências são listas ordenadas de elementos. Podem ser representadas por $\{a_n\}$ ou $a_n$. Seus elementos são representados por $a_0, a_1, a_2, \ldots, a_n$.

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

É dado por:

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

# Fórmulas

## PA

### Termo Geral

$$
a_n = a_1 + (n - 1) \cdot r
$$

### Soma

$$
S_n = \frac{(a_1 + a_n) \cdot n}{2}
$$

## PG

### Termo Geral

$$
a_n = a_1 \cdot q^{n - 1}
$$

### Soma Finita

$$
S_n = \frac{a_1 \cdot (q^n - 1)}{q - 1}
$$

### Soma Infinita

$$
S_\infty = \frac{a_1}{1 - q}
$$

# Exercícios

## Ex. 8

Considere a sequência:

$$
-1, 3, 7, 11, \ldots
$$

Cuja fórmula recursiva é:

- $a_0 = -1$;
- $a_n = a_{n - 1} + 4$, para $n \geq 1$.

E a fórmula fechada é $a_n = 4n - 1$.

Além disso, a soma é dada por $S_n = (2n - 1)(n + 1)$.

> [!example] Exercício
> Demonstre usando a indução matemática que a fórmula fechada está correta.

Por indução.

**Caso base ($n = 0$):**

Note que $a_0 = 4 \cdot 0 - 1 = -1$.

**Passo indutivo:**

> **HI:** $a_k = -1 + 4k$, para $k \geq 0$.

Como $a_n = a_{n - 1} + 4$, então $a_{k + 1} = a_k + 4$.

Calculamos:

$$
\begin{align}
a_{k + 1} &= a_k + 4 \\
          &= (-1 + 4k) + 4 &\quad& (\text{HI}) \\
          &= 4k + 3 \\
          &= 4(k + 1) - 1
\end{align}
$$

> [!example] Exercício
> Demonstre usando a indução matemática que a soma está correta.

Por indução.

**Caso base ($n = 0$):**

Veja que $S_0 = (2 \cdot 0 - 1)(0 + 1) = -1$.

**Passo indutivo:**

> **HI:** $S_k = (2k - 1)(k + 1)$, para $k \geq 0$.

Queremos mostrar que $S_{k + 1} = (2k + 1)(k + 2)$.

Calculamos:

$$
\begin{align}
S_{k + 1} &= S_k + a_{k + 1} \\
		  &= S_k + (-1 + 4(k + 1)) \\
          &= (2k - 1)(k + 1) + (-1 + 4(k + 1)) &\quad& (\text{HI}) \\
          &= 2k^2 + 2k -k - 1 -1 + 4k + 4 \\
          &= 2k^2 + 5k + 2 \\
          &= (2k + 1)(k + 2)
\end{align}
$$
