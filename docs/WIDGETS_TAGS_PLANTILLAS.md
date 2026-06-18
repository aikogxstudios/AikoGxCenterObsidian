# Widgets, tags y plantillas del Command Center CER

## 1. Principio general

Los widgets no son la fuente de verdad.

```txt
Notas reales + tareas + YAML + tags = datos
Widgets = visualizacion
Canvas = panel visual
```

Si un widget no muestra algo, normalmente falta una de estas cosas:

- la nota no esta dentro de `Caos Entre Reinos/`;
- la tarea no tiene tag;
- la tarea no tiene fecha;
- el YAML no tiene el `type` correcto;
- el widget esta leyendo otra carpeta.

## 2. Carpeta principal

Los widgets deben leer desde:

```yaml
project_folder: "Caos Entre Reinos"
```

No usar `Widgets/` como fuente principal de datos reales.

## 3. Tags principales

### Areas de Caos Entre Reinos

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
#caos/general
```

### AikoGx / contenido

```txt
#aikogx/devlog
#aikogx/content
#aikogx/clip
#aikogx/captura
#aikogx/discord
#aikogx/imagen
#aikogx/audio
#aikogx/musica
#aikogx/tiktok
#aikogx/shorts
```

### Estados

```txt
#estado/en-progreso
#estado/bloqueado
#estado/borrador
#estado/publicado
#estado/listo
#estado/idea
#estado/revisar
```

### Prioridad

```txt
#prioridad/alta
#prioridad/media
```

### Bugs y bloqueos

```txt
#bug
#bug/critico
#bug/alto
#bug/medio
#bloqueo
```

## 4. Fechas

Para fechas pendientes:

```md
- [ ] Revisar build del tutorial #caos/tutorial 📅 2026-06-20
```

Para tareas completadas:

```md
- [x] Editar video de la cinematica en espanol #caos/cinematica ✅ 2026-06-17
```

El calendario semanal y mensual dependen del formato:

```txt
📅 YYYY-MM-DD
```

El widget `Lo ultimo hecho` depende del formato:

```txt
✅ YYYY-MM-DD
```

## 5. Notas de progreso por area

Carpeta recomendada:

```txt
Caos Entre Reinos/Progreso/
```

Formato:

```md
---
type: project-area
project: CER
order: 1
icon: 🌸
area: Lore Principal
status: Base principal organizada
---

# Lore Principal

## Tareas de progreso

- [x] Definir Arbol Divino de Sakura #caos/lore ✅ 2026-06-17
- [ ] Ordenar notas antiguas del lore #caos/lore
```

El porcentaje se calcula por tareas completadas / tareas totales.

## 6. Hitos

Carpeta recomendada:

```txt
Caos Entre Reinos/Progreso/Hitos/
```

Formato:

```md
---
type: milestone
project: CER
status: active
order: 1
title: Demo jugable del Abismo
target_date: 2026-08-15
---

# Demo jugable del Abismo

## Tareas del hito

- [x] Definir cinematica inicial #caos/cinematica ✅ 2026-06-17
- [ ] Integrar audios de Benny #caos/audio 📅 2026-06-20
```

## 7. Ideas

Carpeta recomendada:

```txt
Caos Entre Reinos/01 - Produccion/Ideas/
```

Formato:

```md
---
type: idea
project: CER
title: Eventos dinamicos en la Aguja del Caos
category: Aguja
date: 2026-06-17
status: idea
---

# Eventos dinamicos en la Aguja del Caos

Descripcion de la idea.
```

## 8. Mensajes de Codex

Si Codex no puede resolver algo, debe crear un mensaje:

```md
---
type: codex-message
project: CER
status: pendiente
category: Aiko
priority: alta
date: 2026-06-17
---

# Titulo corto

Que paso, que falta y que necesita Fak o Aiko.
```

## 9. Widgets existentes

Los widgets pueden tener nombres visuales diferentes a los ejemplos. Fak uso nombres segun el Command Center de la imagen, no necesariamente `Widgets/01`, `Widgets/02`, etc.

Por eso Codex debe identificar los widgets por:

- nombre visual;
- YAML `widget:`;
- contenido;
- funcion.

Si necesita modificar un widget para anadir tags, rutas o adaptar contenido antiguo, puede hacerlo, siempre que:

- no rompa el diseno visual;
- respete la carpeta principal `Caos Entre Reinos/`;
- deje explicacion de que cambio;
- no convierta widgets en fuente de datos.
