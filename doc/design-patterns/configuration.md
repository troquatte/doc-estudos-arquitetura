# Configuration

---

**Configuration** (ou gerenciamento de configuração) é a prática de separar parâmetros e valores sensíveis do código da aplicação, permitindo que mudanças possam ser feitas **em tempo real**, sem a necessidade de reiniciar ou redeployar o sistema.

Isso é fundamental em ambientes modernos onde aplicações precisam ser dinâmicas, seguras e responsivas a mudanças de infraestrutura, como alteração de senhas, tokens, configurações de email ou endpoints de serviços externos.

A ideia é centralizar e carregar essas configurações por meio de um serviço ou endpoint externo, que disponibiliza os valores necessários para a aplicação funcionar corretamente.

Isso permite que o sistema se adapte em tempo de execução a novas configurações, melhorando a **manutenibilidade**, **escalabilidade** e **segurança** da aplicação.

## Objetivo

- ✅ Alterar comportamentos da aplicação sem recompilar, reiniciar ou redeployar.

## Exemplos de uso

- ✅Mudança de senha do banco de dados.
- ✅Atualização de credenciais de email.
- ✅Troca de endpoints de APIs externas.

## Como funciona

- ✅Aplicação consome configurações de um endpoint externo.
- ✅Essas configurações são recarregadas dinamicamente.
- ✅O sistema se reajusta com base nesses novos parâmetros.

## Vantagens

- ✅Evita downtime por alterações simples.
- ✅Facilita ambientes multiambiente (dev, staging, prod).
- ✅Aumenta a segurança e controle de versões de configuração.

## Ferramentas comuns

- ✅ Spring Cloud Config, Consul, etcd, AWS Parameter Store, Kubernetes ConfigMap.

---

**Configuration** é o processo de externalizar e dinamizar os parâmetros de uma aplicação para que possam ser alterados sem parar o sistema. Ao utilizar serviços externos de configuração, como endpoints que expõem variáveis ou arquivos monitorados, a aplicação se torna mais flexível e resiliente a mudanças de ambiente, senhas ou integrações.

Isso evita interrupções, melhora a manutenção e permite ajustes em tempo real sem necessidade de deploys manuais.
