# Checklist de comprensión — {{NOMBRE_PROGRAMA}}

> Marca cada paso a medida que lo entiendas. No tienes que terminarlo todo de una sentada; vuelve cuando puedas.

## Fase 1 — Visión general

- [ ] He leído `01-vision-general.md`
- [ ] Entiendo qué **hace** el programa
- [ ] Entiendo qué **NO hace** (alcance/no-alcance)
- [ ] Reconozco el stack tecnológico
- [ ] Identifico los entry points principales
- [ ] El diagrama de flujo general me cuadra

## Fase 2 — Mini-flujos

_(Se irá rellenando con un `- [ ]` por cada mini-flujo elegido, anteponiendo su número: `- [ ] Mini-flujo 01 '<nombre>' comprendido`)_

<!-- placeholder:mini_flujos -->

## Fase 2.2 — Drill-down (opcional)

_(Se irá rellenando solo para los mini-flujos que se profundicen)_

<!-- placeholder:drill_down -->

## Fase 3 — Repaso

- [ ] He leído `03-repaso.md`
- [ ] Entiendo las dependencias entre mini-flujos
- [ ] Reconozco los patrones repetidos del programa
- [ ] Tengo localizados los riesgos comunes

## Fase 4 — Implementación con mocks

- [ ] He ejecutado al menos un script de `04-implementacion-mocks/`
- [ ] La salida del script coincide con `NN-<flujo>-expected-output.md`
- [ ] Distingo en cada script qué es código real del programa y qué es mock de frontera
- [ ] Sé cómo modificar el dataset mokeado para probar variantes
- [ ] Podría reproducir cualquier mini-flujo cubierto con datos propios
