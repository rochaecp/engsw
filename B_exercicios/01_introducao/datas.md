# Exercícios - Operações com Datas

## 1) **Calculadora de Datas - Idade e Diferença de Datas**

#### Descrição

- Você deve criar uma calculadora de datas que realize operações comuns com datas, como calcular a idade de uma pessoa e a diferença de dias entre duas datas. 
- O objetivo é praticar manipulação de datas, incluindo cálculos de diferença, adição e formatação de datas.

#### Requisitos

- O programa deve utilizar funções para trabalhar com datas e realizar cálculos de diferenças de tempo.
- O usuário deve poder inserir datas no formato padrão da linguagem (ex: DD/MM/AAAA ou YYYY-MM-DD).
- O programa deve validar as datas inseridas para evitar erros.

#### O programa deve

- Solicitar ao usuário sua data de nascimento.
- Calcular e exibir a idade atual do usuário em anos, meses e dias.
- Solicitar duas datas diferentes e calcular:
    - O número de dias de diferença entre elas.
    - Qual das duas datas é a mais recente.
- Permitir que o usuário adicione ou subtraia um número de dias, meses ou anos de uma data informada.

#### Bônus

- Informar o dia da semana correspondente à data de nascimento do usuário.
- Calcular quantos dias faltam para o próximo aniversário do usuário.
- Exibir a data formatada de diferentes formas (por exemplo: 12 de março de 2024, 03/12/2024, Tuesday, March 12, 2024).

#### Exemplo de Entrada Esperada

~~~yaml
Digite sua data de nascimento (DD/MM/AAAA): 15/08/1995
Digite a primeira data (DD/MM/AAAA): 01/01/2020
Digite a segunda data (DD/MM/AAAA): 25/12/2023
Deseja adicionar ou subtrair dias em uma data? (sim/não): sim
Digite a data (DD/MM/AAAA): 10/03/2022
Quantos dias deseja adicionar? 45
~~~

~~~yaml
===== Cálculo de Idade =====
Idade: 28 anos, 7 meses e 10 dias

===== Diferença entre Datas =====
Diferença entre 01/01/2020 e 25/12/2023: 1454 dias
A data mais recente é: 25/12/2023

===== Adição/Subtração de Datas =====
Nova data após adicionar 45 dias a 10/03/2022: 24/04/2022

===== Estatísticas Avançadas (Bônus) =====
Você nasceu em uma terça-feira.
Faltam 157 dias para o seu próximo aniversário.
Formatos de data:
- 15 de agosto de 1995
- 15/08/1995
- Tuesday, August 15, 1995
===============================
~~~
