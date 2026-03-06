# Demonstração por Contradição

Na demonstração por contradição, para demonstrar $P \implies Q$, supomos que a implicação é falsa, ou seja, $\lnot (P \implies Q)$.

$$
\lnot (P \implies Q) \equiv P \land \lnot Q
$$

Assumimos que $P$ é verdadeiro e $Q$ é falso. A partir dessas hipóteses, obtemos uma contradição.

> [!question] Contradição vs. Contraposição
> Na demonstração por contraposição, demonstramos uma implicação equivalente à original: em vez de $P \implies Q$, mostramos $\lnot Q \implies \lnot P$. Já na demonstração por contradição, supomos que $P$ é verdadeiro e $Q$ é falso (ou seja, $P \implies Q$ é falso) e mostramos que isso leva a uma contradição.

# Demonstração de Cadeia de Equivalências

...

# Exercícios

## Ex. 1

> [!example] Proposição
> $\sqrt{2}$ é irracional.

> Note que nesta proposição não há premissa. É uma proposição simples.

> **Negação:** $\sqrt{2}$ é racional.

**Demonstração (por contradição):**

Suponha, por contradição, que $\sqrt{2}$ é racional.

Por definição de número racional, existem inteiros $p$ e $q$, com $q \neq 0$, tais que $\sqrt{2} = \frac{p}{q}$.

Calculamos:

$$
\begin{align}
\sqrt{2} = \frac{p}{q} &\iff 2 = \frac{p^2}{q^2} \\
                       &\iff 2q^2 = p^2 \quad (1)
\end{align}
$$

Logo, por definição de número par, $p^2$ é par.

Como $p^2$ é par, logo $p$ é par.

Ou seja, existe $x$ inteiro tal que $p = 2x$. Substituindo em (1):

$$
\begin{align}
2q^2 = (2x)^2 &\iff 2q^2 = 4x^2 \\
              &\iff q^2 = 2x^2
\end{align}
$$

Logo, de forma análoga, $q^2$ é par e $q$ é par.

Absurdo, pois se $p$ e $q$ são pares, $\frac{p}{q}$ não é irredutível.

Portanto, $\sqrt{2}$ é racional. $\blacksquare$

## Ex. 2

> [!example] Proposição
> Entre quaisquer 22 dias consecutivos, pelo menos 4 deles caem no mesmo dia da semana.

> **Negação:** Existe um conjunto de 22 dias consecutivos tal que, para todo dia da semana, no máximo 3 desses dias caem nesse dia da semana.

**Demonstração (por contradição):**

Suponha, por contradição, que no máximo 3 dias caem em um mesmo dia da semana.

Como são 7 dias na semana, teremos, no máximo, 21 dias distribuídos.

Absurdo, pois temos um total de 22 dias.

Portanto, pelo menos 4 dias caem no mesmo dia da semana. $\blacksquare$

## Ex. 3

> [!example] Proposição
> Para todo $n$ inteiro, se $3n + 2$ é par, então $n$ é par.

> **Negação:** Existe um inteiro $n$ tal que $3n + 2$ é par e $n$ é ímpar.

**Demonstração (por contradição):**

Seja $n$ inteiro.

Suponha que $3n + 2$ é par (1).

Suponha, por contradição, que $n$ é ímpar (2).

Pela definição de ímpar, existe $k \in \mathbb{Z}$ tal que $n = 2k + 1$ (3).

Substituindo (3) em (1):

$$
\begin{align}
3n + 2 &= 3(2k + 1) + 2 \\
       &= 6k + 3 + 2 \\
       &= 6k + 4 + 1 \\
       &= 2(3k + 2) + 1
\end{align}
$$

Tome $t = 3k + 2$.

Como $t \in \mathbb{Z}$ e $3n + 2 = 2t + 1$, logo $3n + 2$ é ímpar, o que contradiz (1). Chegamos a um absurdo.

Portanto, $n$ é par. $\blacksquare$

## Ex. 4

> [!example] Proposição
> Dado um inteiro $n$, $n$ é par se, e somente se, $n^2$ é par.

**Demonstração:**

