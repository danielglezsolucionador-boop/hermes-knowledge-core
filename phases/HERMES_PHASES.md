# HERMES PHASES

---

# FASE 1 — CORE OPERACIONAL

## 1.1 Backend Base
- FastAPI base
- config
- logging
- startup
- healthcheck

VALIDACIONES:
- backend levanta
- logs visibles
- sin crashes

---

## 1.2 PostgreSQL Base
- conexión DB
- tablas iniciales
- session manager
- persistencia básica

VALIDACIONES:
- conexión estable
- inserts funcionando
- lectura funcionando

---

## 1.3 Telegram Integration
Memory Layer
- conversation memory
- workflow memory
- operational memory
- decision history
- bot Telegram
- recepción mensajes
- envío mensajes
- validación TELEGRAM_CHAT_ID

VALIDACIONES:
- memoria persistente
- lectura correcta
- histórico disponible
- mensajes recibidos
- mensajes enviados
- usuarios externos bloqueados

---

## 1.4 Task Queue System
- pending
- running
- review
- failed
- completed

VALIDACIONES:
- task creation
- task update
- task persistence
- estados correctos

---

## 1.5 Workflow Engine
- fases
- subfases
- checkpoints
- handoffs
- validaciones

VALIDACIONES:
- transición correcta
- bloqueo de saltos
- workflow persistente

---

## 1.7 LLM Provider Layer
- Claude integration
- OpenAI integration
- provider routing
- retry handling
- fallback control

VALIDACIONES:
- prompts enviados
- respuestas recibidas
- errores controlados

---

## 1.8 Agent Coordination
- Vulcano
- auditoría
- seguridad
- revisión

VALIDACIONES:
- routing correcto
- respuesta correcta
- auditoría funcional

---

## 1.9 Operational Logs
- logs tasks
- logs workflows
- logs agentes
- logs errores

VALIDACIONES:
- logs persistentes
- logs visibles
- errores auditables

---

# FASE 2 — CONTROL OPERACIONAL

## 2.1 Execution Supervisor
- control workflows
- control agentes
- control estados

VALIDACIONES:
- workflows rastreables
- estados auditables

---

## 2.2 Approval System
- validación humana
- aprobación manual
- bloqueo acciones críticas

VALIDACIONES:
- acciones bloqueadas
- aprobaciones registradas

---

## 2.3 Audit Engine
- revisión outputs
- revisión errores
- revisión validaciones

VALIDACIONES:
- auditorías guardadas
- errores detectados

---

# FASE 3 — INTEGRACIÓN ECOSISTEMA

## 3.1 FORJA Integration
- task execution
- workflow integration
- operational coordination

---

## 3.2 CENTINELA Integration
- incidents
- alerts
- security coordination

---

## 3.3 CEREBRO Integration
- executive workflows
- operational context
- reporting

---

## 3.4 PLUMA Integration
- content workflows
- publishing workflows
- automation support

---

# REGLAS OPERACIONALES

HERMES NO puede:
- hacer deploy automático
- borrar datos automáticamente
- aprobar fases automáticamente
- ejecutar producción sin aprobación
- modificar arquitectura sin validación

---

# OBJETIVO FINAL

HERMES debe convertirse en:
- coordinador operacional
- supervisor workflows
- gestor de tareas
- interfaz central del ecosistema
- sistema supervisado por humanos