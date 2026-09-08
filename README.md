Elizabeth De la Cruz — Actividad 1: analizar el proceso actual AS-IS

Esta persona debe estudiar cómo se gestionan actualmente las citas, sin diseñar todavía la solución.

Acciones que debe realizar
Dibujar el flujo AS-IS:
Paciente solicita cita por WhatsApp.
Personal revisa mensaje.
Consulta agenda física.
Revisa disponibilidad.
Coordina con fisioterapeuta.
Registra la cita.
Confirma por WhatsApp.
Si existe cambio/cancelación, se procesa manualmente.
Identificar los actores:
Paciente.
Personal administrativo.
Fisioterapeuta.
Administrador, cuando corresponda.
Identificar la información necesaria:
Datos del paciente.
Fisioterapeuta.
Fecha.
Hora.
Disponibilidad.
Estado de la cita.
Marcar en el diagrama:
⏳ Esperas.
🔁 Acciones duplicadas.
✍️ Transcripciones manuales.
⚠️ Posibles errores.
Identificar problemas de:
Retroalimentación.
Visibilidad.
Consistencia.
Explicar 2 factores humanos, por ejemplo:
Carga cognitiva del personal.
Posibilidad de olvidar actualizar una cita.
Explicar 2 factores tecnológicos, por ejemplo:
Información distribuida entre WhatsApp y agenda física.
Falta de sincronización automática.

Todo esto es solicitado expresamente en la Actividad 1.

Entrega de Persona 1

Un diagrama AS-IS + tabla de problemas/fricciones + factores humanos y tecnológicos.

Persona 1 — Actividad 2: usuarios y necesidades

Después de entender el proceso actual, esta misma persona analiza quién utiliza el sistema.

La guía propone paciente, fisioterapeuta, personal administrativo y administrador.

Acciones

Completar:

Usuario	Objetivo	Necesidad	Dificultad actual
Paciente	Conseguir una cita	Ver disponibilidad fácilmente	Espera respuesta por WhatsApp
Fisioterapeuta	Organizar sus citas	Agenda actualizada	Información dispersa
Personal administrativo	Gestionar citas	Registro centralizado	Trabajo manual
Administrador	Supervisar	Indicadores e información consolidada	No existen reportes

Además:

Determinar quién es el usuario principal.
Identificar conocimientos tecnológicos esperados.
Determinar qué acciones necesita realizar cada usuario.
Evitar agregar funciones que estén fuera de la gestión de citas.
Entrega

Matriz de usuarios y necesidades + breve descripción del usuario principal.

Verónica Jaque — Actividad 3: comparar mecanismos

Esta persona estudia cómo se podría solucionar el problema.

La guía exige mínimo tres alternativas.

Yo compararía las cuatro:

Agenda digital interna.
Solicitud con confirmación.
Autoagendamiento.
Mecanismo híbrido.
Acciones

Primero explicar cómo funciona cada mecanismo.

Después construir una matriz de decisión.

Ejemplo:

Criterio	Agenda interna	Solicitud	Autoagendamiento	Híbrido
Tiempo administrativo	2	2	5	4
Tiempo de confirmación	3	2	5	4
Acciones del paciente	4	3	4	4
Acciones del personal	2	2	5	4
Intervención humana	2	2	5	4
Prevención de conflictos	4	4	4	5
Facilidad de uso	4	4	4	4
Accesibilidad	4	4	4	4
Privacidad	4	4	4	4
Factibilidad	5	4	3	4
TOTAL				

Debe justificar cada puntuación, no solamente poner números.

Finalmente:

Seleccionar el mecanismo que obtiene mejores resultados y explicar por qué.

Probablemente terminará siendo híbrido, pero la conclusión debe salir de la matriz, no decidirse antes.

Verónica Jaque — Actividad 4: operacionalizar la eficiencia

Esta persona también se encarga de convertir el concepto abstracto “eficiencia” en algo medible.

La guía indica expresamente que no se debe utilizar el tiempo como único indicador.

Acciones

Analizar las cinco operaciones:

Consultar disponibilidad.
Registrar cita.
Modificar cita.
Cancelar cita.
Reagendar cita.

Para cada una definir:

Inicio.
Final.
Criterio de éxito.
Acciones observables.
Posibles errores.
Indicadores.

Por ejemplo:

Operación	Inicio	Final	Indicadores
Registrar	Usuario selecciona horario	Cita confirmada	Tiempo, acciones, errores, éxito
Cancelar	Abre cita	Horario liberado	Tiempo, acciones, éxito
Reagendar	Selecciona cambiar cita	Nuevo horario confirmado	Tiempo, acciones, errores
Indicadores que debe definir
Tiempo administrativo activo.
Tiempo total.
Acciones del personal.
Acciones del paciente.
Intervención humana.
Tasa de éxito.
Errores/reprocesos.
Satisfacción.

La propia guía recomienda usar el tiempo administrativo activo como indicador principal, acompañado de los demás.