Seja $n$ inteiro.

Separo em duas partes:

**Parte 1 – Se $n$ é par, então $n^2$ é par:**

Suponha que $n$ é par.

Pela definição de par, existe $k$ inteiro tal que $n = 2k$.

Calculamos:

$$
\begin{align}
n^2 &= (2k)^2 \\
    &= 4k^2 \\
    &= 2(2k^2)
\end{align}
$$

Logo, por definição, $n^2$ é par.

**Parte 2 – Se $n^2$ é par, então $n$ é par (por contraposição):**

> **Contrapositiva:** Se $n$ é ímpar, então $n^2$ é ímpar.

Suponha que $n$ é ímpar.

Por definição de número ímpar, existe $k \in \mathbb{Z}$ tal que $n = 2k + 1$.

Calculamos:

$$
\begin{align}
n^2 &= (2k + 1)^2 \\
    &= 4k^2 + 2k + 1 \\
    &= 2(2k^2 + k) + 1
\end{align}
$$

Logo, por definição, $n^2$ é ímpar.

Portanto, concluímos que, para todo $n$ inteiro, $n$ é par se, e somente se, $n^2$ é par. $\blacksquare$

## Ex. 5

> [!example] Proposição
> Para todo $n \in \mathbb{Z}$, as seguintes afirmações são equivalentes:
> - $n$ é par;
> - $n - 1$ é ímpar;
> - $n^2$ é par;
> - $3n + 2$ é par.

**Demonstração:**

Seja $n$ inteiro.

Separo a cadeia de equivalências em três equivalências, e cada equivalência em duas partes:

**1. $n$ é par se, e somente se, $n - 1$ é ímpar:**

**Parte 1:**

Suponha que $n$ é par.

Por definição, existe $k$ inteiro tal que $n = 2k$.

Calculamos:

$$
\begin{align}
n - 1 &= 2k - 1 \\
      &= 2k - 1 + 1 - 1 \\
      &= 2k - 2 + 1 \\
      &= 2(k - 1) + 1
\end{align}
$$

Logo, por definição, $n - 1$ é ímpar.

**Parte 2:**

Suponha que $n - 1$ é ímpar.

Por definição, existe inteiro $m$ tal que $n - 1 = 2m + 1$.

Calculamos:

$$
\begin{align}
n &= 2m + 2 \\
  &= 2(m + 1)
\end{align}
$$

Logo, por definição, $n$ é par.

**2. $n$ é par se, e somente se, $n^2$ é par:**

**Parte 1:**

Suponha que $n$ é par.

Por definição, existe $k$ inteiro tal que $n = 2k$.

Calculamos:

$$
\begin{align}
n^2 &= (2k)^2 \\
    &= 4k^2 \\
    &= 2(2k^2)
\end{align}
$$

Logo, por definição, $n^2$ é par.

**Parte 2 (por contraposição):**

> **Contrapositiva:** Se $n$ é ímpar, então $n^2$ é ímpar.

Suponha que $n$ é ímpar.

Por definição, existe $m$ inteiro tal que $n = 2m + 1$.

Calculamos:

$$
\begin{align}
n^2 &= (2m + 1)^2 \\
    &= 4m^2 + 2m + 1 \\
    &= 2(2m^2 + m) + 1
\end{align}
$$

Logo, por definição, $n^2$ é ímpar.

**3. $n$ é par se, e somente se, $3n + 2$ é par:**

**Parte 1:**

Suponha que $n$ é par.

Por definição, existe $k$ inteiro tal que $n = 2k$.

Calculamos:

$$
\begin{align}
n = 2k &\iff 3n = 6k \\
       &\iff 3n + 2 = 6k + 2 \\
       &\iff 3n + 2 = 2(3k + 1)
\end{align}
$$

Logo, por definição, $3n + 2$ é par.

**Parte 2:**

Suponha que $3n + 2$ é par.

Por definição, existe $m$ inteiro tal que $3n + 2 = 2m$.

Calculamos:

