# Publish - Subscribe

**Publish - Subscribe (Pub/Sub)** é um padrão de arquitetura de comunicação **assíncrona** entre sistemas, ideal para aplicações desacopladas e escaláveis.

Nesse modelo, um **publisher (publicador)** envia mensagens para um **tópico**, e múltiplos **subscribers (assinantes)** consomem essas mensagens.

Em vez de um sistema (como o Sistema A) ter que conhecer e enviar diretamente mensagens para todos os sistemas interessados em uma "compra aprovada", ele simplesmente **publica** esse evento em um **tópico**. Os sistemas que estão interessados em receber esse tipo de informação se **inscrevem (subscribe)** no tópico e recebem os eventos automaticamente.

## Como funciona

- ✅ **Tópico (channel)**: Um ponto de encontro virtual onde mensagens são publicadas.
- ✅ **Publisher**: Emite a mensagem para o tópico (ex: "compra aprovada").
- ✅ **Subscribers**: Sistemas ou serviços que se inscrevem no tópico para receber as mensagens.
- ✅ **Broker de mensagens**: Responsável por receber, armazenar temporariamente e distribuir as mensagens. Exemplos: Kafka, RabbitMQ, Google Pub/Sub, Amazon SNS.

## Vantagens

- ✅ **Desacoplamento**: Publisher não precisa saber quem vai consumir. Isso reduz dependências entre sistemas.
- ✅ **Escalabilidade**: Fácil de adicionar novos consumidores sem alterar o produtor.
- ✅ **Distribuição de carga**: Pode haver múltiplos consumidores processando mensagens em paralelo.

## Exemplo prático

- ✅ Sistema A aprova uma compra e publica no tópico `compra_aprovada`.
- ✅ Sistema de entrega, sistema de notificação e sistema de análise de dados estão inscritos nesse tópico.
- ✅ Todos recebem o evento automaticamente e processam de acordo com sua responsabilidade.

## Cuidados

- ✅ Garantir **ordem das mensagens**, se necessário.
- ✅ Tratar **reentrega de mensagens** (em caso de falha).
- ✅ Monitorar filas para evitar gargalos.

---

**Pub/Sub** é um padrão essencial para construir sistemas **reativos, escaláveis e desacoplados**. Ele melhora a comunicação entre serviços ao permitir que um evento publicado seja **automaticamente distribuído** para todos os interessados, sem a necessidade de conhecer seus destinos diretamente.

> Ferramentas comuns: Kafka, RabbitMQ, Redis Pub/Sub, AWS SNS/SQS, Google Pub/Sub.
