# Registro de riesgos

Tablas del apartado 9 del plan de ejecución (Fase 3). Se revisan en cada hito y cuando un retraso o una incidencia apunta a alguno de estos riesgos.

## Riesgos del desarrollo del proyecto

| ID | Riesgo identificado | Probabilidad | Impacto | Medida preventiva | Actuación si aparece |
|---|---|---|---|---|---|
| R-01 | Retraso acumulado por una estimación muy ajustada y por coincidir con exámenes y entregas de otros módulos. | Alta | Alto | Dedicación de 12 horas semanales, domingos sin planificar, tareas repartidas por entregas y revisión semanal del tablero. | Replanificar el Gantt, dar prioridad al ciclo de reserva y simplificar las pantallas de gestión y la documentación sin quitar funcionalidades. |
| R-02 | Tecnología del servidor sin decidir y herramientas nuevas para mí. | Media | Medio | T03 se hace al principio, con una prueba pequeña de transacción antes de decidir, y la decisión queda documentada. | Elegir la opción más sencilla y documentada, Express, que ya se valoró en la Fase 2, y anotar el cambio. |
| R-03 | Dificultad para garantizar las reservas simultáneas. | Media | Alto | Casos límite definidos en T08, bloqueo de filas y restricción de stock no negativo en PostgreSQL, y prueba con dos peticiones en paralelo en T24. | Recuperar tiempo en los domingos y simplificar apoyando la comprobación en las restricciones de la base de datos. |
| R-04 | Problemas al integrar cliente y servidor (sesión, CSRF o formatos de datos). | Media | Medio | API definida en T07 antes de programar, mismos nombres de campos en datos de prueba y API, y prueba temprana del inicio de sesión desde el cliente. | Registrar la incidencia, corregir primero en el servidor y recuperar el tiempo en los domingos. |
| R-05 | Pérdida de código o de documentos. | Baja | Alto | Subida a GitHub al final de cada sesión, documentos en Drive y copias descritas en el procedimiento. | Recuperar la última versión de GitHub o de Drive en el otro portátil. |
| R-06 | Avería del portátil de desarrollo. | Baja | Alto | El portátil ASUS tiene el entorno instalado y el código actualizado. | Seguir trabajando en el ASUS mientras se repara el otro. |
| R-07 | Pausa o límites de los servicios gratuitos (Supabase y Cloud Run). | Media | Medio | Comprobar que el proyecto de Supabase está activo antes de cada demostración, exportar la base de datos y poner una alerta de presupuesto en Google Cloud. | Reactivar o restaurar el proyecto y, si no da tiempo, hacer la demostración desde el entorno de pruebas. |
| R-08 | Problemas al desplegar el contenedor. | Media | Medio | Probar el contenedor en local antes de subirlo, desplegar varios días antes de la entrega de la Fase 7 y documentar los pasos. | Hacer la demostración desde el entorno de pruebas y valorar el servidor virtual estudiado en la Fase 2. |
| R-09 | No conseguir entrevistas con talleres. | Media | Bajo | Contactar con varios talleres la primera semana y proponer una entrevista breve. | Mantener el alcance de la Fase 2, que no depende de ellas, y dejar constancia en la memoria. |

## Prevención de riesgos laborales

Referencia: Real Decreto 488/1997 sobre trabajo con pantallas de visualización y guía técnica del INSST.

| ID | Riesgo identificado | Probabilidad | Impacto | Medida preventiva | Actuación si aparece |
|---|---|---|---|---|---|
| PRL-01 | Fatiga visual. | Media | Medio | Pausa breve cada hora, pantalla a más de 40 cm, brillo ajustado a la luz de la habitación y tamaño de letra cómodo. | Descansar la vista, acortar las sesiones y acudir a revisión si persiste. |
| PRL-02 | Dolor de espalda, cuello o muñecas por la postura con el portátil. | Media | Medio | Pantalla elevada a la altura de los ojos, teclado y ratón externos, silla regulable con apoyo lumbar y pies apoyados. | Parar, hacer estiramientos, corregir el puesto y consultar al médico si continúa. |
| PRL-03 | Iluminación inadecuada y reflejos. | Baja | Bajo | Mesa colocada de lado respecto a la ventana, luz ambiental suficiente y lámpara de apoyo por la tarde. | Recolocar la pantalla o la lámpara. |
| PRL-04 | Fatiga mental y estrés por la carga de trabajo. | Media | Medio | Sesiones de 2 horas como máximo, planificación realista y al menos un día a la semana sin proyecto. | Reducir la carga de esa semana y replanificar las tareas restantes. |
| PRL-05 | Riesgo eléctrico y caídas por cables. | Baja | Medio | Regleta con interruptor y protección, sin sobrecargar enchufes, cables recogidos y líquidos lejos de los equipos. | Desconectar el equipo y sustituir el cable o la regleta dañados. |

## Plantilla de revisión de riesgos

| Fecha | Hito o motivo de la revisión | Riesgo | ¿Se ha materializado? | Cambio de probabilidad o impacto | Actuación aplicada |
|---|---|---|---|---|---|
| dd/mm/aaaa | Entrega de la fase o incidencia que la provoca. | R-nn o PRL-nn | Sí / No | Nueva valoración, si cambia. | Qué se ha hecho y enlace a la issue o al cambio relacionado. |

## Registro de revisiones

| Fecha | Hito o motivo de la revisión | Riesgo | ¿Se ha materializado? | Cambio de probabilidad o impacto | Actuación aplicada |
|---|---|---|---|---|---|
| | | | | | |
