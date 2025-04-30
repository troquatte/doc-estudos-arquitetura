# Distributed Locking (Lock Distribuído)

---

**Distributed locking**, ou bloqueio distribuído, é uma técnica usada para garantir que apenas uma instância de um sistema distribuído possa acessar um recurso crítico por vez.

Isso é essencial em cenários com alta concorrência, como sistemas de **e-commerce** ou **vendas de ingressos**, onde múltiplas requisições simultâneas podem tentar acessar ou modificar o mesmo recurso - por exemplo, a última unidade de um produto ou os últimos ingressos disponíveis para um evento.

Sem um mecanismo de controle, pode ocorrer de duas pessoas "comprarem" o mesmo item ao mesmo tempo, gerando inconsistências graves. O lock distribuído atua como uma trava temporária, impedindo que outras transações acessem aquele recurso até que a operação atual seja finalizada.

## Problema

- ✅ Concorrência em ambientes distribuídos, como múltiplas pessoas tentando comprar o mesmo produto.

## Solução

- ✅ Uso de locking distribuído para garantir que apenas uma transação acesse o recurso por vez.

## Benefícios

- ✅ Consistência de dados
- ✅ Evita múltiplas atualizações simultâneas em um mesmo dado.
- ✅ Contenção de recursos
- ✅ Controla o acesso a recursos limitados.
- ✅ Evita deadlocks
- ✅ Se bem implementado, reduz a chance de travamentos.
- ✅ Eficiência
- ✅ Melhora a estabilidade e previsibilidade do sistema.

## Ferramentas comuns

- ✅ **Apache Zookeeper**
- ✅ **ETCD**
- ✅ **Redis**
- ✅ **Consul**

## Atenção

- ✅ Cada ferramenta possui vantagens e desvantagens. É importante avaliar qual se adapta melhor ao contexto da sua aplicação.

---

**Distributed locking** é uma técnica usada para controlar o acesso concorrente a recursos compartilhados em sistemas distribuídos, como em compras simultâneas em plataformas de e-commerce ou venda de ingressos.

Ele garante que apenas uma operação acesse um recurso por vez, mantendo a integridade dos dados e evitando comportamentos indesejados. Ferramentas como Redis, Zookeeper, ETCD e Consul são amplamente utilizadas para implementar esse tipo de controle.

A escolha da tecnologia adequada depende do cenário de uso, requisitos de consistência e complexidade da aplicação.
