# Nudo

Aplicación web para pequeños talleres de manualidades y artesanía que gestiona las reservas de plazas de cada sesión conectadas con el stock del material que consume cada plaza.

Proyecto Intermodular de 2º de DAW. Autora: Inés Fuentes Martínez.

Este repositorio forma parte de la organización de GitHub del proyecto, creada el curso pasado, donde se pueden consultar por separado todas las entregas desde primero.

## Problema que resuelve

En los talleres pequeños, las plazas y el material se gestionan por separado y a mano, con mensajes, libretas y hojas de cálculo. Eso provoca sobreinscripciones, material que sobra o que falta y cancelaciones que no liberan nada. En Nudo, reservar consume material, cancelar lo devuelve y sin plaza o sin material no se puede reservar.

## Funcionalidades previstas

- Alta de negocios, cada uno con sus datos separados de los demás.
- Tres perfiles con permisos distintos: alumna, monitora y responsable.
- Gestión de talleres, sesiones, materiales y reglas de material por taller.
- Reserva con elección de material y cálculo del suplemento informativo.
- Cancelación con devolución de la plaza y del material.
- Vista de la monitora con asistentes y material elegido.
- Avisos de stock bajo e historial de reservas y movimientos.

## Tecnologías

React con Vite en el cliente, Node.js en el servidor y PostgreSQL como base de datos. El framework del servidor se decide en la siguiente tarea.

## Estado actual

Fase 3, planificación de la ejecución. El repositorio todavía no contiene código de la aplicación. Las tareas están en las issues y en el tablero del proyecto, organizadas por las fases 4 a 8 del módulo.

## Documentación

Toda la documentación está en la carpeta [`docs/`](docs/):

- `cronograma.md`: tareas, fechas previstas e hitos.
- PDF de las entregas de este curso.

