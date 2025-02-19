# Exercícios - Criação e uso de variáveis

## 1) **Sistema de Controle de Inventário Simplificado**

#### Descrição

- Você foi contratado para desenvolver um sistema simples de controle de inventário para uma pequena loja. 
- O sistema deve permitir o registro de três produtos, armazenando informações básicas sobre cada um, como nome, quantidade em estoque e preço unitário.

#### Requisitos

- Crie variáveis para armazenar as seguintes informações para cada produto:
    - Nome do produto (texto/string)
    - Quantidade em estoque (número inteiro/integer)
    - Preço unitário (número decimal/float/double)

#### O programa deve

- Solicitar ao usuário que insira as informações para três produtos diferentes.
- Calcular o valor total em estoque para cada produto (quantidade em estoque * preço unitário).
- Exibir um relatório final com o nome do produto, quantidade em estoque, preço unitário e o valor total em estoque.

#### Bônus

- Calcule o valor total do inventário da loja (soma do valor total em estoque de todos os produtos).
- Permita ao usuário atualizar a quantidade de um dos produtos e exiba o relatório atualizado.

#### Exemplo de Entrada Esperada

~~~yaml
Informe o nome do produto 1: Caneta
Informe a quantidade em estoque de Caneta: 100
Informe o preço unitário de Caneta: 1.50

Informe o nome do produto 2: Caderno
Informe a quantidade em estoque de Caderno: 50
Informe o preço unitário de Caderno: 7.20

Informe o nome do produto 3: Mochila
Informe a quantidade em estoque de Mochila: 20
Informe o preço unitário de Mochila: 150.00
~~~

#### Exemplo de Saída Esperada  

~~~yaml
Relatório do Inventário:
Produto: Caneta | Quantidade: 100 | Preço Unitário: 1.50 | Valor Total: 150.00
Produto: Caderno | Quantidade: 50 | Preço Unitário: 7.20 | Valor Total: 360.00
Produto: Mochila | Quantidade: 20 | Preço Unitário: 150.00 | Valor Total: 3000.00

Valor total do inventário: 3510.00
~~~

