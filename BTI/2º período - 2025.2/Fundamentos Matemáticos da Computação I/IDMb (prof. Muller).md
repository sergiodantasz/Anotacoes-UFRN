# Função Totiente de Euler

> A Função Totiente de Euler conta quantos números inteiros positivos menores ou iguais a um dado número $n$ são primos entre si com $n$.

Seja $n : Int$ tal que $n > 0$.

$$
\phi(n) ≝ |\{i \in \{1,2,3\ldots,n\} \mid mdc(i,n) = 1\}|
$$

>Os "$||$" de fora significam "cardinalidade do conjunto". O conjunto de fora significa "conjunto de todos os coprimos de $n$".

*Ex.:* O totiente de 14 é 6 (6 primos no conjunto).

> [!quote] Números coprimos
> Dois números são **coprimos** se, e somente se, o máximo divisor comum entre eles é 1.

## Propriedades

**Propriedade 1:** Seja $p$ inteiro. Se $p$ é primo, então $\phi(p) = p - 1$.

Seja $p$ primo.
Logo para todo $i$ tal que $1 \leq i < p$, segue que $mdc(i,p) = 1$, pois nenhum $i$ compartilha outro divisor com $p$ além do próprio 1.
Se $i = p$, então $mdc(i,p) = p$. Ou seja, $i = p$ não pertence ao conjunto de coprimos de $p$.
Portanto, $\phi(p) = p - 1$. ∎

---

> [!question] Questão norteadora
> Quantos múltiplos de $a$ existem em $\{1,2,3,\ldots,a^n\}$?

**Lema:** Sejam $a$ e $n$ inteiros tais que $a, n \geq 1$. O conjunto $\{1,2,3,\ldots,a^n\}$ possui exatamente $a^{n-1}$ múltiplos de $a$.

Seja $a$ inteiro.
Observe que os múltiplos de $a$ podem ser escritos na forma $Ka$, com $K \geq 1$. Logo os múltiplos de $a$ estão no conjunto $\{a,2a,3a,\ldots,Ka\}$, de modo que $Ka = a^n$.
Note que $Ka = a^n \implies K = a^{n-1}$.
Logo os valores possíveis de $K$ são $\{1,2,3,\ldots,a^{n-1}\}$.
Portanto, existem exatamente $a^{n-1}$ múltiplos de $a$ no conjunto $\{1,2,3,\ldots,a^n\}$. ∎

---

**Propriedade 2:** Sejam $p$ e $a$ inteiros tais que $a \geq 1$. Se $p$ é primo, então $\phi(p^a) = p^a - p^{a - 1}$.

Seja $p$ primo.
Logo, pelo lema acima, o conjunto $\{1, \ldots, p^a\}$ — com $a \geq 1$ — contém exatamente $p^{a-1}$ múltiplos de $p$.
Além disso, um inteiro $m$ com $1 \leq m \leq p^a$ não é coprimo com $p^a$ se, e somente se, $p \mid m$, pois $p$ é o único primo que divide $p^a$. Assim, os inteiros não coprimos com $p^a$ são precisamente os múltiplos de $p$.
Como o número total de inteiros em $\{1, \ldots, p^a\}$ é $p^a$, o totiente de $p^a$ é a diferença entre o número total de inteiros e o número de múltiplos de $p$, ambos relativos ao dado conjunto.
Portanto, $\phi(p^a) = p^a - p^{a-1}$. ∎

*Ex.:*
Sejam $p$ primo e $k \in \mathbb{Z}$.
Calculemos o somatório de $\phi(p^i)$ com $i = 0$ até $k$:

$$
\displaylines{
\begin{align*}
\sum_{i=0}^k{\phi(p^i)} &= \phi(p^0) + \sum_{i=1}^k{\phi(p^i)} \\
&= \phi(1) + \sum_{i=1}^k{\left(p^i - p^{i - 1}\right)} \\
&= 1 + \sum_{i=1}^k{p^i} - \sum_{i=1}^k{p^{i - 1}} \\
&= 1 + \sum_{i=1}^k{p^i} - \sum_{i=0}^{k - 1}{p^i} &\quad (\text{Index Shift}) \\
&= 1 + p^k + \sum_{i=1}^{k-1}{p^i} - p^0 - \sum_{i=1}^{k - 1}{p^i} \\
&= 1 + p^k - p^0 \\
&= p^k
\end{align*}
}
$$

---

**Teorema:** Sejam $a$ e $b$ inteiros. Se $mdc(a,b) = 1$, então $\phi(a \cdot b) = \phi(a) \cdot \phi(b)$.

> [!warning] Nota
> O professor não fez demonstração deste teorema.

---

**Teorema de Euler:** Sejam $a, m \in \mathbb{Z}$ com $mdc(a,m) = 1$. Então $a^{\phi(m)} \equiv 1 \pmod m$.



Dem.:

Seja o conjunto $R = \{r_1,r_2,r_3,\ldots,r_{\phi(m)}\}$. [conjunto dos coprimos de m]
Como $mdc(a,m) = 1$, então os elementos do conjunto $S = \{ar_1,ar_2,ar_3,\ldots,ar_{\phi(m)}\}$ são coprimos com m.

OBS.:
Se $ar_i \equiv ar_j \pmod m$, então:

$$
\displaylines{
\begin{align*}
a(r_i - r_j) \equiv 0 \pmod m
&\iff r_i - r_j \equiv 0 \pmod m \qquad (pois\ existe\ a^{-1}) \\
&\iff r_i \equiv r_j \pmod m \qquad (ABSURDO)
\end{align*}
}
$$

Então os elementos de $S$ são distintos de $mod\ m$.

Como $|R| = |S|$, então os conjuntos $R$ e $S$ possuem os mesmos elementos $mod\ m$.
Multiplicando os termos dos conjuntos:
$$
\displaylines{
\begin{align*}
& (ar_1)(ar_2)\ldots(ar_{\phi(m)}) \equiv r_1r_2\ldots r_{\phi(m)} \pmod m \\
\iff& a^{\phi(m)}(r_1r_2\ldots r_{phi(m)}) \equiv r_1r_2\ldots r_{\phi(m)} \pmod m \\
\iff& a^{\phi(m)} \equiv 1 \pmod m
\end{align*}
}
$$

trocar n por m

---
PTF: Caso específico m = p primo

$$
\displaylines{
\begin{align*}
& a^{\phi(p)} \equiv 1 \pmod m \\
\iff& a^{p - 1} \equiv 1 \pmod m \\
\iff& a^p \equiv a \pmod m
\end{align*}
}
$$
