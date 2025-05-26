# IaC

Utilizar Iac (Infrastructure as Code) para provisionar os recursos da plataforma, é uma boa prática para evitar erros e garantir a consistência dos recursos.

Nesse projeto, utilizamos o CloudFormation para provisionar os recursos da plataforma e assim garantir a consistência dos recursos.

# Código da Infraestrutura:

```yaml

Resources:
    EC2Instance:
        Type: AWS::EC2::Instance
        # ...
```