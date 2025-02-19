# Exercícios - Utilização de funções

#### 1) **Calculadora de Operações Matemáticas com Funções**

#### Descrição

- Crie um programa que funcione como uma calculadora simples, permitindo ao usuário realizar operações matemáticas básicas. 
- Cada operação (adição, subtração, multiplicação, divisão) deve ser implementada como uma função separada.

#### Requisitos

- O programa deve definir funções para as seguintes operações:
    - Adição
    - Subtração
    - Multiplicação
    - Divisão
- Deve ser possível chamar cada função de forma independente, dependendo da operação escolhida pelo - usuário.
- O programa deve tratar erros, como a divisão por zero.

#### O programa deve

- Exibir um menu com as opções de operações matemáticas.
- Solicitar ao usuário que escolha uma operação (ex: 1 para adição, 2 para subtração).
- Pedir dois números ao usuário para realizar a operação.
- Chamar a função correspondente com os números informados.
- Exibir o resultado da operação.
- Permitir que o usuário realize novas operações sem encerrar o programa (loop de repetição).

#### Bônus

- Adicionar operações matemáticas avançadas, como:
    - Exponenciação (potência)
    - Cálculo de raiz quadrada
    - Cálculo de fatorial
- Criar uma função para validar as entradas, garantindo que o usuário insira apenas números válidos.
- Implementar um histórico de operações, que armazene os últimos cálculos realizados.
- Permitir que o usuário encerre o programa escolhendo uma opção no menu.

#### Exemplo de Entrada Esperada

~~~yaml
===== Calculadora Simples =====
Escolha uma operação:
1 - Adição
2 - Subtração
3 - Multiplicação
4 - Divisão
0 - Sair
Opção: 1

Digite o primeiro número: 15
Digite o segundo número: 8

Resultado da adição: 23
Deseja realizar outra operação? (s/n): s
~~~

~~~yaml
===== Calculadora Simples =====
Escolha uma operação:
1 - Adição
2 - Subtração
3 - Multiplicação
4 - Divisão
0 - Sair
Opção: 4

Digite o primeiro número: 20
Digite o segundo número: 0

Erro: Não é possível dividir por zero.
Deseja realizar outra operação? (s/n): s
~~~

#### Saída Final (quando o usuário decidir sair):

~~~yaml
Obrigado por usar a Calculadora Simples. Até a próxima!
~~~