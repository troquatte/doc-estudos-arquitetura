# Circuit Breaker

---

**Circuit Breaker** é um padrão de resiliência em sistemas distribuídos que funciona de forma análoga a um disjuntor elétrico: quando detecta uma falha contínua ou lentidão em uma dependência (como outro microserviço), ele "desliga" temporariamente essa comunicação para evitar sobrecarregar o sistema.

Esse padrão é essencial quando lidamos com microsserviços, pois um serviço lento é pior do que um serviço fora do ar. Um serviço degradado pode impactar em cascata outros que dependem dele.

O Circuit Breaker entra nesse cenário para isolar falhas, proteger a aplicação e permitir uma recuperação gradual do serviço com falha.

O ideal é que a lógica de Circuit Breaker seja aplicada fora do código-fonte principal, como via proxy ou service mesh, para evitar acoplamentos excessivos e erros difíceis de depurar.

## Problema resolvido

- ✅ MS1 depende de MS2; se MS2 estiver lento, MS1 também fica lento.
- ✅ Um serviço lento é pior que um serviço inativo.

## Como funciona

- ✅ Monitora chamadas entre serviços.
- ✅ Se um serviço apresenta lentidão ou falha constante, o circuito se “abre”.
- ✅ Enquanto o circuito está aberto, as chamadas ao serviço problemático são bloqueadas imediatamente.
- ✅ Depois de um tempo, entra em modo **meio aberto**, onde faz chamadas esporádicas para verificar se o serviço se recuperou.
- ✅ Se o serviço responder normalmente, o circuito é **fechado** e tudo volta ao normal.

## Estados do Circuit Breaker

- ✅ **Fechado (Closed)**: tudo funcionando normalmente.
- ✅ **Aberto (Open)**: falhas constantes detectadas, chamadas bloqueadas.
- ✅ **Meio-aberto (Half-Open)**: tentativas limitadas para checar se o serviço se recuperou.

## Boas práticas

- ✅ Implementar circuit breaker em nível de infraestrutura (ex.: proxies, service mesh) e não apenas via código.
- ✅ Definir thresholds claros para falhas e tempo de espera antes de reabrir o circuito.

---

O **Circuit Breaker** é um padrão essencial para resiliência em microsserviços. Ele isola falhas, evita que serviços lentos impactem toda a cadeia e permite a recuperação gradual.

Ao monitorar o estado de dependências, o circuit breaker decide quando interromper e quando retomar o tráfego para proteger o sistema como um todo. Idealmente, essa lógica deve ser implementada fora do código, por meio de proxies ou service mesh.
