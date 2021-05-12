# Dicionário Hacking

Um dicionário com técnicas e suas definições

[English](https://github.com/dfop02/hacking-dict/blob/main/README.md) | [Português-BR](https://github.com/dfop02/hacking-dict/blob/main/README_pt-br.md)

### Phishing
--- Significado
> Phishing é um tipo de ataque utilizando engenharia social para roubar dados de um usuário, incluindo credenciais de login e cartão de crédito.

--- Como prevenir

A técnica de Pishing compõe justamente de enganar no usuário com emails ou links chamativos, ou ainda um espelho de sites com o objetivo de você digitar suas credenciais no local errado.

### SQL INJECT
--- Significado
> A injeção de SQL é uma vulnerabilidade de segurança da web que permite que um invasor interfira nas consultas que um aplicativo faz ao seu banco de dados. Geralmente, permite que um invasor visualize dados que normalmente não é capaz de recuperar. Isso pode incluir dados pertencentes a outros usuários ou quaisquer outros dados que o próprio aplicativo é capaz de acessar. Em muitos casos, um invasor pode modificar ou excluir esses dados, causando alterações persistentes no conteúdo ou comportamento do aplicativo. Em algumas situações, um invasor pode escalar um ataque de injeção de SQL para comprometer o servidor subjacente ou outra infraestrutura de back-end, ou realizar um ataque de negação de serviço.

--- Como prevenir

A maioria das instâncias de SQL INJECT pode ser evitada usando consultas parametrizadas (também conhecidas como instruções preparadas) em vez da concatenação de strings na consulta.

As consultas parametrizadas podem ser usadas para qualquer situação em que a entrada não confiável apareça como dados na consulta, incluindo a cláusula WHERE e os valores em uma instrução INSERT ou UPDATE. Eles não podem ser usados ​​para manipular entradas não confiáveis ​​em outras partes da consulta, como nomes de tabelas ou colunas, ou a cláusula ORDER BY. A funcionalidade do aplicativo que coloca dados não confiáveis ​​nessas partes da consulta precisará adotar uma abordagem diferente, como os valores de entrada permitidos da lista branca ou usar uma lógica diferente para fornecer o comportamento necessário.

Para que uma consulta parametrizada seja eficaz na prevenção da injeção de SQL, a string usada na consulta deve ser sempre uma constante embutida em código e nunca deve conter dados variáveis ​​de qualquer origem. Não fique tentado a decidir caso a caso se um item de dados é confiável e continue usando a concatenação de string na consulta para casos considerados seguros. É muito fácil cometer erros sobre a possível origem dos dados ou que as alterações em outro código violem as suposições sobre quais dados estão corrompidos.

### Cross-site Scripting (XSS)
--- Significado
> Cross-site Scripting (XSS) é um ataque de insersão de código através do lado do cliente. O invasor tem como objetivo executar scripts mal-intencionados em um navegador da Web da vítima, incluindo código malicioso em uma página ou aplicativo da Web legítimo. O ataque real ocorre quando a vítima visita a página da web ou o aplicativo da web que executa o código malicioso.

--- Como prevenir

Para se manter protegido do XSS, você deve higienizar sua entrada. O código do seu aplicativo nunca deve gerar dados recebidos como entrada diretamente no navegador, sem verificar se há código malicioso.
