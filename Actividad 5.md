# PPPT01. Reactivos IHC

**Autor:** Andrew Lara  
**Fecha:** Septiembre 2026  
**Actividad 5:** Metáforas de interfaz

## Metáforas de interfaz para la gestión de citas

La propuesta de interfaz para el sistema de gestión de citas de fisioterapia se apoya en tres metáforas principales: la agenda/calendario, la ruta guiada y el comprobante de reserva. Estas metáforas permiten que el usuario comprenda el sistema con base en experiencias conocidas, reduciendo la carga mental y facilitando acciones como consultar disponibilidad, registrar, modificar, cancelar o reagendar una cita.

La propuesta es compatible con un mecanismo híbrido de gestión de citas, donde el paciente puede solicitar o registrar una cita mediante la interfaz y el personal administrativo mantiene control sobre la agenda, la confirmación y los cambios cuando sea necesario.

## Metáfora 1: Agenda o calendario

Esta metáfora toma como referencia la agenda física usada actualmente para registrar citas. En la interfaz digital, la agenda se transforma en un calendario visual donde los días, horarios y espacios disponibles representan la organización de las citas.

| Dominio fuente | Elemento digital | Etiqueta o mensaje | Comportamiento | Riesgo |
|---|---|---|---|---|
| Agenda física | Calendario digital | Consultar disponibilidad | El usuario selecciona una fecha para ver horarios disponibles. | El usuario puede confundir colores si no hay leyenda clara. |
| Página de la agenda | Día del calendario | Seleccione un día | Al elegir un día se muestran los turnos de ese día. | Puede no ser claro si el día no tiene horarios. |
| Espacio vacío | Horario disponible | Disponible | El usuario puede seleccionar ese horario para una cita. | Puede parecer confirmado antes de completar el proceso. |
| Nota escrita | Cita registrada | Cita confirmada | El sistema guarda los datos del paciente, fisioterapeuta, fecha y hora. | Puede haber error si no se muestra un resumen antes de confirmar. |
| Tachar una cita | Cancelación | Cita cancelada | El sistema cambia el estado y libera el horario. | El usuario puede cancelar por error si no hay confirmación previa. |

### Explicación desde HCI

La metáfora de agenda resuelve el problema de la información dispersa entre WhatsApp, agenda física y memoria del personal. Su principal aporte de usabilidad es que permite visualizar rápidamente qué horarios están disponibles, ocupados o cancelados.

Desde la perspectiva de affordance, los horarios visibles invitan a ser seleccionados. El mapeo es directo: un día del calendario representa un día real de atención, y cada bloque horario representa un posible turno. La consistencia se mantiene usando los mismos estados en todo el sistema: disponible, ocupado, pendiente, confirmado y cancelado.

El sistema debe dar retroalimentación inmediata. Por ejemplo, al seleccionar un horario debe mostrarse un cambio visual y un mensaje como **“Horario seleccionado”**. Si el horario ya fue ocupado, debe aparecer un mensaje de error comprensible: **“Este horario ya no está disponible”**.

Desde la perspectiva lingüística, las etiquetas deben ser familiares para pacientes y personal administrativo. Por eso se usan términos como **“Disponible”**, **“Ocupado”**, **“Confirmado”** y **“Cancelado”**. Desde la perspectiva computacional, cada cita debe guardarse con datos persistentes: paciente, fisioterapeuta, fecha, hora, servicio y estado.

Las reglas principales son: no permitir dos citas en el mismo horario con el mismo fisioterapeuta, liberar el horario cuando una cita se cancela y actualizar el estado cuando se modifica o reagenda una cita. El riesgo cultural de esta metáfora es que algunas personas pueden depender demasiado del color; por eso los estados deben mostrarse también con texto.

## Metáfora 2: Ruta guiada

Esta metáfora representa el proceso de agendar una cita como un recorrido por pasos. El usuario avanza desde la consulta de disponibilidad hasta la confirmación final, sin tener que entender todo el sistema de una sola vez.

