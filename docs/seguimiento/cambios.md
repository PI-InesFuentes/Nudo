# Registro de cambios

Se considera un cambio cualquier decisión que modifique lo aprobado en las fases anteriores: el alcance o los requisitos de la Fase 2, la tecnología o los recursos previstos, el cronograma de la Fase 3 cuando afecta a un hito, o los costes. Las decisiones pequeñas de implementación que no tocan nada de esto se anotan solo en [decisiones.md](../decisiones.md).

## Procedimiento

1. **Propuesta.** Abro una issue con la plantilla de cambio (etiqueta `cambio`) explicando qué se quiere cambiar y por qué. Una idea que surge mientras trabajo no se aplica directamente: primero se apunta aquí.
2. **Análisis del impacto.** Respondo en la issue a las preguntas de la tabla siguiente.
3. **Decisión.** Decido si se aprueba, se aplaza o se descarta con los criterios de abajo y lo apunto con la fecha en el registro.
4. **Actualización.** Si se aprueba, creo o modifico las tareas afectadas en el tablero y actualizo los documentos indicados en el registro antes de empezar a aplicarlo.

| Pregunta | Qué se revisa |
|---|---|
| ¿Por qué es necesario? | Qué problema de la Fase 1, requisito u objetivo resuelve, o qué dificultad técnica lo hace necesario. |
| ¿Qué funcionalidades y tareas modifica? | Tareas de la Fase 3 afectadas, tareas nuevas y requisitos que cambian. |
| ¿Qué nuevos recursos necesita? | Librerías, servicios externos, cuentas o conocimientos que no estaban previstos. |
| ¿Cómo afecta al tiempo disponible? | Horas que añade frente a las 154 del plan, que no tienen holgura, y hitos afectados. |
| ¿Modifica el alcance o los costes? | Si pasa al núcleo algo que era de ampliación o estaba fuera de alcance, o si algún servicio deja de ser gratuito. |
| ¿Qué riesgo supone? | Si puede afectar al ciclo de reserva y stock o a funcionalidades ya comprobadas. |

**Criterios de decisión.** Un cambio se **aprueba** si es necesario para cumplir un requisito esencial o resolver un problema técnico y cabe en el tiempo disponible, aunque sea compensándolo con las simplificaciones previstas en los riesgos de la Fase 3. Se **aplaza** si aporta valor pero no es esencial, y queda para después de T35 junto con el resto de funcionalidades de ampliación. Se **descarta** si no responde a ningún objetivo del proyecto o pone en riesgo el ciclo de reserva.

## Plantilla

| ID del cambio | Descripción y motivo | Impacto en tareas, recursos y planificación | Decisión adoptada | Fecha y responsable | Documentos que deberán actualizarse |
|---|---|---|---|---|---|
| CAM-nn | Qué cambia y por qué es necesario. Enlace a la issue de cambio. | Tareas afectadas y nuevas, recursos nuevos, horas añadidas frente a las 154 del plan, hitos afectados y efecto en el alcance o los costes. | Aprobado, aplazado o descartado, con el criterio aplicado. | dd/mm/aaaa de la decisión y quién la toma. | Documentos y registros que hay que cambiar y si ya están actualizados. |

## Registro

CAM-01 y CAM-02 se decidieron en la Fase 3 y se registran aquí para que quede constancia de la evolución del proyecto. CAM-04 es un **ejemplo simulado** que muestra cómo se valoraría una ampliación de la Fase 2; no es un cambio real.

| ID del cambio | Descripción y motivo | Impacto en tareas, recursos y planificación | Decisión adoptada | Fecha y responsable | Documentos que deberán actualizarse |
|---|---|---|---|---|---|
| CAM-01 | Servidor con Node.js en lugar de Laravel. Usar JavaScript en cliente y servidor reduce lo que tengo que aprender y mantener siendo una sola persona. | Se añade T03 para elegir framework y librerías. XAMPP deja de ser necesario y Sanctum y las pruebas de Laravel se sustituyen. Sin coste añadido. | Aprobado. | 15/11/2026 (entrega de la Fase 3). Inés Fuentes. | Plan de la Fase 3, apartados 1.3, 2, 5 y 10. Ya actualizado. |
| CAM-02 | Orden de trabajo adaptado a las entregas del módulo. El cliente se construye con datos de prueba en la Fase 5 y el servidor en la Fase 6. | Las tareas se reordenan sin cambiar las horas. La integración (T31) depende de que la API siga lo definido en T07. | Aprobado. | 15/11/2026 (entrega de la Fase 3). Inés Fuentes. | Plan de la Fase 3, apartados 1.3, 3 y 4. Ya actualizado. |
| CAM-03 | El tablero pasa de las tres columnas de la Fase 3 (Pendiente, En curso, Hecho) a seis: **Backlog** (tareas de fases futuras), **Por hacer** (fase actual con dependencias terminadas), En curso, **Bloqueada** (espera algo externo, como las entrevistas de T02 o las personas de prueba de T34), **En revisión** (pull request abierta, falta el criterio de tarea terminada) y Hecho. Además se amplía la lista de tarea terminada a 10 comprobaciones. Motivo: separar el fin del trabajo de su comprobación, ver aparte lo que no depende de mí y no mezclar las 47 tareas en una sola columna. | Sin tareas nuevas ni coste. Cada tarea tiene un paso más antes de pasar a Hecho. Las incidencias siguen las mismas columnas. | Aprobado. | 27/11/2026. Inés Fuentes. | [procedimiento.md](../procedimiento.md), tablero de GitHub Projects, plantilla de issue de tarea y las 47 issues de tarea. |
| CAM-04 (simulado) | Avisos por correo de confirmación y cancelación de reserva, que en la Fase 2 eran una ampliación. Motivo supuesto: que la alumna tenga constancia fuera de la aplicación. | Tareas nuevas para configurar Brevo, preparar los correos y probarlos, y cambios en T21 y T22. Necesita una librería de correo para Node.js. Sus horas no caben en el plan. Sin coste mientras no se superen los 300 correos diarios del plan gratuito. | Aplazado hasta después de T35, si queda tiempo. | Ejemplo sin fecha real. | Si se aprobara: alcance de la Fase 2, tareas y Gantt de la Fase 3 y matriz de requisitos. |
