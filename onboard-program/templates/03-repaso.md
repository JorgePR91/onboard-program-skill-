# Repaso — {{NOMBRE_PROGRAMA}}

> Documento generado en Fase 3. Consolida lo aprendido antes de pasar a la ejecución con datos mokeados.

## Mini-flujos cubiertos

> La columna `#` es el número estable del mini-flujo, el mismo que en `_progress.md`, el checklist y el nombre de fichero.

| # | Flujo | Drill-down | Documento |
|---|-------|------------|-----------|
| 01 | {{NOMBRE}} | {{SÍ/NO}} | `02-flujos/01-{{ARCHIVO}}.md` |

## Dependencias entre flujos

```mermaid
graph LR
    {{DIAGRAMA_DEPENDENCIAS}}
```

## Patrones repetidos

> Estos son los "ladrillos" que aparecen una y otra vez. Reconocerlos acelera la lectura de cualquier flujo futuro.

### {{PATRON_1}}
{{DESCRIPCION}}  
Aparece en: `{{FILE:LINE}}`, `{{FILE:LINE}}`

### {{PATRON_2}}
{{DESCRIPCION}}  
Aparece en: `{{FILE:LINE}}`, `{{FILE:LINE}}`

## Riesgos y puntos de atención

| Riesgo | Dónde | Por qué importa |
|--------|-------|-----------------|
| {{RIESGO}} | `{{FILE:LINE}}` | {{IMPACTO}} |

## Mapa mental rápido

> Si tuvieras que explicar el programa a otro dev en 60 segundos, di esto:

{{RESUMEN_60_SEGUNDOS}}

## Próximo paso

Fase 4 — Implementación con datos mokeados. Tendrás scripts ejecutables para cada mini-flujo cubierto.
