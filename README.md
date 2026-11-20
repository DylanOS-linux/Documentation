<div align="center">

# Documentación de DylanOS

**Guías, arquitectura, manuales, especificaciones y recursos informativos del ecosistema DylanOS.**

[![Base](https://img.shields.io/badge/base-Debian%2013-A81D33?style=flat-square&logo=debian&logoColor=white)](https://www.debian.org/)
[![Escritorio](https://img.shields.io/badge/escritorio-KDE%20Plasma%206-1D99F3?style=flat-square&logo=kde&logoColor=white)](https://kde.org/plasma-desktop/)
[![Qt](https://img.shields.io/badge/Qt-6.8-41CD52?style=flat-square&logo=qt&logoColor=white)](https://www.qt.io/)
[![Estado](https://img.shields.io/badge/estado-1.1%20pre--beta-DC143C?style=flat-square)](#estado-del-proyecto)
[![Licencia](https://img.shields.io/badge/licencia-GPL--3.0--or--later-blue?style=flat-square)](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/blob/development/LICENSE)

</div>

<img src="https://raw.githubusercontent.com/dylanneymarmontalvo2014-lgtm/DylanOS/development/previews/DylanOS%20shell/escritorio_preview.png" alt="Vista de referencia del escritorio DylanOS Crimson" width="100%">

> [!NOTE]
> Las imágenes de `previews/` son referencias visuales del objetivo del proyecto. Pueden incluir diseños en progreso y no demuestran por sí solas que una función esté implementada en la ISO.

## Sobre este repositorio

Este es el repositorio oficial de documentación de DylanOS. Reúne en un solo lugar la documentación técnica que antes vivía dispersa en el repositorio de código, organizada por tema y con enlaces normalizados.

La documentación describe **DylanOS Crimson 1.1 pre-beta**, en la rama `development`. Se sincronizó desde el repositorio [DylanOS](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS) en el commit [`05abdf0`](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/commit/05abdf03ae3c5e15ad259c4fdb54f4a86b171936) (2026-11-19). Los documentos originales siguen manteniéndose en `docs/` del repositorio de código.

## Estado del proyecto

| Campo | Valor |
|---|---|
| Proyecto | DylanOS Crimson |
| Versión documentada | `1.1.0-pre-beta` (desarrollo) |
| Última versión registrada | `1.0.0-crimson` — 2026-10-18 |
| Base | Debian 13 «trixie» |
| Escritorio | KDE Plasma 6, KWin, Qt 6.8 / QML |
| Identidad visual | Crimson Glass |
| Arquitectura | amd64 |
| Rama de referencia | `development` |

La ISO de trabajo (`DylanOS-1.1.0-pre-beta-amd64.iso`) es un artefacto local de construcción y no forma parte de este repositorio. Antes de presentar el sistema como terminado, revisa las limitaciones documentadas en la [guía de uso](guia/guia-de-uso.md) y la [guía del instalador](instalador/README.md).

## Empezar aquí

| Si quieres… | Empieza por |
|---|---|
| Instalar, arrancar o probar DylanOS | [Instalación, build y QA](guia/instalacion.md) |
| Saber qué hace cada aplicación y qué límites tiene | [Guía de uso y estado de las funciones](guia/guia-de-uso.md) |
| Entender la arquitectura del sistema | [Visión general](arquitectura/vision-general.md) |
| Conocer el escritorio, el shell y los widgets | [Arquitectura](arquitectura/README.md) |
| Revisar una aplicación concreta | [Aplicaciones](aplicaciones/README.md) |
| Entender el instalador propio | [Instalador DylanOS](instalador/README.md) |
| Contribuir al proyecto | [Contribuir](desarrollo/contribuir.md) |
| Ver la hoja de ruta | [Roadmap](desarrollo/roadmap.md) |
| Consultar cambios recientes | [Changelog](desarrollo/changelog.md) |
| Revisar informes y decisiones pasadas | [Auditorías](auditorias/README.md) |

## Navegación

| Sección | Contenido |
|---|---|
| [`guia/`](guia/README.md) | Instalación, uso, compilación, optimización, Gaming, IoT y diagnóstico de arranque/SDDM. |
| [`arquitectura/`](arquitectura/README.md) | Capas del sistema, shell, widgets, Crimson Glass, paquetes y diseños técnicos. |
| [`aplicaciones/`](aplicaciones/README.md) | Workspace, Explorer, Store, Spotlight, App Center, Configuration, Process, Browser y plasmoides. |
| [`instalador/`](instalador/README.md) | Arquitectura, API, particionado, límites y QA del instalador. |
| [`desarrollo/`](desarrollo/README.md) | Contribución, roadmap, changelog, mantenedores, RFC, planes, especificaciones y benchmarks. |
| [`auditorias/`](auditorias/README.md) | Auditorías, correcciones y bitácoras fechadas, conservadas como registro histórico. |
| [`branding/`](branding/README.md) | Paleta oficial, logo, fondos, iconografía y concepto visual Crimson. |
| [`licencias/`](licencias/assets.md) | Procedencia y licencias de recursos y componentes de terceros. |
| [`recursos/`](recursos/README.md) | Paleta SVG, previews generados y utilidades de documentación. |

## El ecosistema en una vista

DylanOS combina una base Debian estable con KDE Plasma y una capa propia de aplicaciones, shell e identidad visual:

- **Base**: Debian 13, systemd, KDE Plasma 6, KWin y Qt 6.8.
- **Shell**: paneles Plasma generados por el look-and-feel `org.dylanos.crimson`, barra superior con aplicación activa, búsqueda, Centro de Control y dock propio con zoom progresivo.
- **Aplicaciones**: Workspace, Explorer (KIO), Store (libdiscover), Configuration, App Center, Spotlight, Calculator, Process, Console y Browser.
- **Widgets**: sistema sobre plasmoides nativos, con escritorio limpio en live y tres widgets iniciales en el primer inicio de un sistema instalado.
- **Identidad**: Crimson Glass coordina Plasma, Aurorae, Qt, GTK, SDDM, GRUB y Plymouth sin un proceso residente.
- **Instalador**: aplicación Qt WebEngine con backend HTTP local, particionado real y validación destructiva en VM.
- **Browser**: fork mantenible de Gecko/Zen, integrado como navegador predeterminado en la ISO 1.1 pre-beta.

Para el detalle de cada pieza, consulta la [arquitectura](arquitectura/README.md) y la [guía de uso](guia/guia-de-uso.md).

## Estructura del repositorio

```text
Documentation/
├── README.md                  # Este documento
├── guia/                      # Guías operativas y de uso
├── arquitectura/              # Diseño vigente del sistema
│   └── diseno/                # Especificaciones técnicas de diseño
├── aplicaciones/              # Documentación por aplicación y plasmoid
├── instalador/                # Instalador, API y diseño
├── desarrollo/                # Contribución, roadmap, RFC, planes y benchmarks
│   ├── rfcs/
│   ├── planes/
│   ├── especificaciones/
│   └── benchmarks/
├── auditorias/                # Informes y bitácoras fechadas
├── branding/                  # Identidad y paleta Crimson
├── licencias/                 # Procedencia y licencias
└── recursos/                  # Assets y previews de documentación
```

## Convenciones de la documentación

- **Guías activas**: `guia/`, `arquitectura/`, `aplicaciones/` e `instalador/`. Describen el comportamiento esperado del código actual.
- **Material histórico**: `auditorias/`, planes cerrados y bitácoras. Se conservan sin reescribir y pueden contener rutas, commits o conclusiones de otra etapa.
- **Estado honesto**: cuando una función es parcial, simulada o depende de servicios externos, se documenta como tal. Las capturas y previews no sustituyen las pruebas.
- **Enlaces**: los enlaces entre documentos son relativos; los enlaces a código, temas y scripts apuntan al repositorio DylanOS en la rama `development`.
- **Actualización**: si un cambio modifica comandos, controles, perfiles o límites, actualiza la guía de uso, el README del componente y el índice correspondiente en el mismo cambio.

## Mantenimiento y sincronización

Este repositorio es la vista organizada de la documentación de DylanOS. Para actualizarlo tras un cambio en el repositorio de código:

1. Identifica los documentos afectados en `docs/` y en los `README` de cada aplicación.
2. Copia el contenido actualizado a la sección correspondiente de este repositorio.
3. Revisa los enlaces relativos y actualiza las rutas si cambió la estructura.
4. Actualiza los índices de sección y, si cambió el alcance del proyecto, este README.
5. Anota la fecha y el commit de sincronización en este documento.

No se deben introducir afirmaciones nuevas que no estén respaldadas por el código o por una prueba verificable.

## Enlaces

- [Repositorio de código DylanOS](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS)
- [Issues](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/issues)
- [Pull requests](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/pulls)
- [Releases](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/releases)
- [Documentación en el repositorio de código](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/tree/development/docs)
- [Repositorio de documentación](https://github.com/DylanOS-linux/Documentation)

## Contribuir

Las correcciones, aclaraciones y mejoras de documentación son bienvenidas. Abre un issue o un pull request describiendo el problema, la sección afectada y la fuente que respalda el cambio. Para cambios de código o de producto, sigue la [guía de contribución](desarrollo/contribuir.md).

## Licencia

La documentación se distribuye bajo la [GNU General Public License v3.0 o posterior](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/blob/development/LICENSE), la misma licencia del proyecto DylanOS, salvo que un documento indique otra cosa.

Los recursos de terceros conservan sus licencias originales. DylanOS Browser mantiene la Mozilla Public License 2.0 (`MPL-2.0`) y sus avisos de autoría. Consulta [Licencias de recursos](licencias/assets.md) para la procedencia detallada.
