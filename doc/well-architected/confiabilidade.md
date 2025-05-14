# Confiabilidade (Reliability) — Pilar do AWS Well-Architected Framework

O pilar de **Confiabilidade** se refere à capacidade de uma carga de trabalho (workload) de **executar corretamente e de forma consistente** sua função ao longo do tempo, mesmo diante de falhas ou mudanças. Isso inclui tanto a **resiliência**, quanto a **capacidade de escalar**, se adaptar e se recuperar automaticamente sem falhas humanas.

A aplicação confiável é aquela que:

- ✅ Funciona como esperado, com consistência;
- ✅ Consegue lidar com picos de demanda;
- ✅ Resiste a falhas;
- ✅ Se recupera rapidamente;
- ✅ Escala de forma previsível;
- ✅ Pode passar por mudanças sem comprometer a disponibilidade.

---

### Objetivo

Projetar workloads que **sobrevivam a falhas**, sejam **auto-recuperáveis**, **testadas continuamente** e que possam escalar **horizontalmente** para manter a performance e disponibilidade sob diferentes cargas.

---

### Princípios fundamentais de confiabilidade:

- ✅ **Recuperação automática de falhas (Self-Healing Systems)**

  - A aplicação deve ser capaz de detectar e se recuperar de falhas sem intervenção manual.
  - Use serviços gerenciados da AWS (como ALB, Auto Scaling, S3, RDS Multi-AZ, etc.)
  - Monitore constantemente com CloudWatch e ative alarmes com respostas automáticas (SNS, Lambda)

- ✅ **Teste dos procedimentos de recuperação com frequência**

  - Faça simulações de falhas reais: desligue servidores, corrompa instâncias, mate bancos temporariamente
  - Tenha backups automáticos e testados (RDS snapshots, S3 versionamento, etc.)
  - Realize **DR drills (Disaster Recovery drills)** para saber o tempo de recuperação real

- ✅ **Escalonamento horizontal para alta disponibilidade**

  - Em vez de uma máquina muito potente, use várias menores em paralelo
  - Aumenta a tolerância a falhas e facilita upgrades
  - Use **Auto Scaling Groups** e **Load Balancers** para distribuir a carga

- ✅ **Pare de adivinhar capacidade (Capacity Planning)**

  - Faça medições e simulações com ferramentas como AWS Compute Optimizer, CloudWatch Metrics, Load Tests
  - Use provisionamento automático com Auto Scaling baseado em métrica (CPU, requests, etc.)
  - Evite over-provisioning (excesso de recursos sem necessidade) e under-provisioning (recursos insuficientes)

- ✅ **Gerencie mudanças automaticamente**
  - Use **Infrastructure as Code (IaC)** com Terraform, AWS CDK ou CloudFormation
  - Faça deploys automatizados com pipelines e etapas de rollback
  - Documente, teste e monitore mudanças em produção com **canary releases** e **blue/green deployments**

---

### Exemplos de boas práticas na AWS:

- ✅ **Amazon RDS Multi-AZ** para garantir replicação automática do banco de dados
- ✅ **Auto Scaling Groups** com políticas de scaling automáticas
- ✅ **Elastic Load Balancer** distribuindo tráfego entre zonas de disponibilidade
- ✅ **Amazon S3 com versionamento e replicação entre regiões**
- ✅ **CloudWatch + Lambda para triggers de recuperação**
- ✅ **Chaos Engineering com ferramentas como AWS Fault Injection Simulator**

---

### Benefícios de aplicar esse pilar:

- Minimiza tempo de inatividade
- Reduz o impacto de falhas em produção
- Aumenta a confiança do time de produto e do usuário final
- Suporte melhor a picos de tráfego inesperado
- Processos de recuperação mais rápidos e eficazes

---

### Resumo

Confiabilidade não é apenas “estar no ar”, mas sim **garantir desempenho, escalabilidade e resiliência**, mesmo em ambientes dinâmicos e sob pressão. No contexto da nuvem, a AWS oferece várias ferramentas que, quando bem utilizadas, tornam sua aplicação **altamente disponível, testável e resiliente**.

Projetar para falhas e automatizar respostas são pilares fundamentais de um sistema moderno e confiável.

---

### Referências:

- [Pilar de Confiabilidade - AWS Docs](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html)
- [AWS Well-Architected Framework](https://aws.amazon.com/pt/architecture/well-architected/)
- [AWS Fault Injection Simulator](https://aws.amazon.com/fis/)
