# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 22/10/2026
**Empresa:** Abstergo Industries
**Responsável:** Anderson Otávio

## Introdução

Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Anderson Otávio. O objetivo do projeto foi elencar 3 serviços AWS com a finalidade de realizar a diminuição de custos imediatos, otimizando o uso da infraestrutura em nuvem sem comprometer o desempenho das operações.

## Descrição do Projeto

O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

### Etapa 1: AWS Cost Explorer e AWS Budgets

- **Nome da ferramenta:** AWS Cost Explorer (em conjunto com o AWS Budgets)
- **Foco da ferramenta:** Visibilidade, análise e controle de gastos na AWS.
- **Descrição de caso de uso:** Antes de qualquer corte, a Abstergo precisa saber para onde o dinheiro está indo. O Cost Explorer permite visualizar os custos por serviço, conta, região e tags, identificar recursos ociosos ou superdimensionados e consultar recomendações de *rightsizing* para instâncias EC2. Com o AWS Budgets, serão configurados orçamentos mensais por departamento com alertas automáticos por e-mail sempre que o gasto real ou previsto ultrapassar os limites definidos, evitando surpresas na fatura.

### Etapa 2: AWS Lambda

- **Nome da ferramenta:** AWS Lambda
- **Foco da ferramenta:** Computação *serverless* com cobrança apenas pelo uso efetivo.
- **Descrição de caso de uso:** Diversas rotinas internas da Abstergo (geração de relatórios, processamento de arquivos enviados, integrações agendadas) rodam hoje em servidores ligados 24 horas por dia, mesmo ficando ociosos na maior parte do tempo. Migrando essas tarefas para o AWS Lambda, a empresa paga somente pelo número de requisições e pelo tempo de execução de cada função, eliminando o custo de servidores parados e reduzindo o esforço de manutenção de sistemas operacionais e atualizações.

### Etapa 3: Amazon S3 Intelligent-Tiering

- **Nome da ferramenta:** Amazon S3 Intelligent-Tiering
- **Foco da ferramenta:** Otimização automática dos custos de armazenamento.
- **Descrição de caso de uso:** A Abstergo armazena grande volume de dados (backups, logs, documentos e arquivos de pesquisa) cujo padrão de acesso varia ao longo do tempo. A classe S3 Intelligent-Tiering monitora o acesso a cada objeto e o move automaticamente entre camadas de armazenamento mais baratas quando ele deixa de ser acessado com frequência, trazendo-o de volta à camada frequente quando volta a ser usado, sem taxas de recuperação e sem impacto no desempenho. Isso reduz o custo de armazenamento sem exigir que a equipe classifique os dados manualmente.

## Conclusão

A implementação de ferramentas na empresa Abstergo Industries tem como esperado a redução imediata de custos com infraestrutura, por meio do monitoramento e controle dos gastos (AWS Cost Explorer e Budgets), da eliminação do pagamento por servidores ociosos (AWS Lambda) e da otimização automática do armazenamento de dados (Amazon S3 Intelligent-Tiering), o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

## Anexos

- Documentação oficial do AWS Cost Explorer: https://aws.amazon.com/aws-cost-management/aws-cost-explorer/
- Documentação oficial do AWS Budgets: https://aws.amazon.com/aws-cost-management/aws-budgets/
- Documentação oficial do AWS Lambda: https://aws.amazon.com/lambda/
- Documentação oficial do Amazon S3 Intelligent-Tiering: https://aws.amazon.com/s3/storage-classes/intelligent-tiering/
- Calculadora de preços da AWS: https://calculator.aws/

---

**Assinatura do Responsável pelo Projeto:**

Anderson Otávio