$$
\begin{align}
3n + 2 = 2m &\iff 3n = 2m - 2 \\
            &\iff n = \frac{2m - 2}{3} \\
            &\iff n = \frac{2(m - 1)}{3} \\
            &\iff n = 2 \cdot \frac{m - 1}{3}
\end{align}
$$

Logo, por definição, $n$ é par.

Portanto, demonstramos a cadeia de equivalências. $\blacksquare$

## Ex. 6

> [!example] Proposição
> Para todo inteiro positivo $n$, se $n \leq 4$, então $(n + 1)^3 \geq 3^n$.

**Demonstração:**

Seja $n$ um inteiro positivo.

Separo em casos:

**Caso $n = 1$:**

$$
\begin{align}
(1 + 1)^3 \geq 3^1 &\iff 2^3 \geq 3 \\
                   &\iff 8 \geq 3
\end{align}
$$

**Caso $n = 2$:**

$$
\begin{align}
(2 + 1)^3 \geq 3^2 &\iff 3^3 \geq 9 \\
                   &\iff 27 \geq 9
\end{align}
$$

**Caso $n = 3$:**

$$
\begin{align}
(3 + 1)^3 \geq 3^3 &\iff 4^3 \geq 27 \\
                   &\iff 64 \geq 27
\end{align}
$$

**Caso $n = 4$:**

$$
\begin{align}
(4 + 1)^3 \geq 3^4 &\iff 5^3 \geq 81 \\
                   &\iff 125 \geq 82
\end{align}
$$

Logo, concluímos a demonstração. $\blacksquare$

## Ex. 7

> [!example] Proposição
> Para todo $n \in \mathbb{Z}$, $n^2 \geq n$.

**Demonstração:**

Seja $n$ inteiro.

Separo em casos:

**Caso $n = 0$:**

Imediato, pois $0^2 = 0 \geq 0$.

**Caso $n \geq 1$:**

Multiplicando por $n$ em ambos os lados:

$$
\begin{align}
n \geq 1 &\implies n \cdot n \geq n \quad (n > 0) \\
         &\implies n^2 \geq n
\end{align}
$$

Logo $n^2 \geq n$.

**Caso $n \leq -1$:**

Note que:

$$
n \leq -1 \leq 0 \leq n^2 \quad (\text{Lema 1})
$$

Por transitividade, $n^2 \geq n$.

Pelos três casos, concluímos que $n^2 \geq n$ para todo inteiro $n$. $\blacksquare$

---

**Lema 1:** Para todo $n$ inteiro, $n^2 \geq 0$.

**Demonstração:**

Seja $n$ inteiro.

Separo em casos:

**Caso $n \geq 0$:**

Multiplicando ambos os lados por $n$:

$$
\begin{align}
n \geq 0 &\implies n \cdot n \geq n \cdot 0 \quad (n \geq 0) \\
         &\implies n^2 \geq 0
\end{align}
$$

**Caso $n < 0$:**

Calculamos:

$$
\begin{align}
n < 0 &\iff -n > 0 \\
      &\implies (-n) \cdot (-n) > (-n) \cdot 0 &\quad& (-n > 0) \\
      &\implies n^2 > 0                        &\quad& (-n > 0)
\end{align}
$$

Portanto, pelos dois casos, concluímos que $n^2 \geq 0$ para todo inteiro $n$. $\blacksquare$

---

## Ex. 8

> [!example] Proposição
> Todo número primo é ímpar.

> **Negação:** Pelo menos um número primo é par.

**Refutação:**

Vamos apresentar um contra-exemplo, isto é, uma testemunha de que a afirmação é falsa.

Tome o número 2. Perceba que 2 é primo e par ao mesmo tempo.

Portanto, concluímos que a afirmação apresentada é falsa. $\blacksquare$

## Ex. 9

> [!example] Proposição
> Todo número primo é par.

> **Negação:** Pelo menos um número primo é ímpar.

**Refutação:**

Tome o número 11. Note que a afirmação é falsa, pois 11 é primo e não é par. $\blacksquare$

## Ex. 10

> [!example] Proposição
> Existe um número par que é ímpar.

**Refutação:**

Suponha que exista um inteiro $n$ que seja par e ímpar.

