# RUNTIME_LOOP

## PURPOSE

Defines the main Hermes operational execution loop.

Hermes runtime must remain stable and observable.

---

# CORE_PRINCIPLE

Runtime stability overrides execution speed.

The loop must survive failures.

---

# LOOP_FLOW

Runtime cycle:

1. scan pending tasks
2. validate runtime state
3. execute eligible task
4. persist task state
5. log execution result
6. continue next cycle

---

# EXECUTION_RULES

Runtime must:
- process tasks sequentially
- preserve loop stability
- avoid uncontrolled execution
- maintain observability

---

# FAILURE_RULES

If task execution fails:
- preserve runtime loop
- persist failure
- continue execution cycle
- avoid runtime crash

---

# RECOVERY_RULES

On startup runtime must:
- scan incomplete tasks
- detect stale executions
- preserve operational visibility

No automatic replay allowed.

---

# OBSERVABILITY_RULES

Runtime loop must expose:
- execution state
- task activity
- failures
- retries
- runtime health

---

# CONSISTENCY_RULES

Runtime state must remain consistent with:
- PostgreSQL
- task lifecycle
- recovery state

---

# PROHIBITED

Do not implement:
- parallel runtime execution
- hidden retries
- autonomous recovery
- uncontrolled loops
- distributed execution

---

# CORE_REQUIREMENT

Hermes runtime must remain:
- deterministic
- observable
- recoverable
- stable