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

Sejam $a, b \in A$.

Suponha que $(a, b) \in R_1 \cap R_2$ (3) e $(b, a) \in R_1 \cap R_2$ (4).

De (3), temos $(a, b) \in R_1$ e $(a, b) \in R_2$.
De (4), temos $(b, a) \in R_1$ e $(b, a) \in R_2$.

Logo, por (1) e (2), segue que $a = b$.

**Transitividade:**

Sejam $a, b, c \in A$.

Suponha que $(a, b) \in R_1 \cap R_2$ (5) e $(b, c) \in R_1 \cap R_2$ (6).

De (5), temos $(a, b) \in R_1$ e $(a, b) \in R_2$.
De (6), temos $(b, c) \in R_1$ e $(b, c) \in R_2$.

Logo, de (1), pela definição de transitividade, $(a, c) \in R_1$. Analogamente, de (2), temos $(a, c) \in R_2$.

Assim, pela definição de interseção, segue que $(a, c) \in R_1 \cap R_2$.

**Comparabilidade:**

Sejam $a, b \in A$.

De (1), temos que $(a, b) \in R_1$ ou $(b, a) \in R_1$.
De (2), temos que $(a, b) \in R_2$ ou $(b, a) \in R_2$.

Precisamos dividir a demonstração em 4 casos:

- $(a, b) \in R_1$ e $(a, b) \in R_2$;
- $(a, b) \in R_1$ e $(b, a) \in R_2$;
- $(b, a) \in R_1$ e $(a, b) \in R_2$;
- $(b, a) \in R_1$ e $(b, a) \in R_2$.

Irei apresentar um contraexemplo para o segundo caso.

Tome $A = \{ a, b \}$, com $a \neq b$. Considere as relações $R_1 = i_A \cup \{ (a, b) \}$ e $R_2 = i_A \cup \{ (b, a) \}$.

Note que tanto $R_1$ quanto $R_2$ são relações de ordem total em $A$, mas $R_1 \cap R_2 = i_A$. Desse modo, $R_1 \cap R_2$ não satisfaz a comparabilidade, pois todos os elementos do conjunto deveriam estar relacionados em algum sentido (faltando, neste caso, $(a, b)$ ou $(b, a)$).

Portanto, pela ausência da comparabilidade em $R_1 \cap R_2$, concluímos que $R_1 \cap R_2$ não é uma relação de ordem total. $\blacksquare$

# Questão 5

Sejam $R \subseteq A \times B$ e $S \subseteq B \times C$. Verifique se $Dom(R) \subseteq Dom(S \circ R)$. Justifique.

Vamos apresentar um contraexemplo.

Tome $A = \{ 1 \}$, $B = \{2\}$ e $C = \{3\}$.

Considere as relações $R = \{ (1,2) \}$ e $S = \emptyset$.

Perceba que $Dom(R) = \{ 1 \}$ e $Dom(S) = \emptyset$. Além disso, $S \circ R = \emptyset$, logo $Dom(S \circ R) = \emptyset$.

Concluímos que $Dom(R) \nsubseteq Dom(S \circ R)$. Portanto a afirmação é falsa. $\blacksquare$
