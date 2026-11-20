# Guía de DylanOS

Documentación práctica para instalar, usar, compilar y diagnosticar DylanOS Crimson. Estas guías describen el estado real de la rama `development`; cuando una función tenga límites conocidos, se indican de forma explícita.

## Documentos

| Documento | Contenido |
|---|---|
| [Instalación, build y QA](instalacion.md) | Requisitos, arranque live en VM, instalación desde el instalador propio, validación mínima y construcción de la ISO. |
| [Guía de uso y estado de las funciones](guia-de-uso.md) | Escritorio, paneles, aplicaciones, comandos, widgets, perfiles de paquetes y limitaciones visibles. |
| [Hosts de compilación](hosts-de-compilacion.md) | Matriz de sistemas anfitrión, dependencias y uso del builder Docker/Compose. |
| [Optimización del sistema e ISO](optimizacion.md) | Política y verificación de optimización, métricas y criterios para comparar cambios. |
| [DylanOS Gaming](gaming.md) | Conjunto opcional de gaming: catálogo, perfiles, integración y límites. |
| [DylanOS IoT](iot.md) | Perfil `--iot`, catálogo de herramientas y perfiles de usuario para sistemas embebidos. |
| [Arranque y GRUB](solucion-boot-hang-y-grub.md) | Diagnóstico del cuelgue de arranque, initramfs y recuperación desde GRUB. |
| [Tema SDDM](sddm-theme-debugging.md) | Compatibilidad del greeter, composición del tema y depuración del inicio de sesión. |

## Orden de lectura sugerido

1. [Instalación y QA](instalacion.md) para preparar el entorno y probar la ISO.
2. [Guía de uso](guia-de-uso.md) para conocer qué hace cada aplicación y qué límites tiene.
3. [Arquitectura](../arquitectura/README.md) para entender cómo encajan el shell, las apps y el empaquetado.
4. [Contribuir](../desarrollo/contribuir.md) antes de enviar cambios.

> [!IMPORTANT]
> La instalación sobre un disco real es destructiva. Usa una máquina virtual o un disco desechable hasta haber validado el flujo completo. Las animaciones de respaldo del frontend no demuestran que el sistema se haya instalado.

## Documentación relacionada

- [Arquitectura del sistema](../arquitectura/vision-general.md)
- [Aplicaciones de DylanOS](../aplicaciones/README.md)
- [Instalador DylanOS](../instalador/README.md)
- [Auditorías e informes históricos](../auditorias/README.md)
