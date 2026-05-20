# HERMES — WORKFLOW OPERACIONAL

━━━━━━━━━━━━━━━━━━━
FLUJO REAL
━━━━━━━━━━━━━━━━━━━

1. CEO envía mensaje Telegram

Ejemplo:
"Hermes inicia FORJA fase 1.4"

↓

2. HERMES recibe mensaje

- valida usuario
- interpreta intención
- identifica app
- identifica fase

↓

3. HERMES consulta Knowledge Core

Lee:
- app
- fases
- subfases
- validaciones
- reglas

↓

4. HERMES crea TASK

Estado inicial:
pending

↓

5. Runner toma TASK

Estado:
doing

↓

6. HERMES llama VULCANO

VULCANO:
- genera prompt técnico
- aplica restricciones
- aplica validaciones
- mantiene disciplina operacional

↓

7. Claude ejecuta trabajo técnico

Ejemplo:
- backend
- frontend
- auth
- endpoints
- fixes

↓

8. Resultado guardado

Guardar:
- output
- logs
- errores
- cambios
- handoff

↓

9. Auditor IA revisa

Valida:
- errores
- inconsistencias
- seguridad básica
- validaciones fase

↓

10. HERMES genera handoff

Incluye:
- qué se hizo
- qué falta
- riesgos
- errores
- siguiente paso

↓

11. HERMES responde al CEO

Ejemplo:

FASE:
FORJA 1.4

ESTADO:
REVIEW

VALIDACIONES:
✅ auth OK
✅ endpoint OK

RIESGOS:
JWT temporal

SIGUIENTE PASO:
auditoría manual