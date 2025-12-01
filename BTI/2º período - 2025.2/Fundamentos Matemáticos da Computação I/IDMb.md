# Função Totiente de Euler

> A Função Totiente de Euler conta quantos números inteiros positivos menores ou iguais a um dado número $n$ são primos entre si com $n$.

Seja $n$ : Int tal que $n > 0$.

$$
\phi(n) \overset{\mathrm{def}}{=} |\{i \in \{1,2,3\ldots,n\} \mid mdc(i,n) = 1\}|
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

> Importaremos quase tudo de $\mathbb{Z}$.

**Especificação:** ($\mathbb{Q}$; 0, 1, +, -, ·, >, Pos)

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

> Vamos importar de $\mathbb{Q}$.

**Especificação:** ($\mathbb{R}$; 0, 1, +, -, ·, <, Pos)

**⛤ O que ganhamos:**
- Radiciação (até certo ponto);
- Reta real;
- Conjunto dos números irracionais.

**✞ O que perdemos:**
- Frações irredutíveis.

> [!question] Perdemos acesso às frações irredutíveis?
> Muller afirma que ao especificarmos os números reais, não podemos mais utilizar frações irredutíveis. Ele usou como exemplo a fração $\frac{\sqrt{2}}{2}$ e disse que não podíamos reduzir ela por causa da raiz quadrada no numerador; isso faz sentido. Mas o problema é que isso sequer é uma fração racional: em sua definição, tanto o numerador quanto o denominador devem ser números inteiros. E então, será que de fato perdemos o acesso?!

## Máximo e Mínimo

Sejam $a, b \in \mathbb{R}$.

