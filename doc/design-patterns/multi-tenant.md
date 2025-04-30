# Multi-Tenant

---

Multi-Tenant é uma abordagem de arquitetura onde uma mesma aplicação é usada por vários clientes (empresas) de forma isolada e segura, comum em modelos white label e SaaS.

- ✅ Uma única aplicação pode atender vários clientes.
- ✅ Estratégias: bancos de dados separados, tabelas distintas ou dados relacionados no mesmo banco.
- ✅ Escolha depende do porte dos clientes e da necessidade de governança.
- ✅ Importante pensar na estratégia desde o início, mas a arquitetura pode ser adaptável.

---

A arquitetura Multi-Tenant permite que uma única aplicação sirva vários clientes sem que seus dados se misturem.

Existem diferentes estratégias para isso, como separar por bancos de dados, tabelas ou apenas por relacionamento dos dados.

A escolha depende do tamanho e das exigências de governança dos clientes, e é fundamental planejar bem desde o começo para facilitar a evolução da solução.
