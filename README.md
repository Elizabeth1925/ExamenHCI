# 🏥 Sistema de Gestión de Citas — Análisis, Diseño HCI y Prototipado

Proyecto de análisis, optimización y prototipado de interfaz para el sistema de gestión de citas de fisioterapia, aplicando principios de Interacción Humano-Computador (HCI).

---

## 👥 Equipo y Distribución de Actividades

| Estudiante | Rol / Actividad | Entregable Principal |
| :--- | :--- | :--- |
| **Elizabeth De la Cruz** | Actividad 1 & 2 | Diagrama AS-IS, Matriz de Fricciones, Matriz de Necesidades |
| **Verónica Jaque** | Actividad 3 & 4 | Matriz de Decisión, Operacionalización de Indicadores |
| **Andrew Lara** | Actividad 5 | Metáforas HCI, Fundamentos de Diseño, Wireflow |
| **Sebastián Vaca** | Actividad 6 & 7 | Prototipo Interactivos (Figma/Penpot), Protocolo de Validación |

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
