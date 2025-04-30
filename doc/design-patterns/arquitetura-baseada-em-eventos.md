# Arquitetura Baseada em Eventos

---

A **arquitetura baseada em eventos** se baseia em algo que _aconteceu_ no passado.

Cada evento é um registro de uma mudança de estado no sistema — como "pedido aprovado", "produto comprado", "item cadastrado", etc. Ao invés de serviços chamarem diretamente uns aos outros, eles **emitem eventos** e outros serviços reagem a esses eventos, promovendo **baixo acoplamento e alta escalabilidade**.

Esse tipo de arquitetura é bastante utilizado em sistemas distribuídos e de alta concorrência, como e- ✅ commerces e plataformas financeiras, onde diversos microsserviços precisam reagir a uma mesma ação de forma independente e assíncrona.

## Event Notification

- ✅ Apenas notifica que algo aconteceu.
- ✅ Exemplo: `{ id: 1, status: "aprovado" }`
- ✅ É leve e ideal quando o consumidor pode buscar os dados depois, se necessário.

## Event Carried State Transfer

- ✅ O evento leva o estado completo da entidade.
- ✅ Exemplo: `{ id: 1, status: "aprovado", produto: "geladeira", especificações: {...} }`
- ✅ Útil quando o consumidor precisa de todos os dados e o produtor quer evitar múltiplas chamadas.

## Event Sourcing

- ✅ Ao invés de salvar apenas o estado final, salvamos todos os eventos que levaram até ele.
- ✅ Isso permite **reconstruir o estado** de qualquer entidade em qualquer momento no tempo.
- ✅ Útil para auditoria, histórico e reprocessamento.

---

## Coreografia vs Orquestração

### Coreografia

- ✅ Cada serviço escuta eventos e age de forma autônoma.
- ✅ Não há um "serviço central" controlando o fluxo.
- ✅ Promove **baixo acoplamento** e maior flexibilidade.
- ✅ Exemplo: Serviço de pagamento emite um evento "Pagamento aprovado", e o serviço de entrega ouve e age.

### Orquestração

- ✅ Um serviço central (orquestrador) coordena o fluxo e chama os outros serviços.
- ✅ Dá mais controle e previsibilidade ao fluxo de processos.
- ✅ Útil em cenários com lógica de negócio complexa.
- ✅ Exemplo: Serviço de orquestração chama o de pagamento, espera a resposta, e depois chama o de entrega.

### Considerações

- ✅ Nem sempre você precisa enviar todos os dados no evento — pense se um **event notification** já resolve.
- ✅ Sistemas baseados em eventos **exigem atenção com consistência eventual**.
- ✅ Mensagerias como **Kafka, RabbitMQ, SQS** são comuns nesse modelo.

---

A **arquitetura baseada em eventos** permite criar sistemas reativos, escaláveis e desacoplados. Ela é fundamentada na emissão e consumo de eventos para reagir a mudanças de estado. Com os padrões de **notificação, state transfer** e **event sourcing**, além das abordagens de **coreografia** e **orquestração**, é possível montar fluxos robustos e flexíveis.

✅ **Leitura recomendada**: [Martin Fowler - ✅ Event- ✅ Driven Architecture](https://martinfowler.com/articles/201701- ✅ event- ✅ driven.html)
