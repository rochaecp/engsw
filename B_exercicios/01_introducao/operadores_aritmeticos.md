# Exercícios - Uso de operadores aritméticos

## 1) **Calculadora de Desempenho de Viagem**

#### Descrição

- Você foi contratado para criar um programa que ajude motoristas a calcular o desempenho de suas viagens. 
- O programa deve usar operadores aritméticos para calcular a distância percorrida, o consumo médio de combustível e o custo total da viagem com base no preço do combustível.

#### Requisitos

- O motorista fornecerá:
    - O odômetro inicial (quilometragem no início da viagem).
    - O odômetro final (quilometragem ao final da viagem).
    - A quantidade de combustível consumida durante a viagem (em litros).
    - O preço por litro do combustível.
- O programa deve realizar cálculos usando os seguintes operadores aritméticos:
    - Subtração para calcular a distância percorrida.
    - Divisão para calcular o consumo médio de combustível (km/l).
    - Multiplicação para calcular o custo total da viagem.

#### O programa deve

- Solicitar ao usuário as informações mencionadas nos requisitos.
- Calcular a distância percorrida:
    - Fórmula: distância = odômetro final - odômetro inicial
- Calcular o consumo médio de combustível:
    - Fórmula: consumo médio = distância percorrida / quantidade de combustível
- Calcular o custo total da viagem:
    - Fórmula: custo total = quantidade de combustível * preço por litro
- Exibir um relatório final com todos os resultados calculados.

#### Bônus

- Permitir que o usuário calcule o desempenho de múltiplas viagens, mostrando um resumo final com a soma total da distância percorrida, combustível consumido e custo total.
- Adicionar uma verificação para garantir que o odômetro final seja maior que o inicial.

#### Exemplo de Entrada Esperada

~~~yaml
Informe o odômetro inicial (km): 12000  
Informe o odômetro final (km): 12500  
Informe a quantidade de combustível consumido (litros): 40  
Informe o preço por litro do combustível: 5.50  
~~~

#### Exemplo de Saída Esperada

~~~yaml
===== Relatório da Viagem =====
Distância Percorrida: 500 km
Consumo Médio de Combustível: 12.5 km/l
Custo Total da Viagem: R$ 220.00
==============================
~~~