Pelas definições de par e ímpar, existem inteiros $k$ e $m$ tais que $n = 2k$ e $n = 2m + 1$.

Calculamos:

$$
\begin{align}
2k = 2m + 1 &\iff 2k - 2m = 1 \\
            &\iff 2(k - m) = 1
\end{align}
$$

Mas o lado esquerdo é par e o lado direito é ímpar, o que é impossível.

Portanto, não existe inteiro que seja simultaneamente ímpar e par. $\blacksquare$

## Ex. 11

> [!example] Proposição
> Se $n = ab$, com $a$ e $b$ inteiros positivos, então $a \leq \sqrt{n}$ ou $b \leq \sqrt{n}$.

> **Contrapositiva:** Se $a > \sqrt{n}$ e $b > \sqrt{n}$, então $n \neq ab$.

**Demonstração (por contraposição):**

Sejam $a$, $b$ e $n$ inteiros positivos.

Suponha que $a > \sqrt{n}$ e $b > \sqrt{n}$.

Multiplicando ambas as inequações:

$$
a \cdot b > \sqrt{n} \cdot \sqrt{n} = n
$$

Como $ab > n$, logo $ab \neq n$. $\blacksquare$

## Ex. 12

> [!example] Proposição
> Para todo $a, b \in \mathbb{R}$, as seguintes afirmações são equivalentes:
> - $a < b$;
> - $\frac{a + b}{2} > a$;
> - $\frac{a + b}{2} < b$.

**Demonstração:**

Sejam $a$ e $b$ inteiros.

Separo a cadeia de equivalências em duas equivalências, e cada equivalência em duas partes:

**1. $a < b$ se, e somente se, $\frac{a + b}{2} > a$:**

**Parte 1:**

Suponha que $a < b$.

Calculamos:

$$
\begin{align}
a < b &\iff a + a < a + b \\
      &\iff 2a < a + b \\
      &\iff a < \frac{a + b}{2}
\end{align}
$$

**Parte 2:**

Suponha que $\frac{a + b}{2} > a$.

Calculamos:

$$
\begin{align}
\frac{a + b}{2} > a &\iff a + b > 2a \\
                    &\iff a - a + b > a \\
                    &\iff a < b
\end{align}
$$

**2. $a < b$ se, e somente se, $\frac{a + b}{2} < b$:**

**Parte 1:**

Suponha que $a < b$.

Calculamos:

$$
\begin{align}
a < b &\iff a + b < b + b \\
      &\iff a + b < 2b \\
      &\iff \frac{a + b}{2} < b
\end{align}
$$

**Parte 2:**

Suponha que $\frac{a + b}{2} < b$.

Calculamos:

$$
\begin{align}
\frac{a + b}{2} < b &\iff a + b < 2b \\
                    &\iff a + b - b < b \\
                    &\iff a < b
\end{align}
$$

Portanto, pelas duas equivalências, concluímos a demonstração. $\blacksquare$

## Ex. 13

> [!example] Proposição
> Pelo menos um dos números reais $a_1$, $a_2$ e $a_3$ é maior ou igual à média desses números.

> **Negação:** Todos os $a_1$, $a_2$ e $a_3$ são menores que a média entre eles.

**Demonstração (por contradição):**

Sejam $a_1, a_2, a_3 \in \mathbb{R}$.

Suponha, por contradição, que todos os $a_1$, $a_2$ e $a_3$ são menores que a média entre eles, isto é:

$$
a_1 < \frac{a_1 + a_2 + a_3}{3} \land a_2 < \frac{a_1 + a_2 + a_3}{3} \land a_3 < \frac{a_1 + a_2 + a_3}{3}
$$

Somando as três inequações:

$$
\begin{align}
& a_1 + a_2 + a_3 < \frac{a_1 + a_2 + a_3}{3} + \frac{a_1 + a_2 + a_3}{3} + \frac{a_1 + a_2 + a_3}{3} \\
\iff& a_1 + a_2 + a_3 < 3 \cdot \frac{a_1 + a_2 + a_3}{3} \\
\iff& a_1 + a_2 + a_3 < a_1 + a_2 + a_3
\end{align}
$$

