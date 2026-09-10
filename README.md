# 🏥 Centro de Fisioterapia GABO'S - Sistema de Gestión de Citas (Propuesta HCI)

![HCI & Usability](https://img.shields.io/badge/Focus-HCI%20%26%20Usability-blue.svg)
![Academic Project](https://img.shields.io/badge/UTA-Facultad%20de%20Ingenier%C3%ADa%20en%20Sistemas-red.svg)
![Ciclo Academico](https://img.shields.io/badge/Ciclo-Julio--Diciembre%202026-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

Este repositorio contiene la propuesta de reingeniería de interfaz, interacción humano-computador (HCI), modelado de usabilidad y diseño de prototipado para la gestión integral de citas del centro de fisioterapia **GABO'S Readaptación y Movimiento**.

---
* **Asignatura:** Interacción Humano Computador (IHC)
* **Docente:** Ing. Caiza Caizabuano José Rubén
* **Institución:** Universidad Técnica de Ambato — Facultad de Ingeniería en Sistemas, Electrónica e Industrial (FISEI)
* **Semestre / Paralelo:** Quinto "B" (Carrera de Software)
---

## 🎯 Objetivos del Proyecto

* **General:** Analizar la situación real del proceso de gestión de citas en el centro de fisioterapia GABO'S y construir una propuesta sustentada en principios de HCI, usabilidad, accesibilidad, modelos mentales y metáforas de interfaz.
* **Específicos:**
  1. Modelar el proceso actual (AS-IS) e identificar los principales actores, necesidades y puntos de fricción cognitivos y tecnológicos.
  2. Comparar diferentes mecanismos de agendamiento y operacionalizar la eficiencia mediante indicadores observables y fórmulas cuantificables.
  3. Diseñar metáforas de interfaz, un prototipo navegable y un protocolo de validación empírica adaptado al contexto operativo del centro.

---
## 👥 Equipo y Distribución de Actividades

| Integrante | Usuario GitHub | Rol | Actividad | Entregable Principal | Issue |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **Elizabeth De la Cruz** | `Elizabeth1925` | Especialista en Prototipado | Actividad 1 & 2 | Diagrama AS-IS, Matriz de Fricciones, Matriz de Necesidades | #1 |
| **Verónica Jaque** | `ArteMisa82` | Diseñador de UX/UI | Actividad 3 & 4 | Matriz de Decisión, Operacionalización de Indicadores | #2 |
| **Andrew Lara** | `Alara05` | Evaluador de Usabilidad y Accesibilidad | Actividad 5 | Metáforas HCI, Fundamentos de Diseño, Wireflow | #3 |
| **Sebastián Vaca** | `Sebas2h` | Líder de Proyecto HCI/UX | Actividad 6 & 7 | Prototipos Interactivos (Figma/Penpot), Protocolo de Validación | #4 |

-----

## 🎨 Prototipo Interactivo

Se desarrolló un prototipo interactivo de la aplicación web con el objetivo de representar el flujo de navegación y las principales funcionalidades del sistema.

### 🔗 Acceso al prototipo

[![Figma](https://img.shields.io/badge/Figma-Prototipo-000000?style=for-the-badge&logo=figma&logoColor=white)](https://www.figma.com/make/m3GEL95cTFQDMWCv6SDo7P/Prototipo-web-de-citas?t=joW9vl3cCfyKkIIp-0)

👉 [Abrir prototipo en Figma](https://www.figma.com/make/m3GEL95cTFQDMWCv6SDo7P/Prototipo-web-de-citas?t=joW9vl3cCfyKkIIp-0)


**Herramienta:** Figma  
**Tipo:** Prototipo web interactivo

## 📌 Situación Actual (Análisis AS-IS)

GABO'S es un centro de fisioterapia atendido por **5 fisioterapeutas**. Actualmente, la gestión de citas presenta una alta fragmentación:
* **Mecanismos actuales:** Solicitudes recibidas por WhatsApp, registro en una agenda física en recepción e historias clínicas almacenadas en Google Drive.
* **Flujo Operativo AS-IS:**
  `Solicitud por WhatsApp` ➔ `Revisión de Mensajes` ➔ `Consulta en Agenda Física` ➔ `Coordinación Manual con Fisioterapeuta` ➔ `Registro y Confirmación Manual`

### Puntos de Fricción e Problemas HCI Identificados
* **Baja visibilidad del estado:** El paciente no sabe si su mensaje fue leído ni en qué estado se encuentra su solicitud.
* **Carga cognitiva y errores de transcripción:** El personal debe duplicar información manualmente entre chats y la libreta física.
* **Falta de fuente centralizada:** Inexistencia de validaciones automáticas contra solapamientos de horario (*double-booking*).

---

## ⚙️ Comparación de Mecanismos de Agendamiento

Se compararon 4 alternativas mediante una matriz de evaluación con 12 criterios de ponderación (Escala 1 a 5):

1. **Agenda Digital Interna** (Puntaje: 41/60): Factible pero mantiene alta carga administrativa.
2. **Solicitud con Confirmación** (Puntaje: 39/60): Conserva control pero no elimina tiempos muertos de espera.
3. **Autoagendamiento Directo** (Puntaje: 44/60): Altamente eficiente, pero rigido frente a excepciones de tratamiento.
4. **Mecanismo Híbrido** *(Seleccionado - Puntaje: 51/60 | 85.00%)*: Automatiza reservas estándar de disponibilidad en tiempo real y deriva casos especiales o excepciones al personal administrativo.

---

## 🎨 Metáforas de Interacción y Principios HCI

Para mantener coherencia con el modelo mental del usuario se implementaron 3 metáforas clave:

```
+-----------------------------------------------------------------------------------+
|                                METÁFORAS DE INTERFAZ                               |
+-----------------------------------------------------------------------------------+
| 🗓️ 1. AGENDA / CALENDARIO   | Responde a: "¿Qué horario puedo elegir?"              |
|                              | Representa bloques horarios, días y disponibilidad.   |
+------------------------------+----------------------------------------------------+
| 🧭 2. RUTA GUIADA (Wizard)   | Responde a: "¿Qué debo hacer para reservar?"       |
|                              | Wizard paso a paso (Horario ➔ Pro ➔ Datos ➔ Conf) |
+------------------------------+----------------------------------------------------+
| 🎫 3. COMPROBANTE DE RESERVA | Responde a: "¿Mi cita quedó registrada?"           |
|                              | Ficha digital resumen con código único (e.g. GAB-5529)|
+-----------------------------------------------------------------------------------+
```

### Principios de Accesibilidad & Usabilidad Aplicados
* **Affordance & Mapping:** Botones e inputs con jerarquía clara; horarios ocupados deshabilitados explícitamente.
* **Retroalimentación en Tiempo Real:** Modificación de estados visible (`Disponible` ➔ `Seleccionado` ➔ `Confirmado`).
* **Accesibilidad Universitaria:** Uso de contraste visual elevado, etiquetas WCAG, navegación estructurada por teclado y representación de estados que no dependen únicamente del color.

---

## 📊 Operacionalización de la Eficiencia

| Indicador | Definición / Fórmula | Método de Medición |
| :--- | :--- | :--- |
| **Tiempo Administrativo Activo** | $\sum \text{Intervalos de trabajo activo del personal}$ | Cronometraje directo por tarea sin contar esperas pasivas. |
| **Tiempo Total de Operación** | $T_{\text{final}} - T_{\text{inicial}}$ | Marca de tiempo desde inicio del paciente hasta confirmación. |
| **Acciones del Usuario / Personal** | $\sum (\text{Clics} + \text{Teclas} + \text{Pasos})$ | Conteo sistemático de interacciones en prototipo. |
| **Tasa de Intervención Humana** | $\left( \frac{\text{Operaciones con intervención personal}}{\text{Total de operaciones}} \right) \times 100$ | Registro binario (Sí/No) por sesión de uso. |
| **Tasa de Éxito en Tareas** | $\left( \frac{\text{Tareas completadas sin error crítico}}{\text{Total de intentos}} \right) \times 100$ | Comprobación de estado final correcto. |

---

## 📱 Prototipado y Flujo del Sistema

El prototipo de fidelidad media/alta fue diseñado integrando las siguientes pantallas y estados:

1. **Pantalla de Inicio:** Landing page limpia con llamados a la acción claros (`Agendar cita` / `Consultar mi cita`).
2. **Disponibilidad y Horarios:** Selector de fecha en formato calendario y parrilla de bloques horarios por color/texto.
3. **Selección de Fisioterapeuta:** Galería con los 5 profesionales del centro y opción "Cualquier fisioterapeuta disponible".
4. **Formulario de Datos:** Entrada de datos del paciente con validaciones en tiempo real cerca del campo.
5. **Resumen y Ticket de Confirmación:** Comprobante final con código único de reserva (`GAB-XXXX`) y accesos directos para reagendar o cancelar.

---

## 🧪 Protocolo de Pruebas y Validación con Usuarios

Se formuló un protocolo de pruebas de usabilidad empírica con **3 participantes (P1, P2, P3)** ejecutando 5 tareas clave:
1. Encontrar un horario disponible.
2. Registrar una cita completa.
3. Cambiar fecha o fisioterapeuta durante el proceso.
4. Cancelar una cita existente mediante código.
5. Volver a agendar una cita tras la cancelación.

---

## 📄 Estructura del Repositorio

```text
.
├── README.md                              # Documentación principal del proyecto
├── docs/
│   └── Informe_GABOS_Final_Completado.pdf # Informe académico en PDF completo
└── assets/
    ├── flow-asis.png                      # Diagrama del proceso actual AS-IS
    ├── flow-tobe.png                      # Diagrama del proceso propuesto (Híbrido)
    └── prototype-screens/                 # Capturas del prototipo de alta fidelidad
```

---

## 💡 Conclusión y Recomendaciones

* **Conclusión Principal:** La sustitución de la agenda física por un **mecanismo híbrido** centralizado reduce la sobrecarga cognitiva del personal administrativo, elimina errores de transcripción manual y provee transparencia inmediata al paciente sobre la disponibilidad del centro.
* **Recomendaciones para Desarrollo Futuro:**
  1. Incorporar la selección explícita del tipo de servicio/tratamiento previo al horario.
  2. Implementar un diálogo modal de confirmación antes de la sustitución de horarios en el flujo de reagendamiento.
  3. Ejecutar la batería de pruebas de campo con pacientes reales del centro GABO'S.

---
*Universidad Técnica de Ambato - Facultad de Ingeniería en Sistemas, Electrónica e Industrial - 2026*



