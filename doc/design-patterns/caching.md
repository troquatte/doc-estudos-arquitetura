# Caching

---

**Caching** é uma técnica utilizada para melhorar a performance de aplicações, reduzindo o tempo de resposta em operações repetitivas de leitura. Em um cenário tradicional, uma aplicação faz requisições diretamente ao banco de dados, o que pode gerar latência considerável - por exemplo, 900ms para uma consulta.

Com o uso de cache, essa consulta é armazenada em memória (em ferramentas como Redis, Memcached, etc), e futuras requisições ao mesmo dado são atendidas diretamente pelo cache, reduzindo drasticamente o tempo de resposta.

Contudo, o uso de cache traz um desafio importante: a **invalidação dos dados**. Quando os dados originais são modificados, o cache pode conter informações desatualizadas. Por isso, existem várias estratégias para manter o cache coerente com o banco de dados.

## Caching

- ✅ Técnica para melhorar performance ao evitar acessos repetitivos ao banco de dados.

## Exemplo de uso

- ✅ Primeira requisição custa 900ms; a segunda, com cache, é quase instantânea.

## Ferramentas comuns

- ✅ Redis, Memcached, entre outras.

## Desafio principal

- ✅ Invalidação do cache (quando atualizar ou remover o dado cacheado).

---

## Técnicas de invalidação

### 1 - Time-based invalidation

- ✅ O cache é automaticamente limpo após um período de tempo pré-definido.

### 2 - Least Recently Used (LRU)

- ✅ Remove os dados menos utilizados recentemente quando o cache atinge seu limite.

### 3 - Most Recently Used (MRU)

- ✅ Remove os dados mais recentes — útil em cenários onde o mais novo tende a ser menos confiável ou redundante.

### 4 - Least Frequently Used (LFU)

- ✅ Remove os dados que são menos acessados com frequência.

### 5 - Write-through

- ✅Cada escrita na base de dados atualiza também o cache.
- ✅Útil quando há muita leitura e poucas escritas.

### 6 - Write-back

- ✅A escrita ocorre primeiro no cache e só depois (ou periodicamente) é sincronizada com o banco.
- ✅Indicado para cenários com muitas escritas, mas exige cuidado com consistência.

---

**Caching** é uma solução para melhorar o desempenho de aplicações, armazenando dados em memória para evitar acessos repetidos ao banco.

A primeira consulta pode ser lenta, mas as subsequentes são muito mais rápidas ao usar cache. Porém, o grande desafio do cache é manter os dados atualizados, o que exige estratégias de invalidação como time-based, LRU, MRU, LFU, write-through e write-back.

A escolha da estratégia adequada depende do perfil de leitura e escrita da aplicação, e é essencial para garantir consistência e performance.
