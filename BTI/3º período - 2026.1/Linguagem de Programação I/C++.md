# Linguagem C++

## 1. Estrutura básica

### 1.1. Função `main`

`main()` é a função principal: a execução do programa começa nela. O C++ exige que o programa tenha uma função `main`.

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Olá Mundo" << endl;
    return 0;
}
```

- `#include <iostream>` — biblioteca para entrada e saída (`cin`, `cout`).
- `using namespace std` — permite usar `cout` em vez de `std::cout`.

### 1.2. Comentários

- `//` — comentário de uma linha.
- `/* */` — comentário de várias linhas.

```cpp
// Comentário simples
/*
   Comentário de múltiplas linhas
*/
```

## 2. Novos tipos de dados em relação ao C

O C++ adicionou tipos que não existem no C:

| Tipo     | Descrição |
| -------- | --------- |
| `bool`   | Valores lógicos: `true` ou `false`. |
| `string` | Classe da biblioteca padrão (`<string>`) para texto; substitui o uso de `char[]` do C. |

**Tipo `bool`:**

- Pode ser `true` ou `false`.
- Usa-se com operadores lógicos: `&&` (E), `||` (OU), `!` (negação).
- **Conversão automática:** inteiro diferente de zero → `true`; zero → `false`.

**Tipo `string`:**

- Em C, strings são arrays de caracteres (`char[]`). Em C++, `string` gerencia memória automaticamente.
- Operações: concatenação com `+`, comparação com `==`, `<`, etc., `.size()` ou `.length()`, `.clear()`, entre outras.
- Incluir: `#include <string>` (e pertence ao `std`).

## 3. Variáveis

Declaração e inicialização dos tipos básicos:

```cpp
int numerointeiro = 5;
double numerosDecimais = 5.99;
char letra = 'D';
string textos = "Hello";
bool boleano = true;
```

**Faixas e exemplos (resumo):**

| Tipo    | Exemplo / Faixa |
| ------- | ----------------- |
| `int`   | -2.147.483.648 a 2.147.483.647 |
| `double`| Ponto flutuante (grande faixa) |
| `char`  | `'a'`, `'b'` |
| `string`| `"Hello World"` |
| `bool`  | `true` ou `false` |

### 3.1. `auto`

O tipo é definido na primeira atribuição e não pode mudar depois. A **inicialização é obrigatória**.

```cpp
auto idade = 10;           // tipo int
auto nome = string("Ana"); // tipo string
```

## 4. Entrada e saída

A biblioteca `iostream` (C++) oferece:

- `cout` — saída padrão (console).
- `cin` — entrada padrão (teclado).

### 4.1. `cout`

Usa-se o operador `<<` para cada parte da saída.

```cpp
cout << "Olá Mundo" << endl;
cout << "Idade: " << idade << endl;
```

**Quebra de linha:** use `\n` ou `endl`.

- `\n` — apenas insere quebra de linha.
- `endl` — insere quebra de linha e faz **flush** do buffer (a saída é mostrada imediatamente).

### 4.2. `cin`

Usado para ler entradas do usuário (oposto do cout).

```cpp
int idade;
cout << "Digite sua idade: ";
cin >> idade;
cout << "Você tem " << idade << " anos." << endl;
```

**Atenção:** `cin` lê até espaço ou Enter; ao ler um número, deixa um `\n` no buffer. Para ler uma **linha inteira com espaços**, use `getline()`.

### 4.3. `getline`

Lê o conteúdo inteiro de uma linha (até o `\n`), não deixando nada no buffer.

```cpp
string linha;
getline(cin, linha);
```

**Problema comum:** depois de `cin >> numero`, o `\n` fica no buffer e o próximo `getline` pode ler linha vazia.

Soluções:

- Remover o `\n` do buffer antes do `getline`, ou
- Ler o número com `getline` e depois converter para o tipo apropriado (veja abaixo).

### 4.4. Conversão de string para número

Funções da biblioteca `<string>` (namespace `std`):

| Função   | Retorno        | Descrição |
| -------- | -------------- | --------- |
| `stoi`   | `int`          | string → int |
| `stol`   | `long`         | string → long |
| `stoll`  | `long long`    | string → long long |
| `stoul`  | `unsigned long`| string → unsigned long |
| `stoull` | `unsigned long long` | string → unsigned long long |
| `stof`   | `float`        | string → float |
| `stod`   | `double`       | string → double |
| `stold`  | `long double`  | string → long double |

