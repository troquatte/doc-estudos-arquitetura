# Stateless vs Stateful

---

O conceito de arquiteturas Stateful e Stateless é fundamental para o design e escalabilidade de aplicações.

Uma arquitetura **Stateful** é aquela que mantém informações sobre o estado da aplicação ao longo do tempo, como sessões de usuário, logs e assets.

Isso significa que ela armazena dados temporários, o que pode ser vantajoso em alguns cenários, mas também traz desafios, como a perda de dados e a dificuldade de escalabilidade. Por outro lado, a arquitetura

---

## Stateless

- ✅ **Stateless** não armazena qualquer estado da aplicação, o que permite uma maior flexibilidade e facilidade de escalabilidade, tanto horizontal quanto vertical.
- ✅ **Stateless**: Não armazena estado.
- ✅ **Vantagens do Stateless**: Escalabilidade horizontal e vertical.

---

## Stateful

- ✅ **Stateful**: Armazena estado.
- ✅ **Exemplo de aplicação Stateful**: Logs, sessões, assets, etc.
- ✅ **Desvantagem de arquiteturas Stateful**: Perda de dados e problemas com escalabilidade.

---

A principal diferença entre as arquiteturas **Stateful** e **Stateless** é que a primeira armazena o estado da aplicação, enquanto a segunda não mantém esse tipo de dado.

Aplicações **Stateful**, como no exemplo do Docker com WordPress, podem enfrentar problemas como a perda de dados de imagens ou falhas ao tentar escalar, uma vez que os dados de estado podem ser corrompidos ou perdidos.

Já as arquiteturas **Stateless** são mais adequadas para ambientes que exigem alta escalabilidade, pois podem crescer tanto na horizontal (adicionando mais servidores) quanto na vertical (aumentando a capacidade de um único servidor), oferecendo mais resistência e flexibilidade, embora possam ser mais caras de manter.
