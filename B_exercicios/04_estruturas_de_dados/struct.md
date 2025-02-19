# Exercícios - Utilizando Structs

## 1) **Sistema de Registro de Produtos usando Structs**

#### Descrição

- Crie um programa para gerenciar um sistema de registro de produtos em um estoque. 
- Cada produto terá informações como código do produto, nome, preço e quantidade em estoque. 
- Essas informações devem ser organizadas usando uma struct, representando o modelo de um produto.

#### Requisitos

- Definir uma struct chamada Produto com os seguintes campos:
    - Código (inteiro)
    - Nome (texto)
    - Preço (número decimal)
    - Quantidade em estoque (inteiro)
- O programa deve permitir adicionar, visualizar e atualizar produtos no estoque.
- O programa deve usar uma lista ou array para armazenar múltiplos produtos.

#### O programa deve

- Cadastrar um novo produto, solicitando as informações do usuário.
- Listar todos os produtos, exibindo seus detalhes de forma organizada.
- Atualizar a quantidade em estoque de um produto, usando o código como identificador.
- Calcular o valor total em estoque de um produto (preço × quantidade).
- Continuar funcionando até o usuário escolher a opção de sair do programa.

#### Bônus

- Adicionar um campo opcional de categoria do produto usando um Enum.
- Implementar a funcionalidade de remover um produto do estoque.
- Calcular e exibir o valor total do estoque com base em todos os produtos registrados.
- Adicionar uma função de pesquisa por nome do produto.

#### Exemplo de Entrada Esperada

~~~yaml
===== SISTEMA DE ESTOQUE =====
1. Cadastrar Produto
2. Listar Produtos
3. Atualizar Estoque
4. Calcular Valor Total em Estoque
5. Sair
Escolha uma opção: 1

Digite o código do produto: 101
Digite o nome do produto: Teclado
Digite o preço do produto: 150.75
Digite a quantidade em estoque: 20
Produto cadastrado com sucesso!
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== LISTA DE PRODUTOS =====
Código: 101
Nome: Teclado
Preço: R$ 150.75
Quantidade em Estoque: 20
Valor Total em Estoque: R$ 3015.00
------------------------------
~~~

#### Exemplo com Bônus (Pesquisa de Produto):

~~~yaml
===== PESQUISAR PRODUTO =====
Digite o nome do produto: Teclado

Produto encontrado:
Código: 101
Nome: Teclado
Preço: R$ 150.75
Quantidade em Estoque: 20
~~~
