 # 🧠 Exercícios de Lógica de Programação em c++
 

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
# EXERCICIO C++: 2
FOLHA DE PAGAMENTO:

Faça um programa para cálculo de uma folha de pagamento, considerando os seguintes descontos e regras:

    Imposto de Renda (IR) descontado conforme tabela do salário bruto:

        Até R$ 900,00 (inclusive): isento

        Até R$ 1500,00 (inclusive): 5%

        Até R$ 2500,00 (inclusive): 10%

        Acima de R$ 2500,00: 20%

    Desconto de 10% para o INSS.

    FGTS corresponde a 11% do salário bruto, mas não é descontado do trabalhador — é um depósito feito pela empresa.

    O salário líquido é o salário bruto menos os descontos (IR + INSS).

O programa deverá solicitar ao usuário:

    Valor da hora trabalhada.

    Quantidade de horas trabalhadas no mês.

    Exemplo de saída: 
    Salário Bruto:                 : R$ 1100,00
    IR (5%)                       : R$   55,00
    INSS (10%)                    : R$  110,00
    FGTS (11%)                    : R$  121,00
    Salário Líquido               : R$  935,00

   FOLHA DE PAGAMENTO:

 ```
#include <iostream>

using namespace std;

int main() {

    double salario_hora, hora_trabalhada, salario_bruto, percentual;
    double ir, inss, fgts, salario_liquido;
    char ops;

    do {
            cout << "[BEM-VINDOS!]";
    cout << "\nQuanto vc ganha por hora?\n" << endl;
    cin >> salario_hora;


    cout << "\nQuantas horas vc trabalha por mes?\n";
    cin >> hora_trabalhada;

    salario_bruto = salario_hora * hora_trabalhada;

        if  (salario_bruto <= 900.0) {
            percentual = 0.0;
        } else if (salario_bruto <= 1500.0) {
            percentual = 5.0;
        } else if (salario_bruto <= 2500.0) {
            percentual = 10.0;
        } else {
            percentual = 20.0;
        }

        ir = salario_bruto * (percentual / 100.0);
        inss = salario_bruto * 0.10;
        fgts = salario_bruto * 0.11;
        salario_liquido = salario_bruto - ir - inss;


    cout << "-----------------------------" << endl;
    cout << "\n[FOLHA-DE-PAGAMENTO!]\n" << endl;
    cout << "SALARIO BRUTO: " << salario_bruto << endl;
    cout << "IR: " << ir << endl;
    cout << "INSS:(10%) " << inss << endl;
    cout << "FGTS:(11%) " << fgts << endl;
    cout << "SALARIO LIQUIDO: " << salario_liquido << endl;


      cout << "Gostaria de reabrir a folha de pagamento? [S/N]" << endl;
      cin >> ops;

    } while (ops == 'S' || ops == 's');

    cout << "[FOLHA-ENCERRADA!]";


    return 0;
}
 ```
# EXERCICIO RUST: 4

CAIXA ELETRONICO: Faça um Programa para um caixa eletrônico.
```
O programa deverá perguntar ao usuário a valor do saque e depois informar quantas notas de cada valor serão fornecidas.

As notas disponíveis serão as de 1, 5, 10, 50 e 100 reais. O valor mínimo é de 10 reais e o máximo de 600 reais.

O programa não deve se preocupar com a quantidade de notas existentes na máquina.

Exemplo 1: Para sacar a quantia de 256 reais, o programa fornece duas notas de 100, uma nota de 50, uma nota de 5 e uma nota de 1;

Exemplo 2: Para sacar a quantia de 399 reais, o programa fornece três notas de 100, uma nota de 50, quatro notas de 10, uma nota de 5 e quatro notas de 1.


```
# CODIGO:

```
#include <iostream>

using namespace std;

int main() {
    
    int  saque, valor_restante;
    int nota100, nota50, nota20, nota10, nota1;
    char ops;
    do {
        cout << "\n[BEM-VINDOS]\n" << endl;
        cout << "\nNOTAS DISPONIVEIS: 100 reais, 50 reais, 20 reais, 10 reais, 5 reais, 1 real\n" << endl;

        cout << "\nQUANTO VOCE GOSTARIA DE SACAR? DISPONIVEL DE 10 A R$600.0 reais\n" << endl;
        cin >> saque;

        if (saque >= 10 && saque <= 600) {
            cout << "saque autorizado de " << saque << endl;
        
        valor_restante = saque;
        
        nota100 = valor_restante / 100;
         valor_restante %= 100;

        nota50 = valor_restante / 50;
         valor_restante %= 50;
        
        nota20 = valor_restante / 20;
         valor_restante %= 20;
        
        nota10 = valor_restante / 10;
         valor_restante %= 10;
        
        nota1 = valor_restante / 1 ;
         valor_restante %= 1;

        cout << "[NOTAS-FORNECIDAS]" << endl;
        if (nota100 > 0) cout << "foram fornecidas " << nota100 << " de 100 reais " << endl;
        if (nota50 > 0) cout << "foram fornecidas " << nota50 << " de 50 reais " << endl;
        if (nota20 > 0) cout << "foram fornecidas " << nota20 << " de 20 reais " << endl;
        if (nota10 > 0) cout << "foram fornecidas " << nota10 << " de 10 reais " << endl;
        if (nota1 > 0)cout << "foram fornecidas " << nota1 << " de 1 real " << endl;

    } else {
            cout << "Valor invalido escolha algo entre 10 e 600" << endl;
        }

        cout << "----------------------------------------" << endl;
        cout << "Gostaria de reiniciar o caixa? [S/N]";
        cin >> ops;

    } while (ops == 'S' || ops == 's');

    cout << "[CAIXA-FECHADO]!";
    
}
```
