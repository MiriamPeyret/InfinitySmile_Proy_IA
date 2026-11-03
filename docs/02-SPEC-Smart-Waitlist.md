
# SPEC — Smart Waitlist

## Objetivo

Crear una lista de espera inteligente que permita recuperar espacios liberados por cancelaciones y reprogramaciones.

## Funcionalidades

1. Registrar pacientes que desean adelantar su cita.
2. Capturar tratamiento, duración y horario preferido.
3. Registrar espacios disponibles.
4. Identificar pacientes compatibles.
5. Registrar aceptación, rechazo o falta de respuesta.
6. Validar disponibilidad antes de confirmar una cita.

## Reglas de negocio

- RN-01: Virginia puede registrar pacientes en espera.
- RN-02: nombre, teléfono, tratamiento, duración y horario son obligatorios.
- RN-03: solo se mostrarán pacientes cuya duración requerida quepa en el espacio disponible.
- RN-04: las preferencias del paciente deben coincidir con el horario ofrecido.
- RN-05: una aceptación no confirma automáticamente la cita.
- RN-06: la Dra. Angélica debe validar disponibilidad y ausencia de traslapes.
- RN-07: un espacio confirmado no puede asignarse nuevamente.
- RN-08: retirar un paciente no debe borrar su historial.

## Criterios de aceptación

**CA-01:** El sistema impide registrar pacientes si faltan campos obligatorios.

**CA-02:** El sistema muestra únicamente pacientes compatibles por duración y horario.

**CA-03:** Virginia puede registrar Aceptada, Rechazada o Sin respuesta.

**CA-04:** Si el espacio ya no está disponible, el sistema impide la confirmación.

**CA-05:** Una vez confirmada la cita, el espacio deja de estar disponible y el paciente sale de la lista activa.

**CA-06:** Los registros retirados conservan su información histórica.

## Métricas de éxito

| Métrica | Fórmula | Meta |
|---|---|---|
| Tasa de recuperación | Citas reasignadas / espacios liberados × 100 | ≥40% |
| Conversión de ofertas | Ofertas aceptadas / ofertas realizadas × 100 | ≥30% |
| Tiempo de reasignación | Tiempo entre liberación y confirmación | ≤4 horas |
| Conflictos de agenda | Citas confirmadas con traslape | 0 |
| Trazabilidad | Ofertas con respuesta registrada / ofertas realizadas × 100 | 100% |

## Fuera de alcance

- Integración real con WhatsApp.
- Sincronización con Google Calendar.
- Expediente clínico.
- Pagos.
- Base de datos multiusuario.

## Limitaciones

El MVP es un prototipo académico con datos ficticios. No debe utilizarse para almacenar información real de pacientes ni sustituye una agenda clínica.
