Considere $g = f \cap (C \times B)$.

Suponha, por contradição, que $g$ não é uma função.

Seja $c \in C$ um elemento que satisfaz a proposição.

Vamos separar a demonstração em dois casos.

**Caso 1:**

Como $c \in C$ e $C \subseteq A$, então $c \in A$. Logo existe $b \in B$ tal que $(c, b) \in f$. Além disso, temos que $(c, b) \in C \times B$. Logo $(c, b) \in f \cap (C \times B)$, isto é, $(c, b) \in g$.

Dado $b \in B$, extraímos da nossa hipótese que $(c, b) \notin g$. Chegamos a um absurdo. Sendo assim, $g$ é função.

**Caso 2:**

Sejam $b_1, b_2 \in B$ tais que $(c, b_1) \in g$, $(c, b_2) \in g$ e $b_1 \neq b_2$. Logo $(c, b_1) \in C \times B$ e $(c, b_2) \in C \times B$.

Como $c \in C$ e $C \subseteq A$, então $c \in A$. Como $f : A \to B$, logo $(c, b_1) \in f$ e $(c, b_2) \in f$. Como $f$ é uma função, $c$ aponta para um mesmo elemento do contradomínio, ou seja, necessariamente $b_1 = b_2$. Absurdo, pois temos como dado $b_1 \neq b_2$. Portanto, $g$ é função.