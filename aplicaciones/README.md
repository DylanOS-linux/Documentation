# Aplicaciones de DylanOS

Documentación de las aplicaciones nativas y los plasmoides propios de DylanOS Crimson. Cada documento describe la función real, el punto de entrada, las dependencias y los límites conocidos.

## Aplicaciones

| Aplicación | Comando | Función | Estado | Documento |
|---|---|---|---|---|
| DylanOS Workspace | `dylanos` | Bienvenida, archivos, notas, desarrollo, monitor y ajustes (6 páginas). | Activo | [workspace.md](workspace.md) |
| DylanOS Explorer | `dylanos-explorer` | Gestor de archivos basado en KIO; único explorador del sistema. | Activo | [explorer.md](explorer.md) |
| DylanOS Store | `dylanos-store` | Catálogo y gestión de software mediante libdiscover y sus backends. | Activo | [store.md](store.md) |
| DylanOS App Center | `dylanos-app-center` | Exploración y lanzamiento de aplicaciones XDG instaladas. | Activo | [app-center.md](app-center.md) |
| DylanOS Configuration | `dylanos-configuration` | Centro de configuración único con módulos KCM nativos y páginas propias. | Activo | [configuration.md](configuration.md) |
| DylanOS Spotlight | `dylanos-spotlight` | Lanzador y búsqueda rápida de aplicaciones y proyectos. | Activo, con filtros incompletos | [spotlight.md](spotlight.md) |
| DylanOS Calculator | `dylanos-calculator` | Calculadora de escritorio Qt 6/QML. | Activo | [calculator.md](calculator.md) |
| DylanOS Process | `dylanos-process` | Monitor real de procesos y recursos con núcleo Rust y UI QML. | Activo | [process.md](process.md) |
| DylanOS Browser | `dylanos-browser` | Navegador basado en Gecko/Zen, integrado como predeterminado en la ISO 1.1 pre-beta. | Pre-beta | [browser.md](browser.md) |

DylanOS Console (`dylanos-console`, Kitty con configuración Crimson) se documenta en [DylanOS Shell](../arquitectura/dylanos-shell.md).

## Plasmoides del shell

| Plasmoid | ID | Función | Documento |
|---|---|---|---|
| Dock | `com.dylanos.dock` | Dock inferior con zoom progresivo e indicadores de aplicaciones abiertas. | [dock.md](dock.md) |
| Centro de Control | `com.dylanos.controlcenter` | Notificaciones, Wi-Fi, Bluetooth, audio, brillo y MPRIS. | [control-center.md](control-center.md) |
| Aplicación activa | `com.dylanos.activeapp` | Nombre de la ventana activa en la barra superior. | [activeapp.md](activeapp.md) |
| Búsqueda | `com.dylanos.search` | Botón de lupa que abre Spotlight. | [search.md](search.md) |

El sistema de widgets de escritorio (`com.dylanos.widgets.*`) se describe en [DylanOS Widgets](../arquitectura/widgets.md).

## Documentación interna

- [Arquitectura de Explorer](explorer-arquitectura.md)
- [Arquitectura de Store](store-arquitectura.md)
- [Store: mapeo de diseño](store-mapeo-diseno.md)
- [Store: integración](store-integracion.md)
- [Store: backend de paquetes](store-backend-paquetes.md)
- [Store: prototipo](store-prototipo.md)

## Componentes históricos

Los siguientes documentos se conservan como referencia, pero **no describen la implementación que se envía en la ISO**:

- [DylanOS Dashboard](dashboard.md): muro de tarjetas de la primera etapa; staging lo elimina de la imagen y el layout inicial ya no lo añade.
- [Archivos](archivos.md): prototipo antiguo; su lanzador vigente delega en Workspace y la gestión completa corresponde a Explorer.

## Documentación relacionada

- [Guía de uso y estado de las funciones](../guia/guia-de-uso.md)
- [Visión general de la arquitectura](../arquitectura/vision-general.md)
- [DylanOS Shell](../arquitectura/dylanos-shell.md)
- [Roadmap](../desarrollo/roadmap.md)
