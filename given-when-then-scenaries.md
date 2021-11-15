# Especificación de la aplicación

Hemos creado esta breve especificación para ayudarlo a crear aplicaciones de tareas pendientes increíbles y
consistentes. Asegúrese no solo de leerlo, sino también de comprenderlo.

## Plantilla de la aplicación

Esta plantilla debe usarse como base al implementar una aplicación de tareas pendientes. Antes de implementar, le
recomendamos que interactué con algunas de las otras aplicaciones para ver como están construidas y cómo se comportan.
Consulte la aplicación Backbone si necesita una implementación de referencia. Si algo no está claro o podría mejorarse,
avísenos.

## Funcionalidad

### Escenario Nueva tarea

* [ ] **Dada** una lista de tareas vacía
* [ ] **Cuando** agrego una tarea para 'Comprar queso'
* [ ] **Entonces** solo se muestra ese elemento en la lista
* [ ] **Y** el resumen de la lista es '1 elemento restante'.
* [ ] **Y** el filtro se establece en 'Todos'; 'Activo' y 'Completado' deshabilitados.
* [ ] **Y** 'Borrar completado' no está disponible

### La Lista vacía puede tener dos elementos agregados

* [ ] **Dada** una lista de tareas vacía
* [ ] **Cuando** agrego tareas para 'Comprar queso' y 'Comprar huevos'
* [ ] **Entonces** solo se muestran dos elementos en la lista
* [ ] **Y** el resumen de la lista es '2 elementos restantes'.
* [ ] **Y** el filtro se establece en 'Todos'; 'Activo' y 'Completado' deshabilitados.
* [ ] **Y** 'Borrar completado' no está disponible

### La finalización de una tarea cambia el estado de la lista

* [ ] **Dada** una lista de tareas pendientes con los elementos 'Comprar queso' y 'Comprar huevos' 
* [ ] **Cuando** marco 'Comprar queso' como completada 
* [ ] **Entonces** solo se muestra 'Comprar huevos' como activo
* [ ] **Y** el resumen de la lista es '1 elemento restante'.
* [ ] **Y** el filtro se establece en 'Todos'; 'Activo' y 'Completado' deshabilitados.
* [ ] **Y** 'Borrar completado' está disponible

### Los elementos completados no deben ser visibles para el filtro 'Activo'

* [ ] **Dada** una lista de tareas pendientes con los elementos 'Comprar queso' y 'Comprar huevos'
* [ ] **Y** marco 'Comprar queso' como completada
* [ ] **Cuando** el filtro cambia a 'Activo'
* [ ] **Entonces** solo se enumera el elemento 'Comprar huevos'
* [ ] **Y** el resumen de la lista es '1 elemento restante'.
* [ ] **Y** 'Borrar completado' está disponible

### Todos los elementos completados no deben estar visibles en el filtro activo

* [ ] **Dada** una lista de tareas pendientes con los elementos 'Comprar queso' y 'Comprar huevos'
* [ ] **Y** marco 'Comprar queso' como completada
* [ ] **Y** marco 'Comprar huevos' como completada
* [ ] **Cuando** el filtro cambia a 'Activo'
* [ ] **Entonces** no se muestran elementos
* [ ] **Y** el resumen de la lista es '0 elementos restantes'.
* [ ] **Y** 'Borrar completado' está disponible

### Los elementos son completar no deben ser visibles en el filtro completado

* [ ] **Dada** una lista de tareas pendientes con los elementos 'Comprar queso' y 'Comprar huevos'
* [ ] **Y** marco 'Comprar queso' como completada
* [ ] **Cuando** el filtro cambia a 'Completado'
* [ ] **Entonces** solo se enumera el elemento 'Comprar huevos'
* [ ] **Y** el resumen de la lista es '1 elemento restante'.
* [ ] **Y** 'Borrar completado' está disponible

### Los elementos se pueden borrar

* [ ] **Dada** una lista de tareas pendientes con los elementos 'Comprar queso' y 'Comprar huevos'
* [ ] **Y** el elemento 'Comprar queso' está marcado como completado
* [ ] **Cuando** se ejecuta la acción 'Borrar completado'
* [ ] **Entonces** solo se enumera 'Comprar huevos'
* [ ] **Y** el resumen de la lista es '1 elemento restante'.

### Completar todas las tareas cuando no se completó ninguno

* [ ] **Dada** una lista de tareas pendientes con los elementos 'Comprar queso' y 'Comprar huevos'
* [ ] **Cuando** la acción 'limpiar todos los items' es ejecutada
* [ ] **Entonces** ambos elementos son listados como completados
* [ ] **Pero** nada en la lista está activo
* [ ] **Y** el resumen de la lista es '0 elementos restantes'.

### Completar todas las tareas cuando se complete una de las dos

* [ ] **Dada** una lista de tareas pendientes con los elementos 'Comprar queso' y 'Comprar huevos'
* [ ] **Y** el elemento 'Comprar queso' está marcado como completado
* [ ] **Cuando** se activa la acción de completar todos los elementos
* [ ] **Luego** se listan ambos elementos
* [ ] **Pero** nada en la lista está activo
* [ ] **Y** el resumen de la lista es '0 elementos restantes'.

### completar todas las tareas no completadas cuando se completen dos de dos

* [ ] **Dada** una lista de tareas pendientes con los elementos 'Comprar queso' y 'Comprar huevos'
* [ ] **Y** el elemento 'Comprar queso' está marcado como completado
* [ ] **Y** el elemento 'Comprar huevos' está marcado como completado
* [ ] **Cuando** se activa la acción de completar todos los elementos
* [ ] **Entonces** ambos elementos son listados
* [ ] **Y** ambos elementos están activos
* [ ] **Y** el resumen de la lista es '2 elementos restantes'.

### Las tareas se pueden quitar directamente
* [ ] **Dada** una lista de tareas pendiente con un solo elemento 'Comprar queso'
* [ ] **Cuando** se elimina el elemento 'Comprar queso'
* [ ] **Entonces** la lista está vacía

