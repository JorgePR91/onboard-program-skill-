# Mini-flujo {{NUMERO_FLUJO}} — {{NOMBRE_FLUJO}}

> Documento generado en Fase 2. Describe un único caso de uso o flujo coherente del programa.

## Qué problema resuelve

{{DESCRIPCION_PROBLEMA}}

<!--
OPCIONAL — Sección "Cuándo ocurre".
Inclúyela si el contexto del despliegue NO es obvio (ej. el flujo solo se dispara
en ciertos escenarios, requiere ciertos tipos de dispositivo, o tiene un disparador
no trivial). Omítela si el flujo siempre se ejecuta de la misma forma uniforme.
-->

## Cuándo ocurre

{{CONTEXTO_DEPLOYMENT}}

_Escenarios típicos en los que este flujo se activa:_

- {{ESCENARIO_1}}
- {{ESCENARIO_2}}

## Disparador

{{COMO_SE_INICIA_EL_FLUJO}}  
_(ej: petición POST a `/api/users`, comando CLI `migrate --apply`, mensaje en la cola `orders.created`, etc.)_

<!--
OPCIONAL — Sección "Por qué este camino".
Inclúyela si hay decisiones de diseño NO triviales en el flujo (workers async,
retries, dedup, DLQs, políticas de backpressure, caches, etc.). Omítela si el
flujo es directo (request → handler → response sin matices).
-->

## Por qué este camino

{{INTRO_RAZONAMIENTO}}

1. **{{DECISION_1}}** — {{JUSTIFICACION_1}}
2. **{{DECISION_2}}** — {{JUSTIFICACION_2}}
3. **{{DECISION_3}}** — {{JUSTIFICACION_3}}

<!--
OPCIONAL — Sección "Conceptos clave que aparecen en este flujo".
Inclúyela si el flujo introduce ≥3 términos técnicos NO explicados aún en otros
docs del onboarding (consulta `mini_flujos_completados` en _progress.md para
saber qué se ha cubierto). La columna "Analogía cercana" NO es opcional dentro
de la tabla: cada definición técnica va acompañada de una comparación con algo
cotidiano que el lector probablemente conoce (una boda, una biblioteca, un
ascensor…). Sin analogía, la definición es solo otra forma de jerga.
-->

## Conceptos clave que aparecen en este flujo

> Si vienes de otro mini-flujo, esta tabla te ahorra tropezar con jerga sin definir antes del diagrama.

| Concepto | Qué es | Analogía cercana | Rol en este flujo |
|----------|--------|------------------|-------------------|
| **{{CONCEPTO_1}}** | {{DEFINICION_BREVE}} | {{ALGO_COTIDIANO_QUE_LO_ILUSTRA}} | {{ROL_AQUI}} |
| **{{CONCEPTO_2}}** | {{DEFINICION_BREVE}} | {{ALGO_COTIDIANO_QUE_LO_ILUSTRA}} | {{ROL_AQUI}} |

<!--
OPCIONAL — Sección "Ejemplo concreto".
Inclúyela si el flujo es abstracto o tiene varios pasos que cuesta visualizar
en frío. Cuenta UNA historia concreta — un valor real, un dispositivo concreto,
un caso de uso — que recorra el flujo de principio a fin con números reales,
anclando los conceptos abstractos a algo tangible. Omítela si los pasos del
flujo ya son suficientemente concretos por sí mismos.
-->

## Ejemplo concreto (para anclar los conceptos)

{{NARRATIVA_PASO_A_PASO_CON_VALORES_REALES}}

## Diagrama de secuencia

```mermaid
sequenceDiagram
    {{DIAGRAMA_SECUENCIA}}
```

## Pasos del flujo

| # | Acción | Dónde ocurre | Notas |
|---|--------|--------------|-------|
| 1 | {{ACCION}} | `{{FILE:LINE}}` | {{NOTA}} |
| 2 | {{ACCION}} | `{{FILE:LINE}}` | {{NOTA}} |

## Datos mokeados de entrada

```{{LENGUAJE_FORMATO}}
{{DATOS_MOCK_ENTRADA}}
```

## Salida esperada

```{{LENGUAJE_FORMATO}}
{{SALIDA_ESPERADA}}
```

## Cómo ejecutarlo manualmente

{{INSTRUCCIONES_EJECUCION}}

## Variantes interesantes

_Casos límite, errores típicos, configuraciones alternativas que merece la pena probar más tarde._

- {{VARIANTE_1}}
- {{VARIANTE_2}}

## Próximo paso sugerido

- ¿Pasar al siguiente mini-flujo?
- ¿Profundizar a nivel de función/fichero? → genera `<nombre>-detalle.md` (Fase 2.2)
- ¿Saltar al repaso (Fase 3)?
