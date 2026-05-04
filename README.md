hi, i'm vishal 👾

backend engineer obsessed with distributed systems, async workflows, and things that don't fall over at 3am.

currently building AI infra — a durable agent execution runtime and an LLM gateway with semantic caching and cost tracking. open to remote backend / AI infra roles.

→ vishalrai10342@gmail.com

---

## things i've built

**[devfleet](https://github.com/eviltwin7648/devfleet)** — distributed job orchestration and agent coordination runtime.

immediate, delayed, and cron jobs with exponential backoff. Go agent runtime with `os/exec` and context-aware timeouts. execution state machine (`CREATED → RUNNING → SUCCESS / FAILED / TIMEOUT`). one-time API keys, JWT auth, heartbeat-based worker liveness, horizontal worker scaling.

the kind of infra you build after a job queue loses work silently at the worst possible time.

```
Node.js · BullMQ · Go · PostgreSQL · Redis · Docker
```

---

**[nexus](https://github.com/eviltwin7648/nexus)** — AI-powered knowledge engine over your codebase and notes.

ingests, chunks, and embeds documents into pgvector. retrieval-augmented generation with cosine similarity search. designed around the failure modes — chunk boundaries, embedding drift, answer confidence.

```
Go · pgvector · OpenAI Embeddings · PostgreSQL · RAG
```

---

**llm-gateway** *(in progress)* — LLM reverse proxy with semantic caching, provider fallback, and cost attribution.

drop-in layer between your app and any OpenAI-compatible endpoint. Redis semantic cache cuts redundant API calls. per-model cost tracking in PostgreSQL. p95 latency metrics. retry with exponential backoff + jitter on provider rate limits.

```
Go · Redis · pgvector · PostgreSQL · Prometheus
```

---

## systems patterns i've actually debugged

```
dead letter exchange + TTL retry loops          materialized read tables for join optimization
atomic credit deduction with row-level locks    event-driven read models
scope-based RBAC middleware                     rate-limit retry with exponential jitter
heartbeat-based worker liveness                 context-cancellable subprocess execution
backpressure handling in async queues           WAL-backed job state
```

---

## stack

```
languages    Go · TypeScript · SQL
backend      Node.js · Express · Prisma
infra        PostgreSQL · Redis · RabbitMQ · BullMQ · Docker · AWS EC2
AI / LLM     pgvector · OpenAI API · embeddings · RAG
```

---

## homelab

```
arch laptop ——— tailscale ——— titan (ubuntu server)
                                └── docker workloads
```

two machines. one mesh. zero downtime goals.

---

open to remote backend / AI infra roles · async-preferred · IST