Chegamos a um absurdo.

Logo, pelo menos um dos números reais $a_1$, $a_2$ e $a_3$ é maior ou igual à média entre eles. $\blacksquare$

## Ex. 14

> [!example] Proposição
> O produto de dois números irracionais é irracional.

**Refutação:**

Vamos refutar essa afirmação por meio de um contra-exemplo.

Tome o número $\sqrt{2}$. Veja que:

$$
\sqrt{2} \cdot \sqrt{2} = 2
$$

Como $\sqrt{2}$ é irracional e o produto entre $\sqrt{2}$ e $\sqrt{2}$ é $2 \in \mathbb{Q}$, logo a afirmação é falsa. $\blacksquare$

## Ex. 15

> [!example] Proposição
> Para todo $n$ inteiro, as seguintes afirmações são equivalentes:
> - $n$ é par;
> - $n + 1$ é ímpar;
> - $3n + 1$ é ímpar;
> - $3n$ é par.

**Demonstração:**

Seja $n \in \mathbb{Z}$.

Separo a cadeia de equivalências em três equivalências, e cada equivalência em duas partes:

**1. $n$ é par se, e somente se, $n + 1$ é ímpar:**

**Parte 1:**

Suponha que $n$ é par.

Por definição, existe $k \in \mathbb{Z}$ tal que $n = 2k$.

Note que:

$$
n = 2k \iff n + 1 = 2k + 1
$$

Logo $n + 1$ é ímpar.

**Parte 2:**

Suponha que $n + 1$ é ímpar.

Por definição, existe $p \in \mathbb{Z}$ tal que $n + 1 = 2p + 1$.

Veja que:

$$
n + 1 = 2p + 1 \iff n = 2p
$$

Logo $n$ é par.

**2. $n$ é par se, e somente se, $3n + 1$ é ímpar:**

**Parte 1:**

Suponha que $n$ é par.

Por definição, existe $k \in \mathbb{Z}$ tal que $n = 2k$.

Note que:

$$
\begin{align}
n = 2k &\iff 3n = 6k \\
       &\iff 3n + 1 = 6k + 1 \\
       &\iff 3n + 1 = 2(3k) + 1
\end{align}
$$

Logo $3n + 1$ é ímpar.

**Parte 2:**

Suponha que $3n + 1$ é ímpar.

Por definição, existe $p \in \mathbb{Z}$ tal que $3n + 1 = 2p + 1$.

Observe que:

$$
3n + 1 = 2p + 1 \iff 3n = 2p
$$

Sabemos que $n$ é inteiro, então $3n$ deve ser múltiplo de $3$. Logo o lado direito também deve ser, ou seja, $3$ divide $2p$. Como $3$ não divide $2$, necessariamente $3$ divide $p$.

Sendo assim, existe $t$ inteiro tal que $p = 3t$. Substituindo na equação:

$$
\begin{align}
3n = 2p &\iff 3n = 2(3t) \\
        &\iff 3n = 3(2t) \\
        &\iff n = 2t
\end{align}
$$

Logo $n$ é par.

**3. $n$ é par se, e somente se, $3n$ é par:**

**Parte 1:**

Suponha que $n$ é par.

Por definição, existe $k \in \mathbb{Z}$ tal que $n = 2k$.

Calculamos

$$
\begin{align}
n = 2k &\iff 3n = 6k \\
       &\iff 3n = 2(3k)
\end{align}
$$

Logo $3n$ é par.

**Parte 2:**

Suponha que $3n$ é par.

Por definição, existe $p \in \mathbb{Z}$ tal que $3n = 2p$.

Logo $3$ divide $2p$. Como $3$ não divide $2$, então $3$ divide $p$.

Desse modo, existe $t$ inteiro tal que $p = 3t$. Substituindo:

$$
\begin{align}
3n = 2p &\iff 3n = 2(3t) \\
        &\iff 3n = 3(2t) \\
        &\iff n = 2t
\end{align}
$$

Logo $n$ é par.

Portanto, pelas três equivalências, concluímos a demonstração. $\blacksquare$
