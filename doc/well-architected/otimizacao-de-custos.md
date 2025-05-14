## Otimização de Custos — Pilar do AWS Well-Architected Framework

A **Otimização de Custos** trata da capacidade de **executar sistemas entregando valor ao negócio pelo menor custo possível**, sem comprometer desempenho, segurança ou escalabilidade.

O objetivo não é apenas reduzir despesas, mas **alocar recursos de forma inteligente**, garantindo que cada real gasto contribua efetivamente para os resultados do negócio.

É o famoso: **“Fazer mais, pagando menos.”**

---

### Conceitos-chave

- ✅ O custo **deve estar sempre atrelado ao valor gerado**.
- ✅ O desperdício de recursos na nuvem acontece com frequência — máquinas ligadas sem uso, superdimensionadas, logs em excesso, backups mal gerenciados etc.
- ✅ Otimizar custos é um **processo contínuo**, não uma tarefa pontual.
- ✅ O preço mais barato **não é sempre a melhor escolha** — o foco é no custo-benefício, não apenas no menor valor.

---

### Princípios da Otimização de Custos

- ✅ **Implemente o Cloud Financial Management (CFM)**

  - Tenha visibilidade, processos, governança e cultura para tomar decisões financeiras na nuvem.
  - Estabeleça KPIs, limites, alertas e processos de revisão contínua.

  **Use ferramentas como:**

  - AWS Cost Explorer
  - AWS Budgets
  - AWS Billing Dashboard
  - AWS Trusted Advisor

- ✅ **Adote um modelo de consumo**

  - Pague apenas pelo que usar. Evite recursos provisionados sem necessidade.
  - Use serviços sob demanda, serverless, spot instances, instâncias reservadas, savings plans.
  - Exemplo: em vez de uma instância EC2 ligada 24h para um sistema batch, use AWS Lambda ou Fargate por demanda.

- ✅ **Meça e melhore a eficiência geral**

  - Avalie se está usando recursos com a capacidade correta.
  - Compare custo por transação, por requisição ou por MB processado.
  - Exemplo: reduzir o tempo de execução de uma função Lambda pode economizar centenas de dólares/mês.

- ✅ **Evite gastar dinheiro com o que não traz valor estratégico**

  - Não gaste recursos com tarefas que não geram diferencial competitivo (ex: hospedar e manter seu próprio banco de dados se o RDS já atende suas necessidades).
  - Prefira serviços gerenciados sempre que possível para reduzir esforço operacional e custo oculto.

- ✅ **Analise e atribua despesas**

  - Implemente **tagging de recursos** (por time, projeto, ambiente, cliente)
  - Use o AWS Cost Allocation Tags para identificar onde estão os maiores gastos
  - Faça chargeback ou showback por departamento ou cliente interno

- ✅ **A complexidade é inimiga da eficiência**
  - Quanto mais complexa a arquitetura, mais difícil controlar custos.
  - Simplifique sua stack, evite dependências desnecessárias, mantenha a documentação atualizada
  - Use arquiteturas desacopladas, reutilizáveis e com responsabilidade financeira clara

---

### Exemplos práticos de Otimização de Custos:

- ✅ Identificar EC2 ociosas com Trusted Advisor e desligá-las
- ✅ Substituir instâncias sob demanda por instâncias spot para cargas tolerantes a falhas
- ✅ Utilizar Savings Plans ou instâncias reservadas para workloads estáveis
- ✅ Consolidar bancos de dados pequenos em um único RDS multi-tenant
- ✅ Usar Lambda para automações simples em vez de EC2
- ✅ Reduzir retenção desnecessária de logs (ex: CloudWatch Logs com retenção infinita)

---

### Ferramentas recomendadas para acompanhar e otimizar custos:

- ✅ **AWS Cost Explorer** – análise detalhada de gastos
- ✅ **AWS Budgets** – definir alertas de orçamento
- ✅ **AWS Pricing Calculator** – estimativas de custo antes de usar um serviço
- ✅ **AWS Compute Optimizer** – recomendações para tipos de instância mais eficientes
- ✅ **AWS Trusted Advisor** – alerta sobre desperdícios e oportunidades de economia
- ✅ **AWS S3 Intelligent-Tiering** – armazenamento que otimiza custo automaticamente

---

### Benefícios de aplicar este pilar:

- ✅ Redução de custos sem comprometer qualidade
- ✅ Visão clara do ROI (Retorno sobre investimento)
- ✅ Mais previsibilidade no orçamento
- ✅ Maior agilidade para testar novas ideias com segurança financeira
- ✅ Cultura de responsabilidade financeira entre desenvolvedores, arquitetos e gestores

---

### Referências:

- [AWS Well-Architected Cost Optimization Pillar (Docs)](https://docs.aws.amazon.com/wellarchitected/latest/cost-optimization-pillar/welcome.html)
- [AWS Cloud Financial Management](https://aws.amazon.com/aws-cost-management/cloud-financial-management/)
- [AWS Pricing Calculator](https://calculator.aws.amazon.com/)
