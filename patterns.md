# Patterns / Padrões

## English

### Cache-aside
1. Read cache; on miss read DB and `SET` with TTL.
2. Invalidate or overwrite on write.

### Distributed lock (simplified)
- `SET key token NX PX ttl` then release with token check (Lua/transaction).
- Always set TTL to avoid deadlocks.

### Simple queue
- Producer: `LPUSH queue payload`
- Consumer: `BRPOP queue timeout`
- For reliability, consider Streams (`XADD`/`XREADGROUP`).

## Português

### Cache-aside
1. Ler cache; em miss ler DB e `SET` com TTL.
2. Invalidar ou sobrescrever no write.

### Lock distribuído (simplificado)
- `SET key token NX PX ttl` e libertar com verificação do token (Lua/transação).
- Defina sempre TTL para evitar deadlocks.

### Fila simples
- Produtor: `LPUSH queue payload`
- Consumidor: `BRPOP queue timeout`
- Para fiabilidade, considere Streams (`XADD`/`XREADGROUP`).
