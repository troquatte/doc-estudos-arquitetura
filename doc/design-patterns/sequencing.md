# Sequencing

---

**Sequencing** é uma abordagem usada para garantir a geração de identificadores únicos em sistemas distribuídos.

Em arquiteturas com múltiplos microsserviços ou instâncias que criam dados simultaneamente, pode surgir o problema de geração de **IDs duplicados**, o que pode causar corrupção de dados ou inconsistência entre sistemas.

Para evitar esse tipo de problema, empresas como o Mercado Livre adotaram uma abordagem centralizada através de um **serviço de sequencing**.

Esse microsserviço é responsável exclusivamente por gerar IDs únicos para qualquer operação que necessite de persistência. Qualquer outro serviço que precise criar um novo registro faz uma requisição ao serviço de sequencing e recebe um ID exclusivo em resposta.

## Problema

- ✅ Geração de múltiplos IDs simultâneos pode causar duplicidade.
- ✅ Sistemas distribuídos dificultam controle central de ID.

## Solução

- ✅ Criar um microsserviço único responsável por gerar todos os IDs (sequencer).
- ✅ Toda operação de gravação no sistema passa primeiro pelo sequencer.

## Vantagens

- ✅ Evita colisão de IDs em sistemas distribuídos.
- ✅ Mantém consistência e integridade dos dados.
- ✅ Possibilita controle e rastreabilidade de geração de IDs.

## Desafios

- ✅ Pode se tornar um ponto único de falha se não for bem escalado.
- ✅ Deve garantir alta disponibilidade e performance, pois será muito requisitado.
- ✅ Pode ser implementado com filas, bancos otimizados ou serviços como Redis, Kafka ou banco de dados com auto-incremento distribuído.

## Exemplo real

- ✅ Mercado Livre criou um serviço específico para sequencing para resolver esse tipo de problema com alto volume de requisições.

---

O **Sequencing** é uma estratégia adotada para garantir a geração de IDs únicos em ambientes distribuídos. Ele centraliza a responsabilidade em um microsserviço que fornece identificadores únicos para qualquer operação que precise persistir dados. Isso evita colisões, mantém a integridade da base de dados e é essencial para sistemas com múltiplos pontos de escrita concorrentes.
