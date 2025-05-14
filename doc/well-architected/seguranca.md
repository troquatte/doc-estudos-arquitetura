# Segurança (Security) — Pilar do AWS Well-Architected Framework

O pilar de **Segurança** foca em proteger dados, sistemas e ativos usando os recursos oferecidos pela nuvem. Isso deve ser feito de forma **proativa**, escalável e automatizada, melhorando a postura de segurança da organização sem comprometer agilidade.

A segurança precisa ser **implementada em todas as camadas**, com **identidade forte, controle de acesso, criptografia, rastreabilidade e preparação para incidentes**.

---

### Objetivo

Ajudar a construir workloads seguras na nuvem AWS, identificando riscos e aplicando práticas para **reduzir exposições**, **limitar acessos** e **aumentar a visibilidade** sobre atividades suspeitas.

---

### Princípios fundamentais de segurança na nuvem:

- ✅ **Implemente uma base forte de identidade (Identity & Access Management - IAM)**

  - Use autenticação forte (MFA, federada, etc.)
  - Crie **permissões mínimas necessárias** (Least Privilege)
  - Separe funções: devs, analistas, ops, etc. com acessos distintos
  - Evite usuários raiz ou com privilégios amplos no dia a dia

- ✅ **Controle e proteja o acesso aos dados e sistemas**

  - Defina políticas claras de acesso
  - Restrinja ao máximo o que cada papel pode ver ou modificar
  - Use roles, groups e policies para gerenciar permissões de forma granular

- ✅ **Rastreabilidade (Traceability)**

  - Ative **logs, auditorias e monitoramento de eventos** com ferramentas como AWS CloudTrail, AWS Config e Amazon CloudWatch
  - Tenha visibilidade de quem fez o quê, quando, de onde e com qual finalidade
  - Guarde logs de forma segura e imutável

- ✅ **Aplique segurança em todas as camadas**

  - Crie defesas em profundidade (Defesa por camadas):
    - Segurança de rede (SG, NACLs, VPC, WAF)
    - Segurança de instância (EC2, EKS, Lambda)
    - Segurança de aplicação (API Gateway, AppConfig)
    - Segurança de dados (S3, RDS, etc.)

- ✅ **Proteja os dados em trânsito e em repouso**

  - Use criptografia com certificados válidos (TLS 1.2 ou superior)
  - Criptografe dados em descanso usando KMS (AWS Key Management Service)
  - Aplique criptografia também em backups, buckets S3, bancos, etc.

- ✅ **Mantenha as pessoas longe dos dados**

  - Evite acesso direto a ambientes de produção
  - Desenvolvedores e analistas devem ter **ambientes separados e mascarados**
  - Use pipelines para promover mudanças entre ambientes
  - Implemente data masking, tokenização e segregação de acesso

- ✅ **Prepare-se para eventos de segurança (Incident Response)**
  - Desenvolva e teste um plano de resposta a incidentes
  - Use automações para isolar e mitigar problemas (Ex: Lambda + SNS)
  - Revise periodicamente as políticas e lições aprendidas
  - Treine sua equipe para saber como reagir diante de um vazamento ou ataque

---

### Ferramentas da AWS que apoiam a segurança:

- ✅ **AWS IAM / IAM Identity Center** – Controle de identidade e acesso
- ✅ **AWS KMS** – Gerenciamento de chaves de criptografia
- ✅ **AWS CloudTrail** – Rastreabilidade e auditoria de ações
- ✅ **Amazon Macie** – Identificação de dados sensíveis
- ✅ **AWS Shield / AWS WAF** – Proteção contra ataques (DDoS, XSS, etc.)
- ✅ **Amazon GuardDuty** – Detecção de ameaças
- ✅ **AWS Config** – Conformidade e rastreamento de mudanças
- ✅ **AWS Secrets Manager / Parameter Store** – Armazenamento seguro de segredos
- ✅ **Security Hub** – Visão centralizada do estado de segurança na AWS

---

### Benefícios de aplicar esse pilar:

- ✅ Redução do risco de vazamentos e acessos indevidos
- ✅ Melhor governança e compliance (LGPD, ISO, SOC, etc.)
- ✅ Capacidade de identificar ameaças em tempo real
- ✅ Auditoria e rastreamento facilitados
- ✅ Preparação para lidar com crises de segurança

---

### Resumo

Segurança não é algo que se “coloca depois” — ela precisa ser **arquitetada desde o início**, **monitorada continuamente** e **evoluída com o tempo**. O pilar de segurança do Well-Architected Framework ajuda equipes a tomarem decisões conscientes e sistematizadas para proteger seus ambientes em nuvem.

A segurança é um processo constante — e, na nuvem, você tem ferramentas poderosas para implementá-la de forma automatizada e escalável.

---

### Referências:

- [Pilar de Segurança - AWS Docs](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)
- [AWS Well-Architected Framework](https://aws.amazon.com/pt/architecture/well-architected/)
- [Melhores práticas de segurança na AWS](https://aws.amazon.com/pt/security/)
