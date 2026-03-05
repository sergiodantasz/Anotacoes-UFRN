# Relembrando...

Sejam $P$ e $Q$ duas proposições.

$$
\text{Se $P$, então $Q$.}
$$

> $P$ é a hipótese, enquanto $Q$ é a conclusão.

Note que não estamos afirmando nem $P$ nem $Q$. Apenas garantimos que se temos $P$, então temos $Q$. **Se não temos $P$, não podemos dizer nada a respeito de $Q$.** É uma proposição condicional, só podemos concluir algo sobre $Q$ quando temos $P$.

# Demonstração Direta

A demonstração direta é usada quando supomos $P$ e chegamos a $Q$. Simplesmente:

$$
P \implies Q
$$

# Demonstração por Contraposição

Diferentemente da direta, a demonstração por contraposição nega tanto o antecedente quando o consequente e inverte a direção de inferência. A contrapositiva de $P \implies Q$ é:

$$
\lnot Q \implies \lnot P
$$

Neste caso, supomos $\lnot Q$ e chegamos a $\lnot P$.

# Definições

> [!info] Ímpar
> Um número $n$ é ímpar se, e somente se, existe um inteiro $k$ tal que $n = 2k + 1$.

> [!info] Par
> Um número $n$ é par se, e somente se, existe um inteiro $k$ tal que $n = 2k$.

> [!info] Quadrado Perfeito
> Um número $a$ é um quadrado perfeito se, e somente se, existe um inteiro $b$ tal que $a = b^2$.

> [!info] Racional
> Um número $n$ é racional se, e somente se, existem inteiros $p$ e $q$, com $q \neq 0$, tais que $n = \frac{p}{q}$.

# Exercícios

## Ex. 1

> [!example] Proposição
> Se $n$ é um inteiro ímpar, então $n^2$ é ímpar.

**Demonstração:**

Seja $n$ um inteiro ímpar.

Por definição de número ímpar, existe $k \in \mathbb{Z}$ tal que $n = 2k + 1$.

Calculamos:

$$
\begin{align}
n^2 &= (2k + 1)^2 \\
    &= 4k^2 + 2k + 1 \\
    &= 2(2k^2 + k) + 1
\end{align}
$$

Tome $t = 2k^2 + k$.

Como $t$ é inteiro e $n^2 = 2t + 1$, logo, por definição, $n^2$ é ímpar. $\blacksquare$

## Ex. 2

> [!example] Proposição
> Se os inteiros $m$ e $n$ são quadrados perfeitos, então $m \cdot n$ é um quadrado perfeito.

**Demonstração:**

Sejam $m$ e $n$ inteiros e quadrados perfeitos.

Por definição de quadrado perfeito, existem inteiros $k_1$ e $k_2$ tais que $m = k_1^2$ e $n = k_2^2$.

Calculamos:

$$
\begin{align}
m \cdot n &= k_1^2 \cdot k_2^2 \\
          &= (k_1 \cdot k_2)^2
\end{align}
$$

Tome $t = k_1 \cdot k_2$.

Como $t$ é inteiro e $m \cdot n = t^2$, logo, por definição, $m \cdot n$ é um quadrado perfeito. $\blacksquare$

## Ex. 3

> [!example] Proposição
> Se $n^2$ é par, então $n$ é par.

> **Contrapositiva:** Se $n$ é ímpar, então $n^2$ é ímpar.

**Demonstração (por contraposição):**

