# Exercícios - Uso do comando Switch

## 1) **Conversor de Notas para Conceitos**

#### Descrição

- Crie um programa que converta uma nota numérica (de 0 a 10) em um conceito de avaliação (A, B, C, D ou F) usando o comando switch. 
- O objetivo é praticar o uso do switch para tomar decisões com base em diferentes faixas de valores.

#### Requisitos

- O programa deve solicitar que o usuário insira uma nota inteira de 0 a 10.
- O comando switch deve ser usado para determinar o conceito correspondente à nota.
- O programa deve considerar as seguintes faixas de notas:
    - 9 e 10: Conceito A
    - 7 e 8: Conceito B
    - 5 e 6: Conceito C
    - 3 e 4: Conceito D
    - 0 a 2: Conceito F

#### O programa deve

- Solicitar que o usuário insira uma nota inteira entre 0 e 10.
- Usar o comando switch para associar a nota ao conceito correto.
- Exibir o conceito correspondente à nota.
- Informar uma mensagem de erro caso o valor inserido não esteja no intervalo permitido.

#### Bônus

- Permitir que o usuário insira várias notas até decidir encerrar o programa.
- Aceitar notas com ponto decimal, convertendo-as para o número inteiro mais próximo antes da avaliação.
- Exibir uma mensagem personalizada com base no conceito, por exemplo:
    - A: "Excelente!"
    - B: "Bom trabalho!"
    - C: "Pode melhorar."
    - D: "Atenção aos estudos!"
    - F: "Reprovado, estude mais!"

#### Exemplo de Entrada Esperada

~~~yaml
Digite a nota (0 a 10): 8
~~~

#### Exemplo de Saída Esperada:

~~~yaml
Conceito: B
Bom trabalho!
~~~

#### Exemplo de Entrada Inválida:

~~~yaml
Digite a nota (0 a 10): 15
~~~

#### Exemplo de Saída com Validação:

~~~yaml
Nota inválida. Por favor, insira um valor entre 0 e 10.
~~~

#### Exemplo com Bônus (várias notas):

~~~yaml
Digite a nota (0 a 10): 10
Conceito: A
Excelente!

Deseja inserir outra nota? (s/n): s
Digite a nota (0 a 10): 3
Conceito: D
Atenção aos estudos!

Deseja inserir outra nota? (s/n): n
Programa finalizado.
~~~