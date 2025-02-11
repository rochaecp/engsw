# Exercícios - Operações com Strings

## 1) Analisador de Texto - Estatísticas de Frase

#### Descrição:

- Você deve criar um analisador de texto que processe uma frase fornecida pelo usuário e gere estatísticas úteis. 
- O objetivo é praticar operações com strings, como concatenação, busca, substituição, contagem de caracteres e palavras, além de manipulação de maiúsculas e minúsculas.

#### Requisitos:

- O programa deve ser capaz de:
    - Receber uma frase digitada pelo usuário.
    - Realizar operações básicas de manipulação de strings.
    - Exibir estatísticas sobre o texto analisado.

#### O programa deve:

- Solicitar uma frase qualquer ao usuário.
- Exibir o número total de caracteres da frase (incluindo espaços).
- Exibir o número de palavras na frase.
- Exibir a frase em letras maiúsculas e letras minúsculas.
- Exibir a primeira e a última palavra da frase.
- Verificar se uma palavra específica informada pelo usuário está presente na frase.
- Substituir uma palavra específica da frase por outra, caso o usuário deseje.

#### Bônus (opcional):

- Identificar e contar quantos caracteres são vogais na frase.
- Inverter a frase e exibi-la ao contrário.
- Exibir a frase com a primeira letra de cada palavra em maiúsculo (capitalização).

#### Exemplo de Entrada Esperada:

~~~yaml
Digite uma frase: A programação é uma habilidade poderosa.  
Digite uma palavra para verificar se está presente na frase: poderosa  
Deseja substituir alguma palavra? (sim/não): sim  
Qual palavra deseja substituir? programação  
Por qual palavra deseja substituir? codificação
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== Estatísticas da Frase =====
Frase original: A programação é uma habilidade poderosa.
Número total de caracteres: 42
Número de palavras: 6
Frase em letras maiúsculas: A PROGRAMAÇÃO É UMA HABILIDADE PODEROSA.
Frase em letras minúsculas: a programação é uma habilidade poderosa.
Primeira palavra: A
Última palavra: poderosa
A palavra "poderosa" está presente na frase? Sim
Frase após substituição: A codificação é uma habilidade poderosa.
===============================
~~~

#### Exemplo de Saída com Bônus (opcional):

~~~yaml
===== Estatísticas Avançadas =====
Número de vogais: 19
Frase invertida: .asoredop edadilabah amu é oãçacifodoc A
Frase com capitalização: A Codificação É Uma Habilidade Poderosa.
===============================
~~~
