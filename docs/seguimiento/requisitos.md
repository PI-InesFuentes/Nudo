# Matriz de cumplimiento de requisitos

Relaciona los requisitos funcionales de la Fase 2 y los no funcionales más importantes con el criterio que permite aceptarlos, la comprobación prevista y la evidencia que se guardará. Sirve de referencia en cada hito para saber qué está cumplido, qué falta y qué necesita correcciones. El estado de un requisito solo cambia cuando existe su evidencia.

**Estados posibles**

- **Pendiente:** todavía no se ha comprobado.
- **Cumple:** la prueba se ha superado y la evidencia está guardada.
- **Cumple parcialmente:** falla en algún caso concreto, anotado en una incidencia.
- **No cumple:** la prueba ha fallado.

## Plantilla

| Requisito o condición | Criterio de aceptación | Comprobación o prueba prevista | Evidencia | Estado de cumplimiento |
|---|---|---|---|---|
| Identificador de la Fase 2 (por ejemplo Reservas 3). | Condición concreta que debe cumplirse para aceptarlo. | Casos PR-nn de [pruebas.md](pruebas.md) e indicadores IC-nn de [indicadores.md](indicadores.md) que lo comprueban. | Tipo de evidencia y, cuando exista, enlace a ella (prueba automática, pull request, archivo de [evidencias/](evidencias/)). | Pendiente / Cumple / Cumple parcialmente / No cumple, con la fecha del último cambio de estado. |

## Matriz

En esta primera versión todos los requisitos están pendientes.

