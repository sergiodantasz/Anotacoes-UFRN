# Função `main`

```cpp
#include <iostream>

using namespace std;

int main() {
  cout << "Olá Mundo" << endl;
  return 0;
}
```

# Comentários

```cpp
// Comentário simples

/*
Comentário
multilinha
*/
```

# Novos tipos de dados

Os novos tipos em relação ao C são `bool` e `string`:

```cpp
bool autenticado = true; // ou false ou 1 ou 0
string nome = "Sérgio Dantas";
```

## Tipagem automática com `auto`

A palavra reservada `auto` também foi introduzida no C++.

```cpp
auto idade = 10;
auto sobrenome = "Dantas";
```

Ao usar `auto`, é necessário declarar a variável na inicialização.

# Saída de dados

```cpp
auto nome = "Sérgio";

if (nome == "Sérgio") {
  cout << "Você é Sérgio.";
} else {
  cout << "Você não é Sérgio, você é " << nome << endl;
}
```

# Variáveis

```cpp
int inteiro = 5;
double decimal = 5.99;
char letra = 'D';
string texto = "Hello";
bool booleano = true;
bool booleano = false;
```

