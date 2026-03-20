## ¿Qué es DevOps?

DevOps es un **conjunto de prácticas, una cultura organizacional y un marco de trabajo** que busca unir el trabajo de **desarrolladores (Dev)** y **operaciones (Ops)** para acelerar la entrega de software sin comprometer la calidad.

Su objetivo principal es **reducir el tiempo entre realizar un cambio en el código y desplegarlo en producción**, manteniendo altos estándares de estabilidad y calidad.

En otras palabras, DevOps proporciona:

- Un marco común para entender cómo se desarrolla, prueba, entrega y opera el software.
- Un vocabulario compartido entre los equipos.
- Prácticas que optimizan el flujo completo desde el código hasta la producción.

### Cómo trabajaban tradicionalmente los equipos

- **Desarrollo (Dev)**: escriben código y lo envían al repositorio de control de versiones.
- **QA (Quality Assurance)**: prueban el software, registran errores y los devuelven al equipo de desarrollo.
- **Operaciones (Ops)**: despliegan el software en producción, siempre que no haya fallos pendientes.

Este modelo secuencial suele generar cuellos de botella, retrasos y tensiones entre equipos.

### Beneficios de adoptar DevOps

- **Reducción del Time To Market (TTM)**: el software llega antes a los usuarios.
- **Mejora de la calidad**: los fallos se detectan antes, se automatizan pruebas y despliegues.
- **Cultura saludable**: menos fricción entre equipos, menos agotamiento, más colaboración.
- **Más valor para el negocio**: ciclos más rápidos, feedback continuo y mejor experiencia de usuario.

### Ejemplo práctico

En un entorno tradicional, un cambio menor (como corregir un error visual) puede tardar días en llegar a producción porque debe pasar por varias capas de revisión manual.

Con DevOps:

- Se hace commit en el repositorio.
- Se ejecutan pruebas automáticas.
- Se despliega automáticamente a un entorno de pruebas y luego a producción si todo es correcto.

Esto puede completarse en minutos.

---

# Azure DevOps y Creación de Proyectos

Azure DevOps es un conjunto de servicios en la nube que soportan todo el ciclo de vida de desarrollo y entrega de software. Su objetivo es facilitar la integración continua (CI) y la entrega continua (CD).

Los principales servicios son:

## Azure Boards

Servicio para **gestionar y rastrear trabajo**. Permite registrar tareas, bugs, historias de usuario, épicas y planificar sprints.  
Ejemplos de uso:

- Crear una historia de usuario como “Como usuario, quiero iniciar sesión para acceder a mi cuenta”.
- Estimar tareas en puntos de historia.
- Visualizar el progreso en tableros tipo Kanban.

## Azure Pipelines

Herramienta para **compilar, probar y desplegar código automáticamente**.  
Permite crear pipelines de CI/CD mediante YAML o interfaz gráfica.  
Ejemplo de comando usado dentro de un pipeline:  
`dotnet build`  
`npm install`  
`az webapp deploy`

## Azure Repos

Sistema de **control de versiones en la nube**, soporta Git y TFVC.  
Permite gestionar ramas, hacer pull requests, revisar código y mantener historial.  
Ejemplo de acción típica:  
`git push origin feature/nueva-funcionalidad`

## Azure Test Plans

Servicio para **gestionar, ejecutar y registrar pruebas** de aplicaciones, tanto manuales como automatizadas.  
Útil para:

- Pruebas manuales exploratorias.
- Escenarios de QA organizados y trazables.

## Azure Artifacts

Repositorio para **paquetes reutilizables** (NuGet, npm, Maven, Python).  
Permite compartir dependencias dentro de una organización.  
Ejemplo típico: publicar un paquete interno npm:  
`npm publish --registry https://pkgs.dev.azure.com/organizacion/_packaging/miFeed/npm/registry/`



