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

# Exercício

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
	    
	    cout << option << endl;
	    
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
