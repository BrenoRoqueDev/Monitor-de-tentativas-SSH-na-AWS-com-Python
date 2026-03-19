# Projeto SSH Shield

## Introdução
Este documento apresenta a documentação do projeto SSH Shield, uma solução desenvolvida para monitorar tentativas de acesso SSH na AWS utilizando Python.

## Objetivo
O principal objetivo do projeto é oferecer uma camada extra de segurança ao monitorar e registrar tentativas de login no serviço SSH, permitindo que administradores de sistema possam responder de forma proativa a potenciais ameaças.

## Arquitetura
A arquitetura do SSH Shield é composta por diversos componentes que trabalham em conjunto:

1. **AWS EC2**: Instâncias EC2 onde o serviço SSH está em execução.
2. **AWS CloudWatch**: Para monitoramento e logs de eventos.
3. **AWS Lambda**: Para processar os logs e desencadear alertas.
4. **Banco de Dados**: Onde os dados das tentativas de acesso são armazenados.

![Arquitetura do SSH Shield](link-para-arquitetura.png)

## Tecnologias Utilizadas
- Python
- Boto3 (biblioteca da AWS para Python)
- AWS CloudWatch
- AWS Lambda
- Amazon RDS (ou DynamoDB por escolha)

## Desafios Enfrentados
- **Integração com serviços da AWS**: A integração com diferentes serviços da AWS foi complexa, principalmente na configuração das permissões necessárias.
- **Gerenciamento de logs**: O volume de dados gerados pelas tentativas de login exigiu uma solução eficaz para armazenamento e análise.

## Resultados e Aprendizados
Ao final do projeto, conseguimos implementar uma solução funcional que não só monitora as tentativas de acesso, mas também alerta os administradores em tempo real. Aprendemos sobre a importância da segurança em ambientes de nuvem e como utilizar as ferramentas da AWS de forma eficiente.

## Conclusão
O projeto SSH Shield representa um passo significativo em direção à segurança aprimorada para serviços expostos na internet, como o SSH. Com a implementação de soluções como esta, é possível reduzir riscos e proteger dados sensíveis contra acessos não autorizados.

## Contato
Para mais informações ou contribuições, entre em contato: BrenoRoqueDev