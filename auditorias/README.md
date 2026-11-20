# Auditorías e informes

Registros fechados de auditoría, correcciones, optimizaciones y bitácoras de DylanOS. Son **material histórico**: documentan el estado y las decisiones de un momento concreto y no sustituyen las guías activas de [uso](../guia/guia-de-uso.md) ni la [arquitectura](../arquitectura/vision-general.md).

| Fecha | Documento | Tema |
|---|---|---|
| 2026-10-09 | [Auditoría de diseño Tahoe/Crimson](auditoria-diseno-tahoe-crimson.md) | Evaluación del shell, fidelidad de marca y eliminación de elementos ficticios. |
| 2026-10-09 | [Bitácora de entrega Crimson 1.0](bitacora-entrega-crimson-1.0.md) | Diagnóstico, estabilización de branding y estado de la entrega. |
| 2026-10-11 | [Auditoría de escritorio](auditoria-escritorio-2026-10-11.md) | Renovación visual, temas, layout, apps y splash. |
| 2026-10-11 | [Auditoría de cuelgue de arranque](auditoria-boot-hang-initramfs.md) | Causa raíz del fallo de initramfs y correcciones de arranque. |
| 2026-10 | [DylanOS Shell: SDDM, escritorio y Centro de Control](dylanos-shell-2026-10.md) | Implementación del shell a partir de las referencias visuales. |
| 2026-10-13 | [Correcciones live, X11, instalador y App Center](correcciones-live-x11-instalador-appcenter-2026-10-13.md) | Ajustes de la sesión live y componentes afectados. |
| 2026-10-21 | [Cambios de CI, staging y dock](cambios-ci-dock-2026-10-21.md) | Registro por archivo de cambios de integración. |
| 2026-10-24 | [Optimización de apps Qt e instalador](optimizacion-apps-qt-instalador-2026-10-24.md) | Cambios de rendimiento y consistencia visual. |
| 2026-11-16 | [Auditoría y arquitectura de Widgets](widgets-auditoria.md) | Decisiones de diseño, visibilidad live/instalado y plan de widgets. |

## Cómo interpretar estos documentos

- Las afirmaciones sobre funciones, límites y comandos pueden haber cambiado; prevalece la [guía de uso](../guia/guia-de-uso.md).
- Los identificadores de commit y las rutas mencionadas corresponden al árbol de DylanOS en la fecha indicada.
- No se reescriben los informes históricos para adaptarlos al estado actual; si una conclusión deja de ser válida, se corrige o retira la guía activa correspondiente.
- Para diagnóstico vigente de arranque y GRUB, usa [Arranque y GRUB](../guia/solucion-boot-hang-y-grub.md).

## Documentación relacionada

- [Guía de uso](../guia/guia-de-uso.md)
- [Arquitectura](../arquitectura/README.md)
- [Changelog](../desarrollo/changelog.md)
- [Planes de desarrollo](../desarrollo/README.md)
