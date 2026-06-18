# Flujo de Notas Codex, redes y calendario

## 1. Objetivo

Fak quiere escribir una entrada rapida y desordenada en un unico lugar. Codex debe procesarla, organizarla y dejar la nota lista para reutilizarse.

## 2. Estructura

```txt
Notas Codex/
  Nota rapida para codex.md
  Apuntes y archivos/
```

La nota fija es:

```txt
Notas Codex/Nota rapida para codex.md
```

La carpeta de salida organizada es:

```txt
Notas Codex/Apuntes y archivos/
```

## 3. Que hace Fak

Fak escribe una entrada rapida en la seccion indicada.

Ejemplo:

```txt
Hoy termine el nivel tutorial, anadi 4 sistemas nuevos y subi fotos a la carpeta de material visual.
Tambien creo que algunas tareas antiguas del tutorial ya se pueden marcar como hechas.
Con las fotos quiza se puede preparar un devlog, una entrada web o ideas para videos cortos.
```

No hace falta que este ordenado.

## 4. Que debe hacer Codex

Cuando procese `Nota rapida para codex.md`:

1. Leer la entrada rapida completa.
2. Detectar avances, tareas hechas, material subido, bugs, dudas e ideas.
3. Buscar tareas similares en `Caos Entre Reinos/`.
4. Si una tarea pendiente esta claramente hecha, marcarla como completada con `✅ YYYY-MM-DD`.
5. Si algo esta parcialmente hecho, crear una tarea nueva mas concreta.
6. Anadir tags correctos para los widgets.
7. Si hay material visual, crear ideas de contenido.
8. Si hay fechas importantes, anotarlas en Google Calendar si hay herramienta/permisos.
9. Crear una copia limpia y organizada en:

```txt
Notas Codex/Apuntes y archivos/YYYY-MM-DD - Titulo limpio.md
```

10. Resetear la nota rapida para que Fak pueda volver a escribir.

## 5. Formato de copia limpia

```md
---
type: codex-processed-note
project: CER
source: "Notas Codex/Nota rapida para codex.md"
date: 2026-06-17
title: Avance tutorial y material visual
areas:
  - Tutorial
  - Cinematica
  - Contenido
---

# Avance tutorial y material visual

## Resumen limpio
...

## Avances detectados
- ...

## Tareas marcadas como completadas
- ...

## Tareas nuevas creadas
- ...

## Material visual detectado
- ...

## Ideas para contenido
- ...

## Fechas importantes
- ...

## Dudas para Fak / Aiko
- ...
```

## 6. Ideas para redes y contenido

Codex debe decidir que formato encaja mejor segun el material.

### YouTube Shorts / TikTok

Usar cuando haya:

- clips cortos;
- gameplay visual;
- antes/despues;
- bugs graciosos;
- mejoras visuales rapidas;
- momentos de combate.

Crear:

- gancho inicial;
- texto corto;
- descripcion;
- hashtags;
- material recomendado;
- estado: idea / listo / pendiente de edicion.

### Discord

Usar cuando haya:

- captura bonita;
- aviso de progreso;
- encuesta;
- evento de comunidad;
- idea para recibir feedback.

Crear mensaje breve, cercano y claro.

### Devlog web

Usar cuando haya:

- avance grande;
- explicacion tecnica;
- varias capturas;
- cambio importante de sistema;
- avance de cinematica, tutorial o Aguja.

Crear:

- titulo;
- resumen;
- cuerpo en secciones;
- lista de imagenes recomendadas;
- CTA final.

### GitHub / companero

Si hay contenido que el companero debe revisar o subir, crear una nota o issue de trabajo con:

- titulo;
- objetivo;
- assets disponibles;
- plataforma recomendada;
- texto base;
- estado.

## 7. Google Calendar

Cuando Codex detecte una fecha importante:

- fecha objetivo de demo;
- entrega de doblaje;
- revision de build;
- publicacion prevista;
- reunion;
- evento de comunidad;

debe crear el evento en Google Calendar si puede.

Si no tiene acceso a Google Calendar, debe dejar un mensaje `codex-message` con el evento sugerido.

Formato sugerido de evento:

```txt
Titulo: CER - Revisar build del tutorial
Fecha: 2026-06-20
Descripcion: Fecha detectada durante procesamiento de Notas Codex. Revisar avance y tareas relacionadas.
```

## 8. Regla de seguridad

No inventar avances, fechas, publicaciones ni estados. Si algo no esta claro, dejarlo como duda para Fak o Aiko.
