# Procedimiento de trabajo

Recoge el procedimiento del apartado 6 del plan de ejecución (Fase 3) con los ajustes del plan de seguimiento de la Fase 4A ([CAM-03](seguimiento/cambios.md)). Si alguna regla no resulta práctica se ajusta aquí y el cambio se anota en el registro de cambios.

## 1. Tablero y estado de las tareas

Cada tarea del plan es una issue de GitHub con su identificador en el título (por ejemplo `T21 · Reserva con plaza y material`), su resultado esperado en la descripción, una etiqueta de fase (`fase-4` a `fase-8`) y el hito de su entrega. Las issues están en el [tablero de GitHub Projects](https://github.com/orgs/PI-InesFuentes/projects/1), con los campos Inicio, Fin y Horas del cronograma. El estado de una tarea es la columna en la que está.

| Columna | Significado | Cuándo entra una tarea |
|---|---|---|
| Backlog | Tarea de una fase futura. | Al darse de alta, si no es de la fase actual. |
| Por hacer | Tarea de la fase actual que ya se puede empezar. | Al empezar cada fase, si sus dependencias están terminadas. |
| En curso | Estoy trabajando en ella. | En la primera sesión dedicada a ella. Nunca hay más de dos a la vez. |
| Bloqueada | Espera algo que no depende de mí. | Cuando no puede avanzar por una causa externa (entrevistas, personas de prueba, un servicio). El motivo se anota en la issue. |
| En revisión | El trabajo está hecho y falta comprobarlo. | Al conseguir el resultado esperado y abrir la pull request. Si la comprobación falla, vuelve a En curso con un comentario de lo que falta. |
| Hecho | Terminada y comprobada. | Cuando cumple la lista de tarea terminada y la pull request está fusionada en main. |

Las incidencias siguen las mismas columnas: entran en Por hacer si son críticas o altas y en Backlog si son medias o bajas.

## 2. Revisiones

- **En cada sesión.** Al empezar elijo la tarea y la paso a En curso. Al terminar subo los cambios a GitHub y, si la tarea no ha acabado, dejo en su issue una línea con lo hecho y lo que falta.
- **Cada semana.** El sábado comparo el tablero con el Gantt y lo anoto en [seguimiento/revisiones.md](seguimiento/revisiones.md).
- **En cada entrega.** Compruebo las tareas del hito, reviso la [matriz de requisitos](seguimiento/requisitos.md) y marco el repositorio con la etiqueta de versión (por ejemplo `fase-4`).

## 3. Control de versiones, ramas y commits

- La rama `main` contiene siempre una versión que arranca.
- Cada tarea se desarrolla en una rama corta con su identificador, por ejemplo `t21-reserva`. Las incidencias usan `inc-<número>-<descripción>`, por ejemplo `inc-34-cancelacion-stock`.
- La rama se fusiona en `main` mediante una pull request cuya descripción incluye `Closes #<número>`, para que GitHub cierre la issue al fusionar.
- Commits pequeños, al menos uno por sesión y siempre que termino un cambio que funciona por sí solo, con un mensaje en español que dice qué cambia e incluye el número de la issue.
- Los mensajes siguen la convención [Conventional Commits](https://www.conventionalcommits.org/es/v1.0.0/). Empiezan por un prefijo que indica el tipo de cambio y terminan con el número de la issue entre paréntesis, por ejemplo `docs: Añadir registro de cambios (#41)`.

| Prefijo | Cuándo se usa |
|---|---|
| `feat` | Funcionalidad nueva de la aplicación. |
| `fix` | Corrección de un error, normalmente de una incidencia. |
| `docs` | Documentación (README, docs/ o documentación de la API). |
| `test` | Pruebas automáticas nuevas o modificadas, sin cambiar la funcionalidad. |
| `refactor` | Cambio en el código que no añade funcionalidad ni corrige errores. |
| `chore` | Configuración del repositorio o de las herramientas (plantillas de issue, ESLint, dependencias). |
- Al final de cada sesión subo los cambios a GitHub.

## 4. Criterio de tarea terminada

Una tarea solo pasa de En revisión a Hecho si cumple todos los puntos que le corresponden. La lista está como casillas en la [plantilla de issue de tarea](../.github/ISSUE_TEMPLATE/tarea.md).

| N.º | Comprobación | Aplica a |
|---|---|---|
| 1 | Se ha conseguido el resultado esperado que figura en la tabla de tareas de la Fase 3. | Todas |
| 2 | La evidencia que corresponde al tipo de tarea está enlazada en la issue. | Todas |
| 3 | Las pruebas automáticas que existan pasan con un solo comando. | Código |
| 4 | ESLint no da errores en el cliente ni en el servidor. | Código |
| 5 | Lo he comprobado a mano en local y, si afecta a pantallas, también en el móvil a través del entorno de pruebas. | Código |
| 6 | Los casos del registro de pruebas relacionados con la tarea están ejecutados y anotados. | Código |
| 7 | No queda abierta ninguna incidencia crítica o alta relacionada con la tarea. | Código |
| 8 | La documentación afectada está actualizada (README, docs/ o documentación de la API). | Todas |
| 9 | La rama está fusionada en main mediante pull request, main sigue arrancando y la issue está cerrada. | Todas |
| 10 | Si la tarea ha cambiado el alcance, los recursos o las fechas de un hito, el cambio está en el registro de cambios. | Todas |

### Evidencia según el tipo de tarea

| Tipo de tarea | Tareas | Evidencia que la da por terminada |
|---|---|---|
| Preparación | T01 a T05 | Enlace o captura que muestre el resultado esperado: repositorio y tablero (T01), resumen en docs/ (T02), entrada en decisiones.md (T03) o el entorno funcionando (T04 y T05). |
| Diseño de la solución y seguimiento | T06 a T08 y T41 | Documento en docs/ enlazado desde la issue y revisado contra lo que pide la tarea. |
| Diseño de la interfaz | T09 a T11 | Enlace al archivo de Figma y bocetos exportados a PDF en docs/. |
| Base de datos y servidor | T12 a T24 | Pull request fusionada, pruebas automáticas superadas y casos del registro de pruebas ejecutados con el cliente de API. |
| Cliente | T25 a T30 | Pull request fusionada, capturas de la pantalla en escritorio y en móvil y ESLint sin errores. |
| Integración y pruebas | T31 a T35 | Registro de pruebas y matriz de requisitos actualizados, e incidencias registradas en GitHub. |
| Despliegue | T36 y T37 | Aplicación accesible en la dirección de Cloud Run y copia de la base de datos guardada fuera de Supabase. |
| Documentación y entregas | T38 a T40 y T42 a T47 | Documento en docs/ y, en las entregas, etiqueta de versión en el repositorio. |

## 5. Decisiones, incidencias y cambios

- Las decisiones técnicas se anotan en [decisiones.md](decisiones.md).
- Los errores se registran como issues con la [plantilla de incidencia](../.github/ISSUE_TEMPLATE/incidencia.md) y la etiqueta `incidencia`.
- Los cambios sobre lo aprobado se proponen con la [plantilla de cambio](../.github/ISSUE_TEMPLATE/cambio.md) y se registran en [seguimiento/cambios.md](seguimiento/cambios.md).

## 6. Copias de seguridad

- El código tiene tres copias: el portátil de desarrollo, GitHub y el portátil de pruebas, que se actualiza en cada despliegue.
- Los documentos de cada fase se escriben en Google Drive y su PDF se guarda en docs/.
- Los diseños están en Figma y los bocetos se exportan a PDF al cerrar el diseño.
- La base de datos local se reconstruye con las migraciones y los datos de ejemplo. La publicada en Supabase se exporta de forma periódica y se guarda fuera de Supabase.
- Las contraseñas y claves no se suben al repositorio: van en un archivo de variables de entorno excluido de Git, y el repositorio solo incluye `.env.example` sin valores.
