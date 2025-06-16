# 🟣 São Paulo (sa-east-1)

## Visão Geral
A região da AWS São Paulo (sa-east-1) foi escolhida para hospedar o banco de dados relacional da plataforma Avalia.AI, utilizando o serviço Amazon RDS (Relational Database Service).

A escolha dessa região se dá pela Conformidade com a LGPD, pois a Lei Geral de Proteção de Dados exige que dados pessoais de brasileiros sejam armazenados em ambiente seguro, privado e, idealmente, no território nacional ou em países com legislação equivalente.

## Configurações

### VPC

- Nome: VPC-sa-east-1
- Cidr: 10.1.0.0/16
- Descrição: rede virtual isolada utilizada para hospedar os recursos de backend da aplicação, como o RDS.

### Subnet Privada

- Nome: Subnet-Privada-sa-east-1
- Cidr: 10.1.2.0/24