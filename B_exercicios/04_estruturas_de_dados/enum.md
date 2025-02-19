# Exercícios - Utilizando Enums

## 1) **Sistema de Gerenciamento de Tarefas com Enums**

#### Descrição

- Crie um programa para gerenciar uma lista de tarefas, onde cada tarefa terá um título, uma descrição e um status. 
- O status da tarefa será representado usando um Enum, com os seguintes estados possíveis:
    - Pendente
    - Em Andamento
    - Concluída
    - Cancelada

#### Requisitos

- O programa deve utilizar um Enum para definir os diferentes estados de uma tarefa.
- O Enum deve ser usado para controlar e exibir o status de cada tarefa.
- O programa deve permitir que o usuário adicione, visualize e atualize o status das tarefas.

#### O programa deve

- Adicionar uma nova tarefa, solicitando o título e a descrição. O status inicial deve ser "Pendente".
- Listar todas as tarefas, mostrando o título, a descrição e o status atual.
- Alterar o status de uma tarefa, permitindo que o usuário escolha entre os estados do Enum.
- Filtrar tarefas por status, exibindo apenas as tarefas com o status selecionado.
- Continuar funcionando até o usuário escolher a opção de sair do programa.

#### Bônus

- Implementar uma função de priorização das tarefas, usando outro Enum para níveis de prioridade (Baixa, Média, Alta).
- Permitir que o usuário edite o título ou a descrição de uma tarefa existente.
- Exibir um resumo com a quantidade de tarefas em cada status.
- Implementar a funcionalidade de remover uma tarefa da lista.

#### Exemplo de Entrada Esperada

~~~yaml
===== GERENCIADOR DE TAREFAS =====
1. Adicionar Nova Tarefa
2. Listar Tarefas
3. Alterar Status da Tarefa
4. Filtrar Tarefas por Status
5. Sair
Escolha uma opção: 1

Digite o título da tarefa: Estudar Enums
Digite a descrição da tarefa: Revisar conceitos de Enums em programação.

===== GERENCIADOR DE TAREFAS =====
Escolha uma opção: 3
Digite o ID da tarefa para alterar o status: 1
Selecione o novo status:
1 - Pendente
2 - Em Andamento
3 - Concluída
4 - Cancelada
Escolha: 2
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== LISTA DE TAREFAS =====
ID: 1
Título: Estudar Enums
Descrição: Revisar conceitos de Enums em programação.
Status: Em Andamento
~~~

#### Exemplo com Bônus (Resumo de Tarefas):

~~~yaml
===== RESUMO DE TAREFAS =====
Pendente: 3
Em Andamento: 1
Concluída: 5
Cancelada: 0
~~~