Entrega

Matriz de operacionalización + fórmulas de indicadores + explicación de cómo se medirán.

Andrew Lara — Actividad 5: metáforas de interfaz

Esta persona trabaja principalmente con lo visto en Semana 4.

Debe proponer al menos tres metáforas, incluyendo una familiar/organizacional y una de navegación.

Yo utilizaría:

Metáfora 1 — Agenda/calendario

Tipo: familiar/organizacional.

Agenda física → Calendario digital
Página → Día
Espacio vacío → Horario disponible
Anotación → Cita
Tachado → Cancelación
Metáfora 2 — Ruta guiada

Tipo: navegación.

Disponibilidad
      ↓
Fisioterapeuta
      ↓
Datos
      ↓
Resumen
      ↓
Confirmación
Metáfora 3 — Comprobante de reserva
Comprobante → Cita confirmada
Número → Código de cita
Fecha → Fecha de atención
Responsable → Fisioterapeuta
Estado → Confirmada / Cancelada
Acciones

Para cada metáfora, completar:

Dominio fuente	Elemento digital	Etiqueta/mensaje	Comportamiento	Riesgo

Además debe explicar:

Qué problema de usabilidad resuelve.
Affordance.
Mapping.
Consistencia.
Retroalimentación.
Perspectiva lingüística.
Perspectiva computacional.
Estados.
Reglas.
Validaciones.
Persistencia.
Riesgo cultural.

Todo eso es obligatorio según la actividad.

Entrega

Tres tablas de metáforas + explicación HCI de cada una.

Andrew Lara — Preparación del diseño para Persona 4

Antes de que Persona 4 abra Figma, Persona 3 debería preparar un pequeño wireflow.

Por ejemplo:

INICIO
  ↓
DISPONIBILIDAD
  ↓
FISIOTERAPEUTA
  ↓
DATOS PACIENTE
  ↓
RESUMEN
  ↓
CONFIRMACIÓN
  ↓
DETALLE CITA
  ├────────────┐
  ↓            ↓
REAGENDAR    CANCELAR

También debe indicar dónde aparece cada metáfora.

Así Sebastián Vaca no inventa las pantallas por su cuenta.

Sebastián Vaca — Actividad 6: prototipo HCI

Esta persona tiene la parte más visual: Figma o Penpot.

Pero no debe diseñar hasta recibir:

AS-IS → usuarios → mecanismo seleccionado → indicadores → metáforas.

Pantallas obligatorias

La guía exige:

Inicio de gestión de citas.
Consulta de disponibilidad.
Selección de fisioterapeuta.
Datos del paciente.
Resumen.
Confirmación.
Detalle de cita.
Reagendamiento.
Confirmación de cancelación.

No necesariamente tienen que ser nueve pantallas totalmente independientes; algunos estados pueden representarse mediante modales.

Acciones en Figma

Debe diseñar:

Pantalla Inicio

Botones grandes:

Agendar cita.
Consultar cita.

Disponibilidad

Calendario.
Fecha.
Horarios.
Horarios disponibles/ocupados.

Fisioterapeuta

Nombre.
Especialidad.
Horarios disponibles.

Paciente

Nombre.
Cédula.
Teléfono.
Correo, si se requiere.

Resumen

Mostrar antes de confirmar:

Paciente
Fisioterapeuta
Fecha
Hora
Servicio

[Volver] [Confirmar cita]

Confirmación

Feedback:

✓ Cita confirmada correctamente.

Detalle

Estado.
Datos.
Reagendar.
Cancelar.

Reagendamiento

Nueva fecha.
Nuevo horario.
Confirmación.

Cancelación

Modal:

¿Está seguro de cancelar la cita?

Volver | Sí, cancelar

Sebastián Vaca — Estados y accesibilidad

No basta con diseñar el “camino feliz”.

Debe mostrar también:

Cargando.
Éxito.
Error.
Horario ocupado.
Sin disponibilidad.
Cita cancelada.

Además:

Contraste adecuado.
Foco visible.
Etiquetas claras.
Navegación con teclado.
Mensajes de error comprensibles.
Botones suficientemente grandes.
No depender solamente del color.

Esto responde directamente a las exigencias del prototipo.

Sebastián Vaca — Actividad 7: validación

Esta persona también prepara el protocolo para comprobar si el diseño realmente funciona.

La guía establece cinco tareas: encontrar horario, registrar cita, cambiar fecha/fisioterapeuta, cancelar y volver a agendar después de una cancelación.

Acciones

Preparar una tabla:

Participante	Tarea	Éxito	Tiempo	Acciones	Intervención	Errores
P1	Agendar					
P2	Reagendar					
P3	Cancelar					

Y definir:

Qué significa completar correctamente cada tarea.
Cuándo empieza el cronómetro.
Cuándo termina.
Qué cuenta como acción.
Qué cuenta como error.
Qué se considera intervención del evaluador.
