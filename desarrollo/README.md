# Desarrollo de DylanOS

Documentos de proceso, planificación y seguimiento del desarrollo de DylanOS Crimson. Esta sección está pensada para colaboradores y mantenedores; para usar o instalar el sistema, empieza por la [guía](../guia/README.md).

## Documentos principales

| Documento | Contenido |
|---|---|
| [Contribuir](contribuir.md) | Flujo de trabajo, estándares, validación mínima y criterios para pull requests. |
| [Roadmap](roadmap.md) | Objetivos de la iteración Crimson y evolución prevista. |
| [Changelog](changelog.md) | Registro de cambios relevantes por versión y estado de `development`. |
| [Mantenedores](mantenedores.txt) | Personas y responsabilidades del proyecto. |
| [Licencias de recursos](../licencias/assets.md) | Procedencia y licencias de recursos, temas y componentes de terceros. |

## Planificación

- [RFC 0001: migración de apps Python a Rust/C++](rfcs/0001-migracion-rust.md) — propuesta y alcance de la migración.
- [Planes](planes/) — planes de implementación aprobados: beta premium, Crimson Glass, DylanOS Browser por fases y estabilización de la beta.
- [Especificaciones](especificaciones/) — especificaciones de diseño que originaron los planes.
- [Benchmarks](benchmarks/) — métodos reproducibles y líneas base de rendimiento.

Los planes y especificaciones se conservan como registro del proceso. Cuando un plan termina, sus resultados deben reflejarse en las guías activas, la arquitectura y el changelog; el plan no se convierte en documentación de uso.

## Ciclo de un cambio

1. **Propuesta**: issue o RFC cuando el cambio afecta a arquitectura, empaquetado o compatibilidad.
2. **Diseño**: especificación breve y plan de tareas con criterios de aceptación.
3. **Implementación**: cambio enfocado en una rama propia.
4. **Validación**: `scripts/check.sh` y las pruebas específicas del componente; arranque e instalación cuando corresponda.
5. **Documentación**: actualizar guía de uso, README del componente, arquitectura e índices en el mismo cambio.
6. **Registro**: entrada en el changelog y cierre del plan.

## Enlaces

- [Repositorio DylanOS](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS)
- [Issues](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/issues)
- [Pull requests](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/pulls)
- [Documentación de arquitectura](../arquitectura/README.md)
