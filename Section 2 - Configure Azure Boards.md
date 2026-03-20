# Azure Boards 101

## ¿Qué es Azure Boards?

Azure Boards es el servicio de Azure DevOps que permite **gestionar, organizar y hacer seguimiento del trabajo** de un equipo mediante elementos como tareas, bugs, épicas, historias de usuario, sprints y tableros Kanban.

Su objetivo es proporcionar transparencia, priorización y una buena planificación del trabajo.

---

# Componentes Principales

## Work Items (Elementos de Trabajo)

Los Work Items representan cualquier unidad de trabajo a realizar. Pueden ser:

- Épicas: grandes bloques de funcionalidad.
- Features: partes importantes dentro de una épica.
- User Stories / Product Backlog Items: funcionalidades para el usuario.
- Tasks: trabajo técnico o pasos específicos.
- Bugs: errores en la aplicación.

Cada elemento tiene un estado, prioridad, asignación y seguimiento histórico.

---

## Boards (Tableros)

Los tableros de Azure Boards implementan un **tablero Kanban** donde puedes:

- Ver el flujo de trabajo del equipo.
- Mover los elementos según su estado.
- Añadir tareas o historias rápidamente.
- Visualizar bloqueos o acumulaciones.

Son ideales para equipos que siguen **Kanban** o incluso híbridos.

---

## Backlogs

Los Backlogs son listas priorizadas de elementos de trabajo. Se usan para:

- Desarrollar el plan del proyecto.
- Preparar qué se hará en futuros sprints.
- Ordenar elementos según su prioridad.
- Añadir, mover, desglosar y reorganizar historias, tareas o bugs.

Los Product Owners suelen trabajar aquí.

---

## Sprints

Un sprint es un **periodo corto y limitado en el tiempo** donde el equipo se compromete a completar trabajo planificado. Normalmente duran entre 1 y 4 semanas.

En Azure Boards puedes:

- Planificar sprints.
- Añadir tareas por historia de usuario.
- Revisar la capacidad del equipo.
- Hacer seguimiento del burndown (progreso).

---

## Dashboards

Los Dashboards permiten crear paneles personalizados con:

- Gráficos de progreso.
- Burndown charts.
- Estado de bugs.
- KPI del equipo.
- Widgets configurables.

Ayudan a visualizar información clave del proyecto.

---

# Tipos de Proceso en Azure Boards

Azure DevOps ofrece diferentes procesos para adaptar el modelo de trabajo a cada equipo.

## Basic

Proceso sencillo con pocos tipos de Work Items. Ideal para equipos no formales o proyectos pequeños.

## Agile

Basado en metodologías ágiles con historias de usuario, tareas y bugs. Es el más usado en general.

## Scrum

Implementa terminología propia de Scrum, con Product Backlog Items, Sprints y Tareas.

## CMMI (Capability Maturity Model Integration)

Proceso orientado a organizaciones que requieren más formalidad, gobernanza y documentación. Incluye más estados, tipos de elementos y flujos.

---

# Flujo de Trabajo Básico

Un workflow sencillo utilizado en la mayoría de tableros.

- **To Do**: elementos pendientes.
- **Doing**: trabajo en curso.
- **Done**: trabajo completado y validado.

Puedes añadir estados intermedios dependiendo del proceso.

---

# Definir un Sprint

Un sprint es:

- Un periodo definido (por ejemplo, 2 semanas).
- Un time-box donde el equipo acuerda terminar ciertos elementos de trabajo.
- La unidad fundamental de planificación en Scrum.

En Azure Boards:

- Seleccionas un sprint.
- Añades elementos (User Stories, PBIs, Tasks).
- Configuras capacidad del equipo.
- Haces seguimiento con el burndown.

---

# Elegir la Vista Correcta del Trabajo

Azure Boards ofrece diferentes vistas según lo que necesites hacer.

## Queries

Sirven para:

- Reportes simples.
- Hacer actualizaciones masivas.
- Asignar o reasignar elementos.
- Enviar listas de elementos por correo.

Puedes crear queries, guardarlas y compartirlas.

Tipos comunes:

- Assigned to you.
- Work items que sigues.
- Elementos donde fuiste mencionado.
- Elementos vistos, actualizados o creados recientemente.

---

## Boards (Vista Kanban)

Útiles para:

- Implementar Kanban.
- Ver el flujo de trabajo visualmente.
- Añadir elementos rápidamente.
- Identificar cuellos de botella.

---

## Backlogs (Vista de Lista Priorizada)

Sirven para:

- Planificar sprints.
- Desarrollar el plan general del proyecto.
- Reordenar la prioridad del trabajo.
- Filtrar y etiquetar según criterio.

---

## Sprints (Vista Scrum)

Ideales cuando trabajas con Scrum:

- Añadir tareas a cada historia de usuario.
- Configurar capacidad del equipo.
- Monitorizar el burndown.
- Revisar el compromiso del sprint.