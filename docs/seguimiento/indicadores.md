# Indicadores de calidad

Los indicadores parten de las condiciones de calidad del apartado 12 de la Fase 2 y de sus requisitos no funcionales. Cada uno se comprueba con una prueba, una herramienta o una revisión concreta. Hasta que exista la funcionalidad que miden, su estado es pendiente.

## Definición de los indicadores

| ID | Indicador | Qué aspecto controla | Cómo se comprobará | Resultado aceptable | Cuándo se comprobará |
|---|---|---|---|---|---|
| IC-01 | Requisitos funcionales superados | Cumplimiento de los 24 requisitos funcionales de la Fase 2. | Matriz de [requisitos.md](requisitos.md), con al menos una prueba por requisito. | 24 de 24 en estado cumple en la entrega de la Fase 7. | En cada hito desde la Fase 6 y en T33. |
| IC-02 | Coherencia de plazas y stock | Que reservar y cancelar dejen plazas y material en el valor correcto. | Prueba automática que compara plazas y cantidades antes y después de reservar y de cancelar. | Los valores coinciden exactamente en todos los casos. | En cada cambio que toque reservas o stock y en T24. |
| IC-03 | Reservas simultáneas | Que la última plaza o el último material no se reserven dos veces. | Dos peticiones de reserva lanzadas en paralelo sobre la última plaza y sobre la última unidad de un material. | Se confirma una sola reserva y la otra recibe un error que explica el motivo. | En T24 y antes de publicar (T36). |
| IC-04 | Sesiones solapadas | Prevención de sesiones incompatibles. | Crear y modificar sesiones que coinciden en espacio o en monitora, y una que empieza justo al terminar otra. | Se rechazan las solapadas y se acepta la consecutiva. | En T19 y en T33. |
| IC-05 | Reservas no permitidas | Rechazo de reservas sin plaza, sin existencias, duplicadas o de sesiones ya comenzadas. | Un intento de cada tipo desde el cliente y otro directamente contra la API. | Los cuatro tipos se rechazan desde los dos sitios y no cambia nada en la base de datos. | En T21 y en T33. |
| IC-06 | Validación de datos | Rechazo de datos incorrectos. | Enviar campos obligatorios vacíos, fechas pasadas, aforos o cantidades menores que uno y correos mal escritos desde los formularios y desde el cliente de API. | Todos se rechazan con un mensaje en español, también cuando se saltan las validaciones del cliente. | En cada tarea con formularios y en T33. |
| IC-07 | Separación entre negocios | Que ningún negocio vea ni modifique datos de otro. | Con cuentas de los tres negocios de ejemplo, pedir a la API talleres, sesiones, stock y reservas de otro negocio. | Ningún dato de otro negocio devuelto ni modificado. | En T15, en T24 y en T34. |
| IC-08 | Control de acceso | Rutas privadas y permisos de cada perfil. | Llamar a cada ruta privada sin sesión y con cada perfil sin permiso. | Sin sesión responde 401 y sin permiso 403. Ninguna devuelve datos. | En T17, en T24 y en T34. |
| IC-09 | Contraseñas y HTTPS | Protección de credenciales y de la conexión. | Revisar la tabla de usuarias en la base de datos y el certificado de la dirección publicada. | Ninguna contraseña en claro y toda la aplicación servida por HTTPS. | En T16 y en T36. |
| IC-10 | Integridad de los datos | Stock nunca negativo y sin borrados con reservas activas. | Intentar dejar un material en negativo y borrar talleres, sesiones y materiales con reservas, por la API y directamente en la base de datos. | La base de datos y el servidor lo impiden en todos los casos. | En T12, en T23 y en T33. |
| IC-11 | Adaptación a pantallas | Uso en móvil y en escritorio. | Revisar cada pantalla a 360, 768 y 1280 píxeles con el modo de dispositivo del navegador y en un móvil real. | Ninguna pantalla con desplazamiento horizontal ni elementos cortados. | En T30 y en T34. |
| IC-12 | Accesibilidad | Nivel AA de WCAG 2.2 en las pantallas principales. | Lighthouse en cada pantalla principal y recorrido completo solo con teclado. | Sin errores graves en Lighthouse, puntuación de accesibilidad de 90 o más y todas las acciones posibles con teclado. | En T30 y en T34. |
| IC-13 | Usabilidad de la reserva | Que una alumna reserve sin ayuda. | Evaluación con usuarias ([usuarias/](usuarias/)). | Las dos personas completan la reserva sin ayuda y en cuatro pasos como máximo desde la ficha del taller. | En T34. |
| IC-14 | Compatibilidad | Funcionamiento en los navegadores previstos. | Recorrer el ciclo de reserva y cancelación en Chrome, Firefox, Edge y Safari. | El ciclo funciona igual en los cuatro. | En T34. |
| IC-15 | Errores comprensibles | Tratamiento de errores. | Provocar errores conocidos, como una plaza ya ocupada o una sesión caducada, y revisar la configuración de producción. | Mensaje en español que explica qué ha pasado y qué hacer, sin detalles técnicos, y depuración desactivada en producción. | En T31 y en T36. |
| IC-16 | Incidencias graves abiertas | Ausencia de errores críticos conocidos. | Filtro de incidencias abiertas por gravedad en GitHub. | Ninguna crítica en cada entrega y ninguna alta en la entrega de la Fase 7. | En cada revisión semanal y en cada hito. |
| IC-17 | Calidad del código | Formato y errores del código. | ESLint en el cliente y en el servidor. | Ningún error. | En cada pull request. |
| IC-18 | Cumplimiento de hitos | Avance según el cronograma. | Comparar en cada entrega las tareas que exige el hito con las que están en Hecho. | Todas las tareas del hito en Hecho, o el retraso registrado y replanificado. | En cada entrega. |

## Plantilla de registro de comprobaciones

| Fecha | Indicador | Versión o tarea | Resultado obtenido | ¿Aceptable? | Evidencia | Observaciones |
|---|---|---|---|---|---|---|
| dd/mm/aaaa | IC-nn | Tarea o etiqueta de versión en la que se comprueba (por ejemplo T24 o `fase-6`). | Valor medido o lo que ocurrió realmente. | Sí / No | Enlace a la prueba, la pull request o el archivo de [evidencias/](evidencias/). | Incidencia abierta si no es aceptable (INC y número de issue). |

## Registro de comprobaciones

| Fecha | Indicador | Versión o tarea | Resultado obtenido | ¿Aceptable? | Evidencia | Observaciones |
|---|---|---|---|---|---|---|
| | | | | | | |

## Estado actual

| Indicador | Última comprobación | Estado |
|---|---|---|
| IC-01 a IC-18 | Sin comprobar | Pendiente |
