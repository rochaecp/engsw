# Exercícios - Utilizando Arrays

## 1) **Analisador de Notas dos Alunos**

#### Descrição:

- Crie um programa que armazene as notas de uma turma de alunos utilizando um array. 
- O objetivo é calcular a média da turma, identificar a maior e a menor nota, e exibir todas as notas ordenadas em ordem crescente.

#### Requisitos:

- O programa deve utilizar um array para armazenar as notas.
- O usuário deverá informar o número de alunos e, em seguida, digitar a nota de cada aluno.
- As notas devem ser números decimais (por exemplo: 7.5, 8.0, 9.3).

#### O programa deve:

- Solicitar ao usuário o número de alunos na turma.
- Criar um array para armazenar as notas.
- Receber as notas dos alunos por meio de entradas do usuário.
- Calcular e exibir:
    - A média da turma.
    - A maior nota e a menor nota.
    - Todas as notas em ordem crescente.

#### Bônus (opcional):

- Exibir o desvio padrão das notas para avaliar a dispersão dos resultados.
- Indicar quantos alunos estão acima da média da turma.
- Permitir que o programa calcule a média ponderada, caso o usuário forneça pesos para as notas.
- Adicionar uma função para buscar a nota de um aluno específico informando o índice.

#### Exemplo de Entrada Esperada:

~~~yaml
Quantos alunos há na turma? 5
Digite a nota do aluno 1: 8.5
Digite a nota do aluno 2: 7.0
Digite a nota do aluno 3: 9.2
Digite a nota do aluno 4: 6.8
Digite a nota do aluno 5: 7.5
~~~

#### Exemplo de Saída Esperada:

~~~yaml
Média da turma: 7.8
Maior nota: 9.2
Menor nota: 6.8
Notas em ordem crescente: 6.8, 7.0, 7.5, 8.5, 9.2
~~~

#### Exemplo de Saída Esperada (com Bônus - Alunos Acima da Média):

~~~yaml
Média da turma: 7.8
Maior nota: 9.2
Menor nota: 6.8
Notas em ordem crescente: 6.8, 7.0, 7.5, 8.5, 9.2
Alunos acima da média: 2
~~~
