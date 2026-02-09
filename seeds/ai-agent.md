# AI Agent - Seed

## Project
Autonomous revenue agent(s)

## Goal
One productionized agent that reliably executes a narrow revenue-linked workflow (e.g., SDR, lead qualification, ops).

## Stack
- LLM: Claude / OpenAI / local
- Router/orchestrator: LangGraph / AutoGen
- Backend: FastAPI
- DB: PostgreSQL / SQLite
- Queue: Celery / simple async
- Logging: Structured logs + monitoring

## Constraints
- Cheap to run
- Observable (logging, metrics)
- Recoverable (persistence, retries)
- Minimal manual babysitting

## Current state
- [ ] Core agent prompt
- [ ] API surface (FastAPI)
- [ ] Persistence (DB schema)
- [ ] Logging/metrics

## Open questions
- Exact user journey?
- Which tools/integrations in v1?
- LLM cost per execution acceptable?

## Next actions
1. Lock v1 scope
2. Define API contracts
3. Implement minimal logging
