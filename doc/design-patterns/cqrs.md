# CQRS (Command Query Responsibility Segregation)

---

**CQRS** (Command Query Responsibility Segregation) é um padrão arquitetural que separa as operações de leitura (queries) e escrita (commands) de uma aplicação em modelos distintos.

Em vez de uma única estrutura tratar tanto mutações quanto consultas, o CQRS propõe duas pilhas separadas: uma para comandos, que alteram o estado do sistema e não retornam dados (apenas possíveis erros), e outra para consultas, que apenas leem dados e retornam resultados.

Essa separação permite otimizar e evoluir de forma independente os fluxos de leitura e escrita, aumentando a escalabilidade, performance e a clareza do sistema.

A arquitetura típica de CQRS inclui uma camada de apresentação, uma pilha de comandos (envolvendo a aplicação e o domínio), uma pilha de consultas (envolvendo principalmente a aplicação) e a camada de infraestrutura.

## CQRS

- ✅ Segregação de responsabilidades entre comandos e consultas.

## Command Stack

- ✅ Trata mudanças e mutações de estado.
- ✅ Executa o comando sem retornar dados, apenas erros.
- ✅ Envolve camadas de Application e Domain.

## Query Stack

- ✅ Realiza apenas buscas e retornos de dados.
- ✅ Envolve a camada de Application.

## Infraestrutura

- ✅ Suporte para operações de persistência e comunicação.

## Benefícios

- ✅ Melhor escalabilidade e performance.
- ✅ Evolução independente de leitura e escrita.
- ✅ Maior clareza de responsabilidades.

---

O padrão **CQRS** propõe a separação de operações de comando (escrita/mutação) e de consulta (leitura) em uma aplicação.

No **Command Stack**, são realizadas as mudanças no estado do sistema, sem retornos de dados além de possíveis erros. Já no **Query Stack**, apenas leituras de informações são feitas. Essa divisão facilita a escalabilidade, permite otimizar leituras e escritas separadamente e melhora a organização do sistema.

A arquitetura típica de CQRS é composta pelas camadas de apresentação, pilhas de comando e consulta, e infraestrutura. Embora poderoso, CQRS deve ser aplicado quando as necessidades de escalabilidade e complexidade justificarem a sua implementação.

✅ **Leitura recomendada**: [Documento sobre CQRS](https://cqrs.wordpress.com/wp-content/uploads/2010/11/cqrs_documents.pdf)