| Dominio fuente | Elemento digital | Etiqueta o mensaje | Comportamiento | Riesgo |
|---|---|---|---|---|
| Ruta o camino | Flujo por pasos | Paso 1 de 5 | El usuario avanza de una pantalla a otra. | Puede sentirse largo si hay demasiados pasos. |
| Punto de partida | Pantalla de disponibilidad | Iniciar agendamiento | El usuario empieza buscando fecha y hora. | Puede abandonar si no encuentra disponibilidad rápido. |
| Paradas del recorrido | Pantallas intermedias | Datos del paciente, fisioterapeuta, resumen | Cada pantalla solicita una decisión o dato específico. | Puede haber confusión si no se indica el paso actual. |
| Retroceder en el camino | Botón volver | Volver | El usuario puede corregir información anterior. | Puede perder datos si el sistema no conserva la información. |
| Meta del recorrido | Confirmación | Cita confirmada | El sistema finaliza el proceso y muestra el resultado. | Puede generar duda si no aparece una confirmación clara. |

### Explicación desde HCI

La metáfora de ruta guiada responde al problema de carga cognitiva, porque divide el proceso en decisiones pequeñas y ordenadas. En lugar de pedir todos los datos al mismo tiempo, la interfaz guía al usuario por una secuencia comprensible.

La affordance aparece en botones como **“Continuar”**, **“Volver”** y **“Confirmar”**. El mapeo se entiende porque cada paso representa una parte real del proceso: elegir disponibilidad, seleccionar fisioterapeuta, ingresar datos, revisar resumen y confirmar. La consistencia se mantiene mostrando siempre el indicador de paso y colocando los botones de avance y retroceso en posiciones similares.

La retroalimentación debe indicar el progreso del usuario y avisar cuando falta información. Por ejemplo: **“Ingrese el número de cédula para continuar”** o **“Revise los datos antes de confirmar”**. Esto reduce errores antes de registrar la cita.

Desde la perspectiva lingüística, la interfaz debe usar instrucciones cortas y claras. Desde la perspectiva computacional, el sistema debe conservar temporalmente la información ingresada mientras el usuario avanza o retrocede. También debe validar los datos antes de pasar al siguiente paso.

Las reglas principales son: no permitir avanzar sin completar los datos obligatorios, mantener la información seleccionada al volver y mostrar un resumen antes de confirmar. Un posible riesgo es que usuarios con poca experiencia digital se pierdan si no ven en qué paso están, por lo que el indicador de progreso debe ser visible.

## Metáfora 3: Comprobante de reserva

Esta metáfora convierte la cita confirmada en un comprobante similar a un recibo o ticket. Su función es dar seguridad al paciente y al personal administrativo de que la cita fue registrada correctamente.

| Dominio fuente | Elemento digital | Etiqueta o mensaje | Comportamiento | Riesgo |
|---|---|---|---|---|
| Recibo o ticket | Pantalla de confirmación | Comprobante de cita | El sistema muestra los datos finales de la cita. | Puede parecer un pago si no se aclara que es una reserva. |
| Número de recibo | Código de cita | Código de cita | El sistema genera un identificador para consultar o modificar la cita. | Puede ser difícil de recordar si el código es muy largo. |
| Fecha del recibo | Fecha y hora de atención | Fecha y hora | El usuario verifica cuándo debe asistir. | Puede haber confusión si no se muestra el formato de hora claramente. |
| Responsable del servicio | Fisioterapeuta asignado | Fisioterapeuta | Se muestra el profesional encargado de la atención. | Puede generar dudas si luego se cambia el fisioterapeuta. |
| Estado del trámite | Estado de la cita | Confirmada, pendiente o cancelada | El sistema informa la situación actual de la cita. | Puede causar confusión si el estado no se actualiza en tiempo real. |

### Explicación desde HCI

La metáfora del comprobante resuelve el problema de falta de confirmación clara. En el proceso actual, el paciente depende de mensajes de WhatsApp y puede no saber si su cita quedó realmente registrada. Con esta metáfora, la interfaz muestra una evidencia concreta de la reserva.

La affordance principal está en las acciones posteriores al registro: **“Ver detalle”**, **“Reagendar”** y **“Cancelar”**. El mapeo es familiar porque un comprobante contiene los datos importantes de una transacción o reserva: código, fecha, hora, responsable y estado.

