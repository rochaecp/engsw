# Exercícios - Criação e uso de constantes

## 1) **Calculadora de Salário com Impostos Fixos**

#### Descrição

- Você foi contratado para desenvolver uma calculadora de salário líquido para uma empresa. 
- O sistema deve considerar impostos fixos que são aplicados sobre o salário bruto dos funcionários. 
- Esses impostos não mudam, portanto, devem ser definidos como constantes no código.

#### Requisitos

- Defina as seguintes constantes:
    - TAXA_IR (Imposto de Renda): 15% (0.15)
    - TAXA_INSS (Contribuição Previdenciária): 11% (0.11)
    - TAXA_SAUDE (Plano de Saúde): 5% (0.05)

#### O programa deve

- Solicitar ao usuário o valor do salário bruto de um funcionário.
- Calcular o valor de cada desconto com base nas taxas definidas.
- Calcular o salário líquido, subtraindo todos os impostos do salário bruto.
- Exibir um relatório detalhado com o salário bruto, cada desconto e o salário líquido.

#### Bônus (opcional)

- Permita calcular o salário líquido para mais de um funcionário usando um laço de repetição.
- Exiba o total de impostos arrecadados ao final do programa.

#### Exemplo de Entrada Esperada

~~~yaml
Informe o salário bruto do funcionário: 5000.00
~~~

#### Exemplo de Saída Esperada

~~~yaml
Descontos:
- Imposto de Renda (15%): 750.00
- INSS (11%): 550.00
- Plano de Saúde (5%): 250.00

Salário Bruto: 5000.00
Total de Descontos: 1550.00
Salário Líquido: 3450.00
~~~