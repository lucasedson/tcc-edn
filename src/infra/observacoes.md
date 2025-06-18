# Além do MVP

O projeto apresentado buscou desenvolver uma solução completa, escalável e funcional de um MVP. Buscamos principalmente projetar o escopo no nível de arquitetura cloud, com o uso de diversos serviços da AWS, como EC2, RDS, S3, SQS, ECS e Fargate. 

## Possíveis Evoluções Futuras:

### IAC:
- Utilizar IaC com o CloudFormation para provisionar os recursos da plataforma, evitando erros e garantindo a consistência dos recursos.

### Serviços de IA:
- **Bedrock com o modelo Amazon Nova**: Para melhorar a qualidade de produção de questões nas avaliações.
- **Amazon Textract + Amazon Comprehend / Amazon SageMaker**:
    - Extrair texto de imagens e PDFs, como redações manuscritas ou provas escaneadas.
    - Realizar análise gramatical e correção automática de textos dissertativos com NLP.

### CI/CD:
Utilizar os serviços para gerenciamento de versionamento e **CI/CD**:
- **AWS CodeCommit**: repositório Git privado para controle de versão;
- **AWS CodePipeline**: orquestração do fluxo de integração contínua;
- **AWS CodeBuild**: compilação e testes automatizados;
- **AWS CodeDeploy**: deploy automatizado e sem downtime nos ambientes ECS/Fargate ou EC2.

