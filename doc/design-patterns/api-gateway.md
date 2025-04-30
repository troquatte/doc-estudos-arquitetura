# API Gateway

---

O **API Gateway** atua como um **ponto central de entrada** para todas as requisições feitas a um conjunto de microsserviços ou sistemas. Ele é responsável por **orquestrar, rotear, filtrar e proteger** as chamadas feitas para os serviços da aplicação.

Em vez de o cliente se comunicar diretamente com cada microsserviço, ele se comunica apenas com o API Gateway, que então direciona a requisição para o serviço correto.

Serviços como o **AWS API Gateway** ou ferramentas open source como o **Kong** são soluções robustas para implementar esse padrão. Elas trazem diversas funcionalidades prontas para produção e facilitam a gestão de múltiplas APIs em sistemas complexos.

## Centralização

- ✅ Todas as requisições passam por um único ponto (API Gateway).

## Roteamento

- ✅ Direciona cada requisição ao microsserviço correto com base em regras.

## Autenticação e Autorização

- ✅ Pode validar tokens JWT, sessões, chaves de API e autenticar o usuário antes de permitir o acesso aos serviços.

## Transformação de dados

- ✅ Pode converter formatos de requisição e resposta (ex.: XML → JSON).

## Throttling

- ✅ Controla a taxa de requisições para evitar sobrecarga nos serviços.

## Rate Limiting

- ✅ Define limites de acesso por usuário, grupo ou rota específica (ex.: 100 requisições/minuto).

## Observabilidade

- ✅ Facilita logging, métricas e rastreamento centralizado de todas as requisições.

---

O **API Gateway** é uma camada intermediária entre o cliente e os microsserviços, oferecendo funcionalidades como roteamento, autenticação, controle de tráfego e transformação de dados. Ele simplifica a arquitetura, melhora a segurança e ajuda a escalar o sistema com controle mais refinado. Ferramentas como **Kong** ou **AWS API Gateway** são muito utilizadas em arquiteturas modernas baseadas em microsserviços.

✅ **Leitura recomendada**: [Documentação oficial do Kong](https://docs.konghq.com/)
