# Sidcards Applications

**Sidcards applications** são aplicações auxiliares que ficam "coladas" ou complementando uma aplicação principal. Elas servem para realizar tarefas específicas, como monitoramento, coleta de dados, ou integração com outros serviços, sem interferir diretamente na lógica principal da aplicação.

Essas aplicações podem atuar como **sidecar containers** ou módulos que rodam em paralelo à aplicação principal, oferecendo **funcionalidades complementares** e **adicionais**. Elas são frequentemente usadas em ambientes **microservices** ou **containers**, onde a aplicação principal foca em uma tarefa específica e o sidecar cuida de outros aspectos, como segurança ou logging.

## Exemplos de uso

- ✅ **Coletor de logs**: Um sidecar pode ser responsável por coletar logs da aplicação principal e enviá-los para um sistema de monitoramento externo, como ELK Stack ou Splunk.
- ✅ **Autenticação e segurança**: Um sidecar pode ser utilizado para aplicar **MTLS (Mutual TLS)**, garantindo que a comunicação entre a aplicação e outros serviços seja segura, sem modificar diretamente a aplicação principal.
- ✅ **Proxy**: Um sidecar pode atuar como um proxy reverso, realizando tarefas de roteamento de tráfego ou balanceamento de carga para a aplicação principal.

## Características

- ✅ **Independente**: O sidecar pode ser independente, mas trabalha sempre em conjunto com a aplicação principal.
- ✅ **Complementar**: Ao invés de adicionar funcionalidades diretamente à aplicação, o sidecar adiciona recursos sem alterar seu código.
- ✅ **Escalável**: Sidecars podem ser facilmente escalados em ambientes distribuídos, garantindo que cada instância da aplicação tenha suas funcionalidades auxiliares.
- ✅ **Isolado**: O sidecar não interfere na lógica principal da aplicação, mas pode ser configurado para trabalhar de maneira eficiente com ela.

## Vantagens

- ✅ **Facilidade de gerenciamento**: O sidecar pode ser atualizado ou gerenciado de forma independente da aplicação principal.
- ✅ **Reutilização**: A mesma aplicação auxiliar (sidecar) pode ser usada para diversas instâncias de aplicações diferentes, facilitando a manutenção e escalabilidade.
- ✅ **Segurança aprimorada**: Sidecars podem ser configurados para adicionar camadas extras de segurança, como encriptação ou autenticação, sem modificar o código da aplicação principal.

## Desafios

- ✅ **Complexidade operacional**: Embora o sidecar seja isolado, ele pode adicionar complexidade à arquitetura, especialmente em grandes sistemas.
- ✅ **Sobrecarga de recursos**: Se mal dimensionado, o uso de sidecars pode consumir muitos recursos de CPU ou memória.

---

**Sidcards applications** são soluções auxiliares que complementam a aplicação principal, oferecendo funcionalidades como logging, segurança e monitoramento, sem interferir diretamente na lógica da aplicação. Eles são uma forma eficaz de adicionar capacidades extras de forma modular e escalável, especialmente em arquiteturas de microserviços.
