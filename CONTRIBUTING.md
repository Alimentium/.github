# Guía de contribución de Alimentium

¡Gracias por tu interés en contribuir al proyecto Alimentium! Valoramos tus contribuciones y queremos asegurarnos de que el proceso de colaboración sea lo más eficiente y agradable posible para todos. Esta guía de contribución tiene como objetivo ayudarte a entender nuestro proceso de desarrollo y cómo puedes contribuir al proyecto.

## Proceso de desarrollo

En Alimentium, utilizamos el flujo de trabajo de GitHub Flow para el desarrollo. A continuación, se presentan los pasos básicos del proceso:

1. Asegúrate de tener acceso al repositorio en la organización de Alimentium.
2. Clona el repositorio en tu máquina local.
3. Crea una rama con un nombre descriptivo para tu tarea, siguiendo la convención de nombres que se detalla más adelante.
4. Realiza tus cambios y commits siguiendo la convención de mensajes de commit (Conventional Commits).
5. Haz push de tu rama al repositorio remoto (No se puede pushear a main directamente, esa rama está protegida).
6. Crea un pull request en el repositorio desde tu rama a la rama dev para desplegar en DEV.
7. Si se valida en DEV crea pull request desde tu rama a la rama staging para desplegar en Staging.
8. Si se valida en Staging crea pull request desde tu rama a la rama main.

## Convención de nombres de ramas

En Alimentium, seguimos una convención de nombres de ramas para mantener la consistencia y facilitar la identificación del propósito de cada rama. Utiliza la siguiente estructura al nombrar tus ramas:

- Para características nuevas: `feature/<codigo-proyecto-en-clickup>-<id-ticket>/<nombre-descriptivo>`
- Para correcciones de errores: `fix/<codigo-proyecto-en-clickup>-<id-ticket>/<nombre-descriptivo>`
- Para tareas de mantenimiento y mejoras que no sean características ni correcciones: `chore/<codigo-proyecto-en-clickup>-<id-ticket>/<nombre-descriptivo>`

### Feature
Indica que se introduce una nueva funcionalidad o mejora en el proyecto. Este prefijo generalmente agrega un nuevo componente, un nuevo módulo o una mejora significativa en la lógica de negocios. Estos cambios son visibles para los usuarios finales y afectan directamente la funcionalidad del software.

- Ejemplo de uso en nombre rama: `feature/PROCLI-1234/agregar-login`
- Ejemplo de uso en commit: `feat: Add search functionality to the application`

### Chore
Indica cambios que no están relacionados directamente con la funcionalidad del proyecto, como cambios en la configuración del proyecto, actualizaciones de dependencias, tareas de limpieza de código o mejoras en el proceso de construcción. Estos cambios no son visibles para los usuarios finales y no afectan la funcionalidad del software.

- Ejemplo de uso en nombre rama: `chore/PROCLI-2478/update-packages-to-last-version`
- Ejemplo de uso en commit: `chore: Update package dependencies to latest versions.`
 
## Mensajes de commit

Utilizamos Conventional Commits para estandarizar nuestros mensajes de commit. Asegúrate de que tus mensajes de commit sigan este formato:

<type>(<scope>): <description>

<body> [OPCIONAL]


Los tipos (type) permitidos son: `feat`, `fix`, `docs`, `refactor`, `test`, `ci`, `chore`, `revert`, `mngt`, `wip`.

En alcance (scope) puedes indicar el componente que ha cambiado. Si es un cambio que afecta a toda la aplicación o es general, puedes omitirlo

Por ejemplo: `feat(login): agregar autenticación con Google
              se ha creado un login que utiliza la cuenta de google. `

El cuerpo del mensaje (body) de commit se utiliza para proporcionar información más detallada sobre los cambios realizados en el commit. Puede incluir detalles adicionales, contexto o justificación para los cambios. El cuerpo debe comenzar en la línea siguiente al título del mensaje de commit y, por lo general, se escribe en formato de texto sin formato o en Markdown, separado por líneas en blanco para facilitar la lectura.

## Reportar problemas y solicitar características

Si encuentras un problema o tienes una idea para una nueva característica, por favor crea un issue en Clickup
