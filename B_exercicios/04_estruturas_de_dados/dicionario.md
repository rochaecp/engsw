# Exercícios - Utilizando Dicionários

## 1) **Gerenciador de Contatos Telefônicos**

#### Descrição

- Crie um programa para gerenciar uma agenda de contatos telefônicos usando um dicionário. 
- O objetivo é permitir que o usuário adicione, busque, atualize e remova contatos. 
- Cada contato será representado por um nome (chave) e um número de telefone (valor).

#### Requisitos

- O programa deve utilizar um dicionário para armazenar os contatos, onde:
- A chave será o nome do contato (único).
- O valor será o número de telefone associado a esse nome.
- O programa deve oferecer um menu interativo para o usuário escolher as opções desejadas.

#### O programa deve

- Adicionar um novo contato, solicitando o nome e o número de telefone.
- Listar todos os contatos existentes, exibindo o nome e o número de telefone.
- Buscar um contato pelo nome, exibindo o número de telefone correspondente.
- Atualizar o número de um contato existente.
- Remover um contato da agenda.
- Continuar funcionando até o usuário escolher a opção de sair do programa.

#### Bônus

- Permitir que o usuário adicione múltiplos números de telefone para o mesmo contato.
- Implementar uma pesquisa parcial, onde o usuário digita parte do nome e o programa lista todos os contatos que correspondem.
- Exibir os contatos em ordem alfabética ao listar.
- Salvar a agenda em um arquivo de texto e permitir carregá-la ao iniciar o programa.

#### Exemplo de Entrada Esperada

~~~yaml
===== AGENDA DE CONTATOS =====
1. Adicionar Contato
2. Listar Contatos
3. Buscar Contato
4. Atualizar Número
5. Remover Contato
6. Sair
Escolha uma opção: 1
Digite o nome do contato: João
Digite o número de telefone: (11) 98765-4321

===== AGENDA DE CONTATOS =====
1. Adicionar Contato
2. Listar Contatos
3. Buscar Contato
4. Atualizar Número
5. Remover Contato
6. Sair
Escolha uma opção: 1
Digite o nome do contato: Maria
Digite o número de telefone: (21) 91234-5678

===== AGENDA DE CONTATOS =====
Escolha uma opção: 2
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== LISTA DE CONTATOS =====
João: (11) 98765-4321
Maria: (21) 91234-5678
~~~

#### Exemplo com Bônus (Pesquisa Parcial):

~~~yaml
===== AGENDA DE CONTATOS =====
Escolha uma opção: 3
Digite o nome do contato para buscar: Ma

===== RESULTADO DA BUSCA =====
Maria: (21) 91234-5678
~~~
