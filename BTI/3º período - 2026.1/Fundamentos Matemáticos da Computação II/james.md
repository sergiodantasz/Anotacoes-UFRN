# Questão 2
## Para cada função $f: \mathbb{R} \rightarrow \mathbb{R}$, verifique se ela é injetiva, sobrejetiva e, caso possível, calcule a função inversa.
## d) $f(x) = 3 - \frac{x}{2}$
### Testando injetividade
Sejam $x_1, x_2 \in \mathbb{R}$

Suponha que $f(x_1) = f(x_2)$

Calculamos:
$$
\begin{align*}
f(x_1) = f(x_2) \\
&\implies 3 - \frac{x_1}{2} = 3 - \frac{x_2}{2} \\
&\implies - \frac{x_1}{2} = - \frac{x_2}{2} \\
&\implies \frac{x_1}{2} = \frac{x_2}{2} \\
&\implies x_1 = x_2
\end{align*}
$$
Imediato. $\blacksquare$

### Testando sobrejetividade
Para provar a sobrejetividade, pegaremos um valor qualquer $y \in \mathbb{R}$ no contradomínio e provaremos que existe um valor $x \in \mathbb{R}$ no domínio.

Seja $y \in \mathbb{R}$.

Calculamos
$$
\begin{align*}
f(x) = 3 - \frac{x}{2}&\\
&\implies y = 3 - \frac{x}{2}\\
&\implies \frac{x}{2} = 3 - y \\
&\implies x = 2(3-y)
\end{align*}
$$
Isso significa que, para qualquer valor de $y$ que escolhermos, conseguiremos encontrar um valor de $x$ correspondente.

Portanto, a função é sobrejetiva. $\blacksquare$
### Função inversa
Se $f$ é injetiva e sobrejetiva, então $f$ é bijetiva.

Logo, $f$ possui função inversa.

Calculamos
$$
\begin{align*}
f(x) = 3 - \frac{x}{2}&\\
&\implies y = 3 - \frac{x}{2} \\
&\implies \frac{x}{2} = 3 - y \\
&\implies x = 2(3-y)\\
&\implies f^{-1}(x) = 2(3-x)
\end{align*}
$$

Imediato. $\blacksquare$

## e) $f(x) = \frac{2x-3}{5}$

### Testando injetividade
Sejam $x_1, x_2 \in \mathbb{R}$

Suponha que $f(x_1) = f(x_2)$

Calculamos

$$
\begin{align*}
f(x_1) = f(x_2)&\\
&\implies \frac{2x_1-3}{5} = \frac{2x_2-3}{5}\\
&\implies 2x_1-3 = 2x_2-3\\
&\implies 2x_1 = 2x_2 \\
&\implies x_1 = x_2
\end{align*}
$$
Imediato. $\blacksquare$


### Testando sobrejetividade
Seja $y \in \mathbb{R}$

Calculamos
$$
\begin{align*}
f(x) = \frac{2x-3}{5}&\\
&\implies y = \frac{2x-3}{5}\\
&\implies 5y = 2x-3 \\
&\implies 5y+3 = 2x\\
&\implies \frac{5y+3}{2} = x
\end{align*}
$$
Portanto, para qualquer valor de $y$, haverá um valor de $x$ correspondente. $\blacksquare$

### Função inversa

Calculamos:
$$
\begin{align*}
f(x) = \frac{2x-3}{5}&\\
&\implies y = \frac{2x-3}{5}\\
&\implies 5y = 2x-3 \\
&\implies 5y+3 = 2x\\
&\implies \frac{5y+3}{2} = x\\
&\implies f^{-1}(x) = \frac{5x+3}{2}
\end{align*}
$$
Imediato. $\blacksquare$

## f) $f(x) = \frac{4-3x}{2}$

### Testando injetividade
Sejam $x_1, x_2 \in \mathbb{R}$

Suponha que $f(x_1) = f(x_2)$

Calculamos:
$$
\begin{align*}
f(x_1) = f(x_2) &\\
&\implies \frac{4-3x_1}{2} = \frac{4-3x_2}{2}\\
&\implies 4-3x_1 = 4-3x_2\\
&\implies -3x_1 = -3x_2\\
&\implies x_1 = x_2
\end{align*}
$$
Imediato. $\blacksquare$

### Testando sobrejetividade
Seja $y \in \mathbb{R}$

