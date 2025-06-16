# Route 53

## Visão Geral
Neste projeto, utilizamos o Amazon Route 53 como serviço de DNS gerenciado para realizar o roteamento de requisições externas para a aplicação hospedada na AWS. Ele atua como o ponto de entrada da aplicação, conectando o domínio personalizado ao Load Balancer que serve o frontend.

## Configuração

### Domínio

**Tipo de Zona**: Pública (Public Hosted Zone)

**Tipo de Registro**: A (Alias)

**Nome**: www.avalia.ai (subdomínio para frontend)

**TTL (Time to Live)**: 300 segundos

**Alias Target**: east1-frontend-alb.dnsname (representa o DNS do Application Load Balancer do frontend)

**Evaluate Target Health**: true (verifica saúde do destino)

**Protocolo de Acesso**: HTTPS (embora configurado no Load Balancer, não no Route 53)

### Política de Roteamento
**Tipo**: Simples (Simple Routing)


