 # 🧠 Exercícios de Lógica de Programação em java
 

Este repositório contém exercícios de lógica de programação que estou resolvendo para treinar minha base em desenvolvimento e fortalecer meu raciocínio lógico, usando a linguagem **C++**.

---

✍️ Objetivo

Praticar a lógica de programação de forma consistente, reforçando conceitos fundamentais como:

    Declaração de variáveis

    Tipos de dados

    Estruturas de decisão (if, else if, else)

    Laços de repetição (for, while, do while)

    Funções

    Vetores (Vec<T>, arrays)

    Manipulação de entrada e saída

    Pequenos projetos com foco em lógica

  
   # EXERCICIOS c++: 1

CALCULADORA SIMPLES:

Crie um programa que funcione como uma calculadora básica, realizando operações matemáticas entre dois números fornecidos pelo usuário.
Funcionalidades:

    Solicitar ao usuário que digite dois números.

    Solicitar qual operação matemática deseja realizar:

        Soma (+)

        Subtração (-)

        Multiplicação (*)

        Divisão (/)

    Realizar a operação escolhida e mostrar o resultado.

    Caso o usuário escolha uma operação inválida, exibir uma mensagem de erro.

    Perguntar ao usuário se deseja realizar outra operação, repetindo o processo enquanto desejar.

   ```
  #include <iostream>

using namespace std;

int main() {

    int num1, num2, resultado;
    char operador, ops;

    do {


    cout << "\nDigite o primeiro numero: \n";
    cin >> num1;

    cout << "\nDigite o operador: (+,-,*,/)\n";
    cin >> operador;
    
    cout << "\nDigite o segundo numero\n";
    cin >> num2;

      switch (operador) {
        case '+':
            cout << "O resultado de " << num1 << " + " << num2 << " = " << num1 + num2 << endl;
        break;

        case '-':
            cout << "O resultado de " << num1 << " - " << num2 << " = " << num1 - num2 << endl;
        break;

        case '*':
            cout << "O resultado de " << num1 << " * " << num2 << " = " << num1 * num2 << endl;
        break;
        
        case '/':
                 if (num2 != 0) {
                 cout << "O resultado de " << num1 << " / " << num2 << " = " << num1 / num2 << endl;
                 } else {
                    cout << "\nErro divisão por zero invalida\n";
                 }
        break;

        default:
                cout << "Operador invalido!";
      }
      
        cout << "-------------------------------------" << endl;
        cout << "\n[GOSTARIA DE REINICIAR A CALCULADORA]\n";
        cin >> ops;

    } while (ops == 'S' || ops == 's');
    

    cout << "\n[CALCULADORA ENCERRADA!]\n";
}
   ```
 
