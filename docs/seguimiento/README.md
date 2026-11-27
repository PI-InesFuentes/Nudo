# Seguimiento y control de Nudo

Esta carpeta guarda los registros del plan de seguimiento y control de la Fase 4A (tarea T41). Cada archivo empieza con su **plantilla**, que explica qué se escribe en cada columna, y sigue con el **registro**, que se va rellenando durante el desarrollo.

Las tareas, las incidencias y los cambios se gestionan además como issues de GitHub y aparecen en el [tablero del proyecto](https://github.com/orgs/PI-InesFuentes/projects/1).

## Registros

| Registro | Archivo | Cuándo se actualiza |
|---|---|---|
| Seguimiento de tareas | Issues de tarea, [tablero](https://github.com/orgs/PI-InesFuentes/projects/1) y [revisiones.md](revisiones.md) | Cada vez que una tarea cambia de columna y en cada revisión semanal (sábado). |
| Indicadores de calidad | [indicadores.md](indicadores.md) | Cuando toca comprobar cada indicador y en cada hito. |
| Pruebas y comprobaciones | [pruebas.md](pruebas.md) | Al añadir un caso, al ejecutarlo y al repetirlo tras una corrección. |
| Incidencias | [Issues con la etiqueta `incidencia`](https://github.com/PI-InesFuentes/Nudo/issues?q=label%3Aincidencia) y plantilla en [.github/ISSUE_TEMPLATE](../../.github/ISSUE_TEMPLATE) | Durante todo el ciclo de cada incidencia. |
| Cambios | [cambios.md](cambios.md) e [issues con la etiqueta `cambio`](https://github.com/PI-InesFuentes/Nudo/issues?q=label%3Acambio) | Al proponer un cambio y al decidir sobre él. |
| Participación de usuarias | [usuarias/](usuarias/) | Antes de T34 para preparar la ficha y al terminar la evaluación. |
| Cumplimiento de requisitos | [requisitos.md](requisitos.md) | Cuando una prueba cambia el estado de un requisito y en cada hito. |
| Evidencias | [evidencias/](evidencias/) | Al guardar cada evidencia. |

## Otros documentos de trabajo

- [../procedimiento.md](../procedimiento.md): procedimiento de trabajo (tablero, ramas, commits, criterio de tarea terminada).
- [../decisiones.md](../decisiones.md): decisiones técnicas que no modifican lo aprobado.
- [../riesgos.md](../riesgos.md): registro de riesgos de la Fase 3 y su revisión en cada hito.
- [../cronograma.md](../cronograma.md): tareas, fechas previstas e hitos.

## Identificadores

| Prefijo | Qué identifica | Ejemplo |
|---|---|---|
| T | Tarea del plan de la Fase 3 | T21 |
| IC | Indicador de calidad | IC-03 |
| PR | Caso de prueba | PR-04 |
| INC | Incidencia (título de la issue) | INC La cancelación no devuelve el stock |
| CAM | Cambio | CAM-03 |
| TU | Tarea de la evaluación con usuarias | TU-2 |
| U | Participante en la evaluación | U1 |

La etiqueta de versión de cada entrega (por ejemplo `fase-4`) conserva el estado de todos estos registros en ese momento.
