# Estado del Command Center CER

Fecha de referencia: 2026-06-19  
Proyecto: Caos Entre Reinos: Reborn  
Uso: documento de referencia para Aiko, Fak y Codex.

Este documento resume cómo quedó planteado el Command Center de Obsidian para Caos Entre Reinos y qué reglas deben respetarse al modificarlo en el futuro.

---

## 1. Regla maestra actual del proyecto

La prioridad real del proyecto ahora mismo es:

```txt
Cerrar cinemática inicial + tutorial del Abismo.
```

Todo lo demás debe ordenarse alrededor de esa prioridad, no competir con ella.

Orden de prioridad recomendado:

```txt
P0 -> Cinemática inicial y tutorial del Abismo.
P1 -> Versión inglesa, guion para Benny, diálogos por zonas, traducción y ajustes del nivel.
P2 -> Entrada a la Aguja del Caos y loop inicial.
P3 -> UI, audio, devlogs, material visual y pulido.
P4 -> Backlog futuro: hub ampliado, consumibles, multijugador, mundo abierto, sistemas avanzados.
```

El widget Hoy debe respetar este foco y no llenarse con backlog.

---

## 2. Estructura principal de la bóveda

La carpeta principal real del proyecto es:

```txt
Caos Entre Reinos/
```

Las rutas más importantes son:

```txt
Caos Entre Reinos/00 - Dashboard/
Caos Entre Reinos/01 - Producción/
Caos Entre Reinos/02 - Lore/
Caos Entre Reinos/03 - Gameplay/
Caos Entre Reinos/04 - Tutorial - Abismo/
Caos Entre Reinos/05 - Aguja del Caos/
Caos Entre Reinos/06 - Orialis - Cartas/
Caos Entre Reinos/07 - Enemigos - IA/
Caos Entre Reinos/08 - Cinemática/
Caos Entre Reinos/09 - Bugs/
Caos Entre Reinos/10 - Devlogs/
Caos Entre Reinos/11 - Material Visual/
Caos Entre Reinos/Progreso/
Caos Entre Reinos/Progreso/Hitos/
Widgets/
Notas Codex/
Notas Codex/Apuntes y archivos/
Inbox/
Migración pendiente/
AikoGx Studios/
```

Regla base:

```txt
Notas reales + tareas + YAML + tags + fechas = fuente de datos.
Widgets = visualización.
Canvas = panel visual.
```

Los widgets no son la fuente de verdad. Solo muestran lo que leen desde notas reales.

---

## 3. Reglas críticas de seguridad

- No modificar archivos originales dentro de carpetas antiguas llamadas `Lore`.
- No inventar fechas, estados, avances ni decisiones.
- No cambiar porcentajes manualmente.
- El progreso se calcula por tareas completadas / tareas totales.
- No activar tareas antiguas grandes sin confirmación de Fak.
- No hacer reestructuraciones grandes de carpetas sin plan previo.
- No renombrar carpetas principales si puede romper rutas o enlaces.
- Usar `Fak` en documentación pública o de trabajo; no usar datos personales.
- Si algo no tiene destino claro, moverlo a `Migración pendiente/` o dejarlo como decisión pendiente.

---

## 4. Sistema de tareas

Formato correcto de tarea pendiente:

```md
- [ ] Nombre de la tarea #tag 📅 YYYY-MM-DD
```

Formato correcto de tarea completada:

```md
- [x] Nombre de la tarea #tag ✅ YYYY-MM-DD
```

Las decisiones tomadas también deben usar formato de tarea completada si los widgets deben leerlas:

```md
- [x] Confirmar Orialis como nombre oficial de las cartas #caos/orialis ✅ 2026-06-18
```

No basta con escribir una frase con una fecha. Para que los widgets la lean debe ser una tarea real.

Incorrecto:

```txt
Día 27 beta test.
```

Correcto:

```md
- [ ] Tener lista una versión jugable para beta test #caos/general #prioridad/alta 📅 2026-06-27
```

---

## 5. Tags principales

Tags de Caos:

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

Tags de AikoGx / contenido:

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

Estados:

```txt
#estado/en-progreso
#estado/bloqueado
#estado/borrador
#estado/publicado
#estado/listo
#estado/idea
#estado/revisar
```

