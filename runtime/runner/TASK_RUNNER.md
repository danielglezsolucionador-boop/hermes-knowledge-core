# TASK_RUNNER

## PURPOSE

Defines Hermes task runner behavior.

The runner executes operational tasks inside runtime loop.

---

# CORE_PRINCIPLE

The runner must remain controlled and deterministic.

Only valid tasks may execute.

---

# RUNNER_FLOW

Runner cycle:

1. fetch pending task
2. validate task eligibility
3. lock execution ownership
4. execute task
5. persist result
6. release execution state

---

# EXECUTION_RULES

Runner must:
- execute sequentially
- preserve runtime stability
- avoid duplicate execution
- persist execution state

---

# TASK_OWNERSHIP

A task in:
doing

belongs to active runner execution.

No parallel ownership allowed.

---

# VALIDATION_RULES

Runner must validate:
- task state
- runtime state
- execution eligibility

before execution.

---

# FAILURE_RULES

If execution fails:
- preserve runtime loop
- persist failure state
- release execution ownership
- continue operational cycle

---

# OBSERVABILITY_RULES

Runner must expose:
- active execution
- execution timestamps
- failure visibility
- runtime activity

---

# CONSISTENCY_RULES

Runner state must remain consistent with:
- PostgreSQL
- task lifecycle
- runtime loop

---

# PROHIBITED

Do not implement:
- parallel runners
- hidden execution
- autonomous retries
- uncontrolled concurrency
- distributed runners

---

# CORE_REQUIREMENT

The runner must remain:
- observable
- deterministic
- stable
- recoverable