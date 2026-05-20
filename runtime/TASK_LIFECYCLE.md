# TASK_LIFECYCLE

## PURPOSE

Defines operational task state transitions inside Hermes runtime.

---

# TASK_STATES

## PENDING

Task waiting execution.

---

## DOING

Task currently executing.

---

## DONE

Task completed successfully.

---

## FAILED

Task execution failed.

---

# VALID_TRANSITIONS

pending
→ doing

doing
→ done

doing
→ failed

failed
→ pending

---

# INVALID_TRANSITIONS

done
→ doing

done
→ pending

doing
→ pending

failed
→ done

---

# TIMESTAMP_RULES

doing:
requires started_at

done:
requires completed_at

failed:
requires completed_at

---

# RETRY_RULES

Retries allowed only:

failed
→ pending

No automatic retries.

---

# RECOVERY_RULES

Startup recovery scan must detect:
- stale tasks
- incomplete tasks
- zombie tasks

No automatic replay.

---

# CONSISTENCY_RULES

Task state must remain consistent with:
- PostgreSQL
- runtime state
- retry state

---

# PROHIBITED

Do not implement:
- hidden transitions
- automatic replay
- distributed execution
- parallel runtime execution

---

# CORE_PRINCIPLE

Operational consistency overrides execution speed.