# Actividad 4 — Operacionalización de la eficiencia

## Variable dependiente

**Eficiencia del proceso de agendamiento:** grado en que una operación se completa correctamente utilizando menor tiempo y esfuerzo humano, sin incrementar errores ni reprocesos.

La eficiencia no será evaluada únicamente mediante el tiempo. También se consideran las acciones realizadas, intervención humana, tasa de éxito, errores y satisfacción.

---

## Operaciones analizadas

Se analizarán cinco operaciones:

1. Consultar disponibilidad.
2. Registrar una cita.
3. Modificar una cita.
4. Cancelar una cita.
5. Reagendar una cita.

---

## Matriz de operacionalización

| Operación | Inicio | Final | Criterio de éxito | Acciones observables | Errores posibles | Indicadores |
|---|---|---|---|---|---|---|
| **Consultar disponibilidad** | El usuario inicia la consulta y selecciona una fecha. | El sistema muestra los horarios disponibles. | Identifica correctamente al menos un horario válido. | Seleccionar fecha, fisioterapeuta y revisar horarios. | Fecha incorrecta, información confusa o mostrar horarios ocupados. | Tiempo total, acciones del paciente, éxito y errores. |
| **Registrar cita** | El usuario selecciona un horario disponible. | La cita queda confirmada. | La reserva contiene paciente, fisioterapeuta, fecha y hora correctos. | Seleccionar horario, ingresar datos, revisar y confirmar. | Datos incorrectos, horario ocupado, cita duplicada. | Tiempo administrativo, tiempo total, acciones, intervención, éxito y errores. |
| **Modificar cita** | Se abre una cita existente. | Los cambios quedan guardados. | Los datos se actualizan sin generar otra cita. | Abrir cita, modificar datos, revisar y guardar. | Pérdida de datos, duplicación, horario inválido. | Tiempo, acciones, éxito, errores y reprocesos. |
| **Cancelar cita** | Se selecciona “Cancelar cita”. | La cita queda cancelada y el horario se libera. | La cancelación se realiza después de una confirmación explícita. | Abrir cita, cancelar y confirmar. | Cancelación accidental, horario no liberado. | Tiempo, acciones, éxito y errores. |
| **Reagendar cita** | Se selecciona “Reagendar”. | El nuevo horario queda confirmado y el anterior se libera. | Existe una sola cita válida en el nuevo horario. | Abrir cita, consultar disponibilidad, seleccionar nuevo horario y confirmar. | Doble reserva, horario anterior ocupado, pérdida de información. | Tiempo administrativo, tiempo total, acciones, intervención, éxito y errores. |

---

# Indicadores de eficiencia

## 1. Tiempo administrativo activo

Mide únicamente el tiempo durante el cual el personal trabaja directamente en una operación.

No incluye períodos de espera donde el personal no realiza ninguna acción.

**Indicador principal:** mediana del tiempo administrativo activo.

---

## 2. Tiempo total

Mide el tiempo completo desde el inicio hasta la finalización de una operación.

**Fórmula:**

`Tiempo total = Hora final - Hora inicial`

---

## 3. Acciones del personal

Número de acciones necesarias por parte del personal administrativo.

Ejemplos:

- Revisar solicitud.
- Consultar disponibilidad.
- Registrar datos.
- Modificar una cita.
- Enviar confirmación.

---

## 4. Acciones del paciente

Número de acciones realizadas por el paciente.

Ejemplos:

- Seleccionar fecha.
- Seleccionar fisioterapeuta.
- Seleccionar horario.
- Ingresar datos.
- Confirmar.

Las acciones del paciente y del personal se contabilizan **por separado**.

---

## 5. Intervención humana

Determina qué porcentaje de operaciones requirió participación del personal.

**Fórmula:**

```text
Intervención humana (%) =
(Operaciones que requirieron personal / Total de operaciones) × 100
```

Ejemplo:

```text
5 operaciones requieren personal
20 operaciones totales

(5 / 20) × 100 = 25 %
```

---

## 6. Tasa de éxito

Permite conocer el porcentaje de operaciones completadas correctamente.

**Fórmula:**

```text
Tasa de éxito (%) =
(Operaciones correctas / Total de intentos) × 100
```

Ejemplo:

```text
18 operaciones correctas
20 intentos

(18 / 20) × 100 = 90 %
```

---

## 7. Errores y reprocesos

Se registrarán situaciones como:

- Citas duplicadas.
- Datos incorrectos.
- Horarios inválidos.
- Correcciones.
- Retrocesos.
- Omisiones.
- Horarios que no se liberan después de una cancelación.

---

## 8. Satisfacción

Al finalizar una tarea se puede solicitar al participante valorar su facilidad:

| Valor | Interpretación |
|---:|---|
| 1 | Muy difícil |
| 2 | Difícil |
| 3 | Neutral |
| 4 | Fácil |
| 5 | Muy fácil |

---

# Procedimiento de medición

Para cada operación se registrará:

1. Momento de inicio.
2. Momento de finalización.
3. Tiempo administrativo activo.
4. Número de acciones del paciente.
5. Número de acciones del personal.
6. Necesidad de intervención humana.
7. Errores o reprocesos.
8. Cumplimiento del criterio de éxito.
9. Satisfacción del usuario.

Una operación se considerará eficiente cuando pueda completarse correctamente utilizando menor tiempo y esfuerzo humano **sin aumentar los errores ni disminuir la tasa de éxito**.

---

# Comparación AS-IS vs propuesta

Los siguientes datos se completarán después de realizar las pruebas de validación.

| Indicador | Proceso AS-IS | Mecanismo híbrido | Mejora |
|---|---:|---:|---:|
| Tiempo administrativo activo | Pendiente | Pendiente | Pendiente |
| Tiempo total | Pendiente | Pendiente | Pendiente |
| Acciones del personal | Pendiente | Pendiente | Pendiente |
| Acciones del paciente | Pendiente | Pendiente | Pendiente |
| Intervención humana | Pendiente | Pendiente | Pendiente |
| Tasa de éxito | Pendiente | Pendiente | Pendiente |
| Errores/reprocesos | Pendiente | Pendiente | Pendiente |
| Satisfacción | Pendiente | Pendiente | Pendiente |

## Fórmula de mejora

Para indicadores donde un valor menor representa un mejor resultado:

```text
Mejora (%) =
((Valor actual - Valor propuesto) / Valor actual) × 100
```

---