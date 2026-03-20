## 1. ¿Qué es Azure Repos?

> **Azure Repos = un sitio en la nube donde guardas y gestionas tu código**, de manera segura, con control de versiones y herramientas para trabajo en equipo.

Piensa en Azure Repos como un **Google Drive especializado para proyectos de software**, donde cada cambio queda registrado y cada miembro del equipo puede trabajar sin interferir con los demás.

---

## 2. ¿Qué es Git?

Git es un sistema que permite:

- Guardar el **historial completo** del código
-  Trabajar en **copias paralelas** sin romper nada
- Juntar el trabajo del equipo de forma controlada
- Volver atrás si algo falla

Azure Repos utiliza Git como motor.

---

## 3. Componentes principales de Azure Repos

### 3.1-. **Repositorio (Repo)**

Un repo es **la carpeta principal del proyecto**, que contiene:

- Archivos
- Carpetas
- Historial del código
- Configuración

Ejemplo típico:

```
MiProyecto/
 ├── backend/
 ├── frontend/
 ├── tests/
 ├── README.md
 └── .gitignore
```

---

### 3.2-. **Branches (Ramas)**

> Una _branch_ es una **copia del código en la que trabajas sin tocar la versión principal**.

Sirve para evitar romper el proyecto.

Ramas típicas:

- `main` → la versión estable
- `develop` → desarrollo activo
- `feature/login` → nueva funcionalidad
- `fix/bug-login` → arreglar un fallo

---

### 3.3-. **Commits**

> Un commit es como **guardar la partida**, pero con una descripción.

Ejemplo:

```
Commit: "Añadida validación de email en login"
```

Un commit guarda:

- Qué cambió
- Quién lo cambió
- Cuándo
- Por qué

---

### 3.4-. **Pull Requests (PRs)**

> Un Pull Request es pedir que revisen tu trabajo antes de unirlo al proyecto principal.

Sirve para:

- Revisar código
- Ver cambios línea a línea
- Comentar sugerencias
- Ejecutar pruebas automáticas
- Asegurar calidad

Proceso habitual:

1. Creas una branch
2. Haces commits
3. Abres un PR
4. Tus compañeros revisan
5. Si todo está OK → se mezcla (merge)

---

### 3.5-. **Policies (Reglas de calidad)**

Las _Policies_ son reglas que se aplican a una rama (normalmente `main` o `develop`) para asegurarse de que nadie puede subir código “a lo loco”.

Ejemplos:

- Se necesitan **revisiones obligatorias**
- El PR debe **pasar las pruebas automáticas (CI)**
- No se puede hacer _push directo_
- El PR debe estar asociado a una tarea (Work Item)

Esto mantiene el proyecto sano y profesional.

---

## 4. ¿Cómo se trabaja en Azure Repos en un Sprint real?

1. El desarrollador elige un PBI o tarea.
2. Crea una branch nueva:

    ```
   feature/nombre-de-la-funcionalidad
    ```

3. Desarrolla y hace commits pequeños y descriptivos.
4. Crea un Pull Request.
5. El PR se revisa (compañeros + pruebas automáticas).
6. Si todo OK → se hace merge a `develop` o `main`.
7. Azure Pipelines despliega automáticamente la nueva versión.

---

## 5. Analogía simple para recordarlo

- **Repositorio** = la carpeta del proyecto
- **Branch** = tu copia temporal para trabajar
- **Commit** = guardar cambios con mensaje
- **Pull Request** = revisión de tu trabajo
- **Policies** = reglas que garantizan calidad

---

## 6. Enlaces útiles

### Documentación oficial

- Azure Repos → https://learn.microsoft.com/azure/devops/repos
- Git (Atlassian) → https://www.atlassian.com/git/tutorials
