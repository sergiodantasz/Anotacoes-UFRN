Suponha que existe $g : B \to C$ tal que $g \circ f = i_A$.

Sejam $a_1, a_2 \in A$ tais que $f(a_1) = f(a_2)$. Note que $i_A(a_1) = a_1$ e $i_A(a_2) = a_2$.

Logo existem $b_1, b_2 \in B$ tais que $f(a_1) = b_1$ e $f(a_2) = b_2$. Logo existem $c_1, c_2 \in C$ tais que $g(b_1) = c_1$ e $g(b_2) = c_2$.

Calculamos:

$$
\begin{align}
a_1 &= i_A(a_1) \\
    &= (g \circ f)(a_1) \\
    &= g(f(a_1)) \\
    &= g(b_1) \\
    &= c_1
\end{align}
$$

Calculamos:

$$
\begin{align}
a_2 &= i_A(a_2) \\
    &= (g \circ f)(a_2) \\
    &= g(f(a_2)) \\
    &= g(b_2) \\
    &= c_2
\end{align}
$$

Como $f(a_1) = f(a_2)$, logo $b_1 = b_2$. Disso, temos que $g(b_1) = g(b_2)$. Por fim, $c_1 = c_2$.

Como $c_1 = a_1$ e $c_2 = a_2$, logo $a_1 = a_2$.

Portanto $f$ é injetiva.