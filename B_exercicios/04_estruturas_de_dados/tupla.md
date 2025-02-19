# Exercícios - Utilizando Tuplas

## 1) **Cadastro de Produtos com Tuplas**

#### Descrição

- Crie um programa para gerenciar o cadastro de produtos em um estoque simples utilizando tuplas para armazenar informações de cada produto. 
- Cada produto terá as seguintes informações: nome, preço e quantidade em estoque.

#### Requisitos

- O programa deve utilizar tuplas para armazenar as informações de cada produto.
- Os produtos serão armazenados em uma lista ou outra estrutura que permita gerenciar vários produtos.
- O programa deve oferecer um menu interativo com opções para o usuário.

#### O programa deve

- Adicionar um novo produto, solicitando o nome, o preço e a quantidade em estoque.
- Listar todos os produtos, exibindo o nome, o preço e a quantidade.
- Buscar um produto pelo nome, mostrando suas informações detalhadas.
- Calcular o valor total em estoque de todos os produtos (preço * quantidade).
- Continuar funcionando até o usuário escolher a opção de sair do programa.

#### Bônus

- Permitir a atualização da quantidade de um produto já cadastrado.
- Calcular o produto mais caro e o mais barato do estoque.
- Exibir os produtos em ordem alfabética ou por ordem de preço.
- Implementar uma função de desconto, permitindo aplicar um desconto percentual a um produto específico.

#### Exemplo de Entrada Esperada

~~~yaml
===== GERENCIADOR DE ESTOQUE =====
1. Adicionar Produto
2. Listar Produtos
3. Buscar Produto
4. Calcular Valor Total em Estoque
5. Sair
Escolha uma opção: 1
Digite o nome do produto: Notebook
Digite o preço do produto: 3500.00
Digite a quantidade em estoque: 5

===== GERENCIADOR DE ESTOQUE =====
Escolha uma opção: 1
Digite o nome do produto: Teclado
Digite o preço do produto: 150.00
Digite a quantidade em estoque: 10

===== GERENCIADOR DE ESTOQUE =====
Escolha uma opção: 2
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== LISTA DE PRODUTOS =====
Produto: Notebook | Preço: R$ 3500.00 | Quantidade: 5
Produto: Teclado  | Preço: R$ 150.00  | Quantidade: 10
~~~

#### Exemplo com Bônus (Cálculo do Valor Total em Estoque):

~~~yaml
===== GERENCIADOR DE ESTOQUE =====
Escolha uma opção: 4

===== VALOR TOTAL EM ESTOQUE =====
R$ 20,750.00
~~~
