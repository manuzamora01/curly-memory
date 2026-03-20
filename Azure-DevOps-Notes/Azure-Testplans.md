## 1. ¿Qué es Azure Test Plans?

**Azure Test Plans** es una herramienta dentro de **Azure DevOps** que permite gestionar y ejecutar **pruebas manuales**, **pruebas exploratorias** y hacer seguimiento de la **calidad del software**.

Sirve para:

- Organizar casos de prueba.
- Ejecutar test de manera controlada.
- Registrar resultados y errores.
- Obtener métricas de calidad.

Es especialmente útil en equipos que trabajan con metodologías Agile o Scrum.

---

## 2. ¿Por qué usar Azure Test Plans?

Antes de usar herramientas como esta, las pruebas manuales se hacían en:

- Documentos Word
- Hojas de Excel
- Aplicaciones no integradas con el código

Esto provocaba:

- Falta de trazabilidad
- Dificultad para repetir pruebas
- Poca visibilidad del estado real de calidad
- Registros incompletos de errores

**Azure Test Plans** soluciona estos problemas ofreciendo:

- Un repositorio central de pruebas
- Integración total con Work Items
- Métricas y reportes en tiempo real
- Registro de errores detallados con capturas e información automática

---

## 3. Conceptos Técnicos Fundamentales

### 3.1 Test Case (Caso de Prueba)

Es un conjunto de pasos diseñados para validar que un comportamiento del software funciona de forma correcta.

Incluye:

- Título
- Pasos a seguir
- Datos de entrada
- Resultado esperado

### 3.2 Test Suite

Conjunto de casos de prueba agrupados bajo un criterio:

- Funcionalidad
- Requisito
- Sprint
- Área del producto

### 3.3 Test Plan

Colección completa de **Test Suites** que se va a ejecutar en un periodo concreto como un Sprint.

Representa el plan de pruebas global.

### 3.4 Test Run

Ejecución real de los casos de prueba.

Al ejecutar, el tester marca cada paso como:

- Passed (Correcto)
- Failed (Falló)
- Blocked (No se puede ejecutar)

### 3.5 Bug

Registro de un defecto detectado durante las pruebas.  
Puede crearse directamente desde un Test Run.

### 3.6 Exploratory Testing

Tipo de prueba donde el tester explora el sistema libremente sin seguir pasos predefinidos.  
Azure Test Plans permite documentarla de forma automática.

---

## 4. Tipos de Pruebas en Azure Test Plans

### 4.1 Pruebas Manuales

Se basan en Test Cases con pasos definidos.  
El tester sigue el guion y marca resultados.

### 4.2 Pruebas Exploratorias

El tester prueba sin guion, registrando:

- Notas
- Capturas de pantalla
- Pasos realizados
- Bugs detectados

Muy útil cuando:

- El producto es nuevo
- No hay Test Cases escritos aún
- Se busca descubrir comportamientos inesperados

### 4.3 Pruebas Automatizadas (en relación con Pipelines)

Azure Test Plans también se integra con pruebas automáticas generadas en Azure Pipelines.  
Aunque no las crea, sí **almacena los resultados**.

---

## 5. Estructura Lógica de un Test Plan

1. **Test Plan**  
    Conjunto general de pruebas.
    
2. **Test Suites**  
    Agrupaciones temáticas o funcionales.
    
3. **Test Cases**  
    Casos de prueba ejecutables.
    
4. **Test Runs**  
    Ejecuciones programadas o espontáneas.
    

---

## 6. Integración con Azure Boards

Azure Test Plans se integra totalmente con:

- **Work Items**
- **Product Backlog Items (PBIs)**
- **Bugs**
- **Tasks**

Beneficios:

- Cada Test Case puede vincularse a un PBI.
- Los Bugs se crean directamente desde la ejecución.
- La trazabilidad es completa: _Requisito → Caso de Prueba → Ejecución → Bug_.

---

## 7. Métricas y Reportes de Calidad

Azure Test Plans ofrece información visual como:

### Resultado de ejecuciones

- Passed
- Failed
- Blocked
- Not Run

### Trazabilidad

Relaciona PBIs con los Test Cases que los validan.

### Código de estado

Gráficos que muestran progreso, cobertura y fallos.

### Historias de calidad por Sprint

Permite evaluar la estabilidad antes de una entrega.

---

## 8. Buenas Prácticas al Usar Azure Test Plans

1. **Mantener Test Cases simples y claros**.
2. Usar un lenguaje descriptivo en los pasos.
3. Vincular los Test Cases a PBIs para mayor trazabilidad.
4. Revisar los Test Cases al inicio de cada Sprint.
5. Separar pruebas funcionales, de regresión y críticas.
6. Ejecutar pruebas de regresión en cada Sprint.
7. Crear Bugs detallados desde la propia ejecución.
8. Reutilizar Test Suites para no duplicar documentación.

---

## 9. Flujo de Trabajo Típico usando Azure Test Plans

1. El equipo identifica los PBIs que necesitan pruebas.
2. Se crean los **Test Cases** y se vinculan a cada PBI.
3. Se organiza un **Test Plan** para el Sprint.
4. Los testers ejecutan los **Test Runs**.
5. Se registran los resultados y se crean Bugs automáticamente.
6. Los desarrolladores corrigen los Bugs.
7. Se repiten los Test Runs para validar las soluciones.
8. El Sprint concluye con un informe de calidad.

# Test Case: TC-001 – Validación del login correcto

## Objetivo

Asegurar que un usuario puede iniciar sesión con credenciales válidas.
## Precondiciones

El usuario existe en el sistema.
## Pasos

1. Navegar a la página de inicio de sesión. 

   Resultado esperado: Se muestra el formulario de login. 

2. Introducir usuario válido. 

   Resultado esperado: El campo acepta la entrada. 

3. Introducir contraseña válida. 

   Resultado esperado: El campo acepta la entrada. 

4. Pulsar el botón "Iniciar sesión". 

   Resultado esperado: El sistema redirige al dashboard.