Calculamos:
$$
\begin{align*}
f(x) = \frac{4-3x}{2}&\\
&\implies y = \frac{4-3x}{2}\\
&\implies 2y = 4 - 3x\\
&\implies 2y-4 = -3x\\
&\implies -2y+4 = 3x\\
&\implies \frac{-2y+4}{3}=x\\
f\left(\frac{-2y+4}{3}\right)&\\
&= \frac{4-3\left(\frac{-2y+4}{3}\right)}{2}\\
&= \frac{4-(-2y+4)}{2}\\
&= \frac{4+2y-4}{2}\\
&= \frac{2y}{2}\\
&= y
\end{align*}
$$
Logo, para cada qualquer valor de $y$ no contradomínio, haverá um valor de $x$ correspondente no domínio.

### Função inversa
Como a função é injetiva e sobrejetiva, então ela possui inversa.

Calculamos:

$$
\begin{align*}
f(x) = \frac{4-3x}{2}&\\
&\implies y = \frac{4-3x}{2}\\
&\implies 2y = 4 - 3x\\
&\implies 2y-4 = -3x\\
&\implies - \frac{2y-4}{3} = x\\
&\implies f^{-1}(x) = -\frac{2y-4}{3}
\end{align*}
$$
Imediato.

# Questão 3
## Seja $f: A \rightarrow B$ e $g: B \rightarrow C$. Mostre que caso uma das funções não seja injetiva/sobrejetiva, $g \circ f$ não vai ser injetiva/sobrejetiva

### Caso 1: $f$ Não é injetiva
Objetivo: $g \circ f$ não é injetiva

Suponha que $f$ não é injetiva.

Logo, $(\exists x_1,x_2 \in A)[f(x_1) = f(x_2) \land x_1 \not= x_2]$

Calculamos:
$$
\begin{align*}
f(x_1) = f(x_2)&\\
& \implies g(f(x_1)) = g(f(x_2))\\
&\implies g \circ f (x_1) = g \circ f (x_2)
\end{align*}
$$

Logo,$(g \circ f (x_1) = g \circ f (x_2)) \land (x_1 \not= x_2)$

Portanto, $g \circ f$ não é injetiva. $\blacksquare$

### Caso 2: $f$ Não é sobrejetiva
Objetivo: $g \circ f$ não é sobrejetiva

Refutação por contraexemplo:

Sejam $f: A \rightarrow B$, $g: B \rightarrow C$
Tome
$$
A = \{1\} \qquad B = \{1,2\} \qquad C = \{1\}
$$
 definidas pelas seguintes leis de formação:
$$
f(1) = 1 \qquad g(1) = 1 \qquad g(2) = 1
$$

Logo, temos que $f$ não é sobrejetiva mas $g$ é sobrejetiva.

Portanto, o fato de $f$ não ser sobrejetiva não implica que $g \circ f$ não seja sobrejetiva. $\blacksquare$

### Caso 3: $g$ Não é injetiva
Objetivo: $g \circ f$ não é injetiva

Refutação por contraexemplo:

Sejam $f: A \rightarrow B$, $g: B \rightarrow C$

Tome
$$
A = \{1\} \qquad B = \{1,2\} \qquad C= \{1\}
$$
definidas pelas seguintes leis de formação:
$$
f(1) = 1 \qquad g(1) = 1 \qquad g(2) = 1
$$
Nesse caso, temos que a função $g$ não é injetiva, mas a composição $g \circ f$ continua sendo injetiva.

### Caso 4: $g$ Não é sobrejetiva
Objetivo: $(\exists c \in C)(\forall a \in A)[g(f(a)) \not= c]$

Suponha que $g$ não é sobrejetiva

Logo, $(\exists c \in C)(\forall b \in B)[g(b) \not= c]$


Escolho $c \in C$

Logo, $(\forall b \in B)[g(b) \not= c]$

Seja $a \in A$

Logo, $f(a) = b$

Logo, $g(f(a)) \not=c$

Logo, $(\exists c \in C)(\forall a \in A)[g \circ f (a) \not= c]$

Logo, $g \circ f (x)$ não é sobrejetiva. $\blacksquare$


# Questão 4
## Seja $f: A \rightarrow B$. Prove que se existir $g: B \rightarrow A$ tal que $g \circ f = i_A$, então $f$ é injetiva.

Seja a função $f: A \rightarrow B$