*Imediato. Já foi demonstrada no [[#Ex. 1]].* $\blacksquare$

## Ex. 4

> [!example] Proposição
> Para todo $n$ inteiro, se $3n + 2$ é ímpar, então $n$ é ímpar.

> **Contrapositiva:** Se $n$ é par, então $3n + 2$ é par.

**Demonstração (por contraposição):**

Seja $n$ inteiro e par.

Por definição de número par, existe $k \in \mathbb{Z}$ tal que $n = 2k$.

Calculamos:

$$
\begin{align}
3n + 2 &= 3(2k) + 2 \\
       &= 2(3k) + 2 \\
       &= 2(3k + 1)
\end{align}
$$

Tome $t = 3k + 1$.

Como $t$ é inteiro e $3n + 2 = 2t$, logo, por definição, $3n + 2$ é par. $\blacksquare$

## Ex. 5

> [!example] Proposição
> A soma de dois números racionais é racional.

**Demonstração:**

Sejam $x$ e $y$ racionais.

Por definição de número racional, existem $p$, $q$, $r$ e $s$ inteiros, com $q \neq 0$ e $s \neq 0$, tais que $x = \frac{p}{q}$ e $y = \frac{r}{s}$.

Calculamos:

$$
\begin{align}
x + y &= \frac{p}{q} + \frac{r}{s} \\
      &= \frac{ps}{qs} + \frac{rq}{qs} \\
      &= \frac{ps + rq}{qs}
\end{align}
$$

Tome $t = ps + rq$ e $z = qs$.

Como $t, z \in \mathbb{Z}$ e $x + y = \frac{t}{z}$, logo, por definição, $x + y$ é racional. $\blacksquare$

## Ex. 6

> [!example] Proposição
> Para todo $m, n, p \in \mathbb{Z}$, se $m + n$ e $n + p$ são pares, então $m + p$ é par.

**Demonstração:**

Sejam $m, n, p \in \mathbb{Z}$ tais que $m + n$ e $n + p$ são pares.

Por definição de número par, existem inteiros $k_1$ e $k_2$ tais que $m + n = 2k_1$ e $n + p = 2k_2$.

Calculamos:

$$
\begin{align}
(m + n) + (n + p) = 2k_1 + 2k_2 &\iff m + p + 2n = 2k_1 + 2k_2 \\
                                &\iff m + p = 2k_1 + 2k_2 - 2n \\
                                &\iff m + p = 2(k_1 + k_2 - n)
\end{align}
$$

Tome $t = k_1 + k_2 - n$.

Como $t$ é inteiro e $m + p = 2t$, logo, por definição, $m + p$ é par. $\blacksquare$

## Ex. 7

> [!example] Proposição
> O produto de dois números ímpares é ímpar.

**Demonstração:**

Sejam $x$ e $y$ inteiros ímpares.

Por definição de número ímpar, existem $k_1$ e $k_2$ inteiros tais que $x = 2k_1 + 1$ e $y = 2k_2 + 1$.

Calculamos:

$$
\begin{align}
x \cdot y &= (2k_1 + 1)(2k_2 + 1) \\
          &= 4k_1k_2 + 2k_1 + 2k_2 + 1 \\
          &= 2(2k_1k_2 + k_1 + k_2) + 1
\end{align}
$$

Tome $t = 2k_1k_2 + k_1 + k_2$.

Como $t \in \mathbb{Z}$ e $x \cdot y = 2t + 1$, logo, por definição, $x \cdot y$ é ímpar. $\blacksquare$

## Ex. 8

> [!example] Proposição
> Para todo $m, n \in \mathbb{Z}$, se $m \cdot n$ é par, então $m$ é par ou $n$ é par.

> **Contrapositiva:** Para todo $m, n \in \mathbb{Z}$, se $m$ é ímpar e $n$ é ímpar, então $m \cdot n$ é ímpar.

**Demonstração (por contraposição):**

*Imediato. Já foi demonstrada no [[#Ex. 7]].* $\blacksquare$

## Ex. 9

> [!example] Proposição
> O produto de dois racionais é racional.

**Demonstração:**

Sejam $x$ e $y$ racionais.

Por definição de número racional, existem $p$, $q$, $r$ e $s$ inteiros, com $q \neq 0$ e $s \neq 0$, tais que $x = \frac{p}{q}$ e $y = \frac{r}{s}$.

Calculamos:

$$
\begin{align}
x \cdot y &= \frac{p}{q} \cdot \frac{r}{s} \\
      &= \frac{p \cdot r}{q \cdot s}
\end{align}
$$

Tome $t = p \cdot r$ e $z = q \cdot s$.

Como $t, z \in \mathbb{Z}$ e $x \cdot y = \frac{t}{z}$, logo, por definição, $x \cdot y$ é racional. $\blacksquare$

## Ex. 10

> [!example] Proposição
> Dados $x, y, z \in \mathbb{Z}$, se $x + y + z$ é ímpar, então pelo menos um dentre $x$, $y$ e $z$ é ímpar.

> **Contrapositiva:** Dados $x, y, z \in \mathbb{Z}$, se $x$, $y$ e $z$ são pares, então $x + y + z$ é par.

**Demonstração (por contraposição):**

Sejam $x$, $y$ e $z$ pares.

Por definição de número par, existem $k_1$, $k_2$ e $k_3$ inteiros tais que $x = 2k_1$, $y = 2k_2$ e $z = 2k_3$.

Calculamos:

$$
\begin{align}
x + y + z &= 2k_1 + 2k_2 + 2k_3 \\
          &= 2(k_1 + k_2 + k_3)
\end{align}
$$

Tome $t = k_1 + k_2 + k_3$.

Como $t$ é inteiro e $x + y + z = 2t$, logo, por definição, $x + y + z$ é par. $\blacksquare$
