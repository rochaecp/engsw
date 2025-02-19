# Exercícios - Uso de operadores lógicos

## 1) **Sistema de Controle de Acesso a um Evento**

#### Descrição

- Você foi contratado para desenvolver um programa de controle de acesso a um evento exclusivo. 
- O programa deverá verificar se uma pessoa está autorizada a entrar, usando operadores lógicos para combinar diferentes condições de acesso.

#### Requisitos

- O programa deve solicitar ao usuário as seguintes informações:
    - Idade da pessoa.
    - Possui convite? (responder "sim" ou "não").
    - Está na lista VIP? (responder "sim" ou "não").
- O programa deve usar operadores lógicos como:
    - AND (e)
    - OR (ou)
    - NOT (não)

#### O programa deve

- Solicitar ao usuário:
    - Idade da pessoa.
    - Se possui um convite válido.
    - Se está na lista VIP.
- Verificar as seguintes condições de acesso:
    - Entrada permitida se a pessoa:
        - Tiver 18 anos ou mais E possuir um convite válido.
        - OU
        - Estiver na lista VIP, independentemente da idade ou do convite.
- Exibir uma mensagem informando se a pessoa pode entrar ou não pode entrar, explicando o motivo da restrição, se for o caso.

#### Bônus

- Permitir a verificação de acesso para várias pessoas até o usuário decidir encerrar o programa.
- Adicionar uma condição para que menores de idade (menos de 18 anos) possam entrar apenas se acompanhados de um responsável.

#### Exemplo de Entrada Esperada (Pessoa Autorizada):

~~~yaml
Informe sua idade: 20  
Você possui um convite válido? (sim/não): sim  
Você está na lista VIP? (sim/não): não  
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== Verificação de Acesso =====
Acesso PERMITIDO. Aproveite o evento!
===================================
~~~

#### Exemplo de Entrada Esperada (Pessoa Não Autorizada):

~~~yaml
Informe sua idade: 16  
Você possui um convite válido? (sim/não): não  
Você está na lista VIP? (sim/não): não  
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== Verificação de Acesso =====
Acesso NEGADO. Motivo: Menor de idade sem convite e não está na lista VIP.
==========================================
~~~

#### Exemplo de Entrada Esperada (Pessoa VIP):

~~~yaml
Informe sua idade: 15  
Você possui um convite válido? (sim/não): não  
Você está na lista VIP? (sim/não): sim  
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== Verificação de Acesso =====
Acesso PERMITIDO. Você está na lista VIP!
=========================================
~~~
