# Exercícios - Operações matemáticas

## 1) **Calculadora de Estatísticas Matemáticas**

#### Descrição

- Você deve criar um programa que funcione como uma calculadora de estatísticas matemáticas básicas. 
- O objetivo é realizar operações matemáticas como soma, subtração, multiplicação, divisão, além de operações mais avançadas, como cálculo de média, mediana, moda, variância e desvio padrão de uma lista de números.

#### Requisitos

- O programa deve permitir que o usuário insira uma lista de números inteiros ou decimais.
- O usuário deve escolher qual operação deseja realizar.
- O programa deve tratar erros de entrada (ex: divisão por zero, entradas inválidas).

#### O programa deve

- Solicitar ao usuário que insira uma lista de números separados por espaço.
- Exibir um menu com as seguintes operações:
    - Soma de todos os números.
    - Subtração sequencial dos números.
    - Multiplicação de todos os números.
    - Divisão sequencial dos números.
    - Cálculo da média dos números.
    - Cálculo da mediana.
    - Identificação da moda (o número que mais se repete).
    - Cálculo da variância e do desvio padrão.
- Exibir o resultado da operação escolhida.

#### Bônus

- Permitir que o usuário escolha se quer calcular com números inteiros ou decimais.
- Implementar uma opção para ordenar os números em ordem crescente ou decrescente.
- Adicionar uma funcionalidade que permita salvar o resultado em um arquivo de texto.
- Implementar uma opção de "Histórico de operações", que armazena os últimos cálculos realizados.

#### Exemplo de Entrada Esperada

~~~yaml
Digite uma lista de números (separados por espaço): 10 20 30 40 50
Escolha a operação que deseja realizar:
1 - Soma
2 - Subtração
3 - Multiplicação
4 - Divisão
5 - Média
6 - Mediana
7 - Moda
8 - Variância e Desvio Padrão
Opção: 5
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== Calculadora de Estatísticas Matemáticas =====
Lista de números: [10, 20, 30, 40, 50]

Operação selecionada: Média
Resultado: 30.0

===== Bônus (Histórico de Operações) =====
1. Média dos números [10, 20, 30, 40, 50]: 30.0
==========================================
~~~