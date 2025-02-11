# Exercícios - Classes, Objetos, Propriedades e Métodos

## 1) **Sistema de Gestão de Biblioteca**

#### Descrição:

- Crie um programa para gerenciar um sistema de biblioteca, permitindo o cadastro de livros, o empréstimo para usuários e o controle de devoluções. 
- O objetivo é praticar o uso de classes, objetos, propriedades e métodos para modelar o comportamento dos livros e da biblioteca.

#### Requisitos:

- Definir uma classe Livro com as seguintes propriedades:
    - Titulo (texto)
    - Autor (texto)
    - AnoPublicacao (inteiro)
    - Disponivel (booleano) - para indicar se o livro está disponível para empréstimo
- Criar uma classe Biblioteca com:
    - Uma lista de livros cadastrados
    - Métodos para:
        - Adicionar um novo livro
        - Listar todos os livros
        - Realizar o empréstimo de um livro
        - Registrar a devolução de um livro

#### O programa deve:

- Permitir o cadastro de novos livros, solicitando informações do usuário.
- Listar todos os livros da biblioteca, indicando se estão disponíveis ou emprestados.
- Realizar o empréstimo de um livro, alterando o status de disponibilidade.
- Registrar a devolução de um livro, tornando-o disponível novamente.
- Continuar executando até o usuário escolher a opção de sair do sistema.

#### Bônus (opcional):

- Implementar uma classe Usuario para associar um usuário ao empréstimo de um livro.
- Limitar o número de livros que um usuário pode emprestar simultaneamente.
- Criar um método para pesquisar livros pelo título ou autor.
- Adicionar uma funcionalidade para ordenar os livros por ano de publicação ou título.

#### Exemplo de Entrada Esperada:

~~~yaml
===== SISTEMA DE BIBLIOTECA =====
1. Cadastrar Livro
2. Listar Livros
3. Emprestar Livro
4. Devolver Livro
5. Sair
Escolha uma opção: 1

Digite o título do livro: O Senhor dos Anéis
Digite o autor do livro: J.R.R. Tolkien
Digite o ano de publicação: 1954
Livro cadastrado com sucesso!
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== LISTA DE LIVROS =====
Título: O Senhor dos Anéis
Autor: J.R.R. Tolkien
Ano de Publicação: 1954
Status: Disponível
------------------------------

Título: 1984
Autor: George Orwell
Ano de Publicação: 1949
Status: Emprestado
------------------------------
~~~

#### Exemplo com Empréstimo e Devolução:

~~~yaml
===== EMPRÉSTIMO DE LIVRO =====
Digite o título do livro para emprestar: O Senhor dos Anéis
Livro emprestado com sucesso!

===== DEVOLUÇÃO DE LIVRO =====
Digite o título do livro para devolver: O Senhor dos Anéis
Livro devolvido com sucesso!
~~~