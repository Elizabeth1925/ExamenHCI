# 🏥 Sistema de Gestión de Citas — Análisis, Diseño HCI y Prototipado

Proyecto de análisis, optimización y prototipado de interfaz para el sistema de gestión de citas de fisioterapia, aplicando principios de Interacción Humano-Computador (HCI).

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

[![Figma](https://img.shields.io/badge/Figma-Prototipo-000000?style=for-the-badge&logo=figma&logoColor=white)](https://www.figma.com/make/aKeX0RpcoIDoCbMUTojEhz/Prototipo-web-de-citas?p=f&t=MRvE37sOPQZfsP0i-0)

**Herramienta:** Figma  
**Tipo:** Prototipo web interactivo

👉 [Abrir prototipo en Figma](https://www.figma.com/make/aKeX0RpcoIDoCbMUTojEhz/Prototipo-web-de-citas?p=f&t=MRvE37sOPQZfsP0i-0)


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
