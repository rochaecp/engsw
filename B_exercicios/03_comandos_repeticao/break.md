# Exercícios - Uso do comando Break

## 1) **Adivinhe o Número Secreto**

#### Descrição

- Crie um programa de adivinhação onde o usuário deve tentar descobrir um número secreto gerado aleatoriamente pelo computador. 
- O programa utilizará o comando break para interromper o loop assim que o número for adivinhado corretamente.

#### Requisitos

- O programa deve gerar um número secreto entre 1 e 100.
- O usuário deve ter tentativas ilimitadas até acertar o número.
- O comando break deve ser usado para encerrar o loop imediatamente quando o número correto for adivinhado.
- O programa deve informar se o palpite do usuário é maior ou menor que o número secreto, ajudando o usuário a ajustar suas tentativas.

#### O programa deve

- Gerar um número secreto aleatório entre 1 e 100.
- Solicitar que o usuário digite um palpite.
- Comparar o palpite com o número secreto:
    - Se o palpite for menor, exibir a mensagem: "Tente um número maior."
    - Se o palpite for maior, exibir a mensagem: "Tente um número menor."
    - Se o palpite for correto, exibir "Parabéns! Você acertou!" e usar o break para sair do loop.
- Continuar pedindo palpites até o número correto ser adivinhado.

#### Bônus

- Limitar o número de tentativas a 10. Se o usuário não acertar após 10 tentativas, o programa deve encerrar e revelar o número secreto.
- Exibir o número de tentativas que o usuário precisou para acertar.
- Adicionar um modo "difícil", onde o número secreto está entre 1 e 1000.
- Permitir que o usuário jogue novamente após o término do jogo.

#### Exemplo de Entrada Esperada

~~~yaml
Bem-vindo ao jogo de adivinhação!
Tente adivinhar o número entre 1 e 100.

Digite seu palpite: 50
Tente um número maior.

Digite seu palpite: 75
Tente um número menor.

Digite seu palpite: 62
Tente um número maior.

Digite seu palpite: 68
Parabéns! Você acertou o número secreto!
~~~

#### Exemplo de Saída Esperada (Bônus com limite de tentativas):

~~~yaml
Bem-vindo ao modo difícil! Você tem 10 tentativas para adivinhar o número entre 1 e 1000.

Tentativa 1: 500
Tente um número menor.

Tentativa 2: 300
Tente um número maior.

Tentativa 3: 400
Tente um número menor.

Tentativa 4: 350
Parabéns! Você acertou o número secreto em 4 tentativas!
~~~
