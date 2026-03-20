## 1. ¿Qué es Azure Pipelines?

**Azure Pipelines** es una herramienta de **CI/CD (Continuous Integration / Continuous Delivery or Deployment)** dentro de Azure DevOps.  
Permite automatizar el proceso de construcción, prueba y despliegue de software.

En otras palabras:

- **CI (Integración Continua):** Automatiza que el código se compile y se pruebe cada vez que alguien hace un cambio.
- **CD (Entrega / Despliegue Continuo):** Automatiza que el software se publique en entornos como desarrollo, preproducción o producción.

Azure Pipelines funciona con:

- Repositorios Git (Azure Repos, GitHub, GitLab, etc.)
- Cualquier lenguaje (Python, .NET, Java, Node.js, etc.)
- Cualquier plataforma (Windows, Linux, macOS, contenedores, Kubernetes)

---

## 2. Conceptos Técnicos Fundamentales

### Pipeline

Es el flujo automatizado que ejecuta pasos como:

1. Compilar
2. Ejecutar pruebas
3. Publicar artefactos
4. Desplegar el software

### Job

Es un conjunto de pasos que se ejecutan en un agente.

### Step (o Task)

Cada acción individual dentro del pipeline: compilar, ejecutar script, copiar archivos, etc.

### Agent

Máquina (física o virtual) donde se ejecuta el pipeline.

Hay dos tipos:

- **Hosted Agents:** proporcionados por Microsoft, ya configurados.
- **Self-hosted Agents:** configurados por tu empresa en servidores propios.

### Artifact (Artefacto)

Resultado empaquetado del build: binarios, archivos ZIP, imágenes de contenedor…

### Release

Proceso donde un artefacto se despliega en un entorno.

---

## 3. Tipos de Pipelines en Azure DevOps

### 3.1 YAML Pipeline

Definido en un archivo YAML dentro del repositorio.  
Ventajas:

- Reproducible
- Controlado por versiones
- Adecuado para equipos DevOps modernos

Ejemplo muy básico:

```
trigger:

- main

pool:

  vmImage: 'ubuntu-latest'

steps:

- script: echo "Hola mundo desde Azure Pipelines"
```

### 3.2 Classic Pipeline

Creado mediante interfaz visual (arrastrar y soltar).  
Ventajas:

- Fácil para principiantes
- No requiere editar código

Ideal para primeras implementaciones, aunque menos escalable que YAML.

---

## 4. Etapas Típicas de un Pipeline CI/CD

### 4.1 Integración Continua (CI)

Incluye:

- Compilación del código
- Análisis estático
- Ejecución de pruebas
- generación de artefactos

Beneficios:

- Detectar errores antes de que lleguen a producción
- Integraciones más rápidas y limpias

### 4.2 Entrega / Despliegue Continuo (CD)

Incluye:

- Despliegues automáticos
- Gestión de entornos
- Tareas de configuración o migraciones

Permite que un cambio pase de código a producción de forma fluida.

---

## 5. Estructura Lógica de un Pipeline YAML

Un pipeline en YAML suele tener:

1. **trigger**  
    Define cuándo debe ejecutarse el pipeline.
    
2. **pool**  
    Selección del agente.
    
3. **variables**  
    Valores reutilizables, tokens, nombres.
    
4. **stages**  
    Fases principales (Build, Test, Deploy…).
    
5. **jobs**  
    Trabajos dentro de una stage.
    
6. **steps**  
    Acciones concretas como ejecutar scripts o tasks.
    

Ejemplo simplificado con stages:

```
trigger:

- main

stages:

- stage: Build

  jobs:

  - job: BuildJob

    steps:

    - script: dotnet build

- stage: Deploy

  jobs:

  - job: DeployJob

    steps:

    - script: echo "Desplegando aplicación..."
```

## 6. Entornos (Environments)

Los entornos representan lugares donde se despliega el software:

- **Dev** (Desarrollo)
- **QA** (Calidad / Testing)
- **Staging** (Preproducción)
- **Prod** (Producción)

Azure Pipelines permite configurar:

- Revisiones manuales
- Aprobaciones obligatorias
- Reglas de seguridad
- Auditorías de despliegues

## 7. Seguridad en Azure Pipelines

### Variables y secretos

Permite almacenar:

- Contraseñas
- Tokens
- Claves de acceso

Con protección para que no se impriman en logs.

### Service Connections

Conexiones seguras a servicios externos:

- Azure
- Kubernetes
- Docker Hub
- GitHub

---

## 8. Ventajas de Usar Azure Pipelines

1. **Automatiza procesos repetitivos** y reduce errores.
2. **Aumenta la velocidad de entrega de software**.
3. Funciona en **cualquier lenguaje** o plataforma.
4. Permite trabajar con **contenedores** y **Kubernetes**.
5. Integración nativa con **Azure**, **GitHub** y otras herramientas.
6. Ofrece **escalabilidad** y agentes alojados por Microsoft.
7. Facilita la **trazabilidad completa** desde el código hasta el despliegue.

---

## 9. Buenas Prácticas al Crear Pipelines

- Hacer que los pipelines sean **modulares** y fáciles de mantener.
- Mantener los archivos YAML dentro del repositorio.
- Usar **plantillas YAML** para evitar duplicación.
- Dividir en stages: _Build_, _Test_, _Deploy_.
- Activar validaciones en _Pull Requests_.
- Configurar notificaciones para fallos de pipeline.
- Mantener los secretos seguros en el servicio de **Variable Groups**.
- Limitar los permisos del agente (principio de mínimo privilegio).

---

## 10. Flujo de Trabajo Típico en Azure Pipelines

1. Un desarrollador hace un cambio y abre un **Pull Request**.
2. Se activa automáticamente el **pipeline de CI**.
3. Si la compilación y las pruebas pasan, se aprueba el PR.
4. La rama principal activa un **pipeline de CD**.
5. El artefacto generado se despliega a Dev/QA/Staging/Prod.
6. Se monitoriza el despliegue para asegurar estabilidad.

Este proceso es totalmente automatizable.