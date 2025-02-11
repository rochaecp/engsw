# Exercícios - Uso de operadores relacionais

## 1) **Sistema de Verificação de Elegibilidade para Votação**

#### Descrição:

- Você foi contratado para desenvolver um programa que verifica se uma pessoa está apta a votar em uma eleição. 
- O programa utilizará operadores relacionais para comparar a idade do usuário com o critério mínimo exigido para votar, além de verificar outras condições de elegibilidade.

#### Requisitos:

- O programa deve solicitar ao usuário as seguintes informações:
    - Idade da pessoa (em anos).
    - Nacionalidade (se é cidadão do país ou não).
    - Título de eleitor ativo (se possui ou não).
- O programa deve usar operadores relacionais como:
    - `==` (igual a)
    - `!=` (diferente de)
    - `> `(maior que)
    - `< `(menor que)
    - `>=` (maior ou igual a)
    - `<=` (menor ou igual a)

#### O programa deve:

- Solicitar ao usuário:
    - Idade da pessoa.
    - Se é cidadão do país (responder "sim" ou "não").
    - Se possui título de eleitor ativo (responder "sim" ou "não").
- Verificar as seguintes condições:
    - Idade mínima para votar: 16 anos.
    - Obrigatório: Ser cidadão do país.
    - Obrigatório: Ter título de eleitor ativo.
- Exibir uma mensagem informando se a pessoa está apta a votar ou não está apta a votar, explicando o motivo da inelegibilidade, se for o caso.

#### Bônus (opcional):

- Verificar se o voto é obrigatório ou facultativo:
    - Voto facultativo: 16-17 anos ou acima de 70 anos.
    - Voto obrigatório: 18 a 70 anos.
- Permitir verificar a elegibilidade de várias pessoas em sequência até o usuário decidir encerrar o programa.

#### Exemplo de Entrada Esperada:

~~~yaml
Informe sua idade: 17  
Você é cidadão do país? (sim/não): sim  
Você possui título de eleitor ativo? (sim/não): sim  
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== Resultado da Verificação =====
Você está apto(a) a votar!
O seu voto é facultativo.
====================================
~~~

---

#### Exemplo de Entrada Esperada (Pessoa Inelegível):

~~~yaml
Informe sua idade: 15  
Você é cidadão do país? (sim/não): sim  
Você possui título de eleitor ativo? (sim/não): sim  
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== Resultado da Verificação =====
Você NÃO está apto(a) a votar.
Motivo: Idade mínima para votar é 16 anos.
========================================
~~~