Prioridades:

```txt
#prioridad/alta
#prioridad/media
```

Bugs:

```txt
#bug
#bug/critico
#bug/alto
#bug/medio
#bloqueo
```

---

## 6. Widget Hoy

El widget Hoy no es un backlog. Es una lista corta de acciones recomendadas para el día actual.

Debe mostrar máximo 5 tareas.

Prioridad de lectura deseada:

```txt
1. Tareas con #hoy.
2. Tareas con 📅 fecha actual.
3. Tareas con #prioridad/alta.
4. Tareas con #estado/en-progreso.
5. Tareas P0/P1 escritas como tareas reales.
```

Hoy debe centrarse en cinemática inicial + tutorial del Abismo mientras esa sea la prioridad real.

Ejemplo de tareas válidas para Hoy:

```md
- [ ] Revisar la cinemática inicial en español y anotar fallos concretos #caos/cinematica #hoy #prioridad/alta 📅 2026-06-19
- [ ] Hacer retoques finales del vídeo español #caos/cinematica #hoy #prioridad/alta 📅 2026-06-19
- [ ] Pasar el guion en español a Benny #caos/audio #caos/cinematica #hoy #prioridad/alta 📅 2026-06-19
- [ ] Organizar los diálogos del tutorial por zonas #caos/tutorial #hoy #prioridad/alta 📅 2026-06-19
- [ ] Ajustar el nivel del tutorial para que encaje con los diálogos nuevos #caos/tutorial #hoy #prioridad/alta 📅 2026-06-19
```

Si Hoy aparece vacío, revisar:

- si las tareas son `- [ ]` reales;
- si tienen `#hoy` o `📅 YYYY-MM-DD`;
- si están dentro de una carpeta que el widget lee;
- si el widget está buscando tareas pero Codex escribió texto normal.

---

## 7. Widgets Semana y Mes

Semana y Mes son calendario, no recomendaciones.

Regla esperada:

```txt
Hoy = máximo 5 tareas recomendadas.
Semana = tareas fechadas dentro de la semana actual + próximos hitos si procede.
Mes = tareas fechadas + hitos del mes.
Hitos = objetivos grandes con fecha límite.
```

El widget Mes debe leer:

- tareas reales con `📅 YYYY-MM-DD`;
- hitos con `target_date`;
- hitos con `start_date` y `end_date`;
- varias tareas en un mismo día si existen;
- tareas dentro de `Caos Entre Reinos/` y subcarpetas relevantes.

El widget Semana puede mostrar solo la semana actual, pero conviene que tenga una sección de próximos hitos de los próximos 14 días para no perder fechas cercanas como beta test.

---

## 8. Sistema de fechas y Google Calendar

Cuando Fak escriba fechas en `Crear tareas` o `Nota rapida`, Codex debe convertirlas en tareas reales, no dejarlas como texto normal.

Ejemplos que debe detectar:

```txt
día 27 y 28 necesito tener lista una beta
mañana revisar cinemática
el viernes pasar guion a Benny
antes del 30 preparar build
la semana que viene probar tutorial
en julio revisar UI
cuando lleguen los audios de Benny integrar doblaje
```

Regla:

```md
- [ ] Nombre de la tarea #tag #prioridad/alta 📅 YYYY-MM-DD
```

Si la fecha es un objetivo grande, crear o actualizar hito en:

```txt
Caos Entre Reinos/Progreso/Hitos/
```

YAML de hito simple:

```yaml
---
type: milestone
project: CER
status: active
title: Nombre del hito
target_date: YYYY-MM-DD
priority: alta
---
```

YAML de hito con rango:

```yaml
---
type: milestone
project: CER
status: active
title: Nombre del hito
start_date: YYYY-MM-DD
end_date: YYYY-MM-DD
target_date: YYYY-MM-DD
priority: alta
---
```

Fechas importantes también deben añadirse a Google Calendar si Codex tiene herramienta/permisos.

Sí deben ir a Calendar:

```txt
beta test
fecha límite de build
entrega de versión
doblaje con Benny
publicación importante
revisión final de cinemática
reunión
lanzamiento
deadline
```

Normalmente no hace falta Calendar para:

