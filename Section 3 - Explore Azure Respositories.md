# Code Management with Azure Repos 101

## Control de versiones

El control de versiones es un sistema que permite:

- Registrar cambios en el código a lo largo del tiempo.
- Conservar un historial completo de modificaciones.
- Crear copias del repositorio sin perder información.
- Colaborar con otras personas sin sobrescribir el trabajo.

Gracias al control de versiones puedes:

- Volver a estados anteriores del código.
- Comparar cambios entre commits.
- Trabajar en paralelo mediante ramas independientes.

---

# Tipos de control de versiones

Existen dos sistemas principales:

## Git

Git es un **sistema de control de versiones distribuido**. Sus características:

- Es software **open source**.
- Cada persona tiene una copia completa del repositorio en su máquina.
- Se hacen commits localmente y luego se sincronizan con la nube.
- Es la opción más utilizada en desarrollo moderno.

Ejemplo de flujo básico:

1. Modificas un archivo.
2. Haces un commit: `git commit -m "mensaje"`.
3. Sincronizas con el servidor: `git push`.

Un ejemplo simple para entenderlo:  
Imagina un archivo de Excel con varias hojas y múltiples versiones guardadas. Git hace esto automáticamente y permite colaborar en el mismo archivo sin perder el historial.

---

## GitHub

GitHub no es Git:  
Es una **plataforma web que aloja repositorios Git** y facilita la colaboración.

Con GitHub puedes:

- Almacenar repositorios en la nube.
- Crear forks (copias independientes) para experimentar.
- Crear Pull Requests para proponer cambios.
- Revisar código con otros desarrolladores.

Alternativas: Bitbucket, Subversion, Azure Repos.

---

# Crear tu entorno de desarrollo

Para trabajar con Git y código necesitas:

- Instalar Node.js (si usas JavaScript/TypeScript).
- Instalar Git.
- Instalar un IDE como Visual Studio o Visual Studio Code.
- Tener una cuenta en GitHub (o usar Azure DevOps Repos).

---

# Crear un repositorio de código

## Crear un repositorio en GitHub (paso a paso)

1. Inicia sesión en GitHub.
2. Haz clic en "New Repository".
3. Introduce un nombre.
4. Selecciona si será público o privado.
5. Opcional: añade un README.
6. Haz clic en "Create Repository".

---

## Crear un repositorio en Azure DevOps (paso a paso)

1. Entra en Azure DevOps y accede a tu proyecto.
2. Ve a "Repos".
3. Selecciona la opción "Initialize Repository" si es nuevo.
4. Añade un README o `.gitignore` si lo necesitas.
5. Copia la URL para clonar:  
    `git clone <url_del_repositorio>`

---

# El archivo .gitignore

`.gitignore` indica a Git qué archivos no deben rastrearse.

Ejemplos típicos:

- Archivos temporales del sistema como `.DS_Store`.
- Carpetas de dependencias como `node_modules`.
- Archivos generados automáticamente.

Para ignorar un archivo, simplemente añádelo al `.gitignore`:

`.DS_Store`

---

# Importar un repositorio Git en Azure DevOps (paso a paso)

1. Entra en "Repos" dentro de tu proyecto.
2. Selecciona "Import Repository".
3. Introduce la URL del repositorio Git existente.
4. Haz clic en "Import".
5. Espera a que Azure DevOps copie todo el contenido.

---

# Gestionar cambios de código

## Branch (Rama)

Una branch es:

- Un conjunto único de cambios.
- Una copia de trabajo del código principal.
- Un espacio seguro para desarrollar sin afectar la rama principal.

La rama principal (main o master) es la que se despliega a producción.

---

## Commit

Un commit registra cambios del repositorio en un instante concreto.  
Ejemplo:  
`git commit -m "Corrige cálculo de totales"`

---

## Pull Request (PR)

Un Pull Request es el proceso de:

- Solicitar que la rama de trabajo se mezcle con otra rama.
- Revisar código antes de integrarlo.
- Asegurar calidad y evitar errores.

---

# Crear una rama (paso a paso)

1. Ve a "Repos" en Azure DevOps.
2. Selecciona "Branches".
3. Haz clic en "New Branch".
4. Asigna un nombre descriptivo.
5. Selecciona la rama base (normalmente `main`).
6. Asocia elementos de trabajo si corresponde.

---

# Realizar un Pull Request (paso a paso)

1. Haz commit de tus cambios.
2. Añade un mensaje explicando el cambio.
3. Crea un Pull Request.
4. Incluye:
    - Título.
    - Descripción.
    - Revisores.
    - Elementos de trabajo relacionados.
5. Espera la revisión.
6. Cuando esté aprobado, selecciona "Complete Pull Request".

---

# Trabajar con código localmente (parte 1)

## Fork

Un fork crea una copia completa del repositorio bajo tu cuenta.

Después lo clonas:

`git clone <url_del_repositorio>`

También puedes clonar desde Visual Studio Code usando "Clone Repository".

---

## Crear una rama local en VS Code

En la barra inferior, selecciona "Create Branch" y define un nombre.

---

# Trabajar con código localmente (parte 2)

## Source Control en VS Code

Aquí puedes:

- Ver cambios pendientes.
- Hacer commits.
- Gestionar ramas.
- Sincronizar con el servidor.

## git fetch

`git fetch` descarga información actualizada del repositorio remoto sin alterar tu código local.

---

# Entender y gestionar el historial

Puedes revisar el historial de commits desde:

- Repos → Files → History.
- Repos → Commits.

Esto permite ver quién cambió qué y cuándo.

---

# Limpiar repositorios

Buenas prácticas:

- Eliminar ramas antiguas.
- Borrar archivos no usados.
- Aplicar reglas de `.gitignore`.
- Mantener un historial limpio mediante commits claros y descriptivos.