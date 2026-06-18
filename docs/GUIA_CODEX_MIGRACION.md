# Guia completa para Codex - Migracion del Command Center CER

## 0. Proposito

Esta guia indica como debe actuar Codex para migrar informacion desde la boveda antigua de Obsidian hacia la nueva boveda visual del proyecto **Caos Entre Reinos: Reborn**.

La nueva boveda no es un almacen de notas sueltas. Es un **Command Center** con widgets, Canvas, Dataview, Tasks, notas reales y flujo de trabajo con Codex.

## 1. Identidad y privacidad

En cualquier archivo publico, README, issue, commit, prompt, documentacion o nota exportable usar unicamente:

```txt
Fak
```

No usar el nombre real del usuario.

## 2. Fuente antigua

La informacion antigua esta en la ruta local:

```txt
H:/Proyectos/Proyectos
```

Codex debe leer esa informacion y migrarla a la nueva estructura.

## 3. Regla critica: Lore antiguo

Si en la boveda antigua hay carpetas llamadas:

```txt
Lore
```

Codex NO debe modificar esos archivos originales.

Puede:

- leerlos;
- analizarlos;
- resumirlos;
- crear copias organizadas en la nueva boveda;
- crear indices o referencias;
- extraer tareas o ideas derivadas.

No puede:

- reescribir los archivos originales de Lore;
- borrar contenido de Lore antiguo;
- mover esos archivos sin permiso;
- mezclar lore antiguo con cambios inventados.

## 4. Carpeta principal de la nueva boveda

Toda la informacion real del proyecto debe ir dentro de:

```txt
Caos Entre Reinos/
```

Los widgets deben leer principalmente desde esta carpeta. No deben contar toda la boveda ni usar `Widgets/` como fuente principal de datos reales.

Estructura recomendada:

```txt
Caos Entre Reinos/
  00 - Dashboard/
  01 - Produccion/
  02 - Lore/
  03 - Gameplay/
  04 - Tutorial - Abismo/
  05 - Aguja del Caos/
  06 - Orialis - Cartas/
  07 - Enemigos - IA/
  08 - Cinematica/
  09 - Bugs/
  10 - Devlogs/
  11 - Material Visual/
  Progreso/
  Progreso/Hitos/
```

Notas auxiliares:

```txt
Widgets/
Notas Codex/
  Nota rapida para codex.md
  Apuntes y archivos/
Inbox/
Migracion pendiente/
```

Si la estructura exacta creada por Fak tiene nombres diferentes, respetar la estructura de Fak y adaptar los widgets o rutas si hace falta.

## 5. Regla de estructura

Codex no debe decidir una estructura nueva desde cero.

Debe:

- respetar la estructura visual y mental creada por Fak;
- no borrar notas;
- no mover carpetas sin permiso;
- no inventar datos;
- si no sabe donde poner algo, mandarlo a `Migracion pendiente/`;
- dejar un resumen claro de todo lo migrado.

## 6. Que se debe migrar

Migrar o reconstruir de forma ordenada:

- tareas;
- bugs;
- lore;
- progreso;
- tutorial / Abismo;
- Aguja del Caos;
- Orialis / cartas;
- enemigos / IA;
- cinematica;
- devlogs;
- ideas;
- material visual;
- notas de produccion;
- fechas importantes;
- contenido para redes;
- tareas futuras.

## 7. Como tratar notas antiguas desordenadas

Para cada nota antigua:

1. Leer el contenido completo.
2. Identificar si es lore, gameplay, tarea, bug, idea, devlog, contenido para redes, material visual, nota historica o nota confusa.
3. Migrar a la carpeta correcta dentro de `Caos Entre Reinos/`.
4. Anadir propiedades YAML si ayudan al Command Center.
5. Anadir tags compatibles con los widgets.
6. No inventar estado, fecha o progreso.
7. Si no hay suficiente contexto, crear una nota en `Migracion pendiente/`.

## 8. Reglas para tareas

Las tareas deben estar en formato markdown compatible con Tasks:

```md
- [ ] Tarea pendiente #caos/tutorial
- [x] Tarea completada #caos/tutorial OK 2026-06-17
```

Preferencia en Obsidian para completadas:

```md
- [x] Tarea completada #caos/tutorial ✅ 2026-06-17
```

No inventar fechas. Si el avance ocurrio en la fecha de una nota rapida y el texto lo confirma, se puede usar esa fecha.

## 9. Reglas para fechas importantes

Si Codex detecta una fecha importante, por ejemplo:

- fecha objetivo de demo;
- reunion;
- entrega;
- doblaje;
- publicacion de devlog;
- revision de build;
- deadline;
- evento de comunidad;

debe anotarla tambien en Google Calendar si tiene permiso y herramienta disponible.

Si no puede usar Google Calendar directamente, debe crear una nota tipo `codex-message` indicando fecha detectada, motivo, titulo sugerido del evento y si debe ser evento, recordatorio o tarea.

## 10. Version actual

El proyecto esta trabajando actualmente alrededor de:

```txt
0.06 / 0.0.6
```

Puede haber referencias antiguas o temporales como `v0.1.0`, `v0.2.0` o `Pre-Alpha`. Codex debe detectarlas y unificarlas cuando Fak lo pida, sin cambiar informacion historica si esta documentada como antigua.

## 11. Resultado esperado

Al terminar una migracion, Codex debe dejar:

```txt
Caos Entre Reinos/ = datos reales organizados
Widgets/ = widgets del Command Center
Notas Codex/ = entrada rapida y archivo de apuntes
Migracion pendiente/ = dudas o contenido no clasificado
```

Y crear un resumen tipo:

```md
# Resumen de migracion

## Archivos revisados
- ...

## Migrado correctamente
- ...

## Tareas creadas
- ...

## Tareas completadas
- ...

## Fechas importantes detectadas
- ...

## Dudas / pendiente de Fak
- ...
```
