# 🟡 Funções (Lambda)

## Visão Geral
Essas funções serão responsáveis pelo acionamento do SNS atráves de um alarme do CloudWatch, permitindo a criação de novos workers para processar as provas pendentes.

## Funções Lambda

### ScaleUp:
A função ScaleUp irá ser acionada quando houver uma ou mais provas pendentes na fila de envio de mensagens e nenhum worker online.
O alarme do CloudWatch irá acionar as Funções Lambda, que irão criar novos workers para processar as provas pendentes.

### ScaleDown:
A função ScaleDown irá ser acionada quando houver um worker online e nenhuma prova pendente na fila de envio de mensagens.
O alarme do CloudWatch irá acionar as Funções Lambda, que irão encerrar os workers online.