$$
\displaylines{
\max(a,b) = \left\{
\begin{array}{l}
a, &\quad \text{se } a > b \\
b, &\quad \text{se } a \leq b
\end{array}
\right.
}
$$

$$
\displaylines{
\min(a,b) = \left\{
\begin{array}{l}
a, &\quad \text{se } a < b \\
b, &\quad \text{se } a \geq b
\end{array}
\right.
}
$$

## Módulo

Seja $a \in \mathbb{R}$.

$$
\displaylines{
|a| = \left\{
\begin{array}{l}
a, &\quad \text{se } a \geq 0 \\
-a, &\quad \text{se } a < 0
\end{array}
\right.
}
$$

## Teto e Piso

Seja $a \in \mathbb{R}$.

**Ceiling:**

$$
\lceil a \rceil = \min(\{x \in \mathbb{R}_\mathbb{Z} \mid x \geq a\})
$$

**Floor:**

$$
\lfloor a \rfloor = \max(\{x \in \mathbb{R}_\mathbb{Z} \mid x \leq a\})
$$

## Os reais são enumeráveis?

Assim como $\mathbb{Q}$, $\mathbb{Z}$ e $\mathbb{N}$ também são enumeráveis. Mas e o $\mathbb{R}$? *Não!*

Vamos demonstrar que $\mathbb{R}$ não é enumerável. Para tanto, basta mostrarmos que $(0,1)$ é não enumerável.

Suponha, por contradição, que $(0,1)$ é um conjunto enumerável. Então existe uma forma de ordenar estes números, denotados $r_i$, com $i \in \mathbb{N}$:

$$
\displaylines{
\begin{align*}
&r_1 = 0{,}a_1a_2a_3\ldots \\
&r_2 = 0{,}b_1b_2b_3\ldots \\
&r_3 = 0{,}c_1c_2c_3\ldots \\
&\vdots
\end{align*}
}
$$

Tome a diagonal $d = 0{,}a_1b_2c_3d_4\ldots$. Vamos construir um novo número que não compartilha nenhum dígito com a diagonal.

Seja $x$ tal que $x = 0{,}\alpha_1\beta_2\gamma_3\delta_4\ldots$, em que $\alpha_1 \neq a_1$, $\beta_2 \neq b_2$, $\gamma_3 \neq c_3$, $\delta_4 \neq d_4$ e assim por diante, de forma análoga. Ou seja, isso implica que $n$ não está na enumeração, contradizendo a hipótese inicial.

Portanto, $\mathbb{R}$ não é enumerável. ∎

> **Curiosidade:** $|(0,1)| = |\mathbb{R}|$

## Sequências

Uma sequência de números reais é uma listagem ordenada de números reais:

$$
x_0,x_1,x_2,x_3,\ldots
$$

**Notação:**
- $(x_n)^\infty_{n=0}$
- $(x_n)_{n \in \mathbb{N}}$
- $(x_n)_n$

### Igualdade de Sequências

Sejam duas sequências $(x_n)_{n \in \mathbb{N}}$ e $(y_n)_{n \in \mathbb{N}}$.

$$
(x_n)_{n \in \mathbb{N}} = (y_n)_{n \in \mathbb{N}} \iff (\forall i)[x_i = y_i]
$$

> Sequências **não** são conjuntos!!!

*Ex.:*
$(x_n)_n$: 1/2, 3/4, 1, -3, ...
$(y_n)_n$: 1/2, 3/4, 8, -3, ...
Não são iguais por que $x_3 \neq y_3$.

### Sequências Recursivas

É uma sequência em que o valor de cada elemento depende de seus antecessores.

*Ex.:*
Seja a sequência $(x_n)_{n=0}^\infty$, em que:
- $x_0 = 3$;
- $x_n = x_{n-1} + 5$, para $n > 0$.

### Sequência de Fibonacci

É uma sequência em que cada valor é a soma dos dois elementos imediatamente anteriores (a partir do terceiro elemento).

$x_0 = 1$
$x_1 = 1$
$x_n = x_{n-1} + x_{n-2}$

Temos, portanto:

$$
1,1,2,3,5,8,13,21,...
$$

### Sequências Crescentes e Decrescentes

$$
(x_n)_{n=0}^\infty \text{ crescrente} \iff (\forall n)[x_{n+1} \geq x_n]
$$

$$
(x_n)_{n=0}^\infty \text{ decrescrente} \iff (\forall n)[x_{n+1} \leq x_n]
$$

---

Seja $(x_n)_{n=0}^\infty$ crescente. Podemos dizer que $x_n \to \infty$ quando $n \to \infty$?
*Não necessariamente!*

Seja a sequência $(x_n)^\infty_{n=0}$ em que $x_n = \frac{1}{n+1}$:

$$
1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \frac{1}{5}, \ldots
$$

Quando $n \to \infty$, temos que $x_n \to 0$; mas sequer alcança 0. Note também que essa sequência é decrescente.

Agora seja a sequência $(x_n)^\infty_{n=0}$ em que $x_n = \frac{-1}{n+1}$.

$$
-1, -\frac{1}{2}, -\frac{1}{3}, -\frac{1}{4}, -\frac{1}{5}, \ldots
$$

Essa, por sua vez, é sempre crescente, mas nunca alcança 0 e também não tende ao infinito quando $x \to \infty$.

### Sequências com Cotas

#### Cotas Inferior e Superior

$$
C \text{ é uma cota inferior de } (x_n)_n \iff (\forall n)[C \leq x_n]
$$

$$
C \text{ é uma cota superior de } (x_n)_n \iff (\forall n)[C \geq x_n]
$$

#### Infimum

Infimum é a melhor (maior) cota inferior de uma sequência.

> **Tipagem:** _ = inf _ : ExtReal ⨯ Set ExtReal → Prop

$$
\displaylines{
\begin{align*}
M \text{ é infimum de } (x_n)_n
&\iff M \text{ é cota inferior de } (x_n)_n \land M \text{ é a melhor cota inferior de } (x_n)_n \\
&\iff (\forall n)[M \leq x_n] \land (\forall c)[c \text{ é cota inferior de } (x_n)_n \implies M \geq c]
\end{align*}
}
$$

#### Supremum

Supremum é a melhor (menor) cota superior de uma sequência.

> **Tipagem:** _ = sup _ : ExtReal ⨯ Set ExtReal → Prop

$$
\displaylines{
\begin{align*}
M \text{ é supremum de } (x_n)_n
&\iff M \text{ é cota superior de } (x_n)_n \land M \text{ é a melhor cota superior de } (x_n)_n \\
&\iff (\forall n)[M \geq x_n] \land (\forall c)[c \text{ é cota superior de } (x_n)_n \implies M \leq c]
\end{align*}
}
$$

Tanto o *Infimum* quanto o *Supremum* podem ou não pertencer à sequência.

### Ordem (Point-wise)

Sejam duas sequências $(x_n)_{n=0}^\infty$ e $(y_n)_{n=0}^\infty$.

Dizemos que:

$$
(x_n)_n > (y_n)_n \iff (\forall n)[x_n > y_n]
$$

*Ex.:*
$(x_n)_n$: 1, 4, 5, 10, 12, 15, ...
$(y_n)_n$: 0, 2, 3, 8, 13, 14, ...
Perceba que $y_4 > x_4$, logo $(x_n)_n \not > (y_n)_n$.

### Conjunto Cotado

É um conjunto que possui cotas superiores e inferiores.

Se o conjunto $A$ não possuir cotas superiores:

$$
\operatorname{sup} A = \infty
$$

*Ex.:* $(\_, \infty)$

Se o conjunto $A$ não possuir cotas inferiores:

$$
\operatorname{inf} A = -\infty
$$

*Ex.:* $(-\infty,\_)$

> Se for somente superior ou inferior, chamamos de conjunto cotado superiormente/inferiormente.

## Reais Estendidos

$$
\overline{\mathbb{R}} = \{-\infty,\infty\} \cup \mathbb{R}
\qquad \text{ou} \qquad
\overline{\mathbb{R}} = [-\infty,\infty]
$$

**Propriedades:**
1. $a + \infty = \infty$;
2. $a + (-\infty) = -\infty$;
3. $\infty + (-\infty)$ é uma indeterminação;
4. $a \cdot \infty = \infty$, se $a > 0$;
5. $a \cdot \infty = -\infty$, se $a < 0$;
6. $0 \cdot \infty$ é uma indeterminação (se o zero vier de um limite);
7. $\infty \cdot \infty = \infty$;
8. $(-\infty) \cdot (-\infty) = \infty$;
9. $(-\infty) \cdot \infty = -\infty$.

## Distâncias

Seja $d$ : α ⨯ α → Real. Dizemos que $d$ é uma distância (métrica) no α se, e somente se, todas as propriedades a seguir são satisfeitas.

Sejam $x$, $y$, $z$ : α.

$$
\displaylines{
\begin{array}{l}
&(\text{D-Range}) & d(x,y) \geq 0 \\
&(\text{D-Sym}) & d(x,y) = d(y,x) \\
&(\text{D-Tri}) & d(x,y) \leq d(x,z) + d(z,y) \quad (\text{Desigualdade Triangular}) \\
&(\text{D-EqZero}) & d(x,x) = 0 \\
&(\text{D-ZeroEq}) & d(x,y) = 0 \implies x = y
\end{array}
}
$$

### Distância Euclidiana

$$
d(a,b) = |a - b|
$$

> **Tipagem:** $d$ : Real ⨯ Real → Real

### Distância Discreta

$$
\displaylines{
d_0(a,b) = \left\{
\begin{array}{l}
0, \quad \text{se } a = b \\
1, \quad \text{se } a \neq b
\end{array}
\right.
}
$$

> **Tipagem:** $d_0$ : Real ⨯ Real → Real

### ε-Perto

Sejam $x$, $y$, $\epsilon$ : Real com $\epsilon > 0$.

$$
x \text{ é $\epsilon$-Perto de } y \iff d(x,y) < \epsilon
$$

**Notação:** $x \sim_\epsilon y$

*Ex.:*
Sejam x = 4 e y = 5.
Se ε = 1/2, então 4 não é 1/2-Perto de 5 ($4 \sim_\frac{1}{2} 5$).
Se ε = 2, então 4 é 2-Perto de 5 ($4 \sim_2 5$).

### ε-Bola

Sejam um conjunto $A$ e um ponto $c \in A$.

$$
A \text{ é $\epsilon$-Bola de } c \iff A = \{x \mid x \sim_\epsilon c\}
$$

**Notação:** $B_\epsilon(c)$ ($\epsilon$ é o raio e $c$ é o centro)

*Ex.:*
Sejam $c = 5$ e $\epsilon = 3$.
Logo $B_3(5) = (2,8)$ (esse conjunto é 3-Bola de 5).

---

**Exemplo com Distância Euclidiana:**

$$
\displaylines{
\begin{align*}
B_\epsilon(c)
&= \{x \mid d(x,c) < \epsilon\} \\
&= \{x \mid |x - c| < \epsilon\}
\end{align*}
}
$$

Se $x - c \geq 0$, então $x - c < \epsilon \implies x < c + \epsilon$.
Se $x - c < 0$, então $-(x - c) < \epsilon \implies -x + c < \epsilon \implies x > c - \epsilon$.
Logo:

$$
\displaylines{
\begin{align*}
B_\epsilon(c)
&= \{x \mid c - \epsilon < x < c + \epsilon\} \\
&= (c - \epsilon, c + \epsilon)
\end{align*}
}
$$

---

**Exemplo com Distância Discreta:**

Seja $c = 3$.

Note que:

$$
B_\frac{1}{3}(3) = \left\{ x \mid d_0(x,3) < \frac{1}{3} \right\}
$$

Para entrar na bola, precisa valer $d_0(x,3) = 0$, porque $1 \not < \frac{1}{3}$. Isso só acontece quando $x = 3$. Então $B_\frac{1}{3}(3) = \{3\}$.

Agora, veja que:

$$
B_2(3) = \{x \mid d_0(x,3) < 2\}
$$

Ora, tanto $0 < 2$ quanto $1 < 2$, logo ambos os casos da distância discreta entram na bola. Então $B_2(3) = \mathbb{R}$.

#### Como representar um intervalo como uma bola?

> Faremos isso utilizando Distância Euclidiana.

Seja um intervalo $(a,b)$ (com $b > a$, por conveniência). Seja $c$ um ponto tal que $c = \frac{a + b}{2}$.

Perceba o seguinte:

$$
d(a,b) = 2\epsilon \implies \epsilon = \frac{d(a,b)}{2} = \frac{b - a}{2} \qquad (a - b < 0)
$$

Logo, podemos representar um intervalo como uma bola da seguinte forma:

$$
B_{\frac{b - a}{2}}\left(\frac{a + b}{2}\right)
$$

### Diâmetro

Sejam $A$ um conjunto de números reais e $S$ um número real.

$$
S = \operatorname{diam} A \iff S = \operatorname{sup}{\{d(a,b) \mid a, b \in A\}}
$$

O conjunto da direita é o conjunto que contém todas as distâncias entre os pontos $a$ e $b$, enquanto $S$ é a maior de todas as distâncias.

> **Obs.:** $\operatorname{diam} A = \infty \iff \operatorname{sup} A = \infty$

### Conjunto Cercado

Seja $A$ um conjunto.

$$
A \text{ é cercado} \iff (\exists c,m)[A \subseteq B_m(c)]
$$

Em outras palavras, $A$ é cercado se, e somente se, $A$ está contido em alguma bola.

### Novos Termos

Sejam $\phi$ : Real → Prop um predicado sobre reais e $(a_n)_n$ uma sequência de reais.

#### "Valores suficientemente grandes"

Dizemos que para valores suficientemente grandes de $n$, $\phi(a_n)$ é válido se, e somente se, a partir de um natural $N$, todos os $a_i$ ($i > N$) satisfazem $\phi(a_i)$.

$$
(\exists N)(\forall n \geq N)[\phi(a_n)]
$$

**Significa:** existe um valor $N$ que, para todo $n$ a partir de $N$, $\phi(a_n)$ é satisfeito.

*Ex.:*
Para valores suficientemente grandes, $2^n > n^4 > 8n$.
$\phi(n=1)$: $2^1 > 1^4 > 8 \cdot 1$ **(F)**
$\phi(n=2)$: $2^2 > 2^4 > 8 \cdot 2$ **(F)**
$\phi(n=3)$: $2^3 > 3^4 > 8 \cdot 3$ **(F)**
$\vdots$
$\phi(n=10)$: $2^{10} > {10}^4 > 8 \cdot 10$ **(F)**
$\vdots$
$\phi(n=20)$: $2^{20} > {20}^4 > 8 \cdot 20$ **(V)**

#### "Eventualmente"

$$
\text{Eventualmente } \phi((a_n)_n) \overset{\mathrm{def}}{\iff} (\exists N)[\phi((a_n)_{n \geq N})]
$$

> **Tipagem:** $\phi$ : Seq Real → Real

### Limite

Sejam $(a_n)_n$ : Seq Real e $l$ : Real.

Dizemos que $(a_n)_n$ tende ao $l$ (ou converge para $l$) se, e somente se, para qualquer bola de $l$, a sequência $(a_n)_n$ *eventualmente* fica dentro dela.

$$
(a_n)_n \to l \overset{\mathrm{def}}{\iff} (\forall \epsilon > 0)[\text{Eventualmente } d(l,a_n) < \epsilon]
$$

> **Tipagem:** $\_ \to \_$ : Seq Real ⨯ Real → Prop

**Notação:**
- $(a_n)_n \to l$
- $\lim_n a_n = l$
- $\lim (a_n)_n = l$

*Ex.:*
1/2, 1/4, 1/8, 1/16, 1/32, ... → 0

---

**Teorema:** $\lim \left(\frac{1}{2^{n+1}}\right)_n = 0$

Seja $\epsilon > 0$. Vamos demonstrar que existe $N$ tal que, para todo $n \geq N$, $d(l,a_n) < \epsilon$ — em outras palavras, eventualmente $d(l,a_n) < \epsilon$.

**Passo 1: Obter $N$ em função do $\epsilon$ dado.**

Vamos deduzir qual valor $N$ deve assumir. Para que $d(a_n,l) < \epsilon$ seja satisfeita, temos o seguinte:

$$
\displaylines{
\begin{align*}
d(a_n,l) < \epsilon
&\implies |a_n - l| < \epsilon \\
&\implies \left|\frac{1}{2^{n+1}} - 0\right| < \epsilon \qquad (l = 0) \\
&\implies \frac{1}{2^{n+1}} < \epsilon \\
&\implies \frac{1}{\epsilon} < 2^{n + 1} \\
&\implies \frac{1}{2\epsilon} < 2^n \\
&\implies \log_2{\left(\frac{1}{2\epsilon}\right)} < n
\end{align*}
}
$$

> Perceba que $\log_2{\frac{1}{2\epsilon}}$ não é um Int.

Tome, então, $N = \left\lceil \log_2{\left(\frac{1}{2\epsilon}\right)} \right\rceil$. Note que $N \geq \log_2{\left(\frac{1}{2\epsilon}\right)}$.

**Passo 2: Demonstrar que $\forall n \geq N$, temos que $d(a_n,l) < \epsilon$.**

Agora, suponha $n > N$. Calculamos:

$$
\displaylines{
\begin{align*}
\left\lceil  \log_2{\left(\frac{1}{2\epsilon}\right)} \right\rceil < n
&\implies  \log_2{\left(\frac{1}{2\epsilon}\right)} \leq \left\lceil  \log_2{\left(\frac{1}{2\epsilon}\right)} \right\rceil < n \\
&\implies  \log_2{\left(\frac{1}{2\epsilon}\right)} < n \\
&\implies \frac{1}{2\epsilon} < 2^n \\
&\implies \frac{1}{\epsilon} < 2^{n+1} \\
&\implies \frac{1}{2^{n+1}} < \epsilon \\
&\implies \frac{1}{2^{n+1}} - 0 < \epsilon \\
&\implies \left| \frac{1}{2^{n+1}} - 0 \right| < \epsilon \qquad \left(\text{pois $\frac{1}{2^{n+1}} - 0$ é positivo}\right) \\
&\implies |a_n - 0| < \epsilon \\
&\implies d(a_n,l) < \epsilon
\end{align*}
}
$$

Portanto, $\lim \left(\frac{1}{2^{n+1}}\right)_n = 0$. ∎

> [!warning] Está faltando algo?
> O teorema exige que a demonstração seja feita para $n \geq N$, mas Muller demonstrou para $n > M$. Isso está correto e é formalmente aceito? Se supormos $n \geq N$, concluímos que $d(a_n,l) \leq \epsilon$, e eu não faço a mínima ideia se isso é aceito. Uma possível solução para esse problema seria tomar $N = \left\lceil \log_2{\left(\frac{1}{\epsilon}\right)} \right\rceil$.

### Sequências Convergente e Divergente

$$
(a_n)_n \text{ é convergente} \overset{\mathrm{def}}{\iff} (\exists l)[(a_n)_n \to l]
$$

$$
(a_n)_n \text{ é divergente} \overset{\mathrm{def}}{\iff} (\nexists l)[(a_n)_n \to l]
$$

**Casos envolvendo $\infty$:**

$$
(a_n)_n \text{ diverge para } \infty \overset{\mathrm{def}}{\iff} (\forall M > 0)[\text{Eventualmente } (a_n)_n > M]
$$

> $(a_n)_n > M$ significa que todos os elementos da sequência são maiores que $M$. O resultado é análogo para $(<)$.

$$
(a_n)_n \text{ diverge para } -\infty \overset{\mathrm{def}}{\iff} (\forall M < 0)[\text{Eventualmente } (a_n)_n < M]
$$

---

**Teorema:** Seja $(a_n)_n$ em que $a_n = (-1)^n$. Então $(a_n)_n$ diverge.

Suponha, por absurdo, que $(a_n)_n \to l$, para algum $l$ : Real (ou seja, eventualmente $d(a_n,l) < \epsilon$).

Tome $d(a_n,a_{n+1}) = 2$. Pela Desigualdade Triangular:

$$
d(a_n,a_{n+1}) \leq d(a_n,l) + d(l,a_{n+1}) \iff 2 \leq d(a_n,l) + d(l,a_{n+1})
$$

Sabemos que $d(a_n,l) < \epsilon$ e $d(l,a_{n+1}) < \epsilon$. "Somando" as duas equações, teríamos, então, $d(a_n,l) + d(l,a_{n+1}) < 2\epsilon$. Sendo assim, por transitividade, segue que $2 < 2\epsilon \iff 1 < \epsilon$. Isto é, a premissa só é verdadeira para $\epsilon > 1$. Se $0 < \epsilon < 1$, temos uma contradição.

Portanto, como não existe $l$ tal que $(a_n)_n \to l$, logo $(a_n)_n$ é divergente. ∎

---

**Teorema (Unicidade):** Se $(a_n)_n$ é convergente, então existe um único $l$ tal que $(a_n)_n \to l$.

Sejam $l_1$ e $l_2$ tais que $(a_n)_n \to l_1$, $(a_n)_n \to l_2$ e $l_1 > l_2$ (por conveniência).

Dado $\epsilon > 0$, eventualmente $d(a_{N1},l_1) < \epsilon_1$ e $d(a_{N2},l_2) < \epsilon_2$. Tomando $N = \max(N1, N2)$, logo $d(a_N,l_1) < \epsilon_1$ e $d(a_N,l_2) < \epsilon_2$.

Pela Desigualdade Triangular, teremos:

$$
d(l_1,l_2) \leq d(a_N,l_1) + d(a_N,l_2) < \epsilon_1 + \epsilon_2
$$

Tomando $\epsilon = \epsilon_1 + \epsilon_2$:

$$
\displaylines{
\begin{align*}
d(l_1,l_2) < \epsilon
&\implies |l_1 - l_2| < \epsilon \\
&\implies 0 \leq |l_1 - l_2| < \epsilon \\
&\implies 0 \leq l_1 - l_2 < \epsilon \qquad (l_1 > l_2)
\end{align*}
}
$$

Como a desigualdade $l_1 - l_2 < \epsilon$ vale para todo $\epsilon > 0$, se tivermos $l_1 - l_2 = \delta > 0$, basta tomar $\epsilon = \frac{\delta}{2}$. Isso contradiz $d(l_1,l_2) < \epsilon$. Logo não pode ocorrer $d(l_1,l_2) > 0$.

Por outro lado, a igualdade $l_1 - l_2 = 0$ ocorre se, e somente se, $l_1 = l_2$.

Portanto, $l_1 = l_2$. ∎

---

**Teorema:** Toda sequência convergente de reais é cercada.

Seja $\epsilon = 1$ arbitrário. Então existe $N$ tal que $(\forall n \geq N)[d(a_n,l) < 1]$ (sequência convergente). Logo $(a_n)_{n \geq N} \subseteq B_1(l)$.

Tomando do conjunto de todas as distâncias entre os $(a_n)_{n < N}$ até $l$ (elementos fora de $B_1(l)$) o seu $\max$:

$$
M = \max{\{ d(a_n,l) \mid n < N \}}
$$

> **Obs.:** todos os elementos deste conjunto são maiores ou iguais a 1, pois não está contidos na bola.

Como $B_1(l) \subseteq B_{M+1}(l)$ e $(a_n)_{n<N} \subseteq B_{M+1}(l)$, então $(a_n)_n \subseteq B_{M+1}(l)$.

Portanto, a sequência é cercada. ∎

#### Propriedades

Sejam $(a_n)_n$ e $(b_n)_n$ sequências que convergem para $a$ e $b$, respectivamente, e $c$ um número real.

---

**Propriedade 1:** $(a_n + c)_n \to a + c$

Seja $(a_n)_n \to a$.

Temos que $(\forall \epsilon > 0)[|a_n - a| < \epsilon]$. Calculamos:

$$
\displaylines{
\begin{align*}
|a_n - a| &= |a_n + c - c - a| \\
&= |(a_n + c) - (a + c)| < \epsilon
\end{align*}
}
$$

Assim, $(a_n + c)_n \to a + c$. ∎

---

**Propriedade 2:** $(a_n + b_n)_n \to a + b$

Sejam $(a_n)_n \to a$ e $(b_n)_n \to b$ sequências e $\epsilon_1 = \frac{\epsilon}{2}$ e $\epsilon_2 = \frac{\epsilon}{2}$ reais.

Teremos o seguinte:

$$
|a_n - a| < \epsilon_1 \quad \text{e} \quad |b_n - b| < \epsilon_2
$$

Pela Desigualdade Triangular, segue que:

$$
|(a_n - a) + (b_n - b)| \leq |a_n - a| + |b_n - b| \implies |(a_n - a) + (b_n - b)| \leq \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon
$$

Portanto, $(a_n + b_n)_n \to a + b$. ∎

---

**Propriedade 3:** $(c \cdot a_n)_n \to c \cdot a$

Seja $(a_n)_n \to a$.

Calculamos:

$$
\displaylines{
\begin{align*}
|a_n - a| < \epsilon'
&\implies |c||a_n - a| < |c|\epsilon' \\
&\implies |c \cdot (a_n - a)| < |c|\epsilon'
\end{align*}
}
$$

Tomando $\epsilon = |c|\epsilon'$, teremos $|c \cdot (a_n - a)| < \epsilon$.

Portanto, $(c \cdot a_n)_n \to c \cdot a$. ∎

---

**Propriedade 4:** $(a_n \cdot b_n)_n \to a \cdot b$

Sejam $(a_n)_n \to a$ e $(b_n)_n \to b$ sequências.

Veja que $|a_n - a| < \epsilon_1$ e $|b_n - b| < \epsilon_2$.

Tomando $a_nb_n - ab = a_nb_n - a_nb + a_nb - ab = a_n(b_n - b) + b(a_n - a)$, teremos:

$$
|a_nb_n - ab| = |a_n(b_n - b) + b(a_n - a)|
$$

Calculamos, pela Desigualdade Triangular:

$$
\displaylines{
\begin{align*}
& |a_nb_n - ab| \leq |a_n(b_n - b)| + |b(a_n - a)| \\
\implies& |a_nb_n - ab| \leq |a_n||b_n - b| + |b||a_n - a| \\
\implies& |a_nb_n - ab| \leq M|b_n - b| + |b||a_n - a| \leq  M\epsilon_2 + |b|\epsilon_1
\end{align*}
}
$$

Sejam $\epsilon_1 < \frac{\epsilon}{2|b|}$ e $\epsilon_2 < \frac{\epsilon}{2|b|}$. Logo $|a_nb_n - ab| < \frac{M\epsilon}{2M} + \frac{|b|\epsilon}{2|b|} = \frac{\epsilon}{2} + \frac{\epsilon}{2}$. Isto é, $|a_nb_n - ab| < \epsilon$.

Portanto, $(a_n \cdot b_n)_n \to a \cdot b$. ∎

---

**Propriedade 5:** $\left(\frac{1}{a_n}\right)_n \to \frac{1}{a}$, com $a_n \neq 0$ (para qualquer $n$) e $a \neq 0$

Seja $(a_n)_n \to a$. Então $|a_n - a| < \epsilon_2$.

Calculamos:

$$
\displaylines{
\begin{align*}
\frac{1}{a_n} - \frac{1}{a} = \frac{a - a_n}{a \cdot a_n}
&\implies \left| \frac{1}{a_n} - \frac{1}{a} \right| = \left| \frac{a - a_n}{a \cdot a_n} \right| \\
&\implies \left| \frac{1}{a_n} - \frac{1}{a} \right| = \left| \frac{a - a_n}{a \cdot a_n} \right| < \frac{\epsilon_1}{|a||a_n|} \\
&\implies \left| \frac{1}{a_n} - \frac{1}{a} \right| < \frac{\epsilon_1}{|a||a_n|} < \frac{\epsilon_1}{|a|N} \qquad (N > 0 \text{ é cota inferior de } |a_n| \neq 0)
\end{align*}
}
$$

Tomando $\epsilon_1 = \epsilon|a|N$, teremos:

$$
\left| \frac{1}{a_n} - \frac{1}{a} \right| < \epsilon \implies \left(\frac{1}{a_n}\right)_n \to \frac{1}{a}
$$

Portanto, $\left(\frac{1}{a_n}\right)_n \to \frac{1}{a}$. ∎

---

**Propriedade 6:** $\left(\frac{a_n}{b_n}\right)_n \to \frac{a}{b}$, com $b_n \neq 0$ (para qualquer $n$) e $b \neq 0$

Calculamos:

$$
\displaylines{
\begin{align*}
\left(a_n \cdot \frac{1}{b_n} \right)_n = (a_n)_n \cdot \left(\frac{1}{b_n} \right)_n
\end{align*}
}
$$

Logo $a \cdot \frac{1}{b} = \frac{a}{b}$.

Portanto, $\left(\frac{a_n}{b_n}\right)_n \to \frac{a}{b}$. ∎

> *Meu Deus! Que demonstração porca!*

#### Propriedades dos Limites

1. $\lim_n(c + a_n)_n = c + a$
2. $\lim_n(c \cdot a_n)_n = c \cdot a$
3. $\lim_n(a_n + b_n)_n = a + b$
4. $\lim_n(a_n \cdot b_n)_n = a \cdot b$
5. $\lim_n\left(\frac{a_n}{b_n}\right)_n = \frac{a}{b}$, se $b_n \neq 0$ e $b \neq 0$
6. $\lim_n\left(\frac{1}{a_n}\right)_n = \frac{1}{a}$, se $a_n \neq 0$ e $a \neq 0$

---

**Teorema do Sanduíche:** Sejam as sequências $(a_n)_n$, $(b_n)_n$ e $(c_n)_n$ que convergem para $a$, $b$ e $c$, respectivamente. Se $(\forall n)[a_n \leq b_n \leq c_n]$ e $a = c = k$, então $b = k$.

> [!warning] Nota
> Infelizmente perdi a demonstração que o professor fez em sala. :(

---

**Lema (Desigualdade de Bernoulli):** Seja $x$ : Real com $x > -1$ e $n$ : Nat. Então $(1 + x)^n \geq 1 + n \cdot x$.

Vamos demonstrar por indução.

**Caso base ($n = 0$):**

Calculamos:

$$
(1 + x)^0 \geq 1 + 0 \cdot x \implies 1 \geq 1
$$

Como $1 \geq 1$ é sempre verdadeiro, concluímos o caso base.

**Passo indutivo:**

Nossa hipótese indutiva é $(1 + x)^n \geq 1 + n \cdot x$.

Calculamos:

$$
\displaylines{
\begin{align*}
(1 + x)^{n + 1} \geq 1 + (n + 1) \cdot x
&\implies (1 + x)(1 + x)^n \geq (1 + x)(1 + n \cdot x) \qquad (\text{H.I.}) \\
&\implies (1 + x)^{n + 1} \geq (1 + x)(1 + n \cdot x) \\
&\implies (1 + x)^{n + 1} \geq 1 + n \cdot x + x + n \cdot x^2 \\
&\implies (1 + x)^{n + 1} \geq 1 + x (n + 1) + n \cdot x^2 \geq 1 + x(n + 1) \qquad (n \cdot x^2 > 0) \\
&\implies (1 + x)^{n + 1} \geq 1 + (n + 1)x
\end{align*}
}
$$

Logo, concluímos o passo indutivo.

Portanto, finalizamos a demonstração da Desigualdade de Bernoulli. ∎

---

**Teorema:** Seja $a$ : Real com $0 < a < 1$. Então a sequência de reais $(a^n)_n \to 0$.

Como $0 < a < 1$, logo $\frac{1}{a} > 1$.

Veja que:

$$
a^n = \left( \frac{1}{\frac{1}{a}} \right)^n
= \frac{1^n}{\left(\frac{1}{a}\right)^n}
= \frac{1}{\left(\frac{1}{a}\right)^n}
$$

Se $\frac{1}{a} > 1$, então definimos $k > -1$ tal que $\frac{1}{a} = k + 1$.

Agora, note o seguinte:

$$
0 < a^n = \frac{1}{\left(\frac{1}{a}\right)^n} = \frac{1}{(k + 1)^n} \leq \frac{1}{1 + k \cdot n} \qquad (\text{Desigualdade de Bernoulli})
$$

Logo, por transitividade, $0 < a^n \leq \frac{1}{1 + k \cdot n}$. Transformando cada termo em uma sequência, teremos:

$$
(0_n)_n < (a^n)_n \leq \left(\frac{1}{1 + k \cdot n}\right)_n
$$

Tomando os limites, pelo Teorema do Sanduíche, segue que:

$$
(0_n)_n \to 0 \quad \text{e} \quad \left(\frac{1}{1 + k \cdot n}\right)_n \to 0 \implies (a^n)_n \to 0
$$

Portanto, $(a^n)_n \to 0$. ∎

### Sequências Autoconvergentes (Sequência de Cauchy)

$$
(a_n)_n \text{ é autoconvergente} \overset{\mathrm{def}}{\iff} (\forall \epsilon > 0)(\exists N)(\forall i, j \geq N)[a_i \text{ e } a_j \text{ são $\epsilon$-Perto}]
$$

A parte direita pode ser traduzida assim: *eventualmente, todos os termos estão em uma mesma bola.*

---

**Teorema:** Toda sequência de reais convergente é autoconvergente.

Seja $(a_n)_n \to l$ uma sequência real. Então existe um $N$ (com $n \geq N$) tal que $d(a_n,l) < \epsilon_1$.

Tomando $i, j \geq N$, teremos $d(a_i,l) < \epsilon_1$ e $d(a_j,l) < \epsilon_1$.

Pela Desigualdade Triangular, vamos ter o seguinte:

$$
\displaylines{
\begin{align*}
d(a_i,a_j) \leq d(a_i,l) + d(a_j,l)
&\implies d(a_i, a_j) \leq \epsilon_1 + \epsilon_1 \\
&\implies d(a_i, a_j) \leq 2\epsilon_1 \\
&\implies d(a_i, a_j) \leq \epsilon
\end{align*}
}
$$

Portanto, $(a_n)_n$ é autoconvergente. ∎

> Por que usar $\epsilon_1$ e não $\epsilon'$?

---

**Teorema:** Toda sequência de reais autoconvergente é cercada.

Seja $(a_n)_n \to l$ uma sequência real autoconvergente. Dado $\epsilon > 0$, existe $N$ tal que $\forall i, j \geq N$, $d(a_i, a_j) < \epsilon$.

Tomando $a_N$ como centro de uma ε-Bola, todos os termos $(a_n)_{n \geq N}$ estão em $B_\epsilon(a_N)$.

Tomando o conjunto de todas as distâncias de $(a_n)_{n < N}$ até $a_N$, dito conjunto $A$.

Definimos, então, $M = \sup(A) + 1$. Assim, os elementos de $(a_n)_{n<N}$ estão dentro de $B_M(a_N)$.

Tomando $D = \max(M,\epsilon)$, teremos:

$$
B_M(a_N) \subset B_D(a_N) \quad \text{e} \quad B_\epsilon(a_N) \subset B_D(a_N)
$$

Portanto, $B_D(a_N)$ contém a sequência inteira. ∎

---

**Corolário:** Toda sequência autoconvergente é cotada.

> [!warning] Nota
> O professor não fez demonstração desse corolário.

### Subsequências

Seja $(a_n)_n$ uma sequência de reais. Dada a sequência estritamente crescente $(n_i)_i$ : Seq Nat, chamamos $(a_{n_i})_i$ de subsequência de $(a_n)_n$.

Alternativamente, temos:

$$
(b_n)_n \text{ é subsequência de } (a_n)_n \overset{\mathrm{def}}{\iff} (\exists n_0, n_1, n_2, \ldots \text{ em que } n_0 < n_1 < n_2 < \ldots)(\forall i)[b_i = a_{n_i}]
$$

*Ex.:*
$(a_n)_n$: 3, -1, 4, √2, 5, 1/3, 9, 10, -1, 7, 3, π, -1/10, ...
$(b_n)_n$: √2, 1/3, 9, -1, 3
Os elementos de $(b_n)_n$ também estão em $(a_n)_n$, na mesma ordem.

---

**Teorema:** Toda sequência autoconvergente que possui uma subsequência convergente é convergente.

Seja $(a_n)_n$ autoconvergente e $(a_{n_i})_i \to l$.

Dado $\epsilon > 0$, existe $N$ tal que $(\forall i, j \geq N)[d(a_i,a_j) < \epsilon_1]$.

Como $(a_{n_i})_i \to l$, logo existe $M$ tal que $(\forall i \geq M)[d(a_{n_i},l) < \epsilon_2]$.

Tomando $P = \max(N,M)$, então $\forall i, j \geq P$

Note que $d(a_i,a_j) < \epsilon_1$ e $d(a_{n_i},l) < \epsilon_2$.

Pela Desigualdade Triangular:

$$
\displaylines{
\begin{align*}
d(a_i,l) \leq d(a_i, a_{n_i}) + d(a_{n_i},l)
&\implies d(a_i,l) \leq \epsilon_1 + \epsilon_2 \\
&\implies d(a_i,l) \leq \epsilon \qquad (\epsilon = \epsilon_1 + \epsilon_2)
\end{align*}
}
$$

Portanto, temos uma sequência convergente. ∎