Exemplo: `int n = stoi("42");`

### 4.5. Comparação de strings

Em C++ é possível comparar `string` com `==` (diferente do C).

```cpp
string nome = "Ana";
if (nome == "Ana") {
    cout << "Olá, Ana!" << endl;
}
```

## 5. Controle de fluxo

### 5.1. `if` / `else if` / `else`

Executa um bloco de código condicionalmente.

```cpp
int x = 10;
if (x > 5) {
    cout << "Maior que 5" << endl;
} else if (x == 5) {
    cout << "Igual a 5" << endl;
} else {
    cout << "Menor que 5" << endl;
}
```

### 5.2. `switch` / `case`

Seleciona entre vários blocos com base no valor de uma variável. Usado quando há muitas opções.

```cpp
switch (opcao) {
    case 1:
        cout << "Opção 1" << endl;
        break;
    case 2:
        cout << "Opção 2" << endl;
        break;
    default:
        cout << "Outra opção" << endl;
        break;
}
```

- **break** — termina o `switch` (ou o loop). Sem `break`, a execução **cai** no próximo `case`.
- A partir do **C++17**, é possível inicializar variável dentro do `switch`.

### 5.3. `while`

Repete um bloco **enquanto** a condição for verdadeira.

```cpp
while (i < 5) {
    cout << "i = " << i << endl;
    i++;
}
```

- **break** — termina o loop.
- **continue** — pula para a próxima iteração.

### 5.4. `do-while`

Executa o bloco **pelo menos uma vez** e repete enquanto a condição for verdadeira. A condição é testada **depois** da execução.

```cpp
do {
    cout << "j = " << j << endl;
    j++;
} while (j < 5);
```

### 5.5. `for`

Repete um bloco com controle de início, condição e incremento.

```cpp
for (int i = 0; i < 5; i++) {
    // Executa 5 vezes
}
```

**Range-based for** (percorrer coleção):

```cpp
vector<int> numeros = {1, 2, 3, 4};
for (int n : numeros) {
    cout << n << endl;
}
```

## 6. Arrays estáticos e `vector`

### 6.1. Array estático `int[]`

Tamanho **fixo**, definido na inicialização. Não é possível adicionar ou remover elementos.

```cpp
int numeros[] = {1, 2, 3, 4};

for (int i = 0; i < 4; i++) {
    cout << numeros[i] << endl;
}
```

### 6.2. `vector` (C++)

Classe da biblioteca padrão que fornece **array dinâmico**: tamanho pode mudar, memória gerenciada automaticamente.

```cpp
#include <vector>

vector<int> numeros = {1, 2, 3, 4};

for (int n : numeros) {
    cout << n << endl;
}

numeros.push_back(6);  // Adiciona no fim
numeros.pop_back();   // Remove do fim
```

# 7. `struct` com ponteiro


```cpp
struct Pessoa {
	string nome;
	int idade;
}

Pessoa p = new Pessoa();
```


## Exercício: calculadora em menu

Criar um programa que realize operações matemáticas simples (adição, subtração, multiplicação e divisão).

```cpp
#include <iostream>

using namespace std;

int main() {
    int option;
    double num1, num2;

    while (true) {
        cout << "--------------------------" << endl;
        cout << "1 - Soma" << endl;
        cout << "2 - Subtração" << endl;
        cout << "3 - Divisão" << endl;
        cout << "4 - Multiplicação" << endl;
        cout << "0 - Sair" << endl;
        cout << "--------------------------" << endl;
        cout << "Escolha uma opção: ";
        cin >> option;

        if (option == 0) {
            cout << "Saindo..." << endl;
            return 0;
        }

        if (option < 1 || option > 4) {
            cout << "Opção inválida." << endl;
            continue;
        }

        cout << "Número 1: ";
        cin >> num1;
        cout << "Número 2: ";
        cin >> num2;

        switch (option) {
            case 1:
                cout << num1 << " + " << num2 << " = " << num1 + num2 << endl;
                break;
            case 2:
                cout << num1 << " - " << num2 << " = " << num1 - num2 << endl;
                break;
            case 3:
                cout << num1 << " / " << num2 << " = " << num1 / num2 << endl;
                break;
            case 4:
                cout << num1 << " * " << num2 << " = " << num1 * num2 << endl;
                break;
        }
    }

    return 0;
}
```
