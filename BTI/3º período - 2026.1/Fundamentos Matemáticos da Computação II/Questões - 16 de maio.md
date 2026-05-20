# Questão 1

Sejam $R$ e $S$ relações tais que $R$ é de $A$ para $B$ e $S$ é de $B$ para $C$.

Mostre que:

##### a) Se $R$ e $S$ são funcionais, então $S \circ R$ é funcional.

Suponha $R$ e $S$ funcionais.

Sejam $a \in A$ e $c_1, c_2 \in C$.

Suponha $(a, c_1) \in S \circ R$ (1) e $(a, c_2) \in S \circ R$ (2).

De (1), pela definição de composição, existe $b_1 \in B$ tal que $(a, b_1) \in R$ e $(b_1, c_1) \in S$.
De (2), existe $b_2 \in B$ tal que $(a, b_2) \in R$ e $(b_2, c_2) \in S$.

Como $R$ é funcional, $(a, b_1) \in R$ e $(a, b_2) \in R$, logo $b_1 = b_2$.
Como $S$ é funcional, $(b_1, c_1) \in S$ e $(b_2, c_2) \in S$, logo $c_1 = c_2$.

Portanto $S \circ R$ é funcional. $\blacksquare$

##### b) Se $R$ e $S$ são totais, então $S \circ R$ é total.

Suponha $R$ e $S$ totais.

Seja $a \in A$.

Como $R$ é total e $a \in A$, logo existe $b \in B$ tal que $(a, b) \in R$ (1).
Como $S$ é total e $b \in B$, logo existe $c \in C$ tal que $(b, c) \in S$ (2).

Pela definição de composição, de (1) e (2) temos que $(a, c) \in S \circ R$.

Portanto $S \circ R$ é total. $\blacksquare$

# Questão 2

Suponha que $R_1$ e $R_2$ sejam ordens parciais em $A$. $R_1 - R_2$ deve ser uma ordem parcial em $A$?

Tome o conjunto $A = \{a\}$ e as relações $R_1 = \{(a, a)\}$ e $R_2 = \{(a, a)\}$. Note que $R_1 - R_2 = \emptyset$.

Para que $R_1 - R_2$ seja uma ordem parcial em $A$, ela precisa obrigatoriamente ser reflexiva.

Como $a \in A$, o par $(a, a)$ deveria pertencer à relação resultante. Contudo, como a relação resultante é vazia, temos que $(a, a) \notin (R_1 - R_2)$. 

Portanto $R_1 - R_2$ não é uma ordem parcial em $A$. $\blacksquare$

# Questão 3

Suponha que $R$ é uma relação de $A$ para $B$ e $S$ e $T$ são relações de $B$ para $C$. Prove ou refute: $(S \cap T) \circ R = (S \circ R) \cap (T \circ R)$.

Vamos tentar demonstrar.

**Parte $(S \cap T) \circ R \subseteq (S \circ R) \cap (T \circ R)$:**

Seja $(a, c) \in (S \cap T) \circ R$.

Pela definição de composição, existe $b \in B$ tal que $(a, b) \in R$ (1) e $(b, c) \in S \cap T$ (2).

Logo, de (2), temos $(b, c) \in S$ (3) e $(b, c) \in T$ (4).

Pela definição de composição, de (1) e (3) temos $(a, c) \in S \circ R$. Além disso, de (1) e (4), temos $(a, c) \in T \circ R$.

Assim, pela definição de interseção, segue que $(a, c) \in (S \circ R) \cap (T \circ R)$.

**Parte $(S \circ R) \cap (T \circ R) \subseteq (S \cap T) \circ R$:**

Mostrarei agora que $(S \circ R) \cap (T \circ R) \nsubseteq (S \cap T) \circ R$ por meio de um contraexemplo.

Tome $A = \{ a \}$, $B = \{ b_1, b_2 \}$ e $C = \{ c \}$. Defino como relações $R = \{ (a, b_1), (a, b_2) \}$, $S = \{ (b_1, c) \}$ e $T = \{ (b_2, c) \}$.

Perceba que $S \circ R = \{ (a, c) \}$ e $T \circ R = \{ (a, c) \}$. Logo $(S \circ R) \cap (T \circ R) = \{ (a, c) \}$.

Agora note que $S \cap T = \emptyset$. Logo $(S \cap T) \circ R = \emptyset$. Como o conjunto vazio não possui elementos, é impossível $(a, c) \in (S \cap T) \circ R$ e a inclusão falha.

Assim, $(S \circ R) \cap (T \circ R) \nsubseteq (S \cap T) \circ R$.

Portanto, pela existência do contraexemplo, concluímos que $(S \cap T) \circ R \neq (S \circ R) \cap (T \circ R)$. $\blacksquare$

# Questão 4

Sejam $R_1$ e $R_2$ relações sobre $A$. Prove ou refute: Se $R_1$ e $R_2$ são relações de ordem total, então $R_1 \cap R_2$ é uma relação de ordem total.

Suponha que $R_1$ (1) e $R_2$ (2) são relações de ordem total.

**Reflexividade:**

Seja $a \in A$.

Por (1), $(a, a) \in R_1$.
Por (2), $(a, a) \in R_2$.

Logo, pela definição de interseção, $(a, a) \in R_1 \cap R_2$.

**Antissimetria:**

Sejam $a_1, a_2 \in A$.

Suponha que $(a_1, a_2) \in R_1 \cap R_2$ (3) e $(a_2, a_1) \in R_1 \cap R_2$ (4).

De (3), temos $(a_1, a_2) \in R_1$ e $(a_1, a_2) \in R_2$.
De (4), temos $(a_2, a_1) \in R_1$ e $(a_2, a_1) \in R_2$.

Logo, por (1) e (2), segue que $a_1 = a_2$.

**Transitividade:**

...

**Comparabilidade:**

...
