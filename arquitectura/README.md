# Arquitectura de DylanOS

Documentación del diseño vigente de DylanOS Crimson: capas del sistema, shell de Plasma, aplicaciones nativas, identidad visual y empaquetado. La fuente principal es [Visión general](vision-general.md); el resto de documentos profundiza en componentes concretos.

## Documentos

| Documento | Contenido |
|---|---|
| [Visión general](vision-general.md) | Capas del sistema, ciclo de vida de ventanas con KWin, Explorer, Configuration, temas GTK/Qt, paquetes, QA y limitaciones. |
| [DylanOS Shell](dylanos-shell.md) | Paneles, dashboard histórico, Centro de Control, DylanOS Console, neofetch y sugerencias de Bash. |
| [DylanOS Widgets](widgets.md) | Sistema de widgets sobre plasmoides de Plasma 6, regla live/instalado y composición del escritorio. |
| [Crimson Glass](crimson-glass.md) | Perfil visual global: temas Plasma/Aurorae, blur, translucidez, acentos y persistencia. |
| [Paquetes y perfiles](paquetes.md) | Perfiles `build`, `default`, `development`, `iot` y perfil de usuario Gaming. |
| [Diseño técnico de Crimson Glass](diseno/crimson-glass.md) | Razonamiento de diseño, límites de cada toolkit y criterios de implementación. |
| [Diseño de DylanOS Browser](diseno/dylanos-browser.md) | Estrategia del fork Gecko/Zen, mantenibilidad, rendimiento y empaquetado. |

## Principios de la arquitectura

- **Base estable**: Debian 13 (trixie), systemd y KDE Plasma 6 / Qt 6 como plataforma del escritorio.
- **Aplicaciones propias**: las tareas principales del escritorio usan componentes DylanOS con identidad e integración propias, sin depender de aplicaciones genéricas del entorno.
- **Shell declarativo**: el layout inicial se genera desde el look-and-feel `org.dylanos.crimson`; los perfiles de usuario existentes no se sobrescriben.
- **Identidad coordinada**: `branding/` y `themes/` alimentan Plasma, KWin, SDDM, GRUB, Plymouth y GTK; Crimson Glass sincroniza el conjunto sin un proceso residente.
- **Validación real**: las pruebas estáticas y de staging se complementan con Plasma real, arranque live, instalación en VM y pruebas de hardware.

> [!NOTE]
> Este repositorio documenta el estado de la rama `development`. Los informes de [auditorías](../auditorias/README.md) y los planes cerrados son registros históricos y pueden describir decisiones que ya cambiaron.

## Documentación relacionada

- [Guía de uso](../guia/guia-de-uso.md)
- [Aplicaciones](../aplicaciones/README.md)
- [Instalador](../instalador/README.md)
- [Roadmap](../desarrollo/roadmap.md)