| Requisito o condición | Criterio de aceptación | Comprobación o prueba prevista | Evidencia | Estado de cumplimiento |
|---|---|---|---|---|
| Negocios 1 | Al registrar un negocio se crean el negocio y la cuenta de su responsable, que accede a su panel. | Alta de un negocio desde la portada de Nudo. | Registro de pruebas | Pendiente |
| Negocios 2 | Ninguna petición devuelve ni modifica datos de otro negocio. | PR-08 y prueba automática con los tres negocios (IC-07). | Prueba automática | Pendiente |
| Negocios 3 | Cada negocio tiene una página pública con sus talleres y sesiones, sin datos de otros. | Abrir sin sesión la página de los tres negocios. | Capturas | Pendiente |
| Cuentas 1 | Una alumna se registra, inicia y cierra sesión, y su contraseña se guarda resumida. | Registro, inicio y cierre de sesión y revisión de la base de datos. | Registro de pruebas | Pendiente |
| Cuentas 2 | La responsable crea, modifica y desactiva monitoras, y una monitora desactivada no puede entrar. | Gestión de una monitora desde la zona de la responsable. | Registro de pruebas | Pendiente |
| Cuentas 3 | Cada perfil ve solo sus pantallas y la API rechaza las peticiones sin permiso. | Llamadas a cada ruta con cada perfil (IC-08). | Prueba automática | Pendiente |
| Talleres 1 | La responsable crea, consulta, modifica y elimina talleres con nombre, descripción y precio. | Prueba de cada operación. | Registro de pruebas | Pendiente |
| Talleres 2 | Cada taller guarda categoría elegible, unidades incluidas y precio por unidad extra, y la reserva las aplica. | Definir las reglas y comprobarlas con PR-02. | Registro de pruebas | Pendiente |
| Sesiones 1 | La responsable gestiona sesiones con fecha, hora, duración, aforo, espacio y monitora. | Prueba de cada operación. | Registro de pruebas | Pendiente |
| Sesiones 2 | Se rechaza una sesión solapada en espacio o monitora, también al modificarla, y se acepta una consecutiva. | PR-05 y prueba automática (IC-04). | Prueba automática | Pendiente |
| Sesiones 3 | La monitora ve sus sesiones con las asistentes y el material de cada una, y no las de otras monitoras. | Consulta con una monitora que tiene reservas en su sesión. | Capturas | Pendiente |
| Stock 1 | La responsable gestiona materiales con categoría, nombre, variante, cantidad y mínimo. | Prueba de cada operación. | Registro de pruebas | Pendiente |
| Stock 2 | El panel muestra los materiales por debajo de su mínimo y deja de mostrarlos al reponerlos. | Bajar un material del mínimo con reservas y reponerlo. | Capturas | Pendiente |
| Reservas 1 | Se consultan sesiones futuras por taller o por fecha, con plazas libres y material disponible. | Consulta con los datos de ejemplo. | Registro de pruebas | Pendiente |
| Reservas 2 | La alumna reserva eligiendo variantes y cantidades solo de la categoría permitida. | PR-01 e intento de elegir otra categoría por la API. | Prueba automática | Pendiente |
| Reservas 3 | Plaza y material se descuentan en una sola operación y, si falta algo, no se guarda nada. | PR-01, PR-03 y PR-04 (IC-02). | Prueba automática | Pendiente |
| Reservas 4 | Se rechazan las reservas sin plazas, sin existencias, duplicadas o de sesiones comenzadas. | Un intento de cada tipo (IC-05). | Prueba automática | Pendiente |
| Reservas 5 | Antes de confirmar se ven material, unidades incluidas, suplemento y condiciones de cancelación, y el importe válido es el que calcula el servidor. | PR-02 y comparación del importe del cliente con el del servidor. | Capturas y prueba automática | Pendiente |
| Reservas 6 | La alumna consulta sus reservas y solo puede cancelar dentro del plazo. | PR-06 y PR-07. | Registro de pruebas | Pendiente |
| Reservas 7 | Al cancelar se libera la plaza y el material vuelve al stock. | PR-06 y prueba automática del stock antes y después. | Prueba automática | Pendiente |
| Reservas 8 | La responsable consulta y cancela cualquier reserva de su negocio y fija el plazo mínimo. | PR-07 y cambio del plazo desde Ajustes. | Registro de pruebas | Pendiente |
| Reservas 9 | Tras reservar o cancelar aparece una confirmación y el cambio se ve en Mis reservas. | Dentro de PR-01 y PR-06. | Capturas | Pendiente |
| Reservas 10 | No se borran talleres, sesiones ni materiales con reservas activas ni se reduce el aforo por debajo de lo reservado. | Intento de cada operación (IC-10). | Prueba automática | Pendiente |
| Historial 1 | Cada reserva, cancelación y movimiento de stock queda registrado con su fecha y se filtra por fechas, taller y material. | Revisar el historial después de PR-01 y PR-06 y aplicar cada filtro. | Capturas | Pendiente |
| Fiabilidad 1 | Con dos reservas simultáneas de la última plaza o del último material, solo se confirma una. | PR-04 (IC-03). | Prueba automática | Pendiente |
| Seguridad 1 y 2 | Contraseñas guardadas con un algoritmo de resumen seguro y toda la comunicación por HTTPS. | Revisión de la base de datos y del certificado (IC-09). | Capturas | Pendiente |
| Seguridad 3 | Las peticiones que modifican datos sin protección CSRF se rechazan y el servidor valida todos los datos. | Peticiones sin token y con datos incorrectos por la API (IC-06). | Registro de pruebas | Pendiente |
| Persistencia 1 | Los datos se guardan en PostgreSQL y existe una copia de la base de datos publicada fuera de Supabase. | Restaurar en local una copia exportada. | Copia guardada | Pendiente |
| Adaptación 1 | Ninguna pantalla con desplazamiento horizontal entre 360 píxeles y escritorio. | Revisión a 360, 768 y 1280 píxeles (IC-11). | Capturas | Pendiente |
| Accesibilidad 1 | Pantallas principales con el nivel AA de WCAG 2.2. | Lighthouse y recorrido con teclado (IC-12). | Informes de Lighthouse | Pendiente |
| Usabilidad 1 | Una reserva sin ayuda en cuatro pasos como máximo desde la ficha del taller. | Evaluación con usuarias (IC-13). | Fichas de evaluación | Pendiente |
| Compatibilidad 1 | La aplicación funciona en las versiones actuales de Chrome, Firefox, Edge y Safari. | Ciclo de reserva en los cuatro navegadores (IC-14). | Registro de pruebas | Pendiente |
