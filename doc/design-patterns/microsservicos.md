# Microsserviços

---

São sistemas que possuem responsabilidades específicas e podem se comunicar entre si, mas idealmente devem ser desacoplados para garantir maior independência e flexibilidade.

Uma atenção especial é necessária para evitar que microsserviços dependam diretamente uns dos outros ou compartilhem o mesmo banco de dados, o que pode gerar acoplamento e comprometer a autonomia dos serviços.

A utilização de padrões de comunicação por eventos, através de "brokers", é recomendada para reduzir a dependência entre os sistemas.

A principal motivação para adotar microsserviços é organizacional: equipes diferentes podem trabalhar em projetos distintos sem quebrar toda a aplicação.

Microsserviços permitem escalabilidade independente, separação clara de responsabilidades e até mesmo o uso de diferentes tecnologias em cada serviço, embora isso também aumente a complexidade.

É importante lembrar que microsserviços exigem uma maturidade organizacional e técnica maior, e que seu uso indiscriminado pode gerar problemas de observabilidade, troubleshooting e deployment.

## Microsserviços

- ✅ Sistemas com responsabilidades específicas.

## Cuidado com acoplamento

- ✅ Microsserviços não devem depender fortemente uns dos outros ou compartilhar bancos de dados.

## Comunicação por eventos

- ✅ Uso de brokers para reduzir dependências.

## Principal motivação

- ✅ Organização de times e independência de projetos.

## Escalabilidade

- ✅ Escala individualmente o microsserviço necessário.

## Separação de responsabilidades

- ✅ Cada aplicação trata de um assunto específico.

## Diferentes tecnologias

- ✅ Possibilidade de usar stacks distintas por serviço (não recomendado em excesso).

## Baixo acoplamento

- ✅ Sistemas independentes facilitam evolução sem grandes impactos.

## Complexidade

- ✅ Microsserviços aumentam a necessidade de maturidade organizacional e técnica
- ✅ Maturidade dos times
- ✅ Gerenciamento de deployments separados
- ✅ Observabilidade aprimorada (e mais cara)
- ✅ Troubleshooting mais difícil

## Microsserviços não são bala de prata

- ✅ Não devem ser usados em qualquer situação.

---

**Microsserviços** são uma arquitetura que divide sistemas em pequenas aplicações independentes, cada uma com uma responsabilidade clara.

Essa abordagem favorece a organização de equipes e a escalabilidade individual de componentes, mas também exige maturidade organizacional, uma estrutura de observabilidade robusta e processos de troubleshooting bem definidos.

Cuidados devem ser tomados para evitar acoplamento, principalmente através de comunicação indireta por eventos usando brokers.

Embora microsserviços ofereçam muitos benefícios, como baixo acoplamento e flexibilidade tecnológica, eles trazem complexidades que nem todas as organizações estão prontas para enfrentar.

Portanto, seu uso deve ser bem avaliado conforme o contexto do projeto e da empresa.

## Leitura recomendada

- ✅ [Martin Fowler - Microservices](https://martinfowler.com/articles/microservices.html)
