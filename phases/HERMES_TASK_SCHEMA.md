# HERMES — TASK SCHEMA

━━━━━━━━━━━━━━━━━━━
OBJETIVO
━━━━━━━━━━━━━━━━━━━

Definir la estructura operacional mínima de tasks para Hermes.

━━━━━━━━━━━━━━━━━━━
TABLA: tasks
━━━━━━━━━━━━━━━━━━━

Campos:

- id
- app
- phase
- subphase
- title
- description
- status
- priority
- assigned_agent
- created_at
- updated_at
- started_at
- completed_at
- retry_count
- validation_status
- audit_status
- handoff
- logs
- errors

━━━━━━━━━━━━━━━━━━━
ESTADOS VÁLIDOS
━━━━━━━━━━━━━━━━━━━

- pending
- doing
- review
- done
- failed
- blocked

━━━━━━━━━━━━━━━━━━━
VALIDACIONES
━━━━━━━━━━━━━━━━━━━

Una task NO puede:

- saltar fases
- cerrar sin auditoría
- cerrar sin handoff
- pasar a done con errores críticos

━━━━━━━━━━━━━━━━━━━
AGENTES POSIBLES
━━━━━━━━━━━━━━━━━━━

- vulcano
- audit
- security
- qa
- docs

━━━━━━━━━━━━━━━━━━━
PRIORIDADES
━━━━━━━━━━━━━━━━━━━

- critical
- high
- medium
- low

━━━━━━━━━━━━━━━━━━━
OBJETIVO OPERACIONAL
━━━━━━━━━━━━━━━━━━━

Toda ejecución importante del ecosistema debe:

- generar task
- guardar estado
- guardar logs
- guardar resultado
- permitir auditoría
- permitir continuidad