# 🏥 Sistema de Gestión de Citas — Análisis, Diseño HCI y Prototipado

Proyecto de análisis, optimización y prototipado de interfaz para el sistema de gestión de citas de fisioterapia, aplicando principios de Interacción Humano-Computador (HCI).

---


## 👥 Equipo y Distribución de Actividades

| Integrante | Usuario GitHub | Rol / Actividad | Issue |
| :--- | :--- | :--- | :---: |
| **Elizabeth De la Cruz** | `Elizabeth1925` | Actividad 1 & 2 — Diagrama AS-IS, Matriz de Fricciones, Matriz de Necesidades | #1 |
| **Verónica Jaque** | `ArteMisa82` | Actividad 3 & 4 — Matriz de Decisión, Operacionalización de Indicadores | #2 |
| **Andrew Lara** | `Alara05` | Actividad 5 — Metáforas HCI, Fundamentos de Diseño, Wireflow | #3 |
| **Sebastián Vaca** | `Sebas2h` | Actividad 6 & 7 — Prototipos Interactivos (Figma/Penpot), Protocolo de Validación | #4 |

---


* **Identificación de Actores:** Paciente, Personal Administrativo, Fisioterapeuta y Administrador.
* **Información Requerida:** Datos del paciente, Fisioterapeuta asignado, Fecha, Hora, Estado de disponibilidad y Estado de la cita.

