# Função Totiente de Euler

> A Função Totiente de Euler conta quantos números inteiros positivos menores ou iguais a um dado número $n$ são primos entre si com $n$.

Seja $n$ : Int tal que $n > 0$.

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

(dist euc) Seja um intervalo (a,b). Como representar como uma bola?
(Se b > a por conveniência)

[foto]

**Def:** Diâmetro:
Seja A um conjunto de reais.
S = Diam A ⇔ S = Sup {d(a,b) | a, b ∈ A} [conjunto com os valores de todas as distãncias entre os pontos a e b; o S é a maior de todas as distâncias]
Obs.: diam A = ∞ ⇔ sup A = ∞

**Def.:** Conjunto Cercado
A é cercado ⇔ (∃c)(∃m)\[A ⊆ $B_m$(c)\]   [A está contido em alguma bola]
