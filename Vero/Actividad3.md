## Caso: GABO'S Readaptación y Movimiento

Este apartado contiene el desarrollo de las **Actividades 3 y 4** del análisis HCI para la gestión de citas de GABO'S.

El objetivo es comparar diferentes mecanismos de agendamiento y determinar cuál se adapta mejor al centro. Posteriormente, se operacionaliza la variable **eficiencia del proceso de agendamiento** mediante indicadores medibles.

---

# Actividad 3 — Comparación de mecanismos de agendamiento

## Objetivo

Analizar diferentes alternativas para mejorar el proceso actual de gestión de citas de GABO'S.

Actualmente las citas se gestionan principalmente mediante **WhatsApp y una agenda física**, por lo que pueden existir tiempos de espera, acciones repetitivas, intervención administrativa y dificultades para mantener actualizada la disponibilidad de los cinco fisioterapeutas.

Se analizaron cuatro alternativas:

1. Agenda digital interna.
2. Solicitud con confirmación.
3. Autoagendamiento.
4. Mecanismo híbrido.

---

## 1. Agenda digital interna

El personal administrativo registra y modifica todas las citas mediante un calendario digital centralizado.

### Funcionamiento

Paciente solicita cita  
→ Personal recibe solicitud  
→ Consulta agenda digital  
→ Revisa disponibilidad  
→ Selecciona fisioterapeuta  
→ Registra cita  
→ Confirma al paciente

### Ventajas

- Centraliza la información.
- Sustituye la agenda física.
- Es fácil de implementar.
- Mantiene una forma de trabajo conocida por el personal.

### Desventajas

- Mantiene una alta intervención administrativa.
- El paciente continúa dependiendo del personal.
- No elimina completamente los tiempos de espera.

---

## 2. Solicitud con confirmación

El paciente selecciona un horario y envía una solicitud, pero la cita solamente queda registrada después de ser revisada por el personal.

### Funcionamiento

Paciente selecciona horario  
→ Envía solicitud  
→ Estado pendiente  
→ Personal revisa  
→ Confirma o rechaza  
→ Paciente recibe respuesta

### Ventajas

- Mantiene control administrativo.
- Permite revisar situaciones especiales.
- Ayuda a prevenir conflictos antes de confirmar.

### Desventajas

- El paciente debe esperar una respuesta.
- Mantiene intervención humana.
- El personal todavía debe revisar las solicitudes.

---

## 3. Autoagendamiento

El paciente consulta directamente los horarios disponibles y selecciona uno sin requerir confirmación manual en los casos normales.

### Funcionamiento

Paciente ingresa  
→ Selecciona fecha  
→ Selecciona fisioterapeuta  
→ Consulta disponibilidad  
→ Selecciona horario  
→ Ingresa datos  
→ Confirma cita

### Ventajas

- Reduce el trabajo administrativo.
- Disminuye el tiempo de confirmación.
- El paciente puede consultar disponibilidad directamente.
- Reduce acciones repetitivas del personal.

### Desventajas

- Requiere reglas de disponibilidad confiables.
- Puede generar conflictos si las reglas están mal configuradas.
- Requiere mayor complejidad técnica.

---

## 4. Mecanismo híbrido

Combina el autoagendamiento con la intervención del personal administrativo.

Los casos normales pueden confirmarse automáticamente, mientras que las excepciones son enviadas al personal para su revisión.

### Funcionamiento

Paciente selecciona horario  
→ Sistema valida condiciones  
→ ¿Caso normal?

**Sí:** confirmación automática.  
**No:** revisión administrativa.

### Ventajas

- Reduce el trabajo administrativo.
- Mantiene control humano en situaciones especiales.
- Permite automatizar las operaciones comunes.
- Ayuda a prevenir conflictos.
- Se adapta al funcionamiento de un centro pequeño.

### Desventajas

- Requiere definir reglas para diferenciar casos normales y especiales.
- Tiene mayor complejidad que una agenda digital simple.
- Deben controlarse correctamente los estados de las citas.

---

# Matriz de decisión

Se utilizó una escala de **1 a 5**:

| Puntuación | Interpretación |
|---:|---|
| 1 | Muy desfavorable |
| 2 | Desfavorable |
| 3 | Aceptable |
| 4 | Favorable |
| 5 | Muy favorable |

> **Nota:** una puntuación mayor representa un mejor desempeño. Por ejemplo, 5 en reducción del tiempo administrativo significa que el mecanismo requiere menos tiempo administrativo.

| Criterio | Agenda digital | Solicitud + confirmación | Autoagendamiento | Híbrido |
|---|---:|---:|---:|---:|
| Reducción del tiempo administrativo | 2 | 2 | 5 | 4 |
| Reducción del tiempo de confirmación | 3 | 2 | 5 | 4 |
| Menor esfuerzo del paciente | 4 | 3 | 4 | 4 |
| Menor cantidad de acciones del personal | 2 | 2 | 5 | 4 |
| Menor intervención humana innecesaria | 2 | 2 | 5 | 4 |
| Prevención de conflictos | 3 | 4 | 3 | 5 |
| Facilidad de uso | 4 | 4 | 3 | 4 |
| Accesibilidad | 4 | 4 | 3 | 4 |
| Privacidad | 4 | 4 | 3 | 4 |
| Factibilidad técnica | 5 | 4 | 2 | 4 |
| Adaptación a los 5 fisioterapeutas | 5 | 4 | 3 | 5 |
| **TOTAL** | **38** | **35** | **41** | **46** |

---

## Justificación de la matriz

### Agenda digital — 38 puntos

Obtiene una puntuación alta en **factibilidad técnica y adaptación al centro**, debido a que representa un cambio pequeño respecto a la agenda física actual.

Sin embargo, obtiene puntuaciones bajas en reducción del tiempo administrativo, acciones del personal e intervención humana porque el personal continúa realizando la mayoría de las operaciones.

### Solicitud con confirmación — 35 puntos

Permite mantener un buen control de las solicitudes y prevenir algunos conflictos antes de confirmar una cita.

Su principal limitación es que todavía requiere intervención administrativa y mantiene un tiempo de espera entre la solicitud y la confirmación.

### Autoagendamiento — 41 puntos

Obtiene puntuaciones altas en reducción de tiempo, acciones administrativas e intervención humana porque el paciente puede completar gran parte del proceso directamente.

Sin embargo, requiere reglas de disponibilidad confiables y una mayor complejidad técnica.

### Mecanismo híbrido — 46 puntos

Obtiene la puntuación más alta porque combina automatización con intervención humana.

Permite automatizar las citas normales y enviar únicamente las excepciones al personal administrativo. Además, mantiene control sobre situaciones especiales y presenta una buena adaptación al funcionamiento del centro.

---

## Mecanismo seleccionado

### Mecanismo híbrido

El **mecanismo híbrido** obtuvo **46 de 55 puntos**, equivalente aproximadamente al **83,64 %** de la puntuación máxima.

Se selecciona provisionalmente porque permite:

- Reducir el tiempo administrativo.
- Disminuir acciones repetitivas.
- Dar una respuesta más rápida al paciente.
- Mantener intervención humana en casos especiales.
- Prevenir conflictos de horarios.
- Adaptarse al funcionamiento de los cinco fisioterapeutas.

La selección definitiva deberá contrastarse con las pruebas de validación del prototipo.