# Exercícios - Utilizando Listas

## 1) **Gerenciador de Lista de Tarefas (To-Do List)**

#### Descrição:

- Crie um programa para gerenciar uma lista de tarefas usando uma lista dinâmica. 
- O objetivo é permitir que o usuário adicione, remova, marque como concluída, e liste todas as tarefas. 
- Cada tarefa terá um título e um status (pendente ou concluída).

#### Requisitos:

- O programa deve utilizar uma lista para armazenar as tarefas.
- Cada tarefa deve conter:
    - Um título (texto descritivo).
    - Um status que indica se está pendente ou concluída.
- O programa deve oferecer um menu de opções para o usuário interagir.

#### O programa deve:

- Permitir que o usuário adicione novas tarefas à lista.
- Permitir que o usuário liste todas as tarefas, mostrando o status de cada uma.
- Permitir que o usuário marque uma tarefa como concluída informando seu número ou nome.
- Permitir que o usuário remova uma tarefa da lista.
- Continuar funcionando até que o usuário escolha a opção de sair do programa.

#### Bônus (opcional):

- Permitir que o usuário edite o título de uma tarefa existente.
- Implementar uma função de pesquisa para encontrar uma tarefa pelo nome.
- Adicionar uma opção para listar somente as tarefas pendentes ou concluídas.
- Exibir a porcentagem de tarefas concluídas em relação ao total.

#### Exemplo de Entrada Esperada:

~~~yaml
===== MENU =====
1. Adicionar Tarefa
2. Listar Tarefas
3. Marcar Tarefa como Concluída
4. Remover Tarefa
5. Sair
Escolha uma opção: 1
Digite o título da tarefa: Estudar programação

===== MENU =====
1. Adicionar Tarefa
2. Listar Tarefas
3. Marcar Tarefa como Concluída
4. Remover Tarefa
5. Sair
Escolha uma opção: 1
Digite o título da tarefa: Fazer exercícios físicos

===== MENU =====
1. Adicionar Tarefa
2. Listar Tarefas
3. Marcar Tarefa como Concluída
4. Remover Tarefa
5. Sair
Escolha uma opção: 2
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== LISTA DE TAREFAS =====
1. Estudar programação [Pendente]
2. Fazer exercícios físicos [Pendente]
~~~

#### Exemplo com Bônus (Marcar como Concluída e Percentual de Conclusão):

~~~yaml
===== MENU =====
Escolha uma opção: 3
Digite o número da tarefa a ser marcada como concluída: 1

===== LISTA DE TAREFAS =====
1. Estudar programação [Concluída]
2. Fazer exercícios físicos [Pendente]

Progresso: 50% das tarefas concluídas.
~~~
