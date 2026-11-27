# Registro de pruebas y comprobaciones

Cada caso de prueba tiene un identificador PR-nn y el requisito de la Fase 2 que comprueba. Las pruebas automáticas llevan el mismo identificador en su nombre, para relacionar el resultado de cada ejecución con este registro.

## Plantilla

| ID | Requisito | Acción o procedimiento | Resultado esperado | Resultado obtenido | Estado | Fecha de ejecución | Observaciones |
|---|---|---|---|---|---|---|---|
| PR-nn | Identificador del requisito de la Fase 2 (por ejemplo Reservas 3). | Pasos y datos de prueba usados, con el perfil que los ejecuta. | Lo que debe ocurrir según el requisito. | Lo que ocurre realmente al ejecutarlo. Nunca se cambia el esperado para que encaje. | Pendiente / Superada / Fallida | dd/mm/aaaa de la última ejecución. | Incidencia relacionada (número de issue) y repeticiones. |

## Qué hacer si una prueba falla

1. Se marca como **Fallida** con lo que ha ocurrido realmente.
2. Se abre una incidencia con la plantilla de incidencia, que indica el identificador del caso.
3. Se corrige en una rama propia, y la pull request cierra la incidencia al fusionarse.
4. Se repite el caso junto con las pruebas automáticas. Si se supera, se marca como **Superada** con la nueva fecha y el número de la incidencia en las observaciones. Si vuelve a fallar, la incidencia se reabre.

Un problema se considera resuelto solo cuando el caso que lo detectó vuelve a ejecutarse y se supera.

## Registro

Casos previstos. Se ejecutarán con los datos de ejemplo que se cargan en T13, sobre un taller que incluye dos unidades de material en el precio. Todavía no hay código, así que todos están pendientes.

| ID | Requisito | Acción o procedimiento | Resultado esperado | Resultado obtenido | Estado | Fecha de ejecución | Observaciones |
|---|---|---|---|---|---|---|---|
| PR-01 | Reservas 2 y 3 | Una alumna reserva una plaza eligiendo dos unidades de una variante con existencias. | Se crea la reserva, las plazas libres bajan en una, el stock de la variante baja en dos y el suplemento es 0 €. | Sin ejecutar | Pendiente | | |
| PR-02 | Reservas 5 | En el mismo taller, la alumna elige tres unidades y llega al resumen. | Antes de confirmar se ven dos unidades incluidas, una extra, el suplemento de una unidad extra y las condiciones de cancelación. | Sin ejecutar | Pendiente | | |
| PR-03 | Reservas 3 y 4 | La alumna intenta reservar más unidades de las que quedan en stock de una variante. | La reserva se rechaza con un mensaje claro y ni las plazas ni el stock cambian. | Sin ejecutar | Pendiente | | |
| PR-04 | Fiabilidad 1 | Con una sola plaza libre, se lanzan en paralelo dos peticiones de reserva de dos alumnas distintas. | Solo se confirma una. La otra recibe un error de plaza no disponible y el stock se descuenta una sola vez. | Sin ejecutar | Pendiente | | |
| PR-05 | Sesiones 2 | Con una sesión de 10:00 a 12:00 en un espacio, la responsable crea otra en el mismo espacio de 11:00 a 13:00 y después otra de 12:00 a 14:00. | La primera se rechaza por solapamiento. La segunda se guarda, porque empieza justo cuando termina la existente. | Sin ejecutar | Pendiente | | |
| PR-06 | Reservas 6 y 7 | La alumna cancela una reserva dentro del plazo mínimo de cancelación. | La reserva queda cancelada, la plaza vuelve a estar libre y el stock recupera las unidades reservadas. | Sin ejecutar | Pendiente | | |
| PR-07 | Reservas 6 y 8 | La alumna intenta cancelar una reserva cuando ya ha pasado el plazo mínimo, y después la cancela la responsable. | La cancelación de la alumna se rechaza explicando el motivo. La de la responsable se acepta. | Sin ejecutar | Pendiente | | |
| PR-08 | Negocios 2 | Con sesión de responsable del negocio de cerámica, se piden a la API los materiales y las reservas del negocio de pintura. | La API no devuelve ni modifica ningún dato del otro negocio. | Sin ejecutar | Pendiente | | |
