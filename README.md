# 🏥 Sistema de Gestión de Citas de Fisioterapia
> **Análisis, Diseño HCI y Prototipado de Interfaz**

Proyecto enfocado en la reingeniería, optimización de procesos y diseño de interacción humano-computador (HCI) para la gestión operativa de citas médicas en un centro de fisioterapia.

---

## 👥 Equipo de Trabajo y Distribución de Roles

| Estudiante | Actividades Asignadas | Entregables Clave |
| :--- | :--- | :--- |
| **Elizabeth De la Cruz** | **Actividades 1 & 2** | • Flujo AS-IS (Diagrama Mermaid)<br>• Matriz de Puntos de Fricción<br>• Matriz de Usuarios y Necesidades |
| **Verónica Jaque** | **Actividades 3 & 4** | • Matriz de Decisión de Soluciones<br>• Operacionalización de Eficiencia<br>• Fórmulas e Indicadores Cuantitativos |
| **Andrew Lara** | **Actividad 5 & Wireflow** | • Metáforas de Interfaz (HCI)<br>• Análisis de Usabilidad y Reglas<br>• Arquitectura del Wireflow |
| **Sebastián Vaca** | **Actividades 6 & 7** | • Prototipo Interactivo (Figma/Penpot)<br>• Criterios WCAG y Estados UI<br>• Protocolo de Validación con Usuarios |

---

## 📋 Detalle de Actividades y Entregables

---

### 📌 Actividad 1: Análisis del Proceso Actual (AS-IS)

Evaluación del flujo de trabajo operativo previo a la intervención tecnológica para identificar ineficiencias en la reserva de citas.

#### Flujo de Trabajo Operativo (AS-IS)
1. **Solicitud:** El paciente envía un mensaje por WhatsApp.
2. **Revisión:** El personal administrativo lee la solicitud.
3. **Consulta:** Se busca la disponibilidad en la agenda física en papel.
4. **Coordinación:** Se valida el horario directamente con el fisioterapeuta.
5. **Registro:** Se escribe manualmente la cita en el cuaderno de agenda.
6. **Confirmación:** Se responde al paciente vía WhatsApp.
7. **Excepciones:** Los cambios y cancelaciones se gestionan manualmente por chat.

#### Diagrama de Flujo AS-IS

```mermaid
graph TD
    A[Paciente solicita cita vía WhatsApp] --> B[Personal administrativo revisa mensaje]
    B --> C[Consulta agenda física]
    C --> D{¿Existe disponibilidad?}
    
    D -- Sí --> E[Coordina con Fisioterapeuta]
    E --> F[Registra cita en agenda física ✍️]
    F --> G[Envia confirmación por WhatsApp ⏳]
    
    D -- No --> H[Notifica indisponibilidad al paciente]

    classDef friction fill:#ffdddd,stroke:#ff0000,stroke-width:2px;
    class F,G friction;
