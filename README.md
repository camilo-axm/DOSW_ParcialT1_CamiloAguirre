# DOSW_ParcialT1_CamiloAguirre


Punto 2 
# 📄 Requerimientos del Sistema

## 1. Lista general de requerimientos

El sistema de TutoECI tiene los siguientes requerimientos:

### 1.1 Requerimientos funcionales

El sistema de TutoEci debe tener las siguientes capacidades:

1. El sistema debe permitir que los estudiantes puedan solicitar tutorías indicando una preferencia de asignación.
2. Tutores - Profesores: El tiempo máximo de reserva de una sesión es de 30 minutos.
Solo pueden impartir tutorías de las materias a las que están asignados.
3. Para su funcionamiento, TutoECI debe interactuar con dos sistemas externos. No debe guardar información redundante localmente


### 1.2 Requerimientos no funcionales

El sistema de TutoEci debe tener:

1. La interfaz gráfica de usuario de TutoECI debe ser completamente adaptable (responsive
design) a dispositivos móviles y de escritorio.
2. El diseño debe incorporar la identidad visual
institucional, respetando la paleta de colores oficial del programa de Ingeniería de Sistemas
de la Escuela y empleando una tipografía legible que cumpla con los estándares mínimos
de contraste y accesibilidad web (WCAG 2.1 Nivel AA) para facilitar la lectura de horarios y
perfiles de tutores.


## 2. Diagramas de caso de uso

### 2.1 Requerimiento Funcional 1

| Campo | Descripción |
|------|-------------|
| **ID** | RF-01 |
| **Nombre del requerimiento** | Solicitar tutorías |
| **Descripción** | El sistema debe permitir que los estudiantes puedan solicitar tutorías indicando una preferencia de asignación y el sistema recomiende la mejor alternativa entre profesores y estudiantes de pregrado o posgrado. |
| **Precondiciones** | El estudiante debe estar autenticado dentro de la universidad. El estudiante puede solicitar las tutorías únicamente si estan inscritos activamente en la materia. |
| **Actor** | Estudiante |
| **Flujo principal** | El estudiante solicita una tutoría dentro de la universidad. --> El sistema solicita la informacion basica del estudiante --> El estudiante ingresa la informacion y confirma --> El sistema valida los base de datos que sea un estudiante (Pregrado) y las materias del mismo--> El sistema recomienda la mejor alternativa disponible para el estudiante -->El estudiante selecciona la monitoria --> El sistema reserva la tutoría y la confirma a NotifyMe --> NotifyMe envia una notificación al estudiante, profesor o estudiante monitor confirmando la tutoría al correo del mismo| 
| **Diagrama de caso de uso** | <img width="676" height="218" alt="image" src="https://github.com/user-attachments/assets/7a63521c-7b6c-4200-82d9-0692c49c4e24" />
|
| **Poscondiciones** | El sistema debe cambiar el estado de la monitoria de disponible a reservado. |

### 2.2 Requerimiento Funcional 2

| Campo | Descripción |
|------|-------------|
| **ID** | RF-02 |
| **Nombre del requerimiento** | Reservar sesion |
| **Descripción** |  Para los profesores tutores el sistema debe permitir reservar una sesion de máximo 30 minutos |
| **Precondiciones** | El profesor debe estar autenticado dentro de la universidad. Validar que la materia a la que va a dar la tutoría este dentro de las asignadas. |
| **Actor** | Profesor |
| **Flujo principal** | El estudiante solicita una reservar una sesión dentro de la universidad. --> El sistema solicita la informacion basica del profesor --> El profesor ingresa la informacion y confirma --> El sistema valida los base de datos que sea un profesor y la materia de la tutoría --> El sistema verifica que este disponible el espacio de tutoría --> El sistema reserva la tutoría y la confirma a NotifyMe --> NotifyMe envia una notificación al profesor de la reservación al correo del mismo. |
| **Diagrama de caso de uso** | <img width="729" height="180" alt="image" src="https://github.com/user-attachments/assets/faca24f2-8b65-42a5-bb99-15bdc4fb33a6" />
 |
| **Poscondiciones** | La reservación de la sesión queda asignada y pasa de estar disponible a reservada durante 30 minutos. |


