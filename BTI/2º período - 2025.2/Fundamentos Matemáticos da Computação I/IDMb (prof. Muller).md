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

Note que $Ka = a^n \implies K = a^{n-1}$. Logo os valores possíveis de $K$ são $\{1,2,3,\ldots,a^{n-1}\}$.

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

Seja $R = \{r_1,r_2,r_3,\ldots,r_{\phi(m)}\}$ o conjunto dos coprimos com $m$. Considere o conjunto $S = \{ar_1,ar_2,ar_3,\ldots,ar_{\phi(m)}\}$.

Suponha, por absurdo, que $ar_i \equiv ar_j \pmod m$, para algum $i \neq j$. Então:

$$
\displaylines{
\begin{align*}
a(r_i - r_j) \equiv 0 \pmod m
&\implies r_i - r_j \equiv 0 \pmod m \qquad (\text{pois existe $a^{-1}$}) \\
&\implies r_i \equiv r_j \pmod m
\end{align*}
}
$$

O que é um absurdo; logo todos os elementos de $S$ são distintos módulo $m$.

Como $|R| = |S|$, então os conjuntos $R$ e $S$ possuem os mesmos elementos módulo $m$.

Multiplicando os termos dos conjuntos, teremos:

$$
\displaylines{
\begin{align*}
& (ar_1)(ar_2)\ldots(ar_{\phi(m)}) \equiv r_1r_2\ldots r_{\phi(m)} \pmod m \\
\iff& a^{\phi(m)}(r_1r_2\ldots r_{\phi(m)}) \equiv r_1r_2\ldots r_{\phi(m)} \pmod m \\
\iff& a^{\phi(m)} \equiv 1 \pmod m
\end{align*}
}
$$

Portanto, $a^{\phi(m)} \equiv 1 \pmod m$. ∎

No caso específico em que o módulo é um número primo $p$, teremos que:

$$
\displaylines{
\begin{align*}
a^{\phi(p)} \equiv 1 \pmod p
& \iff a^{p - 1} \equiv 1 \pmod p \\
& \iff a^p \equiv a \pmod p
\end{align*}
}
$$

Neste caso, chegamos ao Pequeno Teorema de Fermat.

# Números Racionais

Importaremos quase tudo de *Int*.

**Estrutura de $\mathbb{Q}$:** ($\mathbb{Q}$; 0, 1, +, -, ·, >, Pos)

**⛤ Com isso, ganhamos:**
- Açúcar sintático para frações: $\frac{a}{b} \iff a \cdot b^{-1}$.
- QM-Inv: Para todo $a \neq 0$, existe $a^{-1}$ tal que $a \cdot a^{-1} = 1$.

**✞ O que perdemos:**
- Princípio da Boa Ordem (PBO).

Seja $A = \{x \in \mathbb{Q} \mid x > 3\}$, quem é o menor elemento de $A$?
*Não dá pra saber.*

## Definição

Um número $a$ é dito racional se, e somente se, existirem inteiros $p$ e $q$, com $q \neq 0$, tais que $a = \frac{p}{q} = p \cdot q^{-1}$.

> [!important] Argumento de George Cantor
> Embora pareça contra-intuitivo à primeira vista, $\mathbb{Q}$ é enumerável. Isso significa que podemos estabelecer uma bijeção (correspondência um-para-um) entre os racionais e os naturais.

## Fração Irredutível

**Teorema:** Seja $a$ racional, então existem inteiros $p$ e $q$, com $q \neq 0$, tais que $a = \frac{p}{q}$ e $mdc(p,q) = 1$.

Seja $a = \frac{p}{q}$ em que $mdc(p,q) \neq 1$. Logo $a = \frac{p'k}{q'k} = \frac{p'}{q'}$, com $k = mdc(p,q)$.

Suponha, por absurdo, que $mdc(p',q') = d > 1$. Isso significa que $d$ divide $p'$ e $d$ divide $q'$, ou seja, $p' = dm$ e $q' = dn$. Substituindo na equação original, teremos:

$$
a = \frac{p'k}{q'k} = \frac{(dm)k}{(dn)k} = \frac{(dk)m}{(dk)n} = \frac{p}{q}
$$

Isso implica que $dk$ é um divisor comum de $p$ e de $q$. Como $d > 1$, então $dk > k$. Ora, isso é um absurdo! Pois definimos $k = mdc(p,q)$, e não pode existir um divisor comum $dk$ maior que $k$. Logo a suposição de que $d > 1$ é falsa. Concluímos que $mdc(p',q') = 1$.

Portanto, $a = \frac{p'}{q'}$ é uma fração irredutível. ∎

---

> [!question] Questão norteadora
> $\sqrt{2}$ é racional? Como demonstrar que não?

**Teorema:** $\sqrt{2}$ é irracional.

