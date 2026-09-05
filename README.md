# Mi primera práctica con Git
Ana Lucia Goche Lopez

Este repositorio fue creado para aprender los fundamentos de Git.

## Parte 1: Investigación

### ¿Qué es un sistema de control de versiones?

Es una práctica importante de desarrollo de software para hacer un seguimiento y gestionar los cambios realizados en el código y otros archivos.

**Qué problema resuelve:**

Si los desarrolladores codifican simultáneamente y crean cambios incompatibles, el control de versiones identifica las áreas problemáticas para que los miembros del equipo puedan revertir rápidamente los cambios a una versión anterior, comparar los cambios o identificar quién cometió el código del problema a través del historial de revisiones.

**Por qué es útil cuando desarrollamos software:**

Permite una mejor gestión, seguimiento e implementación de los cambios en el código y los archivos relacionados. Al brindar un enfoque estructurado para el control de revisiones, VCS admite entornos dinámicos y colaborativos, y proporciona estabilidad en todos los proyectos de desarrollo.

**Qué ventajas ofrece frente a guardar copias manuales de un proyecto:**
- **Calidad:** 
  El control de versiones fomenta una cultura de revisión y colaboración continua entre pares, lo que lleva a mejoras significativas en la calidad del código.
- **Aceleración:** 
  Los sistemas de control de versiones agilizan los procesos de desarrollo, lo que permite una iteración y entrega más rápidas de las funcionalidades.
- **Visibilidad:** 
  Un repositorio central actúa como la fuente única de la verdad, y mejora la transparencia y la responsabilidad del proyecto.

*Fuente: https://about.gitlab.com/es/topics/version-control/#benefits-of-version-control*

### ¿Qué es Git?

Git es un sistema de control de versiones de código fuente. Es una herramienta que se utiliza para llevar un registro de los cambios en el código fuente de un proyecto y permitir a varios desarrolladores trabajar en el mismo proyecto de manera simultánea.

*Fuente: https://davinciti.com/que-es-y-para-que-sirve-git/*

- **Quién creó Git:** Linus Torvalds
- **En qué año fue creado:** 2005
- **Para qué proyecto fue creado originalmente:** 
  Desarrollado originalmente por Linus Torvalds para el sistema operativo Linux, con el fin de ofrecer velocidad, simplicidad y la capacidad de admitir múltiples versiones paralelas de proyectos (ramas). La herramienta privativa que usaban antes (BitKeeper) dejó de ser gratuita para la comunidad de desarrollo de Linux, lo que llevó a Torvalds a diseñar un sistema propio desde cero.

*Fuente: https://research.wou.edu/git*

**¿Qué significa que Git sea un sistema de control de versiones distribuido?**

Lleva una copia local del repositorio completo a la computadora de cada miembro del equipo, para que puedan confirmar, ramificar y fusionar de manera local. El servidor no tiene que almacenar un archivo físico para cada rama, solo necesita las diferencias entre cada confirmación.

## Parte 2 :Git vs GitHub

**Git:** 
Es un software de VCS local que permite a los desarrolladores guardar instantáneas de sus proyectos a lo largo del tiempo. Generalmente es mejor para uso individual.

**GitHub:** 
Es una plataforma basada en la web que incorpora las características de control de versiones de Git para que puedan ser utilizadas de forma colaborativa. También incluye características de gestión de proyectos y equipos, así como oportunidades para la creación de redes y la codificación social.

*Fuente: https://kinsta.com/es/blog/git-vs-github/*

**GitLab:** 
Es una plataforma web para la gestión del ciclo de vida del desarrollo de software mediante el control de versiones de código fuente, sirviendo también como repositorio online para almacenar proyectos.

*Fuente: https://formadoresit.es/que-es-gitlab-y-para-que-sirve/*

**Bitbucket:** 
Es una plataforma de alojamiento de repositorios basada en Git, desarrollada por Atlassian. Permite a los equipos de desarrollo gestionar, almacenar y colaborar en el código fuente. Conocida por su profunda integración con el ecosistema de Atlassian (como Jira y Confluence), Bitbucket admite la integración y el despliegue continuo (CI/CD), pull requests y controles de acceso robustos.

