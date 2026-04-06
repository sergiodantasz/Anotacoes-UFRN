# Introdução

Se existe uma função bijetiva $f : A \to B$, dizemos que $A$ e $B$ têm a mesma cardinalidade.

Denotamos esse fato por:

$$
A \sim B \quad \text{ou} \quad |A| = |B|
$$

# Propriedades

- $A \sim A$ (reflexividade);
- Se $A \sim B$, então $B \sim A$ (simetria);
- Se $A \sim B$ e $B \sim C$, então $A \sim C$ (transitividade).

# Conjunto Infinito

$$
A \text{ é infinito} \iff \exists B \neq A, B \subseteq A \land A \sim B
$$

# Conjunto Finito

Considere $I_n = \{ x \in \mathbb{N} \mid x < n \}$, com $|I_n| = n$.

$$
A \text{ é finito} \iff \exists n \in \mathbb{N}, A \sim I_n
$$

# Princípio da Casa dos Pombos (PCP)

Se em $n$ caixas colocarmos mais de $n$ objetos, alguma caixa terá mais de 1 objeto.

Seja $f : A \to B$ uma função.

- Se $|A| > |B|$, então $f$ não é injetiva;
- Se $|A| < |B|$, então $f$ não é sobrejetiva.

**Exemplo:**

Sejam $n \in \mathbb{N}$ e $A \subseteq \{ 0, 1, 2, \ldots, 2n - 1 \}$.

Mostre que se $|A| = n + 2$, então existem $a, a' \in A$, com $a \neq a'$, tais que $a + a' = 2n$.

Suponha que $|A| = n + 2$.

Considere $A' = A \setminus \{0, n\}$.

[terminar]

# Conjunto Enumerável

$$
A \text{ é enumerável} \iff A \sim \mathbb{N}
$$

# Conjunto Contável

$$
A \text{ é contável} \iff A \text{ é finito} \lor A \text{ é enumerável}
$$
