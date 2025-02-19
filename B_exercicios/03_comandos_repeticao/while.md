# Exercícios - Uso do comando While

## 1) **Jogo de Adivinhação de Números**

#### Descrição

- Crie um programa que implemente um jogo de adivinhação. 
- O computador escolherá um número aleatório entre 1 e 100, e o usuário deverá tentar adivinhar esse número. O programa usará o comando while para continuar solicitando palpites até o usuário acertar.

#### Requisitos

- O programa deve gerar um número aleatório entre 1 e 100.
- O usuário deve inserir palpites até adivinhar o número corretamente.
- O comando while deve ser usado para manter o loop de tentativas.
- O programa deve informar se o palpite do usuário está "muito alto", "muito baixo" ou "correto".
- O programa deve contar o número de tentativas feitas pelo usuário.

#### O programa deve

- Gerar um número aleatório entre 1 e 100.
- Pedir ao usuário que insira um palpite.
- Comparar o palpite do usuário com o número gerado:
    - Se o palpite for menor, exibir "Muito baixo! Tente novamente."
    - Se o palpite for maior, exibir "Muito alto! Tente novamente."
    - Se o palpite for correto, exibir "Parabéns! Você acertou em X tentativas."
- Continuar pedindo palpites até o número correto ser adivinhado.
- Mostrar o número total de tentativas ao final.

#### Bônus

- Limitar o número de tentativas (por exemplo, máximo de 10 tentativas).
- Permitir o usuário escolher o intervalo do número (por exemplo, entre 1 e 500).
- Adicionar um modo "difícil", onde o programa não dá dicas se o número está alto ou baixo.
- Exibir uma mensagem personalizada com base no número de tentativas (por exemplo, "Você é um gênio!" se acertar em menos de 5 tentativas).

#### Exemplo de Entrada Esperada

~~~yaml
Adivinhe o número entre 1 e 100:
Palpite: 45
Muito baixo! Tente novamente.
Palpite: 78
Muito alto! Tente novamente.
Palpite: 62
Muito baixo! Tente novamente.
Palpite: 70
Parabéns! Você acertou em 4 tentativas!
~~~

#### Exemplo de Saída Esperada:

~~~yaml
Adivinhe o número entre 1 e 100:
Palpite: 50
Muito alto! Tente novamente.
Palpite: 25
Muito baixo! Tente novamente.
Palpite: 37
Muito baixo! Tente novamente.
Palpite: 43
Parabéns! Você acertou em 4 tentativas!
~~~