```txt
bug pequeño
ordenar una nota
probar un botón
buscar un sonido suelto
```

Si no puede añadirlo a Calendar, Codex debe dejar mensaje para Fak en `Inbox/` con fecha, motivo y acción recomendada.

---

## 9. Hito beta test privado 0.0.5.8

Se detectó como fecha importante:

```txt
Beta test privado 0.0.5.8 -> 2026-06-27 / 2026-06-28
```

Debe existir o actualizarse como hito:

```txt
Caos Entre Reinos/Progreso/Hitos/Beta test privado 0.0.5.8.md
```

YAML recomendado:

```yaml
---
type: milestone
project: CER
status: active
title: Beta test privado 0.0.5.8
start_date: 2026-06-27
end_date: 2026-06-28
target_date: 2026-06-28
priority: alta
---
```

Tareas recomendadas:

```md
- [ ] Preparar build jugable para beta test privado 0.0.5.8 #caos/general #prioridad/alta 📅 2026-06-27
- [ ] Probar tutorial del Abismo completo antes del beta test #caos/tutorial #prioridad/alta 📅 2026-06-27
- [ ] Revisar bugs graves antes de compartir la beta #caos/bugs #prioridad/alta 📅 2026-06-27
- [ ] Preparar versión final para testers #caos/general #prioridad/alta 📅 2026-06-28
- [ ] Revisar feedback inicial o checklist de envío de beta #caos/general #prioridad/alta 📅 2026-06-28
```

---

## 10. Flujo Notas Codex

Nota operativa deseada:

```txt
Notas Codex/Nota rapida para codex.md
```

Se detectó previamente una variante problemática con espacio inicial y acentos:

```txt
Notas Codex/ Nota rápida para Codex.md
```

La versión limpia recomendada es sin espacio inicial y sin acentos:

```txt
Notas Codex/Nota rapida para codex.md
```

Uso:

Fak escribe avances rápidos, cosas terminadas, ideas, bugs o material visual.

Codex debe:

1. leer la entrada rápida;
2. detectar avances, bugs, ideas y material visual;
3. buscar tareas relacionadas en `Caos Entre Reinos/`;
4. marcar completadas solo si está claramente hecho;
5. crear tareas nuevas si algo quedó pendiente;
6. añadir tags correctos;
7. decidir si algo va a Hoy;
8. detectar fechas importantes y añadirlas a Semana/Mes/Calendar si procede;
9. guardar copia limpia en `Notas Codex/Apuntes y archivos/`;
10. resetear la nota.

---

## 11. Flujo Crear tareas

Nota:

```txt
Notas Codex/Crear tareas.md
```

Uso:

Fak escribe tareas sueltas, ideas de tareas, bugs o fechas desordenadas.

Codex debe convertirlas en tareas limpias, bien ubicadas y compatibles con widgets.

Debe decidir:

- área correcta;
- tags;
- prioridad;
- si va a Hoy;
- si va a Semana/Mes;
- si requiere hito;
- si requiere Google Calendar;
- si es backlog;
- si es bug;
- si pertenece a una nota `type: project-area`.

No debe dejar fechas como texto suelto.

---

## 12. Decisiones confirmadas

Decisiones cerradas el 2026-06-18:

```md
- [x] Mantener Hub del Abismo como nombre temporal, no definitivo #caos/general #estado/revisar ✅ 2026-06-18
- [x] Confirmar Orialis como nombre oficial de las cartas y Constelación como nombre oficial de la build #caos/orialis #caos/tutorial #estado/revisar ✅ 2026-06-18
- [x] Posponer el pack UI hasta cerrar la cinemática inicial y el tutorial del Abismo #caos/ui #estado/revisar ✅ 2026-06-18
- [x] Limitar combate y UI de la demo a lo mínimo funcional y mandar mejoras grandes al backlog #caos/gameplay #caos/ui #estado/revisar ✅ 2026-06-18
- [x] Separar Web AikoGx entre contenido del estudio y contenido directo de Caos Entre Reinos #aikogx/content #estado/revisar ✅ 2026-06-18
- [x] Mantener ropa modular y armaduras 3D como backlog futuro #caos/general #estado/revisar ✅ 2026-06-18
- [x] Dejar sistemas futuros de multijugador fuera del alcance real de la demo actual #caos/gameplay #estado/revisar ✅ 2026-06-18
```

