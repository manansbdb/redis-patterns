<p align="center">
  <img src="docs/banner.svg" alt="Redis Patterns banner" width="100%" />
</p>

<h1 align="center">redis-patterns</h1>

<p align="center">
  <strong>EN</strong> Cache, lock & queue patterns with key-naming notes<br/>
  <strong>PT</strong> Padrões de cache, lock e filas com notas de naming de keys
</p>

<p align="center">
  <a href="https://github.com/manansbdb/redis-patterns/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-22c55e?style=for-the-badge" alt="MIT" /></a>
  <img src="https://img.shields.io/badge/lang-EN%20%7C%20PT-3b82f6?style=for-the-badge" alt="EN PT" />
  <img src="https://img.shields.io/badge/topic-Redis-dc2626?style=for-the-badge" alt="Redis" />
  <a href="#support--apoio"><img src="https://img.shields.io/badge/donate-BTC-f59e0b?style=for-the-badge" alt="Donate BTC" /></a>
</p>

---

## What it does / Para que serve

| English | Português |
|---------|-----------|
| Notes on common **Redis patterns**: cache-aside, distributed locks, and simple queues. | Notas sobre **padrões Redis** comuns: cache-aside, locks distribuídos e filas simples. |
| Includes key-naming conventions to avoid collisions. | Inclui convenções de naming de keys para evitar colisões. |

```mermaid
flowchart LR
  A["🌐 App"] --> B{"❓ Cache hit?"}
  B -->|yes| C["⚡ Redis GET"]
  B -->|no| D["🗄️ DB + SET"]
  D --> C
  style A fill:#2563eb,stroke:#1d4ed8,color:#fff
  style B fill:#ea580c,stroke:#c2410c,color:#fff
  style C fill:#dc2626,stroke:#991b1b,color:#fff
  style D fill:#16a34a,stroke:#15803d,color:#fff
```

---

## Install / Instalação

### 1) Clone / Clona

```bash
git clone https://github.com/manansbdb/redis-patterns.git
cd redis-patterns
```

### 2) Copy notes / Copia as notas

```bash
mkdir -p docs/redis
cp patterns.md docs/redis/patterns.md
cp key-naming.md docs/redis/key-naming.md
```

### Requirements / Requisitos

- `git`
- Optional: Redis server for trying patterns locally

---

## Quick start / Início rápido

```bash
git clone https://github.com/manansbdb/redis-patterns.git
cd redis-patterns
# read patterns.md + key-naming.md before adding Redis to your app
```

---

## Contents / Conteúdos

| Path | Purpose / Função |
|------|------------------|
| `patterns.md` | Cache / lock / queue patterns |
| `key-naming.md` | Key namespace conventions |
| `SUPPORT.md` | Donations / Doações |

---

## Project layout / Estrutura

```text
redis-patterns/
├── docs/banner.svg
├── patterns.md
├── key-naming.md
├── SUPPORT.md
└── README.md
```

---

## Support / Apoio

Bitcoin donations welcome / Doações em Bitcoin bem-vindas:

```
bc1q0qfnlnxyum9u45stzxe0a7jnhtj4j0usfkqdjw
```

See [SUPPORT.md](./SUPPORT.md).

---

## License / Licença

[MIT](./LICENSE) © 2026 manansbdb
