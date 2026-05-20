# RECOVERY_SCAN

## PURPOSE

Defines Hermes runtime recovery scan behavior.

Recovery scan validates operational consistency after restart.

---

# CORE_PRINCIPLE

Recovery must preserve operational truth.

No hidden recovery allowed.

---

# RECOVERY_SCOPE

Recovery scan must inspect:
- doing tasks
- stale tasks
- incomplete executions
- interrupted runtime states

---

# STARTUP_RULES

On runtime startup:

Hermes must execute recovery scan before normal execution.

---

# STALE_TASK_RULES

A task may become stale if:
- status == doing
- execution incomplete
- runtime interrupted

Stale tasks must remain visible.

---

# ZOMBIE_DETECTION

Recovery scan must detect:
- orphan executions
- incomplete transitions
- broken runtime ownership

---

# RECOVERY_RULES

Recovery scan may:
- mark tasks for review
- preserve operational visibility
- expose inconsistent states

Recovery scan cannot:
- silently replay tasks
- hide interrupted execution
- force automatic completion

---

# OBSERVABILITY_RULES

Recovery scan must expose:
- detected stale tasks
- runtime inconsistencies
- interrupted execution state
- recovery timestamps

---

# CONSISTENCY_RULES

Recovery behavior must remain consistent with:
- PostgreSQL
- task lifecycle
- runtime state

---

# PROHIBITED

Do not implement:
- silent recovery
- automatic replay
- hidden task reset
- autonomous task completion

---

# CORE_REQUIREMENT

Recovery must remain:
- observable
- deterministic
- traceable
- controlled