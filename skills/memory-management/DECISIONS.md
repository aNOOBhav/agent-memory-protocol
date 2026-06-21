# Architecture Decisions

## ADR-001

Decision
Keep a dedicated PROJECT_MEMORY.md for long-lived project context.

Reason
It gives future harnesses a stable summary of project goals, constraints, and active features.

Tradeoffs
The file must be maintained carefully to avoid drift.

---

## ADR-002

Decision
Use a separate HANDOVER.md for the latest state only.

Reason
A single current-state file is faster for agents to read before making changes.

Tradeoffs
History is not stored in HANDOVER.md itself, so the changelog and logs must remain up to date.
