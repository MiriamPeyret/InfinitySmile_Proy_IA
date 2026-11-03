# Prompt de implementación — Infinite Smile SDD

Implementa el feature definido en `specs/seguimiento-tratamientos.md`.

Antes de programar:
1. Lee `AGENTS.md`.
2. Lee `specs/seguimiento-tratamientos.md`.
3. Lee `skills/diseno-marca/SKILL.md`.
4. Resume el alcance, las reglas de negocio y los cinco criterios de aceptación.
5. Señala cualquier ambigüedad antes de implementar.

Implementación:
- Construye una aplicación web funcional para el feature especificado.
- Usa exclusivamente datos ficticios.
- Sigue la skill de diseño de marca.
- No integres Google Calendar, WhatsApp ni servicios externos.
- Mantén separados los estados de tratamiento, seguimiento, disponibilidad, respuesta del paciente, cita e incidencia.
- Implementa duración variable definida por la doctora y cálculo de hora final.
- Evita empalmes entre citas confirmadas.
- La asistente puede registrar incidencias extraordinarias, pero la doctora debe autorizarlas o rechazarlas.
- Conserva el historial de cambios y evita duplicar registros.
- No agregues funciones fuera del alcance.

Validación:
- Ejecuta pruebas para CA-01 a CA-05, individualmente.
- Prueba citas consecutivas, citas empalmadas, duraciones diferentes, cancelaciones, cambios de duración e incidencias pendientes, autorizadas y rechazadas.
- Reporta cada prueba como PASÓ, FALLÓ o NO EJECUTADA, con evidencia.
- Si un criterio válido falla, corrige la implementación.
- Si la especificación es ambigua o contradictoria, explica el problema y propone el cambio antes de continuar.
- No afirmes que una prueba pasó si no la ejecutaste.

Entrega:
1. Resumen de lo implementado.
2. Archivos creados o modificados.
3. Resultados de pruebas por criterio.
4. Instrucciones para ejecutar la aplicación.
5. Limitaciones conocidas.