*Fuente: https://xygeni.io/es/sscs-glossary/what-is-bitbucket-used-for/*

## Parte 3: Instalar y verificar Git

- **Sistema operativo utilizado:** Windows
- **Versión de Git instalada:** 2.46.0.windows.1
- **Comando utilizado para verificarla:** `git --version`
  

## Parte 7: Mi primer commit
### Working Directory
Es un lugar predeterminado donde se buscaran los archivos que se van a subir y se guardaran

### Staging Area
Espacio de almacenamiento temporal es como una estacion pero de archivos donde estan esperanado a ser enviados a su destino final.

### Repository
El repositorio es el lugar donde se almacenan.

### `git add`
git add lleva las modificaciones nuevas del archivo al staging area

### `git commit`
Es la version de tu archivo en ese momento guarda los cambios o lo que agregaste.


## Parte 12: Merge

### ¿Qué es una rama?
Es una linea de trabajo independiente 


### ¿Por qué un equipo de desarrollo utilizaría ramas?
para hacer cambios sin afectar la version principal

### ¿Qué hace `git merge`?
Integrar los cambios realizados en otra rama.

## Parte 13: .gitignore
### ¿Para qué sirve `.gitignore`?
Sirve para indicarle a git cuales son los archivos que debe ignorar y no subir aunque sea git add.

### ¿Por qué normalmente no incluimos `node_modules`?
Porque es muy pesado y inesesarios 

### ¿Por qué un `.env` puede contener información que no debería publicarse?
Porque almacena credenciales secretas y datos sensibles que otorgan acceso directo a bases de datos y servicios externos de una aplicación.




## Preguntas de reflexión

**1. ¿Qué diferencia existe entre `git add` y `git commit`?**

`git add` prepara los archivos (los manda al staging area) y `git commit` ya guarda esos cambios en el historial del proyecto.

**2. ¿Qué ventaja tiene realizar varios commits pequeños en lugar de un solo commit grande?**

Entre más commits hagas, podrás tener la evolución de tu código y, si llegas a "regarla", poder retroceder sin necesidad de rehacer la mitad o todo, sino solo unas líneas.

**3. ¿Qué diferencia existe entre Git y GitHub?**

Git es la herramienta que te permite guardar la evolución de tu código, y GitHub es la plataforma que incorpora las características de control de versiones de Git para que puedan ser utilizadas de forma colaborativa.

**¿Qué problema resuelven las ramas?**

Permiten trabajar en nuevas funciones o experimentos sin afectar el código principal, y varias personas pueden trabajar en paralelo sin generar conflictos hasta que se hace el merge.

**4. ¿Qué información no debería normalmente almacenarse en Git?**

El archivo `.env`, ya que puede contener información sensible como contraseñas o llaves de acceso.

**5. ¿Qué ocurriría si borras tu proyecto local pero está publicado en GitHub?**

Se puede recuperar clonando de nuevo el repositorio desde GitHub, ya que ahí queda todo el historial guardado.

**6. ¿Por qué Git es especialmente importante cuando varias personas trabajan sobre el mismo proyecto?**

Git ayuda a que cada quien tenga su propia copia del proyecto y te avisa si dos personas modifican lo mismo, esto permite que todos puedan trabajar juntos al mismo tiempo, haya más eficiencia y se prevengan errores, ya que con esta herramienta queda todo registrado.

**7. ¿Cuál es la diferencia entre `git clone`, `git pull` y `git push`?**

`git clone` es para traerte una copia completa de un repositorio, `git pull` es cuando quieres traerte los cambios que han hecho otras personas en el repo, y `git push` es para mandar tus propios cambios al repositorio remoto.

**8. ¿Por qué un commit no aparece automáticamente en GitHub?**

Porque le falta el `git push`, que es el comando que sube los commits del repositorio local al remoto.


