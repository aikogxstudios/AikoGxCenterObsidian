# Revision final para Codex

Este archivo resume lo que Codex debe entender antes de tocar la boveda de Obsidian.

## 1. Objetivo real

Organizar la nueva boveda de Obsidian de Caos Entre Reinos como un Command Center visual para Fak.

La boveda antigua esta desordenada. Codex debe migrar y ordenar sin romper informacion.

## 2. Fuente antigua

Ruta de la boveda antigua:

```txt
H:/Proyectos/Proyectos
```

## 3. Regla critica de Lore

No modificar archivos originales dentro de carpetas llamadas Lore en la boveda antigua.

Codex puede leer, resumir y crear copias organizadas en la nueva boveda, pero no alterar los originales.

## 4. Carpeta principal nueva

Toda la informacion real del proyecto debe vivir en:

```txt
Caos Entre Reinos/
```

Los widgets no son fuente de verdad. Solo muestran datos desde notas reales, tareas, YAML y tags.

## 5. Flujo Notas Codex

Estructura:

```txt
Notas Codex/
  Nota rapida para codex.md
  Apuntes y archivos/
```

Fak escribe una entrada rapida desordenada. Codex debe:

1. leerla;
2. detectar avances, bugs, material e ideas;
3. actualizar tareas relacionadas;
4. crear tareas nuevas si hace falta;
5. generar ideas para redes, devlogs, Discord o web si hay material;
6. guardar copia limpia en `Notas Codex/Apuntes y archivos/`;
7. resetear la nota rapida.

## 6. Tags obligatorios

Usar tags para que los widgets funcionen:

```txt
#caos/cinematica
#caos/tutorial
#caos/aguja
#caos/orialis
#caos/enemigos
#caos/gameplay
#caos/lore
#caos/ui
#caos/audio
#caos/bugs
#aikogx/devlog
#aikogx/content
#aikogx/clip
#aikogx/captura
#estado/en-progreso
#estado/bloqueado
#prioridad/alta
```

## 7. Fechas

Tareas completadas:

```md
- [x] Tarea hecha #caos/tutorial ✅ 2026-06-17
```

Fechas futuras:

```md
- [ ] Revisar tutorial #caos/tutorial 📅 2026-06-20
```

Si Codex detecta una fecha importante, debe crear evento en Google Calendar si tiene herramienta y permiso. Si no puede, debe dejar mensaje para Fak.

## 8. Redes y contenido

Si hay capturas, clips o avances visuales, Codex debe decidir el mejor uso:

- YouTube Shorts;
- TikTok;
- Discord;
- Devlog web;
- Entrada AikoGx Studios;
- tarea para companero.

No crear publicaciones inventadas. Preparar borradores e ideas basadas en material real.

## 9. Widgets

Codex puede adaptar widgets para leer nuevos tags o rutas, pero no debe romper el diseno visual creado por Fak.

Si un widget no muestra datos, revisar primero:

- carpeta leida;
- tags;
- YAML;
- formato de fechas;
- si la tarea esta dentro de `Caos Entre Reinos/`.

## 10. Version actual

Version de trabajo actual:

```txt
0.06 / 0.0.6
```

No unificar otras versiones historicas sin permiso si forman parte de notas antiguas.

## 11. Regla final

Fak decide la estructura. Codex organiza, etiqueta, migra y deja trazabilidad.