Decisiones que deben seguir pendientes salvo confirmación nueva:

```md
- [ ] Resolver diferencias entre las versiones del diálogo final de Akuma y César #caos/tutorial #caos/lore #prioridad/alta #estado/revisar
- [ ] Aprobar terminología ES/EN y nombres mostrados en los diálogos #caos/lore #caos/tutorial #estado/revisar
- [ ] Revisar licencias y vigencia de música, sonidos y assets #caos/audio #estado/revisar
- [ ] Decidir si se mantiene una biblioteca técnica dentro del proyecto #caos/general #estado/revisar
- [ ] Decidir si Aiko_Tareas.json se audita o se conserva únicamente como histórico #caos/general #estado/revisar
```

Regla de cierre:

```txt
Completar una decisión significa que Fak tomó la decisión. No significa que la implementación o migración haya comenzado.
```

---

## 13. Nombres oficiales importantes

- Cartas = Orialis.
- Build / mazo = Constelación.
- Hub = Hub del Abismo como nombre temporal, no definitivo.
- Prioridad narrativa/jugable actual = cinemática inicial + tutorial del Abismo.

---

## 14. Visual, iconos y colores

Fak quiere que la bóveda se vea bonita en Obsidian y en Graph View.

Preferencia:

- usar Lucide Icons si el plugin está disponible;
- si no, usar plugin de iconos seguro o emojis;
- no renombrar carpetas importantes solo para poner emojis si eso rompe rutas;
- aplicar iconos a todas las carpetas de la bóveda, no solo a `Caos Entre Reinos/`;
- usar colores por áreas si el plugin o Graph Groups lo permite.

Estilo visual:

```txt
fantasía indie
azul profundo
morado
magenta
cian
sakura suave
abismo / cristal / magia
limpio y bonito, no sobrecargado
```

Iconos sugeridos:

```txt
Caos Entre Reinos -> sparkles / cherry-blossom / wand / gamepad
00 - Dashboard -> compass
01 - Producción -> wrench / hammer
02 - Lore -> book-open / flower / scroll
03 - Gameplay -> sword / gamepad-2
04 - Tutorial - Abismo -> diamond / route / portal
05 - Aguja del Caos -> swirl / tornado / tower
06 - Orialis - Cartas -> sparkle / cards / star
07 - Enemigos - IA -> eye / skull / bot
08 - Cinemática -> clapperboard / film
09 - Bugs -> bug
10 - Devlogs -> newspaper / megaphone
11 - Material Visual -> image / palette
Progreso -> chart / activity
Hitos -> flag / trophy
Widgets -> panels-top-left / sparkles
Notas Codex -> bot / brain-circuit
Crear tareas -> list-plus / square-check
Inbox -> inbox
Migración pendiente -> archive / folder-clock
AikoGx Studios -> building-2 / sparkle / monitor
Ideas redes -> lightbulb / share-2
Diarios -> calendar-days
Plantillas -> file-text
Canvas -> network / map
.trash -> trash
```

---

## 15. Prompt base actualizado para Crear tareas

La prompt principal de `Crear tareas` debe incluir:

- leer `Notas Codex/Crear tareas.md`;
- convertir frases sueltas en tareas reales;
- añadir tags;
- detectar fechas;
- crear tareas con `📅 YYYY-MM-DD`;
- crear hitos si corresponde;
- añadir fechas importantes a Google Calendar si tiene herramienta/permisos;
- hacer que aparezcan en Semana/Mes;
- no meter todo en Hoy;
- resetear la nota;
- guardar copia limpia en `Notas Codex/Apuntes y archivos/`.

---

## 16. Estado mental del sistema

Para futuras conversaciones, recordar:

```txt
Fak quiere un Command Center bonito, práctico y visual.
No quiere burocracia ni listas enormes.
Quiere abrir Obsidian y saber qué hacer hoy.
Quiere que Codex procese notas desordenadas, cree tareas limpias, detecte fechas, actualice widgets y no rompa nada.
```

La meta no es tener una bóveda perfecta. La meta es ayudar a Fak a avanzar en Caos Entre Reinos sin perder foco.
