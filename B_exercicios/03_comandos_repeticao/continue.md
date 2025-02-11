# Exercícios - Uso do comando Continue

## 1) **Filtro de Números Pares**

#### Descrição:

- Crie um programa que leia uma sequência de números inteiros e exiba apenas os números pares. 
- O programa deve usar o comando continue para pular a exibição dos números ímpares.

#### Requisitos:

- O programa deve aceitar uma lista de números fornecida pelo usuário.
- O comando continue deve ser usado para ignorar os números ímpares.
- O programa deve funcionar com qualquer quantidade de números.
- O programa deve ser eficiente, processando cada número uma única vez.

#### O programa deve:

- Solicitar ao usuário que insira uma sequência de números separados por espaço.
- Ler cada número da sequência.
- Verificar se o número é ímpar.
    - Se for ímpar, usar o comando continue para pular para o próximo número.
- Exibir apenas os números pares.

#### Bônus (opcional):

- Permitir que o usuário decida se quer filtrar pares ou ímpares.
- Exibir a quantidade de números pares encontrados ao final da execução.
- Implementar uma verificação para que o programa continue pedindo entradas até que o usuário digite "sair".
- Exibir uma mensagem informando que o número foi ignorado se for ímpar (antes do continue).

#### Exemplo de Entrada Esperada:

~~~yaml
Digite uma sequência de números inteiros (separados por espaço): 
12 7 9 20 15 8 3 4
~~~

#### Exemplo de Saída Esperada:

~~~yaml
Números pares encontrados:
12
20
8
4
~~~

#### Exemplo com Bônus (Filtragem de ímpares):

~~~yaml
Você deseja filtrar pares ou ímpares? (Digite 'pares' ou 'ímpares'): ímpares
Digite uma sequência de números inteiros: 
5 14 23 42 11 8 3 9

Números ímpares encontrados:
5
23
11
3
9
~~~