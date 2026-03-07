# Indução

Queremos demonstrar que uma propriedade $P(n)$ vale para todo $n, a \in \mathbb{Z}$, com $n \geq a$. Separamos isso em duas etapas.

**Caso base:**

Mostramos que $P(a)$ é verdadeira.

**Passo indutivo:**

>**HI:** Supomos que $P(k)$ é verdadeira para algum inteiro $k \geq a$.

Mostramos que $P(k + 1)$ também é verdadeira.

# Exercícios

## Ex. 1

> [!example] Proposição
> 0 é o único elemento neutro da soma.

> **Negação:** Existe um elemento neutro da soma diferente de 0.

**Demonstração (por contradição):**

Suponha, por contradição, que existe $x \neq 0$ tal que $x$ é elemento neutro da soma.

Logo, para todo $a$ inteiro, temos:

$$
a + x = a \quad \text{e} \quad x + a = a
$$

Tome $a = 0$.

Logo $0 + x = 0$.

Mas como 0 é elemento neutro da soma, então $0 + x = x$.

Um absurdo, pois supomos $x \neq 0$.

Portanto, 0 é o único elemento neutro da soma. $\blacksquare$

## Ex. 2

> [!example] Proposição
> Existe um número par que pode ser escrito como a soma de dois primos distintos.

**Demonstração:**

Tome o número 10. Note que ele pode ser escrito na forma $3 + 7$. Como 3 e 7 são primos, logo 10 é par. $\blacksquare$

## Ex. 3

> [!example] Proposição
> Existem números irracionais $x$ e $y$ tais que $x^y$ é racional.

**Demonstração:**

> Este é um exemplo de demonstração não construtiva, pois mostramos que objetos com tais características existem, mas não dizemos quais são.

Sabemos que $\sqrt{2}$ é irracional.

Separo em dois casos a partir de $\sqrt{2}^\sqrt{2}$:

**Caso $\sqrt{2}^\sqrt{2}$ é racional:**

Tome $x = y = \sqrt{2}$. Pela hipótese do caso, segue que $x^y$ é racional.

**Caso $\sqrt{2}^\sqrt{2}$ é irracional:**

Tome $x = \sqrt{2}^\sqrt{2}$ e $y = \sqrt{2}$.

Calculamos:

$$
x^y = \left(\sqrt{2}^\sqrt{2}\right)^\sqrt{2} = \sqrt{2}^{\sqrt{2} \cdot \sqrt{2}} = \sqrt{2}^2 = 2
$$

Como $2 \in \mathbb{Q}$, logo $x^y$ é racional.

Portanto, concluímos que existem números irracionais $x$ e $y$ tais que $x^y$ é racional. $\blacksquare$

## Ex. 4

> [!example] Proposição
> Para todo $n \in \mathbb{N}^*$, $1 + 2 + 3 + \cdots + n = \frac{n(n + 1)}{2} = \sum_{i = 1}^n{i}$.

Seja $n \in \mathbb{N}^*$.

**Demonstração (por indução):**

**Caso base ($n = 1$):**

Calculamos:

$$
1 = \frac{1(1 + 1)}{2} = \frac{2}{2} = 1
$$

Logo a propriedade é válida para $n = 1$.

**Passo indutivo:**

> **HI:** $1 + 2 + \cdots + k = \frac{k(k + 1)}{2}$, para $k \geq 1$.

Queremos demonstrar que a propriedade é válida para $k + 1$.

Calculamos:

$$
\begin{align}
\sum_{i = 1}^{k + 1}{i} &= \sum_{i = 1}^{k}{i} + (k + 1) \\
                        &= \frac{k(k + 1)}{2} + (k + 1) &\quad& (\text{HI}) \\
                        &= \frac{k(k + 1) + 2(k + 1)}{2} \\
                        &= \frac{(k + 1)(k + 2)}{2} \\
                        &= \frac{(k + 1)((k + 1) + 1)}{2}
\end{align}
$$

Logo a propriedade é válida para $n = k + 1$.

Portanto, pelo princípio da indução matemática, concluímos a demonstração. $\blacksquare$

## Ex. 5

> [!example] Proposição
> 1 é o único elemento neutro da multiplicação.

> **Negação:** Existe um elemento neutro da multiplicação diferente de 1.

**Demonstração (por contradição):**

Suponha, por contradição, que existe $x \neq 1$ tal que $x$ é elemento neutro da multiplicação.

Logo, para todo $a$ inteiro, temos:

$$
a \cdot x = a \quad \text{e} \quad x \cdot a = a
$$

Tome $a = 1$.

Logo $1 \cdot x = 1$.

Mas como 1 é elemento neutro da soma, então $1 \cdot x = x$.

Um absurdo, pois supomos $x \neq 1$.

Portanto, 1 é o único elemento neutro da multiplicação. $\blacksquare$

## Ex. 6

