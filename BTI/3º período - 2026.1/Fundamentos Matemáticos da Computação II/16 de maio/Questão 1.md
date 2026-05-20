# a)

Suponha $R$ e $S$ funcionais.

Sejam $a \in A$ e $c_1, c_2 \in C$.

Suponha $(a, c_1) \in S \circ R$ (1) e $(a, c_2) \in S \circ R$ (2).

De (1), pela definição de composição, existe $b_1 \in B$ tal que $(a, b_1) \in R$ e $(b_1, c_1) \in S$.
De (2), existe $b_2 \in B$ tal que $(a, b_2) \in R$ e $(b_2, c_2) \in S$.

Como $R$ é funcional, $(a, b_1) \in R$ e $(a, b_2) \in R$, logo $b_1 = b_2$.
Como $S$ é funcional, $(b_1, c_1) \in S$ e $(b_2, c_2) \in S$, logo $c_1 = c_2$.

Portanto $S \circ R$ é funcional. $\blacksquare$

# b)

Suponha $R$ e $S$ totais.