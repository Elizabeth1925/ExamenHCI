# 🏥 Sistema de Gestión de Citas — Análisis, Diseño HCI y Prototipado

Proyecto de análisis, optimización y prototipado de interfaz para el sistema de gestión de citas de fisioterapia, aplicando principios de Interacción Humano-Computador (HCI).

---

## 👥 Equipo y Distribución de Actividades

| Estudiante | Actividades Asignadas | Entregables Principales |
| :--- | :--- | :--- |
| **Elizabeth De la Cruz** | **Actividad 1 & Actividad 2** | Flujo AS-IS, Diagrama del proceso actual, Matriz de fricciones, Matriz de Usuarios y Necesidades. |
| **Verónica Jaque** | **Actividad 3 & Actividad 4** | Comparación de mecanismos (Matriz de decisión), Operacionalización de la eficiencia, Fórmulas de indicadores. |
| **Andrew Lara** | **Actividad 5 & Preparación Wireflow** | Metáforas de Interfaz (HCI), Análisis de usabilidad y reglas computacionales, Wireflow preliminar. |
| **Sebastián Vaca** | **Actividad 6 & Actividad 7** | Prototipo interactivo (Figma/Penpot), Pantallas obligatorias, Manejo de estados/accesibilidad, Protocolo de validación. |

---

## 📋 Detalle de Actividades y Entregables

### 📌 Elizabeth De la Cruz — Actividades 1 y 2

#### Actividad 1: Analizar el Proceso Actual (AS-IS)
Análisis de cómo se gestionan actualmente las citas en el centro de fisioterapia antes de proponer una solución tecnológica.

* **Acciones Realizadas:**
  * **Flujo AS-IS:**
    1. Paciente solicita cita por WhatsApp.
    2. Personal administrativo revisa el mensaje.
    3. Consulta la agenda física.
    4. Revisa disponibilidad de horarios.
    5. Coordina directamente con el fisioterapeuta.
    6. Registra la cita manualmente en la agenda física.
    7. Confirma la cita por WhatsApp.
    8. En caso de cambios o cancelaciones, el proceso se realiza manualmente.
  * **Actores Identificados:** Paciente, Personal administrativo, Fisioterapeuta y Administrador.
  * **Información Necesaria:** Datos del paciente, Fisioterapeuta asignado, Fecha, Hora, Estado de disponibilidad y Estado de la cita.

* **Diagrama del Flujo AS-IS:**

