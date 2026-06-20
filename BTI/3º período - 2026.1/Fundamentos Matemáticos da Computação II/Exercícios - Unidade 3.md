# Exercícios

## Resumo

### Ex. 2

> [!example] Exercício
> Com as propriedades da álgebra booleana, simplifique os termos da expressão abaixo:
> $((x \land y') \lor ((x \land 0) \lor (x' \land 1)))'$

$$
\begin{align}
((x \land y') \lor ((x \land 0) \lor (x' \land 1)))'
            &= (x \land y')' \land ((x \land 0) \lor (x' \land 1))' \\
            &= (x \land y')' \land (0 \lor x')' \\
            &= (x \land y')' \land (x')' \\
            &= (x' \lor (y')') \land x \\
            &= (x' \lor y) \land x \\
            &= (x' \land x) \lor (y \land x) \\
            &= 0 \lor (y \land x) \\
            &= x \land y
\end{align}
$$

### Ex. 3

Considere o operador abaixo definido em uma álgebra booleana:

$$
x \oplus y \overset{def}{=} (x \lor y) \land (x \land y)'
$$

> [!example] Exercício
> Demonstre que $x \oplus y = (x \land y') \lor (x' \land y)$.

$$
\begin{align}
(x \lor y) \land (x \land y)'
	       &= (x \lor y) \land (x' \lor y') \\
           &= (x \land x') \lor (x \land y') \lor (y \land x') \lor (y \land y') \\
           &= 0 \lor (x \land y') \lor (y \land x') \lor 0 \\
           &= (x \land y') \lor (x' \land y)
\end{align}
$$

### Ex. 4

> [!example] Exercício
> Com as propriedades da álgebra booleana, demonstre ou refute que:
> $x = y \iff (x \land y') \lor (x' \land y) = 0$

**Parte ($\implies$):**

Suponha que $x = y$. Calculamos:

$$
\begin{align}
(x \land y') \lor (x' \land y) &= (x \land x') \lor (x' \land x) \\
                               &= 0 \lor 0 \\
                               &= 0
\end{align}
$$

**Parte ($\impliedby$):**

Suponha que $(x \land y') \lor (x' \land y) = 0$. Por definição, $x \land y' \leq (x \land y') \lor (x' \land y)$ e, consequentemente, $x \land y' \leq 0$. Note que, como $0$ é o mínimo, necessariamente $0 \leq x \land y'$. Pela antissimetria, temos $x \land y' = 0$. De modo análogo, $x' \land y = 0$. Calculamos:

$$
\begin{align}
x &= x \land 1 \\
  &= x \land (y \lor y') \\
  &= (x \land y) \lor (x \land y') \\
  &= (x \land y) \lor 0 \\
  &= x \land y
\end{align}
$$

Pelo teorema 1, segue que $x \leq y$. Calculamos:

$$
\begin{align}
y &= y \land 1 \\
  &= y \land (x \lor x') \\
  &= (y \land x) \lor (y \land x') \\
  &= (y \land x) \lor 0 \\
  &= y \land x
\end{align}
$$

Novamente pelo teorema 1, $y \leq x$. Pela antissimetria, concluímos que $x = y$. $\blacksquare$

### Ex. 5

> [!example] Exercício
> Determine se podemos produzir um reticulado sobre os divisores de 231, dado pela ordem parcial da relação de divisibilidade, e que seja isomórfico de uma álgebra booleana.

Os divisores de 231 são: 1, 3, 7, 11, 21, 33, 77, 231. O diagrama de Hasse é o seguinte:

![[Ex. 5.svg]]

Note que conseguimos obter um reticulado, pois quaisquer dois elementos $a$ e $b$ possuem ínfimo e supremo através do MMC e do MDC:

$$
a \lor b = \operatorname{mmc}(a, b) \quad \text{e} \quad a \land b = \operatorname{mdc}(a, b)
$$

Perceba que 1 divide todos os divisores de 231, logo $0 = 1$ (mínimo). Além disso, 231 é dividido por todos os elementos do conjunto, ou seja, $1 = 231$ (máximo). Logo o reticulado é limitado.

[Demonstrar que o reticulado é distributivo, complementado e isomórfico.]

### Ex. 6

> [!example] Exercício
> Com as propriedades da álgebra booleana, para quaisquer $x, y \in B$, se $x \lor y = x \lor z$ e $x \land y = x \land z$, então $y = z$.

Sejam $x, y \in B$. Suponha que $x \lor y = x \lor z$ e $x \land y = x \land z$. Pela lei da absorção, $y = y \land (x \lor y)$. Substituindo:

$$
\begin{align}
y &= y \land (x \lor z) \\
  &= (y \land x) \lor (y \land z) \\
  &= (x \land y) \lor (y \land z) \\
  &= (x \land z) \lor (y \land z) \\
  &= (x \lor y) \land z \\
  &= z \land (x \lor y) \\
  &= z \land (x \lor z)
\end{align}
$$

Novamente pela lei da absorção, temos $z = z \land (x \lor z)$. Portanto, concluímos que $y = z$. $\blacksquare$

### Ex. 7

> [!example] Exercício
> Demonstre na álgebra booleana que $b \land (a \lor (a' \land (b \lor b'))) = b$.

$$
\begin{align}
b \land (a \lor (a' \land (b \lor b'))) &= b \land (a \lor (a' \land 1)) \\
                                        &= b \land (a \lor a') \\
                                        &= b \land 1 \\
                                        &= b
\end{align}
$$

### Ex. 8

> [!example] Exercício
> Demonstre na álgebra booleana que $((a \lor c) \land (b' \lor c))' = (a' \lor b) \land c'$.

$$
\begin{align}
((a \lor c) \land (b' \lor c))' &= ((a \land b') \lor c)' \\
                                &= (a \land b')' \land c' \\
                                &= (a' \lor b) \land c'
\end{align}
$$

### Ex. 9

> [!example] Exercício
> Sejam $A = \{1, 2, 3, 4\}$ e $R = \{(1, 1), (1, 2), (2, 2), (3, 3), (4, 4), (1, 4)\}$. Desenha o diagrama de Hasse da relação de ordem parcial definida por $R$.

![[Ex. 9.svg]]

## Livro 5

### Teoremas

#### Teorema 1

Sejam $L$ um reticulado e $a, b \in L$.

> [!example] Proposição (a)
> $a \lor b = b \iff a \leq b$

**Parte ($\implies$):**

Suponha que $a \lor b = b$. Como $a \leq a \lor b = b$, logo $a \leq b$.

**Parte ($\impliedby$):**

Suponha que $a \leq b$. Disso e de $b \leq b$ (reflexividade), segue que $b$ é um limitante superior de $a$ e de $b$. Pela definição de menor limitante superior, temos $a \lor b \leq b$. Como $a \lor b$ é um limitante superior, logo $b \leq a \lor b$ e, consequentemente, pela antissimetria, $a \lor b = b$. $\blacksquare$

> [!example] Proposição (b)
> $a \land b = a \iff a \leq b$

**Parte ($\implies$):**

Suponha que $a \land b = a$. Como $a = a \land b \leq b$, logo $a \leq b$.

**Parte ($\impliedby$):**

Suponha que $a \leq b$. Segue que, disso e de $a \leq a$ (reflexividade), $a$ é um limitante inferior de $a$ e de $b$. Pela definição de maior limitante inferior, então $a \leq a \land b$. Isto é, $a \land b$ é um limitante inferior. Assim, $a \land b \leq a$ e, por consequência, pela propriedade da antissimetria, $a \land b = a$. $\blacksquare$

> [!example] Proposição (c)
> $a \land b = a \iff a \lor b = b$

**Parte ($\implies$):**

Suponha que $a \land b = a$. Pela proposição (b), temos $a \leq b$. Pela proposição (a), obtemos $a \lor b = b$.

**Parte ($\impliedby$):**

Suponha que $a \lor b = b$. Pela proposição (a), segue que $a \leq b$. Pela proposição (b), temos $a \land b = a$. $\blacksquare$

#### Teorema 2

Sejam $L$ um reticulado e $a, b, c \in L$.

##### Idempotência

> [!example] Proposição (a)
> $a \lor a = a$

Pela definição de limitante superior, temos $a \leq a \lor a$. Pela reflexividade, $a \leq a$, ou seja, $a$ é um limitante superior de $a$. Pela definição de supremo, temos que $a \lor a$ é o menor limitante superior de $a$, logo necessariamente $a \lor a \leq a$. Por fim, pela antissimetria, concluímos que $a \lor a = a$. $\blacksquare$

> [!example] Proposição (b)
> $a \land a = a$

Segundo a definição de limitante inferior, $a \land a \leq a$. Temos $a \leq a$ pela propriedade da reflexividade. Logo $a$ é limitante inferior de $a$. Pela definição de ínfimo, $a \land a$ é o maior limitante inferior de $a$. Assim, $a \leq a \land a$. Portanto, pela antissimetria, $a \land a = a$. $\blacksquare$

##### Comutatividade

> [!example] Proposição (a)
> $a \lor b = b \lor a$

Sabemos que $a \lor b$ é o supremo de $\{a, b\}$. Similarmente, $b \lor a$ é o supremo de $\{b, a\}$. Ora, $\{a, b\} = \{b, a\}$, pois a ordem dos elementos nos conjuntos não importa. Desse modo, sendo os conjuntos estritamente iguais, é impossível que eles tenham supremos diferentes. Portanto, concluímos diretamente que $a \lor b = b \lor a$. $\blacksquare$

> [!example] Proposição (b)
> $a \land b = b \land a$

Note que $a \land b$ é o ínfimo de $\{a, b\}$ e $b \land a$, o de $\{b, a\}$. De forma análoga à proposição (a), segue imediatamente que $a \land b = b \land a$. $\blacksquare$

##### Associatividade

> [!example] Proposição (a)
> $a \lor (b \lor c) = (a \lor b) \lor c$

Pela definição de supremo, temos $a \leq a \lor (b \lor c)$ e $b \lor c \leq a \lor (b \lor c)$. Além disso, $b \leq b \lor c$ e $c \leq b \lor c$. Por transitividade, $b \leq a \lor (b \lor c)$ e $c \leq a \lor (b \lor c)$. Logo $a \lor (b \lor c)$ é um limitante superior de $a$ e de $b$. Pela definição de menor limitante superior, segue que $a \lor b \leq a \lor (b \lor c)$. Como $a \lor (b \lor c)$ é um limitante superior de $a \lor b$ e de $c$, obtemos $(a \lor b) \lor c \leq a \lor (b \lor c)$. De forma análoga, temos que $a \lor (b \lor c) \leq (a \lor b) \lor c$. Pela antissimetria, concluímos que $a \lor (b \lor c) = (a \lor b) \lor c$. $\blacksquare$

> [!example] Proposição (b)
> $a \land (b \land c) = (a \land b) \land c$

A demonstração é análoga à da proposição (b). $\blacksquare$

##### Absorção

> [!example] Proposição (a)
> $a \lor (a \land b) = a$

Como $a \land b \leq a$ e $a \leq a$, vemos que $a$ é um limitante superior de $a \land b$ e de $a$. Logo $a \lor (a \land b) \leq a$. Pela definição de menor limitante superior, temos $a \leq a \lor (a \land b)$. Pela antissimetria, $a \lor (a \land b) = a$. $\blacksquare$

> [!example] Proposição (b)
> $a \land (a \lor b) = a$

Como $a \leq a$ e $a \leq a \lor b$, então $a$ é um limitante inferior de $a$ e de $a \lor b$. Segue que $a \leq a \land (a \lor b)$. Pela definição de maior limitante inferior, $a \land (a \lor b) \leq a$. Portanto, por antissimetria, $a \land (a \lor b) = a$. $\blacksquare$

#### Teorema 3

Sejam $L$ um reticulado e $a, b, c \in L$.

> [!example] Proposição 1 - (a)
> $a \leq b \implies a \lor c \leq b \lor c$

Suponha que $a \leq b$. Pela definição de limitante superior, $a \leq a \lor c$ e $c \leq a \lor c$; isto é, $a \lor c$ é o menor limitante superior de $a$ e de $c$. Além disso, $b \leq b \lor c$ e $c \leq b \lor c$. Por transitividade, temos $a \leq b \lor c$. Note que $b \lor c$ é um limitante superior de $a$ e de $c$. Logo, como $a \lor c$ é supremo de $\{a, c\}$, logo $a \lor c \leq b \lor c$. $\blacksquare$

> [!example] Proposição 1 - (b)
> $a \leq b \implies a \land c \leq b \land c$

Suponha que $a \leq b$. Por definição, $a \land c \leq a$ e $a \land c \leq c$. Por transitividade, $a \land c \leq b$, logo $a \land c$ é um limitante inferior de $\{b, c\}$ (1). Além disso, por definição, temos $b \land c \leq b$ e $b \land c \leq c$, ou seja, $b \land c$ é o ínfimo de $\{b, c\}$ (2). De (1) e (2), concluímos, portanto, que $a \land c \leq b \land c$. $\blacksquare$

> [!example] Proposição 2
> $a \leq c \quad \text{e} \quad b \leq c \iff a \lor b \leq c$

**Parte ($\implies$):**

Suponha que $a \leq c$ e $b \leq c$. Isso significa que $c$ atua como limitante superior de $\{a, b\}$. Por definição, é imediato que $a \lor b \leq c$.

**Parte ($\impliedby$):**

Suponha que $a \lor b \leq c$. Como $a \lor b$ é um limitante superior de $\{a, b\}$, logo $a \leq a \lor b$ e $b \leq a \lor b$. Por transitividade, segue que $a \leq c$ e $b \leq c$. $\blacksquare$

> [!example] Proposição 3
> $c \leq a \quad \text{e} \quad c \leq b \iff c \leq a \land b$

**Parte ($\implies$):**

Suponha que $c \leq a$ e $c \leq b$. Logo $c$ é um limitante inferior de $\{a, b\}$. Por definição, temos que $c \leq a \land b$.

**Parte ($\impliedby$):**

Suponha que $c \leq a \land b$. Por ser limitante inferior de $\{a, b\}$, segue que $a \land b \leq a$ e $a \land b \leq b$. Por transitividade, $c \leq a$ e $c \leq b$. $\blacksquare$

> [!example] Proposição 4 - (a)
> $a \leq b \quad \text{e} \quad c \leq d \implies a \lor c \leq b \lor d$

Suponha que $a \leq b$ e $c \leq d$. Pelo teorema 3.1, temos $a \lor c \leq b \lor c$ e $c \lor b \leq d \lor b$. Logo, pela comutatividade, $b \lor c \leq b \lor d$. Por transitividade, concluímos que $a \lor c \leq b \lor d$. $\blacksquare$

> [!example] Proposição 4 - (b)
> $a \leq b \quad \text{e} \quad c \leq d \implies a \land c \leq b \land d$

Suponha que $a \leq b$ e $c \leq d$. Pelo teorema 3.1, segue que $a \land c \leq b \land c$ e $c \land b \leq d \land b$. Disso, pela propriedade comutativa, temos $b \land c \leq b \land d$. Logo, por transitividade, $a \land c \leq b \land d$. $\blacksquare$

### Capítulo 7.1

> [!important] Nota
> Nos exercícios 5 e 6, determine o diagrama de Hasse da relação $R$.

#### Ex. 5

> [!example] Exercício
> - $A = \{1, 2, 3, 4\}$
> - $R = \{ (1, 1), (1, 2), (2, 2), (2, 4), (1, 3), (3, 3), (3, 4), (1, 4), (4, 4)\}$

![[7.1 - Ex. 5.svg]]

#### Ex. 6

> [!example] Exercício
> - $A = \{a, b, c, d, e\}$
> - $R = \{ (a, a), (b, b), (c, c), (a, c), (c, d), (c, e), (a, d), (d, d), (a, e), (b, c), (b, d), (b, e), (e, e) \}$

![[7.1 - Ex. 6.svg]]

#### Ex. 7

> [!example] Exercício
> Descreva os pares ordenados nas relações determinadas pelos diagramas de Hasse.

##### (a) $A = \{1, 2, 3, 4\}$

![[7.1 - Ex. 7 - (a).png]]

$$
R = \{ (1, 1), (2, 2), (3, 3), (4, 4), (1, 3), (2, 3), (3, 4), (1, 4), (2, 4) \}
$$

##### (b) $A = \{1, 2, 3, 4\}$

![[7.1 - Ex. 7 - (b).png]]

$$
R = \{ (1, 1), (2, 2), (3, 3), (4, 4), (1, 2), (1, 3), (1, 4), (2, 3), (2, 4), (3, 4) \}
$$

> [!important] Nota
> Nos exercícios 8 e 9, determine o diagrama de Hasse da ordem parcial dados os dígrafos.

#### Ex. 8

![[7.1 - Ex. 8 - Dígrafo.png|243]]

![[7.1 - Ex. 8 - Hasse.svg]]

#### Ex. 9

![[7.1 - Ex. 9 - Dígrafo.png|267]]

![[7.1 - Ex. 9 - Hasse.svg]]

> [!important] Nota
> Nos exercícios 16 e 17, descreva o diagrama de Hasse de uma ordenação topológica dos *posets* dados.

#### Ex. 16

![[7.1 - Ex. 16.png]]

$$
\displaylines{
8 \\
| \\
7 \\
| \\
6 \\
| \\
5 \\
| \\
4 \\
| \\
3 \\
| \\
2 \\
| \\
1
}
$$

#### Ex. 17

![[7.1 - Ex. 17.png]]

$$
\displaylines{
9 \\
| \\
8 \\
| \\
7 \\
| \\
6 \\
| \\
5 \\
| \\
3 \\
| \\
2 \\
| \\
1 \\
| \\
4 \\
}
$$

### Capítulo 7.2

> [!important] Nota
> Nos exercícios 1 a 4, determine todos os maximais e minimais.

#### Ex. 1

##### (a)

- Maximais: 3, 5
- Minimais: 1, 6

##### (b)

- Maximais: f, g
- Minimais: a, b, c

#### Ex. 2

##### (a)

- Maximais: e, f
- Minimais: a

##### (b)

- Maximais: 4, 7
- Minimais: 1, 9, 8

#### Ex. 3

##### (a)

> $A = \mathbb{R}$ com a ordem parcial $\leq$.

- Maximais: nenhum
- Minimais: nenhum

##### (b)

> $A = \{ x \mid x \in \mathbb{R} \land 0 \leq x \leq 1 \}$ com a ordem parcial $\leq$.

- Maximais: 1
- Minimais: 0

#### Ex. 4

##### (a)

> $A = \{ x \mid x \in \mathbb{R} \land 0 < x \leq 1 \}$ com a ordem parcial $\leq$.

- Maximais: 1
- Minimais: nenhum

##### (b)

> $A = \{ 2, 3, 4, 6, 8, 24, 48 \}$ com a ordem parcial de "divide".

- Maximais: 48
- Minimais: 2, 3

> [!important] Nota
> Nos exercícios 5 a 8, determine os maiores e menores elementos, caso existam.

#### Ex. 5

##### (a)

- Máximo: f
- Mínimo: a

##### (b)

- Máximo: e
- Mínimo: nenhum

#### Ex. 6

##### (a)

- Máximo: nenhum
- Mínimo: nenhum

##### (b)

- Máximo: 5
- Mínimo: nenhum

#### Ex. 7

##### (a)

> $A = \{ x \mid x \in \mathbb{R} \land 0 < x < 1 \}$ com a ordem parcial $\leq$.

- Máximo: nenhum
- Mínimo: nenhum

##### (b)

> $A = \{ x \mid x \in \mathbb{R} \land 0 \leq x \leq 1 \}$ com a ordem parcial $\leq$.

- Máximo: 1
- Mínimo: 0

#### Ex. 8

##### (a)

> $A = \{ 2, 4, 6, 8, 12, 18, 24, 36, 72 \}$ com a ordem parcial de "divide".

- Máximo: 72
- Mínimo: 2

##### (b)

> $A = \{ 2, 3, 4, 6, 12, 18, 24, 36 \}$ com a ordem parcial de "divide".

- Máximo: nenhum
- Mínimo: nenhum

> [!important] Nota
> Nos exercícios 9 a 18, determine (em relação ao conjunto $B$), caso existam: (a) todos os limitantes superiores; (b) todos os limitantes inferiores; (c) o menor limitante superior; (d) o maior limitante inferior.

#### Ex. 9

(a) g, h, f
(b) a, b, c
(c) f
(d) c

#### Ex. 10

(a) 4, 5
(b) 1, 2
(c) nenhum
(d) nenhum

#### Ex. 11

(a) f, e, d
(b) a, b
(c) d
(d) b

#### Ex. 12

(a) 5
(b) 1, 2, 3
(c) 5
(d) 3

#### Ex. 13

(a) nenhum
(b) b
(c) nenhum
(d) b

#### Ex. 14

##### (a)

(a) nenhum
(b) nenhum
(c) nenhum
(d) nenhum

##### (b)

(a) nenhum
(b) 1, 2, 3
(c) nenhum
(d) 3

#### Ex. 15

(a) $[2, \infty)$
(b) $(-\infty,1]$
(c) 2
(d) 1

#### Ex. 16

(a) $[2, \infty)$
(b) $(-\infty,1]$
(c) 2
(d) 1

#### Ex. 17

(a) $\{a, b\}$, $\{a, b, c\}$
(b) $\emptyset$
(c) $\{a, b\}$
(d) $\emptyset$

#### Ex. 18

(a) 12, 24, 48
(b) 2
(c) 12
(d) 2

#### Ex. 19

$$
\displaylines{
h \\
| \\
g \\
| \\
f \\
| \\
e \\
| \\
d \\
| \\
c \\
| \\
b \\
| \\
a
}
$$

#### Ex. 20

$$
\displaylines{
5 \\
| \\
4 \\
| \\
3 \\
| \\
2 \\
| \\
1
}
$$

### Capítulo 7.3

> [!important] Nota
> Nos exercícios 1 a 3, determine se o diagrama de Hasse representa um reticulado.

#### Ex. 1

(a) 
(b) 