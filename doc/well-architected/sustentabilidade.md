# Sustentabilidade — AWS Well-Architected Framework

O pilar de **Sustentabilidade** foca na **redução dos impactos ambientais das cargas de trabalho na nuvem**, maximizando a eficiência energética e minimizando o uso desnecessário de recursos. Esse pilar é essencial não apenas para reduzir custos operacionais, mas também para alinhar a tecnologia às **práticas ambientais, sociais e de governança (ESG)**.

Sustentabilidade vai além de "apagar luzes" ou "usar menos servidores" — trata-se de **tomar decisões conscientes sobre arquitetura, uso de recursos e eficiência energética**, visando o longo prazo, o planeta e a reputação da empresa.

---

### O que significa ser sustentável na nuvem?

- ✅ **Executar cargas de trabalho com menor consumo energético**.
- ✅ **Aproveitar ao máximo os recursos provisionados**, evitando desperdícios.
- ✅ **Planejar com consciência**, usando tecnologias mais recentes, otimizadas e com menor impacto.
- ✅ **Desenhar sistemas eficientes**, que escalam corretamente e utilizam hardware moderno e energeticamente eficiente.

---

### Princípios

- ✅ **Entenda seus impactos**

  - Meça a pegada de carbono das suas cargas de trabalho e identifique quais recursos mais consomem energia.
  - Use ferramentas como o [AWS Customer Carbon Footprint Tool](https://aws.amazon.com/aws-cost-management/aws-customer-carbon-footprint-tool/) para rastrear e monitorar o impacto ambiental do seu uso na nuvem.
  - Compreenda como escolhas de arquitetura, regiões e serviços influenciam o consumo energético.

- ✅ **Estabeleça metas de sustentabilidade**

  - Defina KPIs relacionados à sustentabilidade, como **redução de consumo por requisição** ou **uso de energia por transação**.
  - Estabeleça objetivos claros como “reduzir em 30% a energia usada por instância” ou “migrar 50% das cargas para serviços gerenciados até o final do ano”.
  - Isso ajuda a incorporar sustentabilidade como um objetivo contínuo, e não apenas uma preocupação pontual.

- ✅ **Maximize a utilização**

  - Evite instâncias ociosas, subutilizadas ou superdimensionadas.
  - Implemente **auto scaling**, uso eficiente de containers e workloads event-driven com **serverless**.
  - Compartilhe infraestrutura entre equipes ou serviços sempre que possível (multi-tenant).

- ✅ **Antecipe e adote novas ofertas de hardware e software mais eficientes**

  - Acompanhe atualizações de instâncias EC2, como os processadores Graviton, que oferecem maior eficiência energética.
  - Atualize bibliotecas e aplicações para versões mais otimizadas, aproveitando melhorias de performance com menor consumo.
  - Avalie constantemente se existe uma forma mais leve e moderna de executar a mesma tarefa.

- ✅ **Use serviços gerenciados**
  - Serviços como Amazon S3, DynamoDB, Fargate e Lambda são **otimizados pela AWS para rodar com eficiência máxima**, com menor impacto ambiental comparado a soluções autogerenciadas.
  - Isso reduz o overhead operacional e o consumo desnecessário de recursos subutilizados.
  - Os data centers da AWS também usam **infraestrutura alimentada por energia renovável**, o que ajuda a reduzir o impacto total.

---

### Dicas práticas para maior sustentabilidade

- ✅ Evite usar ambientes de desenvolvimento e testes 24/7 — desligue quando não estiver em uso.
- ✅ Faça **rightsizing** regularmente (ajuste de tamanho das instâncias com base no uso).
- ✅ Prefira regiões da AWS com melhor matriz energética (ex: us-east-1, eu-west-1).
- ✅ Otimize pipelines de CI/CD para evitar execuções desnecessárias.
- ✅ Use cache, compressão e técnicas de otimização de rede para reduzir consumo.

---

### Benefícios

- ✅ Redução direta de custos operacionais.
- ✅ Menor impacto ambiental (pegada de carbono).
- ✅ Melhora na reputação da empresa (práticas ESG).
- ✅ Eficiência e modernização contínua dos sistemas.
- ✅ Conformidade com exigências legais e de mercado.

---

### Referências e Recursos

- [AWS Well-Architected Sustainability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/sustainability-pillar/)
- [Customer Carbon Footprint Tool](https://aws.amazon.com/aws-cost-management/aws-customer-carbon-footprint-tool/)
- [AWS Graviton Processors](https://aws.amazon.com/ec2/graviton/)