```mermaid
graph TD
    A[Paciente solicita cita vía WhatsApp] --> B[Personal revisa mensaje]
    B --> C[Consulta agenda física]
    C --> D{¿Existe disponibilidad?}
    D -- Sí --> E[Coordina con Fisioterapeuta]
    E --> F[Registra cita en agenda física ✍️]
    F --> G[Confirma por WhatsApp ⏳]
    D -- No --> H[Notifica indisponibilidad al paciente]
    
    subgraph Puntos de Fricción
        F
        G
    end


**Puntos de Fricción Identificados:**

*   **Esperas:** Retrasos en la respuesta debido a la gestión manual de WhatsApp.
*   **Acciones Duplicadas:** Verificación doble de agendas entre el personal administrativo y los fisioterapeutas.
*   **Transcripciones Manuales:** Transferencia constante de información de chats a registros en papel.
*   **Posibles Errores:** Riesgo de conflictos de horarios o sobre-reservas.

**Problemas Adicionales:**

*   **Retroalimentación:** Los pacientes desconocen el estado de su solicitud hasta recibir respuesta.
*   **Visibilidad:** Imposibilidad de ver la disponibilidad de citas en tiempo real.
*   **Consistencia:** Discrepancias entre los registros físicos y las solicitudes pendientes en el chat.
*   **Factores Humanos:** Alta carga cognitiva y riesgo de olvido en el personal administrativo.
*   **Factores Tecnológicos:** Información descentralizada (WhatsApp y agenda física) sin sincronización automática.

**Actividad 2: Usuarios y Necesidades**

Se realizó un estudio detallado de los perfiles de usuario, sus metas y dificultades actuales en la gestión de citas.

**Matriz de Usuarios y Necesidades:**

| Usuario                 | Objetivo                       | Necesidad                                | Dificultad Actual                                   |
| :---------------------- | :----------------------------- | :--------------------------------------- | :-------------------------------------------------- |
| Paciente                | Conseguir una cita             | Ver disponibilidad fácilmente            | Espera prolongada por WhatsApp                      |
| Fisioterapeuta          | Organizar sus citas            | Agenda siempre actualizada               | Información dispersa y desactualizada               |
| Personal Administrativo | Gestionar citas                | Registro centralizado de información     | Trabajo manual repetitivo y propenso a errores      |
| Administrador           | Supervisar el centro           | Indicadores e información consolidada    | Falta de reportes y métricas consolidadas           |

**Definición del Usuario Principal:** El paciente es el usuario principal; la interfaz debe enfocarse en el autoservicio y la simplicidad.
**Conocimientos Tecnológicos Esperados:** Nivel básico-medio (uso habitual de smartphones y navegadores web).
**Alcance:** Estrictamente la gestión operativa de citas (agendar, consultar, reagendar, cancelar).

**Actividad 3: Comparación de Mecanismos de Solución**

Se evaluaron cuatro alternativas para la gestión de citas mediante una matriz de decisión:

1.  **Agenda Digital Interna:** Manejo centralizado solo por el personal administrativo.
2.  **Solicitud con Confirmación:** El paciente solicita un horario y un operador valida manualmente.
3.  **Autoagendamiento:** El paciente reserva de forma 100% autónoma en tiempo real.
4.  **Mecanismo Híbrido:** Autoagendamiento con opción de gestión manual/asistida para casos excepcionales.

**Matriz de Decisión (Escala 1-5):**

| Criterio              | Agenda Digital Interna | Solicitud con Confirmación | Autoagendamiento | Mecanismo Híbrido |
| :-------------------- | :--------------------- | :------------------------- | :--------------- | :---------------- |
| Tiempo administrativo | 2                      | 2                          | 5                | 4                 |
| Tiempo de confirmación | 3                      | 2                          | 5                | 4                 |
| Acciones del paciente | 4                      | 3                          | 4                | 4                 |
| Acciones del personal | 2                      | 2                          | 5                | 4                 |
| Intervención humana   | 2                      | 2                          | 5                | 4                 |
| Prevención de conflictos | 4                      | 4                          | 4                | 5                 |
| Facilidad de uso      | 4                      | 4                          | 4                | 4                 |
| Accesibilidad         | 4                      | 4                          | 4                | 4                 |
| Privacidad            | 4                      | 4                          | 4                | 4                 |
| Factibilidad          | 5                      | 4                          | 3                | 4                 |
| **TOTAL**             | **34**                 | **31**                     | **43**           | **42**            |

**Justificación y Selección:** Aunque el Autoagendamiento obtuvo un puntaje ligeramente superior, se seleccionó el Mecanismo Híbrido por su flexibilidad para imprevistos y excepciones, manteniendo la máxima prevención de conflictos.

**Actividad 4: Operacionalización de la Eficiencia**

Definición de indicadores cuantitativos para evaluar el sistema, más allá del tiempo global.

**Definición de Operaciones Principales e Indicadores:**

| Operación                | Inicio                          | Final                             | Indicadores Asociados                                                                                                                                                                                                                                  |
| :----------------------- | :------------------------------ | :-------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Consultar disponibilidad | Selección de fecha/especialista | Despliegue de horarios libres     | Tiempo de consulta, Acciones del paciente                                                                                                                                                                                                    |
| Registrar cita           | Usuario selecciona horario      | Cita confirmada                   | Tiempo administrativo activo ($\sum \text{Tiempo de trabajo manual dedicado a procesar una cita}$), Acciones del Personal/Paciente ($\text{Número de clics o pasos requeridos para completar el proceso}$), Errores, Tasa de éxito ($\left( \frac{\text{Citas completadas sin error}}{\text{Total de intentos de reserva}} \right) \times 100$) |
| Modificar cita           | Selección de opción "Cambiar"   | Nuevo horario asignado            | Tiempo total, Reprocesos, Intervención humana                                                                                                                                                                                                |
| Cancelar cita            | Abre detalle de cita            | Horario liberado en el sistema    | Tiempo, Acciones del usuario, Satisfacción                                                                                                                                                                                                   |
| Reagendar cita           | Solicitud de reasignación       | Confirmación de nuevo slot        | Tiempo activo, Tasa de errores/reprocesos ($\left( \frac{\text{Número de equivocaciones o reintentos}}{\text{Total de citas gestionadas}} \right) \times 100$), Intervención                                                                |

**Actividad 5: Metáforas de Interfaz e Ingeniería HCI**

Diseño de metáforas visuales basadas en modelos mentales del usuario para simplificar el aprendizaje y la usabilidad.

**Metáforas Propuestas:**

*   **Agenda / Calendario Digital:** Transforma la agenda de papel en un calendario interactivo.
*   **Ruta Guiada / Wizard:** Guía al usuario paso a paso (Disponibilidad $\rightarrow$ Fisioterapeuta $\rightarrow$ Datos $\rightarrow$ Resumen $\rightarrow$ Confirmación).
*   **Comprobante de Reserva / Ticket:** Resumen de la reserva en formato de pase digital.

**Estructura de Análisis HCI por Metáfora:**

| Dominio Fuente    | Elemento Digital    | Etiqueta / Mensaje              | Comportamiento                       | Riesgo Identificado                               |
| :---------------- | :------------------ | :------------------------------ | :----------------------------------- | :------------------------------------------------ |
| Agenda Física     | Bloque de horario   | "Horario Disponible / Ocupado"  | Cambia de color al seleccionar       | Confundir horas pasadas con disponibles          |
| Camino / Ruta     | Barra de progreso   | "Paso 2 de 4: Fisioterapeuta"   | Avanza/retrocede sin perder datos    | Perder el contexto si se recarga la página      |
| Ticket en Papel   | Tarjeta de resumen  | "Código de Reserva #1234"       | Muestra botón de descarga/impresión | Pensar que se debe imprimir obligatoriamente    |

**Fundamentos HCI Considerados:** Usabilidad, Affordance & Mapping, Consistencia & Feedback, Reglas y Validaciones.

**Preparación del Wireflow para la Actividad 6:**

[INICIO] $\rightarrow$ [DISPONIBILIDAD] (Calendario Digital) $\rightarrow$ [FISIOTERAPEUTA] $\rightarrow$ [DATOS PACIENTE] $\rightarrow$ [RESUMEN] (Comprobante/Ticket) $\rightarrow$ [CONFIRMACIÓN] $\rightarrow$ [DETALLE CITA] $\rightarrow$ [REAGENDAR] / [CANCELAR].

**Actividad 6: Prototipo HCI en Figma / Penpot**

Creación de un prototipo funcional de alta/media fidelidad.

**Pantallas Diseñadas:** Inicio de gestión, consulta de disponibilidad, selección de fisioterapeuta, datos del paciente, resumen de reserva, confirmación, detalle de cita, reagendamiento, modal de cancelación.

**Manejo de Estados de Interfaz:** Cargando, éxito/error, sin disponibilidad/horario ocupado.

**Criterios de Accesibilidad (WCAG):** Contraste de colores elevado, focus visible para navegación con teclado, botones con área de toque adecuada ($>44\times44\text{ px}$), mensajes de error claros e independientes del color.

**Actividad 7: Protocolo de Validación con Usuarios**

Diseño de un plan de pruebas de usabilidad para medir la efectividad del prototipo.

**Tareas Obligatorias de la Evaluación:** Encontrar un horario, registrar una cita, reagendar, cancelar una cita, volver a agendar.

**Matriz del Protocolo de Pruebas:**

| Participante | Tarea           | Criterio de Éxito                      | Medición de Tiempo                  | Acciones / Clics                      | Intervenciones                     | Errores / Reprocesos                          |
| :----------- | :-------------- | :------------------------------------- | :---------------------------------- | :------------------------------------ | :--------------------------------- | :-------------------------------------------- |
| P1           | Agendar cita    | Llega a la pantalla de confirmación    | Desde Inicio hasta Cita Confirmada  | Clics requeridos vs realizados        | Preguntas o bloqueos               | Clics en elementos no interactivos            |
| P2           | Reagendar       | Asigna un nuevo horario con éxito      | Desde Detalle hasta Nueva Confirmación | Navegación dentro del formulario      | Ayudas brindadas por el evaluador  | Intentos de selección de horarios ocupados    |
| P3           | Cancelar        | El horario queda liberado en el sistema | Desde Detalle hasta Confirmación de Modal | Clics hasta confirmar en el modal      | Dificultad para encontrar la opción | Cancelación accidental                        |

**Herramientas Utilizadas:**

*   **Diagramación:** Mermaid.js / Mind42 / Diagrams.net
*   **Diseño UI/UX:** Figma / Penpot
*   **Control de Versiones:** Git & GitHub
