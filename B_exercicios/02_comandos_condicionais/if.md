# Exercícios - Uso do comandoo If

## 1) Classificador de Idade

#### Descrição:

- Crie um programa que classifique uma pessoa de acordo com sua idade. 
- O programa deve receber a idade como entrada e, utilizando a estrutura condicional if, determinar a categoria correspondente (criança, adolescente, adulto ou idoso).

#### Requisitos:

- O programa deve solicitar que o usuário insira sua idade.
- Deve utilizar o comando if (e, se necessário, else if/elif e else) para verificar em qual faixa etária a idade se encaixa.
- As categorias devem ser definidas da seguinte forma:
    - Criança: 0 a 12 anos
    - Adolescente: 13 a 17 anos
    - Adulto: 18 a 59 anos
    - Idoso: 60 anos ou mais

#### O programa deve:

- Solicitar a idade do usuário.
- Verificar a faixa etária usando estruturas condicionais.
- Exibir a categoria correspondente de forma clara.
- Validar se a idade é um número positivo.

#### Bônus (opcional):

- Adicionar uma verificação para garantir que o usuário não insira números negativos ou valores não numéricos.
- Permitir que o programa continue rodando até o usuário optar por sair.
- Adicionar uma categoria adicional, como "recém-nascido" para idades de 0 a 1 ano.
- Calcular o ano de nascimento com base na idade informada, considerando o ano atual.

#### Exemplo de Entrada Esperada:

~~~yaml
Digite sua idade: 25
~~~

#### Exemplo de Saída Esperada:

~~~yaml
Você é classificado como: Adulto
~~~

#### Exemplo de Entrada com Erro (Bônus):

~~~yaml
Digite sua idade: -5
~~~

#### Exemplo de Saída com Validação (Bônus):

~~~yaml
Idade inválida. Por favor, insira um número positivo.
~~~

#### Saída Final (quando o usuário decidir sair - Bônus):

~~~yaml
Obrigado por usar o Classificador de Idade. Até a próxima!
~~~