La consistencia se logra mostrando siempre el mismo formato de comprobante en la confirmación, el detalle de cita y las consultas posteriores. La retroalimentación debe ser clara: **“Cita confirmada correctamente”**, **“Solicitud pendiente de confirmación”** o **“Cita cancelada”**.

Desde la perspectiva lingüística, se debe evitar usar solo palabras técnicas. Es preferible usar mensajes directos como **“Su cita está confirmada”** en lugar de **“Registro procesado”**. Desde la perspectiva computacional, el comprobante representa un registro guardado en la base de datos y asociado a un código único.

Las reglas principales son: generar un código de cita, mostrar los datos completos, permitir consultar el estado y actualizar el comprobante si la cita se modifica, cancela o reagenda. El riesgo cultural es que la palabra **“comprobante”** podría relacionarse con pago; por eso se recomienda usar **“Comprobante de cita”** o **“Resumen de cita”**.

## Wireflow propuesto para Persona 4

El siguiente recorrido sirve como base para que Persona 4 construya el prototipo en Figma:

1. **Inicio de gestión de citas:** el usuario elige entre agendar una cita o consultar una cita existente.
2. **Disponibilidad:** se muestra un calendario con fechas y horarios disponibles. Aquí aparece la metáfora de agenda/calendario.
3. **Selección de fisioterapeuta:** el usuario elige el profesional disponible según fecha, hora o especialidad.
4. **Datos del paciente:** se ingresan nombres, cédula, teléfono y otros datos necesarios.
5. **Resumen:** se muestran paciente, fisioterapeuta, fecha, hora y servicio antes de confirmar.
6. **Confirmación:** el sistema informa si la cita fue confirmada o si queda pendiente de revisión.
7. **Detalle de cita:** se presenta el comprobante con código, datos de la cita y estado.
8. **Reagendar:** el usuario puede seleccionar una nueva fecha u horario disponible.
9. **Cancelar:** el usuario confirma la cancelación y el sistema libera el horario.

## Relación entre metáforas y pantallas

| Metáfora | Pantallas donde aparece | Función principal |
|---|---|---|
| Agenda o calendario | Disponibilidad, reagendar, detalle de cita | Organizar visualmente días, horarios y estados de las citas. |
| Ruta guiada | Inicio, disponibilidad, fisioterapeuta, datos del paciente, resumen, confirmación | Guiar al usuario paso a paso durante el agendamiento. |
| Comprobante de reserva | Confirmación, detalle de cita, cancelación y reagendamiento | Dar evidencia clara del estado y datos de la cita. |

## Estados y reglas de la interfaz

Para mantener una experiencia clara y consistente, el prototipo debe considerar los siguientes estados:

- **Disponible:** horario libre que puede seleccionarse.
- **Ocupado:** horario que no puede seleccionarse.
- **Pendiente:** cita solicitada pero aún no confirmada por el personal.
- **Confirmada:** cita registrada correctamente.
- **Cancelada:** cita anulada y horario liberado.
- **Sin disponibilidad:** mensaje cuando no existen horarios para una fecha.
- **Error:** aviso cuando falta información o existe conflicto de horario.

Las reglas básicas de funcionamiento son:

- El sistema no debe permitir dos citas en el mismo horario con el mismo fisioterapeuta.
- El usuario no debe avanzar si faltan datos obligatorios.
- Antes de confirmar, siempre debe mostrarse un resumen de la cita.
- Al cancelar una cita, el horario debe volver a estar disponible.
- Al reagendar, el sistema debe actualizar fecha, hora, fisioterapeuta si aplica y estado de la cita.
- Cada acción importante debe mostrar retroalimentación clara al usuario.

## Conclusión

Las tres metáforas propuestas ayudan a transformar el proceso manual actual en una experiencia digital más comprensible. La agenda permite visualizar disponibilidad, la ruta guiada ordena el proceso de registro y el comprobante confirma el resultado. En conjunto, estas metáforas reducen errores, disminuyen la carga cognitiva del usuario y preparan una base clara para el prototipo de Persona 4.
