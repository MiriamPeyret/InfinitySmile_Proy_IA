# Infinite Smile — Instrucciones generales del agente

## 1. Objetivo del proyecto
Construir una aplicación web para apoyar a un consultorio dental pequeño en la gestión de tratamientos pendientes, seguimientos, confirmaciones de citas e incidencias extraordinarias de agenda.

## 2. Usuarios y responsabilidades
- **Doctora:** registra tratamientos y fechas de seguimiento, define la duración de las citas, valida su disponibilidad y autoriza o rechaza incidencias extraordinarias.
- **Asistente:** consulta seguimientos, registra incidencias extraordinarias, gestiona alertas, contacta a los pacientes y registra sus respuestas y confirmaciones.

## 3. Alcance del prototipo
- Utilizar exclusivamente datos ficticios.
- Implementar el feature descrito en `specs/seguimiento-tratamientos.md`.
- Permitir registrar tratamientos y sesiones pendientes.
- Gestionar fechas de seguimiento y propuestas de citas.
- Separar disponibilidad de la doctora, respuesta del paciente y estado de confirmación.
- Permitir registrar y autorizar incidencias extraordinarias.
- Validar duración variable y evitar empalmes de citas confirmadas.
- No enviar mensajes reales ni conectarse a servicios externos.

## 4. Fuera de alcance
- Integración real con Google Calendar.
- Envío real de WhatsApp, SMS o correo.
- Expedientes clínicos, diagnósticos, recetas, facturación o pagos.
- Uso de información personal o clínica real de pacientes.

## 5. Principios de desarrollo
1. Leer esta guía, la especificación y la skill de marca antes de implementar.
2. La especificación define el comportamiento esperado; no inventar reglas de negocio.
3. Implementar únicamente el alcance aprobado.
4. Mantener separados los estados de tratamiento, seguimiento, disponibilidad, respuesta del paciente, cita e incidencia.
5. Evitar duplicar citas al editar fechas u horarios.
6. Conservar el historial de cambios relevantes.
7. Mantener el código modular, legible y mantenible.
8. Usar datos ficticios claramente identificados.
9. No incluir credenciales, claves ni datos sensibles en el repositorio.

## 6. Reglas generales de agenda
- La doctora define la duración de cada cita.
- La hora final se calcula a partir de la hora inicial y la duración.
- Antes de confirmar, validar disponibilidad, aceptación del paciente y ausencia de empalmes.
- Una cita cancelada o todavía no confirmada no bloquea la disponibilidad.
- Las citas confirmadas deben volver a validarse si cambia su fecha, hora o duración.
- Una incidencia extraordinaria pendiente de autorización no modifica la agenda.

## 7. Validación y pruebas
- Verificar individualmente los cinco criterios de aceptación de la especificación.
- Incluir pruebas para duraciones variables, citas consecutivas, empalmes, cancelaciones e incidencias autorizadas/rechazadas.
- Si un criterio válido falla, corregir la implementación.
- Si una regla está incompleta o es contradictoria, explicar el problema y proponer una modificación de la especificación antes de continuar.
- No afirmar que una prueba pasó si no se ejecutó; reportar evidencia y limitaciones.

## 8. Privacidad y seguridad
- No utilizar nombres, teléfonos ni historiales reales.
- No enviar comunicaciones reales.
- No presentar el prototipo como un sistema clínico listo para producción.
