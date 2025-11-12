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
Codigo: 
<img width="1041" height="930" alt="image" src="https://github.com/user-attachments/assets/577b3ad4-632e-497d-a572-51147c7345e3" />

 
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

  
   Exemplo de saída: 
    
    [FOLHA-DE-PAGAMENTO]
    SALARIO_BRUTO: R$24420
    IR:(5%) R$4884
    INSS:(10%) R$2442
    FGTS:(11.0) R$2686.2
    SALARIO_LIQUIDO: R$17094

#CODIGO: 
<img width="2656" height="2248" alt="folha" src="https://github.com/user-attachments/assets/e34e1b47-07fa-4d78-b455-bab2e31ff2fd" />

# EXERCICIO c++: 3

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
# EXERCICIO c++: 4

TABUADA: Desenvolva um programa que faça a tabuada de um número qualquer inteiro que será digitado pelo usuário, mas a tabuada não deve necessariamente iniciar em 1 e terminar em 10, o valor inicial e final devem ser informados também pelo usuário, conforme exemplo abaixo:
```
Montar a tabuada de: 5
Começar por: 4
Terminar em: 7

Vou montar a tabuada de 5 começando em 4 e terminando em 7:
5 X 4 = 20
5 X 5 = 25
5 X 6 = 30
5 X 7 = 35

```
COGIDO: 
<img width="1680" height="1276" alt="tabuada cplus" src="https://github.com/user-attachments/assets/6ff66802-ee86-4677-8c1a-fd25bfd56ed3" />

# EXERCICIO c++: 5
CAIXA REGISTRADORA: Crie um programa em Rust que simule o funcionamento de um caixa registradora. O sistema deve permitir o registro de múltiplos produtos em uma única compra, calcular o valor total, receber o pagamento do cliente, verificar se o valor é suficiente e calcular o troco. Ao final da operação, o programa deve perguntar se o caixa deve ser reaberto para uma nova compra.

codigo: 
<img width="2146" height="1996" alt="registradoracpp" src="https://github.com/user-attachments/assets/332e73e1-1fd9-4aa0-a30a-5e8367eb31bc" />

# EXERCICIO c++: 6
Um simples e divertido **jogo da velha (tic-tac-toe)** feito em **C++**, jogado no terminal por **dois jogadores**.

---

## 🧠 Funcionalidades

- ✅ Dois jogadores locais (X e O)
- ✅ Verificação automática de vitória
- ✅ Detecção de empate
- ✅ Validação de entradas
- ✅ Interface em modo texto

COGIDO JOGO DA VELHA: 
<img width="2618" height="3420" alt="code-snapshot" src="https://github.com/user-attachments/assets/cfb05fa4-54b8-47af-88cb-8f2e25eaa45b" />

# EXERCICIO CPP: 7
Um jogo da forca simples programado em C++

codigo:
<img width="941" height="760" alt="image" src="https://github.com/user-attachments/assets/38033195-2d9b-461e-89f3-a745e0a2e121" />