> [!example] Proposição
> Para todo $n \in \mathbb{N}^*$, $1 + 3 + 5 + \cdots + (2n - 1) = n^2$.

**Demonstração (por indução):**

Seja $n \in \mathbb{N}^*$.

**Caso base ($n = 1$):**

Calculamos:

$$
1 = 1^2 = 1
$$

Logo a propriedade é válida para $n = 1$.

**Passo indutivo:**

> **HI:** $1 + 3 + \cdots + (2k - 1) = k^2$, para $k \geq 1$.

Calculamos:

$$
\begin{align}
\sum_{i = 1}^{k + 1}{2i - 1} &= \sum_{i = 1}^{k}{2i - 1} + (2(k + 1) - 1) \\
                             &= k^2 + 2k + 2 - 1 &\quad& (\text{HI}) \\
                             &= k^2 + 2k + 1 \\
                             &= (k + 1)^2
\end{align}
$$

Logo a propriedade vale para $n = k + 1$.

Portanto, concluímos a demonstração. $\blacksquare$

## Ex. 7

> [!example] Proposição
> Para todo $n \in \mathbb{N}^*$, $1^2 + 2^2 + \cdots + n^2 = \frac{n(n + 1)(2n + 1)}{6}$.

**Demonstração (por indução):**

Seja $n \in \mathbb{N}^*$.

**Caso base ($n = 1$):**

Calculamos:

$$
1 = \frac{1(1 + 1)(2 \cdot 1 + 1)}{6} = \frac{1 \cdot 2 \cdot 3}{6} = 1
$$

Logo a propriedade é válida para $n = 1$.

**Passo indutivo:**

> **HI:** $1^2 + 2^2 + \cdots + k^2 = \frac{k(k + 1)(2k + 1)}{6}$, para $k \geq 1$.

Calculamos:

$$
\begin{align}
\sum_{i = 1}^{k + 1}{i^2} &= \sum_{i = 1}^{k}{i^2} + (k + 1)^2 \\
                          &= \frac{k(k + 1)(2k + 1)}{6} + (k + 1)^2 &\quad& (\text{HI}) \\
                          &= \frac{k(k + 1)(2k + 1) + 6(k + 1)^2}{6} \\
                          &= \frac{(k + 1)(k(2k + 1) + 6(k + 1))}{6} \\
                          &= \frac{(k + 1)(2k^2 + k + 6k + 6)}{6} \\
                          &= \frac{(k + 1)(2k^2 + 7k + 6)}{6} \\
                          &= \frac{(k + 1)((k + 2)(2k + 3))}{6} \\
                          &= \frac{(k + 1)((k + 1) + 1)(2k + 2 + 1)}{6} \\
                          &= \frac{(k + 1)((k + 1) + 1)(2(k + 1) + 1)}{6} \\
\end{align}
$$

Logo a propriedade é válida para $n = k + 1$.

Portanto, concluímos a demonstração. $\blacksquare$

## Ex. 8

> [!example] Proposição
> Para todo $n \in \mathbb{N}$, $2^0 + 2^1 + 2^2 + \cdots + 2^n = 2^{n + 1} - 1$.

**Demonstração (por indução):**

Seja $n \in \mathbb{N}$.

**Case base ($n = 0$):**

Calculamos:

$$
2^0 = 1 = 2^{0 + 1} - 1 = 2 - 1 = 1
$$

Logo a propriedade é válida para $n = 0$.

**Passo indutivo:**

> **HI:** $2^0 + 2^1 + 2^2 + \cdots + 2^k = 2^{k + 1} - 1$, para $k \geq 0$.

Calculamos:

$$
\begin{align}
\sum_{i = 0}^{k + 1}{2^i} &= \sum_{i = 0}^{k}{2^i} + 2^{k + 1} \\
	                      &= 2^{k + 1} - 1 + 2^{k + 1} &\quad& (\text{HI}) \\
	                      &= 2 \cdot 2^{k + 1} - 1 \\
	                      &= 2^{(k + 1) + 1} - 1
\end{align}
$$

Logo a propriedade é válida para $n = k + 1$.

Portanto, concluímos a demonstração. $\blacksquare$

## Ex. 9

> [!example] Proposição
> Para todo $n \in \mathbb{N}$, $n < 2^n$.

**Demonstração (por indução):**

Seja $n \in \mathbb{N}$.

**Caso base ($n = 0$):**

Calculamos:

$$
2^0 = 1 > 0
$$

Logo a propriedade é válida para $n = 0$.

**Passo indutivo:**

> **HI:** $k < 2^k$, para $k \geq 0$.

Como $k \geq 0$, temos $2^k \geq 2^0 = 1$ (1).

Somando (1) e (HI):

$$
k + 1 < 2^k + 2^k = 2 \cdot 2^k = 2^{k + 1}
$$

Logo a propriedade é válida para $n = k + 1$.

Portanto, concluímos a demonstração. $\blacksquare$
