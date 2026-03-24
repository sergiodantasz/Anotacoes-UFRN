# Medidas de Tendência Central

## Média Aritmética

É a soma de todos os valores dividida pela quantidade de elementos.

$$
\text{Média} = \frac{x_1 + x_2 + \cdots + x_n}{n}
$$

## Mediana

É o valor que fica no meio dos dados quando eles estão ordenados.

Se o número de elementos for par, a mediana é a média aritmética entre os dois elementos centrais.

$$
\text{Mediana} =
\begin{cases}
x_{\frac{n+1}{2}}, & \text{se } n \text{ é ímpar} \\\\
\frac{x_{\frac{n}{2}} + x_{\frac{n}{2}+1}}{2}, & \text{se } n \text{ é par}
\end{cases}
$$

## Moda

É o valor que aparece com mais frequência.

# Medidas de Posição

## Quartis

Dividem os dados ordenados em 4 partes iguais.

- ($Q_1$): separa os primeiros 25% dos dados;
- ($Q_2$): separa 50% dos dados (é a mediana);
- ($Q_3$): separa 75% dos dados.

$$
Q_k = x_{\frac{k(n+1)}{4}}, \quad k = 1,2,3
$$

## Decis

Dividem os dados ordenados em 10 partes iguais.

- ($D_1$): 10% dos dados abaixo;
- ($D_5$): 50% (mediana);
- ($D_9$): 90% dos dados abaixo.

$$
D_k = x_{\frac{k(n+1)}{10}}, \quad k = 1,2,\dots,9
$$

## Percentis

Dividem os dados ordenados em 100 partes iguais.

- ($P_1$): 1% dos dados abaixo;
- ($P_{50}$): mediana;
- ($P_{90}$): 90% dos dados abaixo.

$$
P_k = x_{\frac{k(n+1)}{100}}, \quad k = 1,2,\dots,99
$$

# Medidas de Dispersão

## Amplitude

É a diferença entre o maior e o menor valor do conjunto de dados.

$$
\text{Amplitude} = x_{\text{máx}} - x_{\text{mín}}
$$

## Variância

Mede o quanto os dados estão dispersos em relação à média.

$$
\sigma^2 = \frac{\sum_{i=1}^{n} (x_i - \mu)^2}{n}
$$

Para amostras:

$$
s^2 = \frac{\sum_{i=1}^{n} (x_i - \bar{x})^2}{n-1}
$$

## Desvio Padrão

É a raiz quadrada da variância.

$$
\sigma = \sqrt{\sigma^2}
$$

Para amostras:

$$
s = \sqrt{s^2}
$$

## Desvio Médio

É a média dos desvios absolutos em relação à média.

$$
\text{Desvio Médio} = \frac{\sum_{i=1}^{n} |x_i - \mu|}{n}
$$

## Intervalo Interquartil

É a diferença entre o terceiro e o primeiro quartil.

$$
IQR = Q_3 - Q_1
$$

## Coeficiente de Variação

Mede a dispersão relativa em relação à média.

$$
CV = \frac{\sigma}{\mu}
$$

Para amostras:

$$
CV = \frac{s}{\bar{x}}
$$

# Medidas de Relação e Associação

## Covariância

Mede como duas variáveis variam juntas.

- Valor positivo: crescem juntas;
- Valor negativo: uma cresce enquanto a outra diminui;
- Valor próximo de 0: pouca relação linear.

$$
\text{Cov}(X,Y) = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{n}
$$

## Correlação de Pearson

Mede a força e a direção da relação linear entre duas variáveis. Varia entre -1 e 1.

- 1: correlação positiva perfeita;
- -1: correlação negativa perfeita;
- 0: sem correlação linear.

$$
r = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\left(\sum_{i=1}^{n} (x_i - \bar{x})^2\right)\left(\sum_{i=1}^{n} (y_i - \bar{y})^2\right)}}
$$

> A correlação é a covariância normalizada.

## Coeficiente de Determinação

Indica a proporção da variação de uma variável que é explicada pela outra.

Varia entre 0 e 1. Quanto maior, melhor a explicação do modelo.

$$
R^2 = r^2
$$

## Regressão Linear Simples

Modela a relação entre duas variáveis por meio de uma reta.

$$
y = a + bx
$$

Onde:

- $b$ é o coeficiente angular (inclinação da reta);
- $a$ é o coeficiente linear (intercepto).

$$
b = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^{n} (x_i - \bar{x})^2}
$$

$$
a = \bar{y} - b\bar{x}
$$

# Medidas de Forma  

## Assimetria

Mede o grau de simetria da distribuição.

- Assimetria > 0: cauda à direita;
- Assimetria < 0: cauda à esquerda;
- Assimetria = 0: distribuição simétrica.

$$
\text{Assimetria} = \frac{\frac{1}{n}\sum_{i=1}^{n}(x_i - \mu)^3}{\sigma^3}
$$

## Curtose

Mede o grau de concentração dos dados em torno da média.

Considere o excesso de curtose:

$$
\text{Excesso de Curtose} = \text{Curtose} - 3
$$

- > 0: leptocúrtica (mais concentrada, caudas pesadas);
- < 0: platicúrtica (mais achatada, dados mais espalhados);
- = 0: mesocúrtica (semelhante à normal).

$$
\text{Curtose} = \frac{\frac{1}{n}\sum_{i=1}^{n}(x_i - \mu)^4}{\sigma^4}
$$
