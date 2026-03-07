# Linguagem C 

## 1. Estrutura básica

```c
#include <stdio.h>

int main() {
    printf("Olá, mundo!\n");
    return 0;
}
```

## 2. Fundamentos

### 2.1. Tipos de dados

| Tipo     | Descrição        |
| -------- | ---------------- |
| `int`    | Inteiro          |
| `float`  | Ponto flutuante  |
| `double` | Precisão dupla   |
| `char`   | Caractere        |
| `void`   | Ausência de tipo |

**Modificadores de tipo:**

| Modificador | Aplica-se a     |
| ----------- | --------------- |
| `signed`    | `char`, `int`   |
| `unsigned`  | `char`, `int`   |
| `short`     | `int`           |
| `long`      | `int`, `double` |

### 2.2. Variáveis e constantes

**Declaração:**

```c
int x;
```

**Inicialização:**

```c
int x = 10;
const int y = 20;
```

## 3. Entrada e saída de dados

As funções de entrada e saída padrão estão na biblioteca `stdio.h`. O programa se comunica com o teclado (entrada) e com o terminal (saída).

### 3.1. Saída com `printf`

`printf` envia texto e valores formatados para a saída padrão (tela).

**Texto simples:**

```c
printf("Olá, mundo!\n");
```

**Especificadores de formato** — placeholders que são substituídos pelos valores das variáveis:

| Especificador | Tipo                           | Exemplo                |
| ------------- | ------------------------------ | ---------------------- |
| `%d` ou `%i`  | `int`                          | `printf("%d", x);`     |
| `%f`          | `float` / `double`             | `printf("%f", y);`     |
| `%c`          | `char`                         | `printf("%c", letra);` |
| `%s`          | string                         | `printf("%s", nome);`  |
| `%lf`         | `double` (leitura com `scanf`) | —                      |
| `%%`          | literal `%`                    | `printf("50%%");`      |

**Controlando casas decimais em `float`/`double`:**

```c
double pi = 3.14159;
printf("%.2f", pi);   /* 3.14 */
printf("%5d", 42);   /* "   42" (largura 5) */
```

### 3.2. Entrada com `scanf`

`scanf` lê dados da entrada padrão (teclado). É preciso passar o **endereço** da variável (usa-se `&` antes do nome, exceto em strings/arrays).

**Sintaxe:**

```c
scanf("formato", &variavel);
```

**Exemplos:**

```c
int idade;
scanf("%d", &idade);

float preco;
scanf("%f", &preco);

double valor;
scanf("%lf", &valor);

char letra;
scanf(" %c", &letra);   /* o espaço antes de %c consome Enter/whitespace anterior */

char nome[50];
scanf("%s", nome);      /* nome já é endereço; lê até espaço ou Enter */
```

**Lendo vários valores de uma vez:**

```c
int a, b;
scanf("%d %d", &a, &b);
```

### 3.3. `getchar` e `putchar`

Para um único caractere:

```c
char c = getchar();   /* lê um caractere da entrada */
putchar(c);           /* imprime um caractere na saída */
```

`getchar()` retorna um `int` (para poder representar `EOF`). Em uso simples, pode ser atribuído a um `char`.

## 4. Operadores

### 4.1. Aritméticos

| Operador | Descrição     |
| -------- | ------------- |
| `+`      | Soma          |
| `-`      | Subtração     |
| `*`      | Multiplicação |
| `/`      | Divisão (inteira se os dois operandos forem `int`) |
| `%`      | Resto (módulo) |

**Exemplo:**

```c
soma = 1 + 2;
subtracao = 6 - 9;
multiplicacao = 2 * 2;
divisao = 2 / 2;           /* com int: divisão inteira */
divisao_inteiro = 5 / 2;   /* resultado: 2 */
resto = 10 % 3;
```

### 4.2. Relacionais

```c
==   !=   >   <   >=   <=
```

### 4.3. Lógicos

| Operador | Significado |
| -------- | ----------- |
| `&&`     | E (AND)     |
| `\|\|`   | OU (OR)     |
| `!`      | NÃO (NOT)   |

### 4.4. Atribuição

```c
=   +=   -=   *=   /=   %=
```

### 4.5. Incremento e decremento

```c
++   --
```

**Exemplo:**

```c
i++;
--j;
```

## 5. Controle de fluxo

### 5.1. Condicionais

**`if` / `else if` / `else`:**

