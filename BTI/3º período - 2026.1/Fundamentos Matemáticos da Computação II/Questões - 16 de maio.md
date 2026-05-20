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

