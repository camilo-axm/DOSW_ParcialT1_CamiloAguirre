# 📄 Requerimientos del Sistema

## 1. Lista general de requerimientos

El sistema de TutoECI tiene los siguientes requerimientos:

### 1.1 Requerimientos funcionales

El sistema de TutoEci debe tener las siguientes capacidades:

1. El sistema debe permitir que los estudiantes puedan solicitar tutorías indicando una preferencia de asignación 
2. En el sistema deben existir tipos de usuarios(Solicitantes: Estudiantes de Pregado, Tutores: Profesores, Tutores:Estudiates)
3. Para su funcionamiento, TutoECI debe interactuar con dos sistemas externos. No debe
guardar información redundante localmente


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
| **Diagrama de caso de uso** | ![Diagrama_de_casos_de_uso_RF1](../images/Diagrama_de_casos_de_uso_RF1.png)|
| **Poscondiciones** | El torneo queda creado en el sistema con estado pendiente, disponible para que un organizador cambie su estado posteriormente. |

### 2.2 Requerimiento Funcional 2

| Campo | Descripción |
|------|-------------|
| **ID** | RF-02 |
| **Nombre del requerimiento** | Crear equipo |
| **Descripción** | El sistema debe permitir a un capitan crear un equipo, ingresando la informacion basica del mismo. |
| **Precondiciones** | El usuario debe estar autenticado como capitan. |
| **Actor** | Capitan |
| **Flujo principal** | El capitan solicita crear un equipo --> El sistema solicita la informacion del equipo --> El capitan ingresa la informacion y confirma. --> El sistema valida los datos y registra el equipo. |
| **Diagrama de caso de uso** | ![Diagrama_de_casos_de_uso_RF2](../images/Diagrama_de_casos_de_uso_RF2.png) |
| **Poscondiciones** | El equipo queda creado en el sistema, disponibilidad para que el capitan lo registre posteriormente en un torneo activo. |



