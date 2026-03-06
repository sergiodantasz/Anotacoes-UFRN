# Indução

Queremos demonstrar que uma propriedade $P(n)$ vale para todo inteiro $n$, com $n \geq a$.

**Caso base:** $P(a)$ é verdadeiro.

Suponha que vale $P(k)$, para $k \geq a$. (HI)

**Passo indutivo:** mostrar que vale $P(k + 1)$.

# Exercícios

## Ex. 1

> [!example] Proposição
> $0$ é o único elemento neutro da soma.

> **Negação:** ...

**Demonstração (por contradição):**

Suponha, por contradição, que existe $x \neq 0$ tal que $x$ é elemento neutro da soma:

$$
\begin{align}
x + 0 = x &\quad& (1) \\
0 + x = 0 &\quad& (2)
\end{align}
$$

De (1) e (2), temos que $0 = x + 0 = x$.

Um absurdo, pois supomos $x \neq 0$.

Portanto, $0$ é o único elemento neutro da soma. $\blacksquare$

## Ex. 2

> [!example] Proposição
> Existe um número par que pode ser escrito como a soma de dois primos distintos.

**Demonstração:**

Note que $10 = 3 + 7$, $3$ e $7$ são primos e $10$ é par. $\blacksquare$

## Ex. 3

> [!example] Proposição
> Existem números irracionais $x$ e $y$ tal que $x^y$ é racional.

**Demonstração:**

> Este é um exemplo de demonstração não construtiva.

Sabemos que $\sqrt{2}$ é irracional.

Se $\sqrt{2}^\sqrt{2}$ for racional, tome $x = y = \sqrt{2}$.

...

Se $\sqrt{2}^\sqrt{2}$ não for racional, tome $x = \sqrt{2}^\sqrt{2}$ e $y = \sqrt{2}$.

Calculamos:

$$
x^y = \left(\sqrt{2}^\sqrt{2}\right)^\sqrt{2} = \sqrt{2}^{\sqrt{2} \cdot \sqrt{2}} = \sqrt{2}^2 = 2
$$

Como $2 \in \mathbb{Q}$, logo $x^y$ é racional. $\blacksquare$

## Ex. 4

> [!example] Proposição
> Para todo $n \in \mathbb{N}^*$, $1 + 1 + 3 + \cdots + n = \frac{n(n + 1)}{2} = \sum_{i = 1}^n{i}$.

**Demonstração (por indução):**

**Caso base:** $n = 1$.

$$
1 = \frac{1(1 + 1)}{2} = \frac{2}{2}
$$

[foto]

## Ex. 5

> [!example] Proposição
> $1$ é o único elemento neutro da multiplicação.

> **Negação:** ...

**Demonstração (por contradição):**

Suponha, por contradição, que existe $x \neq 1$ tal que $x$ é elemento neutro da multiplicação:

$$
\begin{align}
x \cdot 1 = x &\quad& (1) \\
1 \cdot x = 1 &\quad& (2)
\end{align}
$$

De (1) e (2), segue que $x = x \cdot 1 = 1$.

Isso é um absurdo, pois supomos $x \neq 1$.

Portanto, $1$ é o único elemento neutro da multiplicação. $\blacksquare$

## Ex. 6

> [!example] Proposição
> Para todo $n \in \mathbb{N}^*$, $1 + 3 + 5 + \cdots + (2n - 1) = n^2$.

**Demonstração (por indução):**

...

## Ex. 7

> [!example] Proposição
> Para todo $n \in \mathbb{N}^*$, $1^2 + 2^2 + \cdots + n^2 = \frac{n(n + 1)(2n + 1)}{6}$.

**Demonstração (por indução):**

...

## Ex. 8

> [!example] Proposição
> Para todo $n \in \mathbb{N}^*$, $2^0 + 2^1 + 2^2 + \cdots + 2^n = 2^{n + 1} - 1$.

**Demonstração (por indução):**

...

## Ex. 9

> [!example] Proposição
> Para todo $n \in \mathbb{N}$, $n < 2^n$.

**Demonstração (por indução):**

...
