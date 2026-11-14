# Cronograma

Planificación inicial con una dedicación de 12 horas semanales, de lunes a sábado, organizada por las fases del módulo. El diagrama de Gantt está en [Google Sheets](https://docs.google.com/spreadsheets/d/1ONJ4jMtMiodZj_f51nATdA46F4xQM923tnt3TA9thY8/edit?usp=sharing). Se actualiza al cerrar cada entrega o si una tarea se desvía más de una semana.

## Fase 4. Seguimiento inicial y prototipado

Del 14/11/2026 al 28/11/2026, 26 horas.

| ID | Tarea | Inicio | Fin | Horas | Depende de |
|---|---|---|---|---|---|
| T01 | Crear el repositorio y el tablero | 14/11/2026 | 15/11/2026 | 2 | Ninguna |
| T02 | Entrevistar a talleres reales | 16/11/2026 | 16/11/2026 | 2 | Ninguna |
| T03 | Elegir la tecnología del servidor | 17/11/2026 | 17/11/2026 | 2 | T01 |
| T04 | Preparar el entorno local | 18/11/2026 | 18/11/2026 | 2 | T03 |
| T05 | Preparar el entorno de pruebas | 19/11/2026 | 19/11/2026 | 2 | T04 |
| T09 | Bocetar las pantallas | 20/11/2026 | 21/11/2026 | 4 | T02 |
| T10 | Definir la identidad visual | 23/11/2026 | 23/11/2026 | 2 | T09 |
| T11 | Montar el prototipo de reserva | 24/11/2026 | 24/11/2026 | 2 | T09, T10 |
| T41 | Definir el seguimiento y el control | 25/11/2026 | 27/11/2026 | 6 | T01 |
| T42 | Preparar la entrega de la Fase 4 | 28/11/2026 | 28/11/2026 | 2 | T11, T41 |

## Fase 5. Interfaz y cliente

Del 30/11/2026 al 26/12/2026, 48 horas.

| ID | Tarea | Inicio | Fin | Horas | Depende de |
|---|---|---|---|---|---|
| T06 | Diseñar el modelo de datos | 30/11/2026 | 01/12/2026 | 4 | T02, T03 |
| T07 | Definir la API y los permisos | 02/12/2026 | 03/12/2026 | 4 | T06 |
| T08 | Concretar los casos límite | 04/12/2026 | 04/12/2026 | 2 | T07 |
| T25 | Montar la base del cliente | 05/12/2026 | 07/12/2026 | 4 | T04, T10 |
| T26 | Pantallas públicas y de acceso | 08/12/2026 | 09/12/2026 | 4 | T11, T25 |
| T27 | Zona de la alumna | 10/12/2026 | 12/12/2026 | 6 | T26 |
| T28 | Zona de la monitora | 14/12/2026 | 14/12/2026 | 2 | T25 |
| T29 | Zona de la responsable | 15/12/2026 | 18/12/2026 | 8 | T25 |
| T30 | Adaptación a móvil y accesibilidad | 19/12/2026 | 21/12/2026 | 4 | T26 a T29 |
| T12 | Crear el esquema de la base de datos | 22/12/2026 | 23/12/2026 | 4 | T04, T06 |
| T13 | Cargar los datos de ejemplo | 24/12/2026 | 24/12/2026 | 2 | T12 |
| T43 | Preparar la entrega de la Fase 5 | 25/12/2026 | 26/12/2026 | 4 | T30 |

## Fase 6. Servidor e integración

Del 28/12/2026 al 23/01/2027, 48 horas.

| ID | Tarea | Inicio | Fin | Horas | Depende de |
|---|---|---|---|---|---|
| T14 | Montar la base del servidor | 28/12/2026 | 28/12/2026 | 2 | T12 |
| T15 | Alta de negocios y separación de datos | 29/12/2026 | 30/12/2026 | 4 | T14 |
| T16 | Registro e inicio de sesión | 31/12/2026 | 01/01/2027 | 4 | T15 |
| T17 | Permisos y cuentas de monitora | 02/01/2027 | 04/01/2027 | 4 | T16 |
| T18 | Gestión de talleres y reglas de material | 05/01/2027 | 06/01/2027 | 4 | T17 |
| T19 | Gestión de sesiones y solapamientos | 07/01/2027 | 08/01/2027 | 4 | T18 |
| T20 | Gestión de materiales y stock | 09/01/2027 | 09/01/2027 | 2 | T17 |
| T21 | Reserva con plaza y material | 11/01/2027 | 14/01/2027 | 8 | T08, T19, T20 |
| T22 | Cancelación de reservas | 15/01/2027 | 16/01/2027 | 4 | T21 |
| T23 | Historial y protecciones | 18/01/2027 | 18/01/2027 | 2 | T22 |
| T24 | Pruebas automáticas del servidor | 19/01/2027 | 20/01/2027 | 4 | T23 |
| T31 | Conectar el cliente con la API | 21/01/2027 | 22/01/2027 | 4 | T24, T30 |
| T44 | Preparar la entrega de la Fase 6 | 23/01/2027 | 23/01/2027 | 2 | T31 |

## Fase 7. Despliegue, pruebas e informes

Del 25/01/2027 al 06/02/2027, 24 horas.

| ID | Tarea | Inicio | Fin | Horas | Depende de |
|---|---|---|---|---|---|
| T32 | Revisar el ciclo completo | 25/01/2027 | 25/01/2027 | 2 | T05, T31 |
| T33 | Comprobar cada requisito | 26/01/2027 | 26/01/2027 | 2 | T32 |
| T34 | Pruebas de seguridad, compatibilidad y usabilidad | 27/01/2027 | 27/01/2027 | 2 | T32 |
| T35 | Corregir las incidencias | 28/01/2027 | 29/01/2027 | 4 | T33, T34 |
| T36 | Publicar la aplicación en Cloud Run | 30/01/2027 | 01/02/2027 | 4 | T35 |
| T37 | Base de datos publicada y copias | 02/02/2027 | 02/02/2027 | 2 | T13, T36 |
| T45 | Proyecto de transformación digital | 03/02/2027 | 03/02/2027 | 2 | T02 |
| T46 | Informe de sostenibilidad | 04/02/2027 | 04/02/2027 | 2 | T02 |
| T38 | Documentar la API y la instalación | 05/02/2027 | 05/02/2027 | 2 | T35 |
| T39 | Escribir el manual de uso | 06/02/2027 | 06/02/2027 | 2 | T37 |

## Fase 8. Cierre del seguimiento

Del 08/02/2027 al 11/02/2027, 8 horas.

| ID | Tarea | Inicio | Fin | Horas | Depende de |
|---|---|---|---|---|---|
| T47 | Cerrar el seguimiento | 08/02/2027 | 09/02/2027 | 4 | T35, T41 |
| T40 | Memoria final y presentación | 10/02/2027 | 11/02/2027 | 4 | T38, T39, T47 |

## Entregas

| Entrega | Fecha |
|---|---|
| Fase 3 | 15/11/2026 |
| Fase 4 | 29/11/2026 |
| Fase 5 | 27/12/2026 |
| Fase 6 | 24/01/2027 |
| Fase 7 | 07/02/2027 |
| Fase 8 | Semana del 08/02/2027 |

Total: 154 horas en 47 tareas.