```mermaid
graph TD
    A[Paciente solicita cita via WhatsApp] --> B[Personal revisa mensaje]
    B --> C[Consulta agenda física]
    C --> D{¿Hay disponibilidad?}
    D -- Sí --> E[Coordina con Fisioterapeuta]
    E --> F[Registra cita manualmente ✍️]
    F --> G[Confirma por WhatsApp ⏳]
    D -- No --> H[Notifica indisponibilidad]

Link FIGMAN: https://www.figma.com/make/aKeX0RpcoIDoCbMUTojEhz/Prototipo-web-de-citas?t=z9pZM4pKCqNE2c37-1
1. Descripción general

Este proyecto corresponde al diseño HCI de un mecanismo para la gestión de citas de GABO'S Readaptación y Movimiento, un centro de fisioterapia con cinco fisioterapeutas.

El proceso actual utiliza principalmente WhatsApp, una agenda física y coordinación manual, lo que genera problemas como esperas, transcripciones, duplicación de acciones, riesgo de errores, información desactualizada y poca visibilidad del estado de una cita.

El objetivo del trabajo fue analizar ese proceso, identificar las necesidades de los usuarios, comparar mecanismos de agendamiento, definir indicadores de eficiencia, construir metáforas de interfaz, elaborar un prototipo navegable y establecer un protocolo de validación.

2. Actividades realizadas

Actividad 1 — Análisis del proceso actual

Se modeló el flujo AS-IS del proceso de citas:

El paciente solicita una cita mediante WhatsApp.

El personal revisa los mensajes y consulta la agenda física.

Se coordina el horario con el fisioterapeuta.

La cita se registra y se confirma.

Los cambios y cancelaciones se procesan manualmente.

Principales fricciones encontradas

Espera hasta que el personal revise los mensajes.

Información distribuida entre WhatsApp y agenda física.

Posibilidad de datos desactualizados.

Dependencia de memoria y comunicación.

Transcripción manual.

Riesgo de omisiones.

Duplicación de acciones.

Posibles conflictos de horarios.

Factores humanos considerados

Carga cognitiva.

Dependencia de memoria.

Riesgo de errores de transcripción.

Factores tecnológicos considerados

Ausencia de una fuente centralizada.

Falta de validaciones automáticas para conflictos de horarios.

Actividad 2 — Usuarios y necesidades

Se identificaron cuatro tipos principales de usuarios.

Paciente

Objetivo: obtener, cambiar o cancelar una cita.
Necesidad: ver disponibilidad y recibir una confirmación clara.
Problema actual: depende de la respuesta del personal y no conoce claramente el estado del proceso.

Fisioterapeuta

Objetivo: conocer su agenda y sus cambios.
Necesidad: disponer de horarios consistentes y actualizados.
Problema actual: los cambios se comunican manualmente.

Personal administrativo

Objetivo: gestionar citas con rapidez y precisión.
Necesidad: una fuente única de información y prevención de conflictos.
Problema actual: existe trabajo repetitivo entre WhatsApp y la agenda física.

Administrador

Objetivo: supervisar el proceso.
Necesidad: información consolidada e indicadores.
Problema actual: no existen reportes consolidados.

Para el prototipo se consideró al paciente como usuario principal, ya que inicia la consulta y necesita confirmar, consultar, reagendar o cancelar su cita con el menor esfuerzo posible.

3. Actividad 3 — Evaluación de mecanismos de agendamiento

Se compararon cuatro mecanismos:

Agenda digital interna

Solicitud con confirmación

Autoagendamiento

Mecanismo híbrido

La evaluación se realizó con una escala de 1 a 5, donde el documento define:

1 = muy desfavorable

5 = muy favorable

Para explicar la escala de manera práctica durante una exposición puede interpretarse así:

Valor

Interpretación práctica

1

Muy desfavorable

2

Desfavorable

3

Intermedio / aceptable

4

Favorable

5

Muy favorable

Los valores 2, 3 y 4 son una interpretación intermedia de apoyo para explicar la escala; el documento establece expresamente los extremos 1 y 5.

Criterios considerados

Se evaluaron los mecanismos mediante 12 criterios:

Reducción del tiempo administrativo.

Reducción del tiempo de confirmación.

Menos acciones del paciente.

Menos acciones del personal.

Menor intervención innecesaria.

Prevención de conflictos.

Facilidad de uso.

Accesibilidad.

Privacidad.

Factibilidad técnica.

Compatibilidad con cinco fisioterapeutas.

Menor tasa de errores.

Matriz de evaluación

Criterio

Agenda interna

Solicitud

Autoagendamiento

Híbrido

Reducción tiempo administrativo

2

2

5

4

Reducción tiempo de confirmación

3

2

5

4

Menos acciones del paciente

4

3

4

4

Menos acciones del personal

2

2

5

4

Menor intervención innecesaria

2

2

5

4

Prevención de conflictos

3

4

3

5

Facilidad de uso

4

4

3

4

Accesibilidad

4

4

3

4

Privacidad

4

4

3

4

Factibilidad técnica

5

4

2

4

Compatibilidad con 5 fisioterapeutas

5

4

3

5

Menor tasa de errores

3

4

3

5

TOTAL

41

39

44

51

Cada mecanismo podía obtener como máximo:

12 criterios × 5 puntos = 60 puntos

Por lo tanto:

Agenda digital interna: 41/60 = 68,33 %

Solicitud con confirmación: 39/60 = 65,00 %

Autoagendamiento: 44/60 = 73,33 %

Mecanismo híbrido: 51/60 = 85,00 %

El mecanismo híbrido obtuvo la puntuación más alta porque equilibra automatización y control humano. Los casos normales pueden resolverse de forma más automática y las excepciones continúan siendo revisadas por el personal.

4. Actividad 4 — Indicadores de eficiencia

La variable dependiente definida fue la eficiencia del proceso de agendamiento.

Se entiende como el grado en que una operación se completa correctamente utilizando menor tiempo y esfuerzo humano, sin incrementar errores ni reprocesos.

Las operaciones evaluadas fueron:

Consultar disponibilidad.

Registrar una cita.

Modificar una cita.

Cancelar una cita.

Reagendar una cita.

Para cada operación se definió:

Inicio.

Final o criterio de éxito.

Acciones observables.

Errores posibles.

Indicadores.

Indicadores utilizados

Tiempo administrativo activo

Suma de los intervalos en los que el personal trabaja realmente en la operación.

Tiempo total

Tiempo total = hora final - hora inicial

Incluye también las esperas.

Acciones del personal

Cantidad de:

clics,

consultas,

mensajes,

llamadas,

transcripciones.

Acciones del paciente

Cantidad de:

clics,

pantallas,

mensajes,

campos necesarios.

Intervención humana

Intervención humana (%) = operaciones que requirieron personal / total de operaciones × 100

Tasa de éxito

Tasa de éxito (%) = operaciones correctas / total de intentos × 100

Errores y reprocesos

Se contabilizan:

duplicados,

datos incorrectos,

correcciones,

retrocesos,

omisiones.

Satisfacción

Se propone medir la percepción de facilidad mediante una escala de 1 a 5.

Una interpretación práctica para esta escala puede ser:

Valor

Interpretación

1

Muy difícil / muy insatisfecho

2

Difícil / insatisfecho

3

Aceptable / neutral

4

Fácil / satisfecho

5

Muy fácil / muy satisfecho

Esta interpretación sirve para aplicar el instrumento; los resultados reales deben obtenerse con participantes y no deben inventarse.

5. Actividad 5 — Metáforas de interfaz

Se seleccionaron tres metáforas principales:

Agenda o calendario

Ruta guiada

Comprobante de reserva

Las metáforas no se calificaron con la misma matriz numérica 1–5 utilizada para los mecanismos. Su evaluación fue principalmente cualitativa desde HCI.

¿Cómo se evaluaron las metáforas?

Para cada metáfora se revisaron los siguientes aspectos:

Dominio fuente.

Elemento digital que representa.

Etiquetas y mensajes.

Comportamiento esperado.

Problema de usabilidad que resuelve.

Affordance.

Mapeo.

Consistencia.

Retroalimentación.

Perspectiva lingüística.

Perspectiva computacional.

Estados.

Reglas.

Validaciones.

Persistencia.

Riesgos y límites culturales o contextuales.

Metáfora 1 — Agenda o calendario

Dominio fuente

Una agenda o calendario tradicional.

Elemento digital

Vista de fechas, bloques horarios y citas.

Etiquetas

Disponible.

Ocupado.

Cancelado.

Affordance

Los bloques libres sugieren que pueden seleccionarse, mientras que los horarios ocupados aparecen deshabilitados.

Mapeo

Horario libre → se puede reservar.

Horario ocupado → no se puede seleccionar.

Cancelación → el horario vuelve a estar disponible.

Consistencia

Se mantienen las mismas etiquetas y estados durante el flujo.

Retroalimentación

Después de reservar, cancelar o cambiar una cita, el estado debe actualizarse visualmente.

Perspectiva lingüística

Se utilizan palabras conocidas por el usuario:

cita,

horario,

fisioterapeuta,

confirmar,

cancelar.

Perspectiva computacional

El sistema maneja estados como:

Disponible.

Retenido.

Confirmado.

Reagendado.

Cancelado.

También considera validación de conflictos y prevención de reservas dobles.

Riesgo considerado

Un usuario puede confundirse si los estados dependen solamente del color.

Solución

Se utilizan texto, estado visual y color, evitando depender únicamente de diferencias cromáticas.

Metáfora 2 — Ruta guiada

Dominio fuente

Un recorrido dividido en pasos.

Representación en la interfaz

Horario.

Fisioterapeuta.

Datos.

Confirmación.

Affordance

Los botones Continuar y Volver comunican la dirección del flujo.

Mapeo

Cada acción lleva al siguiente paso y Volver permite regresar a la etapa anterior.

Persistencia

Los datos ya ingresados deben conservarse cuando el usuario retrocede.

Consistencia

El indicador de progreso mantiene la misma apariencia durante el proceso.

Retroalimentación

El sistema muestra:

paso actual,

pasos completados,

pasos pendientes.

Perspectiva lingüística

Se utilizan verbos directos:

Selecciona.

Completa.

Revisa.

Confirma.

Perspectiva computacional

El sistema conserva:

fecha,

hora,

fisioterapeuta,

datos del paciente.

Además, valida campos obligatorios antes de avanzar.

Riesgo

Un proceso con demasiadas etapas puede sentirse largo.

Consideración de diseño

Se utilizaron únicamente los pasos necesarios y se hizo visible el progreso.

Metáfora 3 — Comprobante de reserva

Dominio fuente

Un comprobante o recibo.

Elemento digital

Resumen final de la cita.

Información mostrada

Código de cita.

Paciente.

Fecha.

Hora.

Fisioterapeuta.

Estado.

Affordance y mapeo

El resumen y el código indican que existe un resultado verificable después de finalizar la reserva.

Retroalimentación

El usuario recibe inmediatamente:

confirmación,

código,

información de la cita,

estado.

Acciones disponibles

Consultar.

Reagendar.

Cancelar.

Perspectiva lingüística

Se utilizan expresiones como:

Cita confirmada.

Código de cita.

Reagendar.

Cancelar.

Perspectiva computacional

Se genera un identificador y se conserva el estado de la cita. Si la cita se cancela o reagenda, el detalle debe actualizarse.

Riesgo

El código podría confundirse con otro identificador, por ejemplo un número de historia clínica.

Consideración tomada

El código se acompaña de una explicación y de la información completa de la cita.

6. Consideraciones HCI utilizadas para construir la interfaz

La interfaz no se diseñó únicamente desde el punto de vista estético. Las decisiones surgieron de las fricciones encontradas en el proceso AS-IS.

Visibilidad

El usuario debe conocer en todo momento:

dónde se encuentra,

qué información seleccionó,

cuál es el estado de la cita.

Retroalimentación

Cada acción importante debe generar una respuesta visual.

Ejemplos:

cita confirmada,

horario ocupado,

cita cancelada,

cambio realizado,

error de formulario.

Consistencia

Se mantienen patrones similares en:

botones,

tarjetas,

etiquetas,

colores,

campos,

mensajes,

estados.

Prevención de errores

Se consideró:

deshabilitar horarios ocupados,

validar campos obligatorios,

evitar citas duplicadas,

confirmar acciones delicadas,

mostrar errores cerca del elemento donde ocurren.

Control del usuario

El usuario puede:

avanzar,

regresar,

revisar información,

modificar datos,

cancelar operaciones.

Persistencia

Al regresar a una pantalla anterior no deben perderse los datos previamente ingresados.

Accesibilidad

Se consideró:

contraste.

texto legible.

foco de teclado.

etiquetas visibles.

mensajes comprensibles.

estados que no dependen únicamente del color.

Reducción de carga cognitiva

Cada pantalla presenta solamente la información necesaria para la etapa actual.

7. Actividad 6 — Prototipo

Se construyó un prototipo de fidelidad media para representar el mecanismo híbrido.

El flujo incluye:

Inicio.

Consulta de disponibilidad.

Selección de horario.

Selección de fisioterapeuta.

Datos del paciente.

Resumen.

Confirmación.

Código de cita.

Detalle.

Reagendamiento.

Cancelación.

Los principales criterios HCI aplicados fueron:

navegación hacia adelante y atrás,

persistencia de información,

estado visible,

prevención de horarios ocupados,

confirmación antes de cancelar,

mensajes próximos a los campos,

controles consistentes,

foco visible,

estados que utilizan texto además de color.

8. Actividad 7 — Validación

Se diseñó un protocolo para probar el prototipo con usuarios representativos.

Las tareas propuestas son:

Encontrar un horario disponible.

Registrar una cita.

Cambiar la fecha o fisioterapeuta.

Cancelar la cita.

Volver a agendar después de una cancelación.

Datos a registrar

Para cada participante deben registrarse:

Dato

Qué representa

Éxito

Si logró completar correctamente la tarea

Tiempo

Duración total de la tarea

Acciones

Cantidad de acciones necesarias

Intervención

Si necesitó ayuda del personal/evaluador

Errores

Número y tipo de errores cometidos

Satisfacción

Percepción del participante en escala 1–5

Los participantes se identifican como:

P1

P2

P3

Los campos se mantienen preparados para ingresar resultados reales.

No se deben inventar tiempos, errores, tasas de éxito o satisfacción si las pruebas todavía no han sido ejecutadas.

9. Comprobación técnica realizada

Además del protocolo de usuarios, se realizó una comprobación técnica del prototipo.

Se revisaron:

Pantalla de inicio.

Disponibilidad.

Fisioterapeutas.

Datos del paciente.

Resumen.

Detalle.

Navegación atrás.

Persistencia.

Horarios ocupados.

Prevención de selección.

Confirmación antes de cancelar.

Reagendamiento.

Retroalimentación.

Estados.

Accesibilidad mediante etiquetas y teclado.

La comprobación técnica no sustituye la validación con personas. Son dos evaluaciones diferentes.

10. Actividad 8 — Recomendación

Con base en la matriz de decisión, se recomienda utilizar el mecanismo híbrido.

Su puntuación fue:

51/60 = 85 %

Este resultado fue superior a:

Autoagendamiento: 73,33 %

Agenda interna: 68,33 %

Solicitud con confirmación: 65 %

¿Por qué se recomienda?

Porque permite:

reducir coordinación manual,

disminuir acciones repetitivas,

mejorar la visibilidad de las citas,

prevenir conflictos,

automatizar casos normales,

mantener intervención humana para excepciones,

adaptarse a un centro con cinco fisioterapeutas.

La selección se sustenta en la matriz y en los problemas encontrados en el proceso AS-IS; no corresponde únicamente a una preferencia personal.

11. Resumen del proceso de diseño

La interfaz final se obtuvo siguiendo esta secuencia:

Proceso actual (AS-IS)
↓
Identificación de problemas y fricciones
↓
Identificación de usuarios y necesidades
↓
Comparación de mecanismos
↓
Selección del mecanismo híbrido
↓
Definición de indicadores
↓
Construcción de metáforas
↓
Aplicación de principios HCI
↓
Diseño del flujo de interacción
↓
Construcción del prototipo
↓
Comprobación técnica
↓
Protocolo de validación con usuarios

12. Diferencia entre las evaluaciones utilizadas

Es importante no confundir las tres formas de evaluación del proyecto.

Matriz de mecanismos

Utiliza una puntuación de 1 a 5 para comparar las cuatro alternativas de agendamiento.

Evaluación de metáforas

Es principalmente cualitativa y considera affordance, mapeo, consistencia, retroalimentación, lenguaje, comportamiento computacional, reglas, persistencia y riesgos.

Validación con usuarios

Registra datos observables como:

éxito,

tiempo,

acciones,

intervención,

errores,

satisfacción de 1 a 5.

Resultado principal

El trabajo concluye que el mecanismo híbrido es la alternativa más adecuada para GABO'S porque ofrece un equilibrio entre automatización y control humano y permite construir una interfaz más clara, consistente y preventiva frente a los problemas encontrados en el proceso actual.

Asignatura: Interacción Humano-Computador
Caso: GABO'S Readaptación y Movimiento
Proyecto: Diseño HCI de un mecanismo para la gestión de citas
