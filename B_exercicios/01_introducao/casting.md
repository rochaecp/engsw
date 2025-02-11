# Exercícios - Operações de Casting

## 1) **Conversor de Tipos - Calculadora de Compras**

#### Descrição:

- Você foi contratado para desenvolver uma calculadora de compras que realiza operações matemáticas simples, mas que envolve diferentes tipos de dados. 
- O objetivo é trabalhar com operações de casting (conversão de tipos) para garantir que os cálculos sejam feitos corretamente.

#### Requisitos:

- O programa deve solicitar:
    - O nome do produto.
    - O preço unitário do produto (como número decimal).
    - A quantidade do produto desejada (como número inteiro).
- O programa deve realizar as operações de cálculo aplicando casting sempre que necessário.

#### O programa deve:

- Solicitar as informações do produto: nome, preço unitário e quantidade.
- Calcular o valor total da compra, multiplicando o preço unitário pela quantidade.
- Converter o valor total para um inteiro, descartando os centavos, e exibir o resultado.
- Exibir o valor original com centavos e o valor convertido (casting para inteiro).

#### Bônus (opcional):

- Adicionar uma funcionalidade para calcular um desconto percentual informado pelo usuário.
    - O valor do desconto deve ser convertido de inteiro para decimal para o cálculo correto.
- Permitir que o usuário realize várias operações, até decidir sair do programa.

#### Exemplo de Entrada Esperada (Sem Desconto):

~~~yaml
Informe o nome do produto: Camiseta  
Informe o preço unitário (ex: 49.99): 49.99  
Informe a quantidade desejada: 3  
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== Resumo da Compra =====
Produto: Camiseta
Preço unitário: R$ 49.99
Quantidade: 3
Valor total (com centavos): R$ 149.97
Valor total (arredondado para baixo): R$ 149
============================
~~~

#### Exemplo de Entrada Esperada (Com Desconto - Bônus):

~~~yaml
Informe o nome do produto: Tênis  
Informe o preço unitário (ex: 120.50): 120.50  
Informe a quantidade desejada: 2  
Deseja aplicar um desconto? (sim/não): sim  
Informe o percentual de desconto (ex: 10): 15  
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== Resumo da Compra =====
Produto: Tênis
Preço unitário: R$ 120.50
Quantidade: 2
Valor total (antes do desconto): R$ 241.00
Desconto aplicado (15%): R$ 36.15
Valor final (com desconto): R$ 204.85
Valor final (arredondado para baixo): R$ 204
============================
~~~
