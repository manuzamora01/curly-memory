## 1. ¿Qué es DevOps?

**DevOps** es un conjunto de prácticas, principios y una cultura de trabajo cuyo objetivo es unir a los equipos de **Desarrollo de Software (Development)** y **Operaciones de Sistemas (Operations)** para entregar software de forma más rápida, eficiente y confiable.

DevOps no es una herramienta concreta, sino una combinación de:

- Cultura y mentalidad de colaboración.
- Prácticas de automatización.
- Integración constante entre equipos.
- Monitorización y mejora continua.

El propósito principal es reducir la distancia entre desarrollar software y operarlo en producción.

---

## 2. ¿Por qué surge DevOps?

Antes de DevOps, los equipos de Desarrollo y Operaciones trabajaban de forma separada. Esto generaba:

- Largas demoras entre versiones.
- Fallos por falta de comunicación.
- Problemas al pasar software de entorno de desarrollo a producción.
- Dificultad para corregir errores rápidamente.

DevOps surge para resolver estos problemas mediante:

- **Colaboración constante**.
- **Automatización del ciclo de vida del software**.
- **Feedback rápido** entre equipos.

---

## 3. Componentes Clave del Enfoque DevOps

DevOps se suele representar mediante un **ciclo infinito** que refleja mejora continua.  
Cada fase está altamente automatizada.

### 3.1. Plan (Planificación)

Definición de requisitos, funcionalidades y tareas del proyecto.

### 3.2. Code (Desarrollo)

Creación del código del software.  
Incluye buenas prácticas como control de versiones (por ejemplo, Git).

### 3.3. Build (Construcción)

Compilación del código y generación de artefactos (versiones empaquetadas del software).

### 3.4. Test (Pruebas automatizadas)

Ejecución de pruebas para garantizar calidad.  
Incluye tests unitarios, de integración o de seguridad.

### 3.5. Release (Publicación)

Preparación del software para desplegarlo en entornos.

### 3.6. Deploy (Despliegue)

Entrega del software al entorno de producción o preproducción.  
Idealmente automatizado.

### 3.7. Operate (Operación)

Ejecución del software en producción y mantenimiento de su infraestructura.

### 3.8. Monitor (Monitorización)

Supervisión del rendimiento, uso, logs y fallos del sistema.  
Permite detectar errores antes de que afecten a usuarios.

---

## 4. Prácticas Fundamentales en DevOps

### 4.1. CI (Continuous Integration – Integración Continua)

Práctica donde los desarrolladores integran su código frecuentemente en un repositorio común.  
Cada integración lanza pruebas automáticas.

Beneficios:

- Detectar errores rápidamente.
- Reducir conflictos de código.

### 4.2. CD (Continuous Delivery / Deployment)

Extensión de la Integración Continua que automatiza la **entrega** o el **despliegue**.

- **Continuous Delivery:** el software siempre está listo para ser desplegado, pero el despliegue exige confirmación humana.
- **Continuous Deployment:** el software se despliega automáticamente en producción sin intervención manual.

### 4.3. IaC (Infrastructure as Code – Infraestructura como Código)

Gestión de servidores, redes o bases de datos mediante código.  
Ejemplos: Terraform, Ansible, ARM Templates.

Ventajas:

- Configuraciones reproducibles.
- Escalabilidad automatizada.

### 4.4. Automatización

Automatizar tareas repetitivas: pruebas, despliegues, configuraciones, pipelines.

### 4.5. Observabilidad

Monitorizar el sistema para entender su comportamiento real: métricas, logs, trazas.

---

## 5. Cultura DevOps

DevOps no funciona sin un cambio cultural. Sus pilares son:

1. **Colaboración** entre Desarrollo y Operaciones.
2. **Responsabilidad compartida** sobre todo el ciclo de vida.
3. **Comunicación continua** y transparente.
4. **Autonomía** de los equipos.
5. **Aprendizaje constante** y mejora continua.

---

## 6. Herramientas típicamente asociadas a DevOps

DevOps no depende de herramientas concretas, pero algunas son muy habituales:

### Control de versiones

- Git
- GitHub
- Azure Repos

### CI/CD

- Azure Pipelines
- GitHub Actions
- Jenkins

### Contenedores y Orquestación

- Docker
- Kubernetes

### Infraestructura como Código

- Terraform
- Ansible
- ARM Templates

### Monitorización

- Azure Monitor
- Grafana
- Prometheus

---

## 7. Beneficios de Adoptar DevOps

1. **Entrega más rápida de software**.
2. **Mayor calidad y menos fallos en producción**.
3. **Mejor comunicación entre equipos**.
4. **Automatización que reduce errores humanos**.
5. **Escalabilidad más sencilla** mediante IaC y contenedores.
6. **Feedback continuo** que mejora el producto desde el día uno.

---

## 8. DevOps vs Agile

Aunque DevOps y Agile se combinan muy bien, no son lo mismo:

| Agile                                               | DevOps                                                     |
| --------------------------------------------------- | ---------------------------------------------------------- |
| Se centra en cómo se desarrolla el software.        | Se centra en cómo se construye, entrega, opera y mantiene. |
| Enfoque en colaboración entre roles del desarrollo. | Colaboración entre desarrollo y operaciones.               |
| Entregas frecuentes.                                | Automatización y despliegues continuos.                    |

En conjunto, Agile + DevOps permiten crear y entregar software rápidamente y de forma estable.