```c
if (x < 0) {
    printf("negativo");
} else if (x > 0) {
    printf("positivo");
} else {
    printf("nulo");
}
```

**`switch` / `case`:**

```c
switch (op) {
    case 1:
        printf("um");
        break;
    case 2:
        printf("dois");
        break;
    default:
        printf("inválido");
}
```

### 5.2. Laços de repetição

**`for`:**

```c
for (int i = 0; i < 10; i++) {
    printf("%d\n", i);
}
```

**`while`:**

```c
while (x < 10) {
    x++;
}
```

**`do-while`:**

```c
do {
    x++;
} while (x < 10);
```

## 6. Funções

**Definição:**

```c
int soma(int a, int b) {
    return a + b;
}
```

**Uso:**

```c
int r = soma(3, 4);
```

## 7. Arrays e strings

### 7.1. Arrays

**Declaração:**

```c
int v[5];
```

**Inicialização:**

```c
int v[5] = {1, 2, 3, 4, 5};
```

**Acesso:**

```c
v[0];
v[1];
```

### 7.2. Strings

Em C, strings são **arrays de `char`** terminados pelo caractere nulo `\0`.

**Declaração:**

```c
char nome[] = "Sergio";
```

Representação em memória (sem espaços):

```
S  e  r  g  i  o  \0
```

## 8. Ponteiros

### 8.1. Conceito

Um **ponteiro** é uma variável que armazena o **endereço de memória** de outra variável.

**Declaração:**

```c
int *p;
```

**Operadores:**

| Operador | Significado   |
| -------- | ------------- |
| `&`      | Endereço de   |
| `*`      | Desreferência |

**Exemplo:**

```c
int x = 10;
int *p = &x;           /* p guarda o endereço de x */

printf("%d", *p);      /* desreferencia: acessa o valor 10 */
```

### 8.2. Ponteiros e arrays

O nome de um array equivale ao endereço do primeiro elemento. Arrays e ponteiros estão fortemente relacionados.

```c
int v[3] = {1, 2, 3};
int *p = v;
```

**Acesso equivalente:**

```c
v[i]
*(v + i)
```

### 8.3. Aritmética de ponteiros

Ponteiros podem ser incrementados/decrementados (o valor avança de acordo com o tamanho do tipo).

```c
int v[3] = {1, 2, 3};
int *p = v;

p++;    /* agora p aponta para v[1] */
```

### 8.4. Ponteiro para ponteiro

Um ponteiro pode apontar para outro ponteiro.

```c
int x = 5;
int *p = &x;
int **pp = &p;
```

Representação: `pp` → `p` → `x`

**Acesso:**

```c
**pp == 5
```

### 8.5. Ponteiros e funções

Em C os argumentos são passados **por valor**. Para alterar a variável original, usa-se ponteiro (passagem por referência).

```c
void f(int *x) {
    *x = 10;
}

/* Uso: */
int a = 5;
f(&a);   /* a passa a ser 10 */
```

## 9. Tipos compostos

### 9.1. Structs

**Structs** permitem criar tipos compostos (agrupar vários campos).

**Definição e uso:**

```c
struct Pessoa {
    char nome[50];
    int idade;
};

struct Pessoa p;
p.idade = 20;
```

**Inicialização:**

```c
struct Pessoa p1 = {"Ana", 25};

struct Pessoa p2 = {
    .nome = "Ana",
    .idade = 25
};
```

### 9.2. Structs e ponteiros

Com ponteiro para struct, o acesso ao campo pode ser feito de duas formas:

```c
struct Pessoa *p;

(*p).idade   /* forma explícita */
p->idade     /* forma usual: -> desreferencia e acessa o campo */
```

### 9.3. Typedef

`typedef` cria um **alias** para um tipo existente (útil para encurtar nomes, principalmente com structs).

```c
/* Sem typedef */
struct Point { int x, y; };
struct Point p1;

/* Com typedef */
typedef struct { int x, y; } Point;
Point p2;
```

### 9.4. Enum

`enum` define um conjunto de **constantes inteiras nomeadas**. Por padrão começam em 0 e incrementam.

**Definição:**

```c
enum Dia {
    SEG,
    TER,
    QUA,
    QUI,
    SEX
};
```

Valores implícitos: `SEG = 0`, `TER = 1`, `QUA = 2`, …

**Uso:**

```c
enum Dia hoje = SEG;
```

**Valores explícitos:**

```c
enum Status {
    OK = 200,
    NOT_FOUND = 404,
    ERROR = 500
};
```
