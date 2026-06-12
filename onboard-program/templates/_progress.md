---
fase_actual: 1
estado_fase: en_curso  # en_curso | completada
# Cada mini-flujo se registra con su número estable, p. ej. "01-nombre-del-flujo".
# El número se asigna al identificarlos y NO cambia aunque se exploren en otro orden.
mini_flujos_identificados: []
mini_flujos_completados: []
mini_flujos_pendientes: []
mini_flujos_profundizados: []  # los que pasaron por Fase 2.2
ultimo_paso: "Inicio del onboarding"
fecha_creacion: AAAA-MM-DD
fecha_actualizacion: AAAA-MM-DD
ruta_repo: ""
stack_detectado: ""
nivel_tecnologias:
  # Tecnologías que el usuario eligió que le explicaran de paso.
  # Si la lista está vacía, asumimos que domina todo el stack.
  - tecnologia: ""
    explicada_en: "01-vision-general.md"  # dónde se documentó
---

# Estado del onboarding

> Este archivo es el **estado persistente** del proceso. Claude lo lee al inicio de cada turno y lo actualiza al final. No lo edites a mano salvo que quieras forzar un punto del recorrido.

## Histórico

- _AAAA-MM-DD_ — Onboarding iniciado.

## Notas del usuario

_(Sección libre — el usuario puede dejar aquí anotaciones que Claude tendrá en cuenta en el próximo turno)._
