# Backend (EC2)
### Motivação
Escolhemos o EC2 para o backend, pois ele oferece uma grande flexibilidade, permitindo a escalabilidade e a disponibilidade da plataforma.

### Configurações da Instância

- **Tipo**: t3.micro
- **GB de armazenamento:** 8
- **VPC**: east1-vpc
- **AMI**: ami-backend (Baseado no Ubuntu Server 24 LTS)
- **Grupo de Segurança:** east1-backend-sg
- **Auto Scaling:** east1-backend-asg
  

### Grupo de Segurança - east1-backend-sg


<table>
  <tr>
    <th>Porta</th>
    <th>Protocolo</th>
    <th>Ips</th>
    <th>Descrição</th>
  </tr>
  <tr>
    <td>22</td>
    <td>SSH</td>
    <td>[Meu IP]</td>
    <td>Conexão SSH</td>
  </tr>
  <tr>
    <td>80, 443</td>
    <td>HTTP, HTTPS</td>
    <td>0.0.0.0/0</td>
    <td>Conexão HTTP e HTTPS</td>
  </tr>
</table>


### Grupo do Auto Scaling - east1-backend-asg
Utilizamos o Auto Scaling para gerenciar o escalonamento da instância, primariamente com base no uso de CPU.
#### Configurações:
- **Quantidade de minima de instancias:** 1
- **Quantidade de maxima de instancias:** 8
- **Quantidade de instancias desejadas:** 1
- **Familia de instancias:** t3.micro
- **Gatilho:**
  - **Metrica**: CPUUtilization
  -  **Limite**: 70%

### Load Balancer
Configuramos o load balancer para o backend, para distribuir as solicitações de forma equilibrada entre as instancias do backend. Além de servir o endpoint de acesso ao backend.



### Load Balancer
Configuramos o load balancer para o frontend, utilizando o Application Load Balancer (ALB) do Amazon Elastic Load Balancing Service (ELB).

- **Tipo**: Application Load Balancer
- **Protocolo**: HTTPS
- **Porta**: 443
- **VPC**: east1-vpc