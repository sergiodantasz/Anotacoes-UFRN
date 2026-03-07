# Linguagem C++

## 1. Estrutura básica

### 1.1. Função `main`

```cpp
#include <iostream>

using namespace std;

int main() {
    cout << "Olá, mundo!" << endl;
    return 0;
}
```

`#include <iostream>` fornece `cout`, `cin` e outros para entrada e saída. `using namespace std` permite usar `cout` em vez de `std::cout`.

### 1.2. Comentários

```cpp
// Comentário de uma linha

/*
   Comentário
   de várias linhas
*/
```

## 2. Tipos de dados e variáveis

### 2.1. Tipos em relação ao C

Além dos tipos do C (`int`, `float`, `double`, `char`, etc.), o C++ traz:

| Tipo     | Descrição                    |
| -------- | ---------------------------- |
| `bool`   | Booleano: `true` ou `false`   |
| `string` | Texto (da biblioteca `<string>`) |

**Exemplo:**

```cpp
bool autenticado = true;   // ou false, ou 1, ou 0
string nome = "Sérgio Dantas";
```

Para usar `string`, inclua: `#include <string>`.

### 2.2. Tipagem automática com `auto`

A palavra-chave `auto` deixa o compilador inferir o tipo a partir da inicialização. A variável **precisa** ser inicializada na declaração.

```cpp
auto idade = 10;        // int
auto sobrenome = "Dantas";  // const char* (literal)
auto nome = string("Sérgio");  // std::string
```

### 2.3. Declaração de variáveis

```cpp
int inteiro = 5;
double decimal = 5.99;
char letra = 'D';
string texto = "Hello";
bool ok = true;
bool erro = false;
```

## 3. Entrada e saída

### 3.1. Saída com `cout`

O operador `<<` envia dados para a saída padrão. É possível encadear várias saídas.

```cpp
cout << "Olá";
cout << nome << endl;           // endl quebra a linha
cout << "Idade: " << idade << endl;
```

### 3.2. Entrada com `cin`

O operador `>>` lê da entrada padrão (teclado). O tipo da variável define como o valor é interpretado.

```cpp
int opcao;
cin >> opcao;

double x, y;
cin >> x >> y;   // lê dois valores em sequência
```

### 3.3. Comparação de strings

Diferente do C, em C++ podemos comparar `string` com `==`.

```cpp
string nome = "Sérgio";

if (nome == "Sérgio") {
    cout << "Você é Sérgio.";
} else {
    cout << "Você não é Sérgio, você é " << nome << endl;
}
```

## 4. Exercício: calculadora em menu


Exemplo que usa `cout`, `cin`, `switch`, `while` e tipos básicos:

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
        cout << "5 - Sair" << endl;
        cout << "--------------------------" << endl;
        cout << "Escolha uma opção: ";
        cin >> option;

        if (!(option >= 1 && option <= 5)) {
            cout << "Opção inválida." << endl;
            continue;
        }

        if (option == 5) {
            cout << "Saindo..." << endl;
            return 0;
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