Vamos demonstrar que $\sqrt{2}$ é irracional. Suponha, por absurdo, que existe uma fração irredutível que represente $\sqrt{2}$.

Seja $\sqrt{2} = \frac{a}{b}$, com $a$ e $b$ inteiros tais que $b \neq 0$. Disso segue que $2 = \frac{a^2}{b^2} \implies 2b^2 = a^2$. Logo $a^2$ é um número par. Calculemos:

$$
\displaylines{
\begin{align*}
2 \mid a^2
&\implies 2 \mid a \cdot a \\
&\implies 2 \mid a \lor 2 \mid a \\
&\implies 2 \mid a
\end{align*}
}
$$

Logo $a$ também é par. Sendo assim, existe $k$ inteiro tal que $a = 2k$.

Observe o seguinte:

$$
\displaylines{
\begin{align*}
2b^2 = a^2
&\implies 2b^2 = (2k)^2 \\
&\implies 2b^2 = 4k^2 \\
&\implies b^2 = 2k^2
\end{align*}
}
$$

Analogamente, temos que $b^2$ e $b$ são pares. Sendo assim, $b = 2m$, para algum $m$ inteiro.

Agora note que $\sqrt{2} = \frac{a}{b} = \frac{2k}{2m} = \frac{k}{m}$. Veja que não existe uma fração irredutível que represente $\sqrt{2}$, pois tanto o numerador quanto o denominador são pares. Logo, a suposição inicial é, de fato, um absurdo.

Portanto, $\sqrt{2}$ é irracional. ∎

---

**Teorema:** Seja $p$ primo. Então $\sqrt{p}$ é irracional.

Suponha, por absurdo, que $\sqrt{p}$ é racional. Logo $\sqrt{p} = \frac{a}{b}$, com $a$ e $b$ inteiros, é uma fração irredutível. Teremos:

$$
\displaylines{
\begin{align*}
\sqrt{p} = \frac{a}{b}
&\implies p = \frac{a^2}{b^2} \\
&\implies pb^2 = a^2 \\
&\implies p \mid a \\
&\implies a = kp, \quad k \in \mathbb{Z}
\end{align*}
}
$$

Substituindo, vamos ter o seguinte:

$$
\displaylines{
\begin{align*}
pb^2 = a^2
&\implies pb^2 = (kp)^2 \\
&\implies pb^2 = k^2p^2 \\
&\implies b^2 = k^2p \\
&\implies p \mid b
\end{align*}
}
$$

Se $p \mid a$ e $p \mid b$, então a fração $\frac{a}{b}$ não é irredutível, o que é um absurdo.

Portanto, toda raiz quadrada de um número primo é racional. ∎

## Conjuntos Notáveis

> Vamos abortar a ideia padrão dos **conjuntos contidos em outros** que conhecemos. Por exemplo, *5 : Int* é diferente de *5 : Real*. Adotemos, então, a ideia de que $\mathbb{R}_\mathbb{N} \subset \mathbb{R}_\mathbb{Z} \subset \mathbb{R}_\mathbb{Q} \subset \mathbb{R}$.

### Números Algébricos

São números que podem ser obtidos como raízes de um polinômio de coeficientes inteiros.

Inclui:
- Racionais;
- Alguns irracionais (radiciação).

*Ex.:*
$x = \frac{a}{b} \implies bx - a = 0$
$x^2 - 2 = 0 \implies x^2 = 2 \implies x = \pm \sqrt{2}$

### Números Transcendentais

São números que não podem ser obtidos como raízes de um polinômio de coeficientes inteiros.

*Ex.:* $\pi$, $e$, $e^\pi$.

### Números Computáveis

São números que podem ser aproximados até a precisão desejada a partir de um algoritmo computacional.

A maioria dos números reais **não é computável**, porque existem contáveis algoritmos, mas incontáveis números reais (infinitos).

*Ex.:* todos os números algébricos e muitos transcendentais importantes.

# Números Reais

Especificação: importar de ℚ
(ℚ; 0, 1, +, -, ·, <, Pos)

**O que ganhamos:**

- Radiciação (até certo ponto)
- Reta real
- Irracionais

**O que eu perco:**

- Frações irredutíveis : √(2)/2 o raiz de 2 nao eh par

**Máximo e Mínimo:**

Sejam a, b ∈ ℝ, define-se:

max(a,b) =
- a, se a > b
- b, caso contrário

min(a,b) =
- a, se a < b
- b, caso contrário

**Módulos:**

|a| =
- a, se ≥ 0
- -a, caso contrário

**Piso/Teto:**

(ceiling)
$\lceil a \rceil$: teto de $a$
$\lceil a \rceil ≝ min(\{x \in \mathbb{R_\mathbb{Z}} \mid x \geq a\})$

(floor)
$\lfloor a \rfloor$: piso de $a$
$\lfloor a \rfloor ≝ max(\{x \in \mathbb{R_\mathbb{Z}} \mid x \leq a\})$

