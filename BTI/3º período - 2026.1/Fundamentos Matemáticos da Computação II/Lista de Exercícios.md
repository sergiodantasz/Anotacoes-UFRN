# Questão 1

**Injetividade:**

Note que $f(-1) = (-1)^2 + 2 = 1 + 2 = 3$. Veja também que $f(1) = 4 - 1^2 = 4 - 1 = 3$. Como $f(-1) = f(1)$ e $-1 \neq 1$, logo $f$ não é injetiva.

**Sobrejetividade:**

Seja $y \in \mathbb{R}$.

**Caso $y \geq 3$:**

Tome $x = -\sqrt{y - 2}$.

Calculamos:

$$
\begin{align}
f(x) &= f\left(-\sqrt{y - 2}\right) \\
     &= \left(-\sqrt{y - 2}\right)^2 + 2 \\
     &= y - 2 + 2 \\
     &= y
\end{align}
$$

Logo $f$ é sobrejetiva.

**Caso $y < 3$:**

Tome $x = \sqrt{4 - y}$.

Calculamos:

$$
\begin{align}
f(x) &= f\left(\sqrt{4 - y}\right) \\
     &= 4 - \left(\sqrt{4 - y}\right)^2 \\
     &= 4 - (4 - y) \\
     &= 4 - 4 + y \\
     &= y
\end{align}
$$

Logo $f$ é sobrejetiva.

**Inversa:**

Como $f$ não é sobrejetiva, logo ela não possui inversa.

# Questão 2

## (c)

**Injetividade:**

Sejam $x_1, x_2 \in \mathbb{R}$ tais que $f(x_1) = f(x_2)$.

Calculamos:

$$
\begin{align}
f(x_1) = f(x_2)
             &\implies \frac{x_1}{3} + \frac{3}{2} = \frac{x_2}{3} + \frac{3}{2} \\
             &\implies \frac{x_1}{3} = \frac{x_2}{3} \\
             &\implies x_1 = x_2
\end{align}
$$

Logo $f$ é injetiva.

**Sobrejetividade:**

Seja $y \in \mathbb{R}$.

Tome $x = 3\left( y - \frac{3}{2} \right)$.

Calculamos:

$$
\begin{align}
f(x) &= f\left(3\left( y - \frac{3}{2} \right)\right) \\
     &= \frac{3\left( y - \frac{3}{2} \right)}{3} + \frac{3}{2} \\
     &= y - \frac{3}{2} + \frac{3}{2} \\
     &= y
\end{align}
$$

Logo $f$ é sobrejetiva.

**Inversa:**

Como $f$ é bijetiva, vamos encontrar sua inversa.

Calculamos:

$$
\begin{align}
f(x) = \frac{x}{3} + \frac{3}{2} &\iff f(x) - \frac{3}{2} = \frac{x}{3} \\
                              &\iff x = 3\left(f(x) - \frac{3}{2}\right)
\end{align}
$$

Após a troca de variáveis teremos:

$$
f^{-1}(y) = 3\left(y - \frac{3}{2}\right)
$$

Logo a inversa de $f$ é dada por $f^{-1}(y) = 3\left(y - \frac{3}{2}\right)$.

# Questão 6

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

# Questão 9

Como a $A \cup B = B$, é imediato que $A \subseteq B$. Então sobram duas possibilidades: $A = \emptyset$ ou $A \neq \emptyset$. Mas perceba que $A \setminus B = A$. Logo, como $A \subseteq B$, então $A \setminus B = \emptyset$. Se $A \neq \emptyset$, chegamos a uma contradição. Desse modo, temos necessariamente $A = \emptyset$.

Dado $A = \emptyset$, segue que $A \cap C = \emptyset$. Como $A \cap C = B \cap C$, logo $B \cap C = \emptyset$. Podemos afirmar que $B$ e $C$ são conjuntos disjuntos. Nada mais além disso.

# Questão 10

Vamos refutar essa afirmação.

Tome $A = \{ 1 \}$, $B = \emptyset$, $C = \emptyset$ e $D = \{ 2 \}$.

Perceba que $A \cup C = \{ 1 \}$ e $B \cup D = \{ 2 \}$. Disso, temos:

$$
(A \cup C) \times (B \cup D) = \{ (1, 2) \}
$$

Agora, note que $A \times B = \emptyset$ e $C \times D = \emptyset$. Disso, segue que:

$$
(A \times B) \cup (C \times D) = \emptyset
$$

Como $\{ (1, 2) \} \nsubseteq \emptyset$, logo a afirmação é falsa.

# Questão 13

**a)** $f(D) \subseteq f(C) \implies D \subseteq C$

Vamos refutar essa afirmação.

Tome $f(x) = 0$, $C = \{ 1 \}$ e $D = \{ 2 \}$.

Note que $f(C) = \{ 0 \}$ e $f(D) = \{ 0 \}$. Logo $f(D) \subseteq f(C)$, mas $D \nsubseteq C$.

Sendo assim, a afirmação é falsa.

**b)** $D \subseteq C \implies f(D) \subseteq f(C)$

Suponha que $D \subseteq C$.

Seja $y \in f(D)$.

Pela definição de imagem, existe $x \in D$ tal que $f(x) = y$.

Como $x \in D$ e $D \subseteq C$, logo, pela definição de subconjunto, $x \in C$.

Como $x \in C$ e $f(x) = y$, então $y \in f(C)$.

Portanto, $f(D) \subseteq f(C)$.
