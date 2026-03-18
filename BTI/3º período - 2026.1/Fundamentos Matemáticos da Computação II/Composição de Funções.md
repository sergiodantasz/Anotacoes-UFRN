# Composição de Funções

Sejam $f : A \to B$ e $g : B \to C$ duas funções. A composição de $g$ com $f$, dada por $g \circ f$, é:

$$
\displaylines{
g \circ f : A \to C \\
(g \circ f)(x) = g(f(x))
}
$$

$$
g \circ f = \{ (a, c) \mid \exists b \in B \text{ tal que } (a, b) \in f \land (b, c) \in g\}
$$

# Função Identidade

A função identidade $i_A : A \to A$ é uma função cujo domínio e contradomínio são iguais, isto é, $i_A(x) = x$.

# Exercícios

> Demonstre ou refute as seguintes proposições.

Sejam $f : A \to B$ e $g : B \to C$ duas funções.

## Ex. 1

> [!example] Proposição
> Se $f$ e $g$ são injetivas, então $g \circ f$ é injetiva.

**Demonstração:**

Suponha que $f$ e $g$ são injetivas.

Sejam $x_1, x_2 \in A$.

Suponha que $g \circ f (x_1) = g \circ f (x_2)$.

Calculamos:

$$
\begin{align}
g \circ f (x_1) = g \circ f (x_2)
                     &\iff g(f(x_1)) = g(f(x_2)) \\
                     &\iff f(x_1) = f(x_2) &\quad& (g \text{ é injetiva}) \\
                     &\iff x_1 = x_2 &\quad& (f \text{ é injetiva})
\end{align}
$$

Logo $g \circ f$ é injetiva. $\blacksquare$

## Ex. 2

> [!example] Proposição
> Se $g \circ f$ é injetiva, então $f$ é injetiva.

**Demonstração:**

Suponha que $g \circ f$ é injetiva.

Sejam $x_1, x_2 \in A$ tais que $f(x_1) = f(x_2)$.

Como $g \circ f$ é injetiva, então $g \circ f (x_1) = g \circ f (x_2) \implies x_1 = x_2$.

Por $g$ ser função, veja que $f(x_1) = f(x_2) \implies g(f(x_1)) = g(f(x_2))$. Logo $g \circ f (x_1) = g \circ f (x_2)$. De sua injetividade, temos que $x_1 = x_2$.

Portanto $f$ é injetiva. $\blacksquare$

## Ex. 3

> [!example] Proposição
> Se $f$ e $g$ são sobrejetivas, então $g \circ f$ é sobrejetiva.

**Demonstração:**

Suponha que $f$ e $g$ são sobrejetivas.

Seja $c \in C$.

Como $g$ é sobrejetiva, logo existe $b \in B$ tal que $g(b) = c$ (1). Logo, por $f$ ser sobrejetiva, então existe $a \in A$ tal que $f(a) = b$ (2).

De (1) e (2), temos que:

$$
\begin{align}
c &= g(b) \\
  &= g(f(a)) \\
  &= g \circ f (a)
\end{align}
$$

Portanto $g \circ f$ é sobrejetiva. $\blacksquare$

## Ex. 4

> [!example] Proposição
> Se $g \circ f$ é sobrejetiva, então $g$ é sobrejetiva.

**Demonstração:**

Suponha que $g \circ f$ é sobrejetiva.

Seja $c \in C$.

Aplicando a sobrejetividade de $g \circ f$ em $c$, temos que existe $a \in A$ tal que $g \circ f(a) = c$.

Como $f$ é função, então existe $b \in B$ tal que $f(a) = b$.

Note que:

$$
g \circ f (a) = g(f(a)) = g(b) = c
$$

Portanto $g$ é sobrejetiva. $\blacksquare$

## Ex. 5

> [!example] Proposição
> $g \circ f : A \to C$ é uma função.

> **Formalização:** $(\forall a \in A)(\exists! c \in C)[g \circ f (a) = c]$

**Demonstração:**

**Existência:**

Seja $a \in A$.

Como $f$ é função, então existe $b \in B$ tal que $f(a) = b$. Ou seja, $g(f(a)) = g(b)$.

Como $g$ também é função, logo existe $c \in C$ tal que $g(b) = c$.

Logo, para um elemento arbitrário $a \in A$, temos $c \in C$ tal que $g \circ f (a) = c$.

**Unicidade:**

Suponha, por contradição, que existe $a \in A$ que vá para dois elementos distintos em $C$, isto é, existem $c_1 \in C$ e $c_2 \in C$, com $c_1 \neq c_2$, tais que $g \circ f (a) = c_1$ e $g \circ f (a) = c_2$.

Note que $c_1 = g \circ f (a) = g(f(a))$.

Como $f$ é função, existe $b \in B$ tal que $f(a) = b$, ou seja, $c_1 = g(f(a)) = g(b)$.

Veja também que $c_2 = g \circ f (a) = g(f(a)) = g(b)$.

Como $g$ é função, $g(b)$ retorna exatamente um resultado. Logo $c_1 = g(b) = c_2$. Isso é uma contradição, pois supomos que $c_1 \neq c_2$.

Portanto, pela existência e pela unicidade, temos que $g \circ f$ é uma função. $\blacksquare$

## Ex. 6

> [!example] Proposição
> Se $f$ possui inversa, então $f \circ f^{-1} = i_B$ e $f^{-1} \circ f = i_A$.

**Demonstração:**

Seja $b \in B$.

Como $f^{-1}$ é função, existe $a \in A$ tal que $f^{-1}(b) = a$.

Veja que:

$$
f \circ f^{-1} (b) = f(f^{-1}(b)) = f(a) = b
$$

Como $f$ também é função, existe $b \in B$ tal que $f(a) = b$.

Note também que:

$$
f^{-1} \circ f (a) = f^{-1}(f(a)) = f^{-1}(b) = a
$$

Portanto, $f \circ f^{-1} = i_B$ e $f^{-1} \circ f = i_A$. $\blacksquare$

## Ex. 7

> [!example] Proposição
> A inversa de uma função é única.

**Demonstração:**

Seja $f : A \to B$.

Suponha, por contradição, que $f$ possui duas inversas distintas $f^{-1}$ e $f'$.

Calculamos:

$$
\begin{align}
f^{-1} &= f^{-1} \circ i_B &\quad& (\text{Ex. 9}) \\
       &= f^{-1} \circ (f \circ f') &\quad& (\text{Ex. 6}) \\
       &= (f^{-1} \circ f) \circ f' &\quad& (\text{Ex. 8}) \\
       &= i_A \circ f' &\quad& (\text{Ex. 6}) \\
       &= f' &\quad& (\text{Ex. 9})
\end{align}
$$

Absurdo, pois supomos $f^{-1} \neq f'$.

Portanto, a inversa de uma função qualquer é única. $\blacksquare$

## Ex. 8

> [!example] Proposição
> Seja $h : C \to D$. Então $h \circ (g \circ f) = (h \circ g) \circ f$.

**Demonstração:**

...

## Ex. 9

> [!example] Proposição
> $f \circ i_A = f = i_b \circ f$

**Demonstração:**

...
