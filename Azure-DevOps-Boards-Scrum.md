## 1. ¿Qué es Azure Boards?

**Azure Boards** es una herramienta dentro de la plataforma **Azure DevOps** que permite gestionar el trabajo de un equipo mediante metodologías ágiles como **Scrum** o **Kanban**.  
Su función principal es ayudar a planificar, hacer seguimiento y visualizar el progreso del proyecto.

Azure Boards proporciona:

- Gestión de **Work Items** (elementos de trabajo).
- **Dashboards** con métricas.
- **Backlogs** para organizar el trabajo.
- **Boards** (tableros) para visualizar estados.
- **Sprints** para planificar ciclos de trabajo cortos.

---

## 2. Conceptos Clave de Scrum para Usar Azure Boards

### Scrum

Es un **marco de trabajo ágil** para gestionar proyectos. Se organiza en ciclos cortos llamados **Sprints**, donde el equipo entrega valor de forma incremental.

### Sprint

Periodo de trabajo de duración fija (normalmente 2–4 semanas) donde se desarrolla un conjunto de funcionalidades.

### Product Backlog

Lista priorizada de todo el trabajo pendiente del proyecto. Evoluciona constantemente.

### Sprint Backlog

Selección del trabajo que el equipo se compromete a realizar durante un Sprint.

### Roles importantes

- **Product Owner (PO):** Prioriza el trabajo y define el valor del producto.
- **Scrum Master:** Facilita el proceso y elimina impedimentos.
- **Development Team:** Personas que diseñan, desarrollan, prueban y entregan el producto.

---

## 3. Work Items en Azure Boards

Los _Work Items_ son elementos que representan trabajo. En Scrum, se utilizan principalmente:

### **Product Backlog Item (PBI)**

Elemento que describe una funcionalidad o requisito solicitado por el usuario o negocio.  
Representa el **qué** se quiere construir, no el _cómo_.

### **Task (Tarea)**

Trabajo más detallado que debe ejecutarse para completar un PBI.  
Describen el **cómo** se implementará esa funcionalidad.

### **Bug**

Registro de un error o comportamiento incorrecto del producto.

### **Epic**

Conjunto grande de funcionalidades relacionadas entre sí.  
Un Epic suele dividirse en PBIs.

### **Feature**

Funcionalidad mediana compuesta por varios PBIs; está entre un Epic y un PBI.

---

## 4. Backlogs en Azure Boards

### 4.1. Product Backlog

Azure Boards permite ver los PBIs ordenados por prioridad.  
Incluye información como:

- Título
- Descripción
- Criterios de aceptación
- Tamaño o historia de usuario
- Estado
- Etiquetas

### 4.2. Sprint Backlog

Creado por el equipo en la **Sprint Planning**.  
Incluye PBIs seleccionados para el Sprint, cada uno con sus tareas.

### Priorización

Se basa en criterios como valor al negocio, impacto, urgencia y dependencias.

---

## 5. Boards (Tableros Kanban)

Los tableros muestran el flujo de trabajo visualmente.

Columnas típicas:

- **To Do** (Pendiente)
- **In Progress** (En progreso)
- **Review / Testing** (Revisión / Testing)
- **Done** (Completado)

Beneficios:

- Fácil seguimiento del estado.
- Identificación de bloqueos.
- Visualización rápida de la carga de trabajo del equipo.

---

## 6. Sprints en Azure Boards

### 6.1 Configuración del Sprint

Es necesario definir:

- Fechas exactas de inicio y fin
- PBIs seleccionados
- Tareas asociadas

### 6.2 Sprint Planning

Se divide en dos partes:

1. **Qué** trabajo entra al Sprint (decisión del equipo y del Product Owner).
2. **Cómo** se realizará (desglose en tareas).

### 6.3 Daily Scrum

Reunión de 15 minutos donde cada miembro revisa:

- Lo que hizo ayer
- Lo que hará hoy
- Si tiene algún impedimento

Azure Boards ayuda mostrando:

- Trabajo asignado
- Avance de tareas
- Bloqueos registrados

### 6.4 Sprint Review

Demostración del producto construido durante el Sprint.

### 6.5 Sprint Retrospective

Revisión interna para mejorar el proceso.

---

## 7. Métricas y Reportes

Azure Boards ofrece herramientas para medir el progreso:

### **Burndown Chart (Gráfico de quemado)**

Muestra cómo disminuye el trabajo pendiente del Sprint día a día.

### **Velocity Chart**

Indica cuántos PBIs (o puntos) el equipo ha completado en los últimos Sprints.  
Sirve para estimar la capacidad futura del equipo.

### **Cumulative Flow Diagram**

Gráfico que ayuda a detectar cuellos de botella visualizando el flujo del trabajo.

---

## 8. Buenas Prácticas al Usar Azure Boards

1. **Mantener los Work Items actualizados**.
2. **Estimar PBIs con Story Points** para medir el esfuerzo (no tiempo).
3. **Desglosar las tareas** para facilitar el seguimiento.
4. **Evitar Sprints sobrecargados** revisando la Velocidad.
5. Usar **comentarios y links** para mejorar la trazabilidad.
6. Revisar diariamente los tableros para evitar bloqueos.
7. Utilizar **etiquetas** y **áreas** para organizar mejor el trabajo.
8. Hacer que los criterios de aceptación sean claros y revisables.

---

## 9. Flujo de Trabajo Típico con Azure Boards en Scrum

1. El Product Owner añade y prioriza PBIs al **Product Backlog**.
2. En el **Sprint Planning**, el equipo selecciona PBIs y los convierte en tareas.
3. Durante el Sprint, los miembros avanzan el trabajo moviendo elementos en el **Board**.
4. El equipo revisa métricas como **Burndown** y **Boards** en los **Daily**.
5. Se presenta el incremento del producto en la **Sprint Review**.
6. Se analizan mejoras del proceso en la **Retrospective**.