# Secret Management

---

**Secret Management** é a prática de armazenar, proteger, acessar e rotacionar credenciais sensíveis como senhas, tokens de API, chaves de acesso, certificados e outros dados confidenciais de forma centralizada e segura.

Em ambientes modernos, onde microserviços, automações e múltiplos ambientes convivem, é essencial evitar que segredos "circulem livremente" entre times, canais como Slack ou Discord, ou fiquem hardcoded no código-fonte.

A má gestão de segredos pode resultar em vazamentos de dados, falhas de segurança e comprometer a infraestrutura inteira da aplicação. Para mitigar esses riscos, utilizam-se ferramentas e serviços especializados que permitem:

- ✅ **Armazenamento seguro**
- ✅ **Controle de acesso granular**
- ✅ **Rotacionamento automático**
- ✅ **Recuperação segura em tempo de execução**

## Problemas comuns

- ✅ Segredos compartilhados manualmente em chats (Slack, Discord).
- ✅ Armazenamento hardcoded no código.
- ✅ Falta de processos de rotacionamento.

## Boas práticas

- ✅ Armazenar segredos em cofres gerenciados.
- ✅ Evitar que devs e apps tenham acesso direto a dados sensíveis.
- ✅ Automatizar o ciclo de vida dos secrets.

## Ferramentas populares

- ✅ **Hashicorp Vault**: solução robusta para armazenamento, acesso e políticas de controle de segredos.

## AWS Secrets Manager

- ✅Armazenamento seguro de segredos.
- ✅Rotacionamento automático (por exemplo, senhas de banco RDS).
- ✅SDK para leitura segura em tempo de execução.

## Benefícios

- ✅ Redução de riscos de vazamento.
- ✅ Automação de segurança.
- ✅ Conformidade com normas e boas práticas.

---

**Secret Management** é uma prática essencial para proteger credenciais sensíveis dentro de aplicações modernas.

Em vez de compartilhar manualmente ou armazenar no código, os segredos devem ser gerenciados por ferramentas como Hashicorp Vault ou AWS Secrets Manager, que permitem armazenamento seguro, rotacionamento automático e recuperação programática.

Isso evita riscos, melhora a segurança da infraestrutura e traz mais controle sobre quem pode acessar o quê e quando.
