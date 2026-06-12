# onboard-program

Pues aquí tienes una skill que guía a un desarrollador/a nuevo/a en la comprensión paso a paso de un programa, servicio o repositorio. Convierte la pregunta "no entiendo este programa" en un recorrido pedagógico con documentación, diagramas, checklist y scripts ejecutables con datos mokeados. 

*En el curro te han dado un programa y tienes que saberlo PARA AYER...*

## Cuándo se activa

Cuando el usuario diga frases como:
- "Quiero entender este programa"
- "Onboarding de este repo"
- "Explícame este código paso a paso"
- "Preséntame este servicio"
- "Ayúdame a comprender qué hace este código"

## Cómo funciona

Cuatro fases, separadas por paradas explícitas para preguntar al usuario:

| Fase | Objetivo | Salida |
|------|----------|--------|
| 1. Visión general | Qué hace, qué no hace, cómo lo hace | `01-vision-general.md` + diagrama Mermaid |
| 2. Mini-flujos | Desglose por funcionalidades, una a una | `02-flujos/NN-<nombre>.md` por flujo elegido |
| 2.2 Drill-down (opcional) | Funciones, ficheros, flujos transversales | `02-flujos/NN-<nombre>-detalle.md` |
| 3. Repaso | Consolidación y patrones | `03-repaso.md` |
| 4. Implementación con mocks | Drivers ejecutables sobre el código real con datos sintéticos | `04-implementacion-mocks/` |

### Numeración estable de mini-flujos

Al identificar los mini-flujos (Fase 2), cada uno recibe un número correlativo (`01`, `02`…) que **no cambia** aunque se exploren en otro orden o se descarten algunos. Ese número aparece en todos los sitios donde el flujo se menciona: lista presentada al usuario, `_progress.md`, nombre de fichero, título del documento, checklist, repaso y artefactos de la Fase 4 (`run-NN-<flujo>.<ext>`, `NN-<flujo>-input.json`, `NN-<flujo>-expected-output.md`).

### Filosofía de la Fase 4: mock mínimo, código real máximo

Los scripts de la Fase 4 **no reimplementan** los flujos: son drivers delgados que importan e invocan el código del propio programa. Solo se mockean las fronteras de E/S (red, base de datos, colas, reloj…), se prefiere la invocación in-process (`TestClient`, `MockMvc`, `supertest`…), se reutilizan los fixtures y helpers de test que el repo ya tenga, y la salida esperada se captura de una ejecución real del script, nunca se escribe de memoria. Las dependencias son las del propio programa; los scripts no declaran un entorno paralelo.

## Estructura de archivos

| Archivo | Función |
|---------|---------|
| `SKILL.md` | Instrucciones para Claude (qué hacer en cada fase) |
| `README.md` | Esta documentación humana |
| `templates/` | Plantillas que rellena Claude al generar artefactos |

Plantillas disponibles: `01-vision-general.md`, `02-flujo.md`, `02-flujo-detalle.md`, `03-repaso.md`, `04-expected-output.md`, `checklist.md`, `_progress.md`.

## Estado entre turnos

La continuidad se mantiene mediante `docs/onboarding/_progress.md` que se escribe en el repo del programa analizado, no aquí. Claude lo lee al inicio de cada turno y lo actualiza al final.

## Instalación

Instalada como skill de usuario en `~\.agents\skills\onboard-program\`. Cuando esté madura, empaquetar como `.skill` si se quiere distribuir.
