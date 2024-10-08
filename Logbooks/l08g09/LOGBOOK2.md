# Trabalho realizado nas Semanas #2 e #3

## Identificação

- Na aplicação para Android <code>com.cutestudio.colordialer</code>, que funciona como uma interface personalizável de chamadas telefónicas e contactos, o componente <code>com.cutestudio.dialer.activities.DialerActivity</code> apresenta uma exportação imprópria.
- Esta vulnerabilidade permite que aplicações externas possam efetuar chamadas telefónicas para um número arbitrário sem qualquer consentimento do utilizador.


## Catalogação

- Descoberta por: Edward Warren
- Data de publicação: 02-09-2023
- Nível de gravidade: 5.3

## Exploit

- A aplicação recorre à ação <code>android.intent.action.CALL</code>, que recebe como parâmetro o número de telefone introduzido pelo utilizador.
- No entanto, através do componente vulnerável, uma aplicação externa pode mudar o parâmetro para um número qualquer, sem o utilizador dar por isso.

## Ataques

- Como se trata de um exploit bastante recente, não há registo de nenhum ataque efetuado.
