# Exercícios - Operações com números aleatórios

## 1) **Jogo de Adivinhação com Números Aleatórios**

#### Descrição

- Crie um jogo de adivinhação onde o programa gera um número aleatório dentro de um intervalo definido pelo usuário, e o objetivo é que o jogador tente adivinhar o número correto. 
- O programa dará dicas se o número informado é maior ou menor do que o número gerado, até que o jogador acerte.

#### Requisitos

- O programa deve utilizar uma função de geração de números aleatórios da linguagem escolhida.
- O intervalo dos números aleatórios deve ser definido pelo próprio usuário (ex: de 1 a 100).
- O programa deve contar o número de tentativas feitas pelo jogador.
- O programa deve verificar se o valor inserido é um número válido.

#### O programa deve

- Solicitar ao usuário que informe o intervalo mínimo e máximo para o número aleatório.
- Gerar um número aleatório dentro do intervalo definido.
- Solicitar que o jogador tente adivinhar o número.
- Após cada tentativa, o programa deve informar se o número inserido é:
    - Maior do que o número gerado.
    - Menor do que o número gerado.
    - Correto, encerrando o jogo.
- Exibir o número total de tentativas realizadas até acertar.

#### Bônus

- Implementar um modo difícil, onde o jogador tem um número limitado de tentativas.
- Criar um ranking de melhores pontuações, registrando o menor número de tentativas em jogos anteriores.
- Adicionar uma opção de jogar novamente sem reiniciar o programa.
- Permitir que o jogador escolha entre adivinhar números inteiros ou números decimais.

#### Exemplo de Entrada Esperada

~~~yaml
===== Jogo de Adivinhação =====
Informe o intervalo de números:
Mínimo: 1
Máximo: 50

Tente adivinhar o número gerado!
Digite seu palpite: 25
O número é maior que 25. Tente novamente.

Digite seu palpite: 40
O número é menor que 40. Tente novamente.

Digite seu palpite: 32
Parabéns! Você acertou o número 32 em 3 tentativas.
~~~

~~~yaml
===== Resultado =====
Número gerado: 32
Tentativas realizadas: 3
Status: Você venceu!

Deseja jogar novamente? (s/n): n
Obrigado por jogar!
~~~