Suponha que exista $g: B \rightarrow A$ tal que $g \circ f = i_A$

Objetivo: $(\forall x_1, x_2 \in A)[f(x_1) = f(x_2) \implies x_1 = x_2]$

Sejam $x_1, x_2 \in A$

Suponha que $f(x_1) = f(x_2)$

Calculamos
$$
\begin{align*}
f(x_1) = f(x_2)&\\
&\implies g(f(x_1)) = g(f(x_2))\\
&\implies x_1 = x_2
\end{align*}
$$
Imediato. $\blacksquare$

# Questão 5
## Seja $f: A \rightarrow B$. Prove que se existir $g: B \rightarrow A$ tal que $f \circ g = i_B$, então $f$ é sobrejetiva.

Seja a função $f: A \rightarrow B$

Suponha que exista $g: B \rightarrow A$ tal que $f \circ g = i_B$.

Objetivo: $(\forall y \in B)(\exists x \in A)[f(x) = y]$

Seja $y \in B$

Tome $x = g(y)$. Como $g$ é função de $B$ para $A$, então $x \in A$

Calculamos

$$
\begin{align*}
f(x) = f(g(y)) &\\
&= f \circ g (y)\\
&= i_B(y)\\
&= y
\end{align*}
$$
Logo, para qualquer valor $y \in B$, encontramos um valor $x \in A$ ligado a ele.

# Questão 6
## Seja $f: A \rightarrow B$ e $C \subseteq A$. Mostre que quando restringimos o domínio de $f$ a $C$, o resultado ainda é uma função. Isto é, mostre que $f \cap (C \times B)$ é uma função.
Seja $f: A \rightarrow B$ e $C$ tal que $C \subseteq A$

Logo, $(\forall x \in C)[x \in A]$    $\qquad$[Hip.1]

Objetivo: $(\forall c \in C)(\exists! b \in B)[(c,b) \in f \cap (C \times B)]$

Seja $c \in C$

Logo, pela [Hip. 1], $c \in A$

Como $f: A \rightarrow B$ é função, então $(\exists! b \in B)[(c,b) \in f]$

Como $(c,b) \in f$ e $(c,b) \in C \times B$, então $(c,b) \in f \cap (C \times B)$

Portanto, ao restringir o domínio da função $f$, esta continua sendo função. $\blacksquare$

# Questão 7
## Seja $f: A \rightarrow B$ e $X,Y \subseteq A$. Prove ou refute: $f(X \cup Y) = f(X) \cup f(Y)$

Seja $f: A \rightarrow B$ e $X,Y$ tais que $X,Y \subseteq A$

Objetivo: $f(X \cup Y) = f(X) \cup f(Y)$

O que queremos provar aqui é a igualdade entre imagens

### Parte 1: $f(X \cup Y) \subseteq f(X) \cup f(Y)$

Seja $n \in f(X \cup Y)$

Logo, $(\exists m \in X \cup Y)[f(m) = n]$

Escolho $m \in X \cup Y$

Logo, $m \in X \lor m \in Y$

Logo, $f(m) \in f(X) \lor f(m) \in f(Y)$

Logo, $n \in f(X) \cup f(Y)$

Imediato. $\blacksquare$


### Parte 2: $f(X) \cup f(Y) \subseteq f(X \cup Y)$

Seja $n \in f(X) \cup f(Y)$

Logo, $n \in f(X) \lor n \in f(Y)$

%Logo, $(\exists m \in X)[f(m) = n] \lor (\exists m \in Y)[f(m) = n]$

#### Caso 1: $n \in f(X)$

Logo, $(\exists m \in X)[f(m)  = n]$

Logo, $(\exists m \in X \cup Y)[f(m)  = n]$

Escolho $m \in X \cup Y$

Logo, $f(m) \in f(X \cup Y)$

Logo, $n \in f(X \cup Y)$

Imediato. $\blacksquare$

#### Caso 2: $n \in f(Y)$

Logo, $(\exists m \in Y)[f(m)  = n]$

Logo, $(\exists m \in X \cup Y)[f(m)  = n]$

Escolho $m \in X \cup Y$

Logo, $f(m) \in f(X \cup Y)$

Logo, $n \in f(X \cup Y)$

Imediato. $\blacksquare$

Pelas partes 1 e 2, a proposição é verdadeira. $\blacksquare$