---

N, Z e Q sao enumeráveis. Mas e o R? **Não!**

Demons.:

Vamos provar que (0,1) não é enumerável (ordenável). [Se (0,1) não é enumerável, então R não será]
Demonstração por absurdo (Diagonal de Cantor):
Suponha que (0,1) é um conjunto enumerável, então existe uma forma de ordenar estes números (denotados $r_i$, com $i \in \mathbb{N}$).
$r_1 = 0,a_1a_2a_3\ldots$
$r_2 = 0,b_1b_2b_3\ldots$
$r_3 = 0,c_1c_2c_3\ldots$
$r_4 = 0,d_1d_2d_3\ldots$
$\vdots$
diagonal: $0,a_1b_2c_3d_4$
Construir um número que não compartilha nenhum dígito com a diagonal:
Agora construímos um número $n$ tal que $n = 0,\alpha_1\beta_2\gamma_3\delta_4$ em que $\alpha_1 \neq a_1$, $\beta_2 \neq b_2$, $\gamma_3 \neq c_3$, $\delta_4 \neq d_4$.
$n$ está na enumeração? Não. Absurdo!

**Curiosidade:**

$|(0,1)| = |\mathbb{R}|$

---

**Sequências de Números Reais:**

Uma sequência de números reais é uma listagem ordenada de números reais:
$x_0,x_1,x_2,x_3,\ldots$
Notação: $(x_n)^\infty_{n=0}$ ou $(x_n)_{n \in \mathbb{N}}$ ou $(x_n)_n$

**Igualdade de Sequências**

Sejam duas sequências $(x_n)_{n \in \mathbb{N}}$ e $(y_n)_{n \in \mathbb{N}}$.
$$
(x_n)_{n \in \mathbb{N}} = (y_n)_{n \in \mathbb{N}} \iff (\forall i)[x_i = y_i]
$$

Ex:
$(x_n)_n$ : 1/2, 3/4, 1, -3, ...
$(y_n)_n$ : 1/2, 3/4, 8, -3, ...
não são iguais por que $x_3 \neq y_3$

Obs.: sequências não são conjuntos!!!

**Sequências Recursivas:**

É uma sequência em que o valor de cada elemento depende de seus antecessores.

Ex.:
$(x_n)_{n=0}^\infty$  em que:
- $x_0 = 3$
- $x_n = x_{n-1} + 5$, para $n > 0$

**Sequência de Fibonacci**

$x_0 = 1$
$x_1 = 1$
$x_n = x_{n-1} + x_{n-2}$
1,1,2,3,5,8,13,21,...

**Sequências Crescentes e Decrescentes**

$(x_n)_{n}^\infty$ é crescente se, e somente se, $(\forall n)[x_{n+1} \geq x_n]$
$(x_n)_{n}^\infty$ é decrescente se, e somente se, $(\forall n)[x_{n+1} \leq x_n]$

Obs.:
Seja $(x_n)_{n=0}^\infty$ crescente.
Podemos dizer que $x_n \to \infty$ quando $n \to \infty$?
*Não necessariamente!*

Seja a sequência $(x_n)^\infty_{n=0}$ em que $x_n = \frac{1}{n+1}$.
1,1/2, 1/3,1/4,1/5,... Sequer alcança zero

Seja a sequência $(x_n)^\infty_{n=0}$ em que $x_n = \frac{-1}{n+1}$.
-1,-1/2,-1/3,-1/4,... nunca alcança zero, mas é sempre crescente

**Sequências com Cotas**

i) cota inferior

$C$ é uma cota inferior de $(x_n)_n$ ⇐≝⇒ (∀n)[c ≤ x_n]

> Ínfimum: melhor (maior) cota inferior

Ex.:
$C = 0$
$0 = Inf(x_n)_n$

ii) cota superior

$C$ é uma cota superior de $(x_n)_n$ ⇐≝⇒ (∀n)[c ≥ x_n]

**Infimum**

$M$ é infimum de $(x_n)_{n=0}^\infty$ ⇔ (∀n)[M ≤ x_n] ∧ (∀c)[c é cota de (x_n)n ⇒ M ≥ c]
                      M é cota de $(x_n)_n$              M é a melhor cota

**Supremum**

> Supremum: melhor (menor) cota superior

$M$ é supremum de $(x_n)_{n=0}^\infty$ ⇔ (∀n)[M ≥ x_n] ∧ (∀c)[c é cota de (x_n)n ⇒ M ≤ c]

**Ordem (Point-wise)**

Sejam duas sequências $(x_n)_{n=0}^\infty$ e $(y_n)_{n=0}^\infty$.
Dizemos que
$$
(x_n)_n > (y_n)_n \iff (\forall n)[x_n > y_n]
$$

ex.:
[add duas sequencias]
