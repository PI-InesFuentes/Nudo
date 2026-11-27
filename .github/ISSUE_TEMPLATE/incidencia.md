---
name: Incidencia
about: Error o problema que hace que la aplicación no se comporte como se espera
title: "INC "
labels: incidencia
assignees: ''
---

<!--
Gravedad (añade también su etiqueta):
- Crítica: impide reservar o cancelar, deja plazas o stock con valores incorrectos, pierde datos o muestra datos de otro negocio. Se atiende antes que cualquier otra tarea.
- Alta: falla una funcionalidad esencial, pero el resto se puede usar. Dentro de la misma semana y antes del siguiente hito.
- Media: falla una validación, un mensaje o una pantalla secundaria, sin afectar a los datos. Antes de la entrega de la Fase 7.
- Baja: problema visual, de textos o de comodidad de uso. Se agrupan y se resuelven en T35 si hay tiempo.
Si dudas entre dos niveles, elige el más alto.
-->

### Descripción
<!-- Qué falla, en qué pantalla o ruta de la API y con qué perfil. -->

### Entorno
<!-- Local, entorno de pruebas o aplicación publicada, con el navegador y el dispositivo. -->

### Pasos para reproducirlo
1. 
2. 
3. 

### Resultado esperado
<!-- Lo que debería ocurrir según el requisito o el caso de prueba. -->

### Resultado obtenido
<!-- Lo que ocurre realmente, con captura o mensaje de error si lo hay. -->

### Requisito o prueba relacionada
<!-- Requisito de la Fase 2 (por ejemplo Reservas 7) y caso PR-nn, si existe. -->

### Gravedad
<!-- Crítica / Alta / Media / Baja, y por qué. Si cambia al investigar, anótalo aquí. -->

### Estado
<!-- Columna del tablero en la que se encuentra. -->

### Solución aplicada
<!-- Se rellena al corregir: causa del fallo, cambio realizado y enlace a la pull request (con "Closes #número"). -->

### Comprobación posterior
<!-- Se rellena antes de cerrar: pasos y caso de prueba repetidos, pruebas automáticas, fecha y resultado. -->
- [ ] Repetidos los pasos para reproducirlo sin que aparezca el fallo
- [ ] Repetido el caso de prueba relacionado y marcado como superado en docs/seguimiento/pruebas.md
- [ ] Pruebas automáticas superadas (y añadida una nueva si el fallo era del servidor y no la tenía)
