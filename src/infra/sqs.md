# ⭕ SQS
## Visão Geral
Para garantir a escalabilidade e desacoplamento dos microserviços, utilizamos o Amazon SQS como mecanismo de mensageria assíncrona. O SQS permite que os produtores de mensagens (como o frontend ou outros serviços) enviem tarefas para uma fila, que são posteriormente consumidas por workers do microserviço responsável pelo processamento automático.

Esse modelo melhora o desempenho geral da aplicação, evita perda de mensagens e permite que o sistema seja horizontalmente escalável, pois múltiplas instâncias do microserviço podem consumir da mesma fila de forma distribuída.



## Configuração

### Fila de Envio de Mensagens
**Nome da Fila:** avalia-ai-queue

**URL:** https://sqs.us-east-1.amazonaws.com/123456789012/avalia-ai-queue

**Tipo de Fila**: Standard

**Região**: us-east-1 (Norte da Virgínia)

## Considerações:

Essa arquitetura permite o escalonamento automático do microserviço em conjunto ao Alarme do CloudWatch com Funções Lambda, adaptando a quantidade de instâncias do microserviço (ECS + Fargate) conforme a demanda.