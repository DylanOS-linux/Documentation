# Recursos de documentación

Material gráfico y utilidades de apoyo usadas por la documentación. No son recursos de instalación del sistema; los recursos oficiales de marca viven en el repositorio DylanOS bajo `branding/` y `themes/`.

## Contenido

| Ruta | Descripción |
|---|---|
| [`assets/crimson-palette.svg`](assets/crimson-palette.svg) | Paleta oficial Crimson en formato SVG. |
| [`previews/`](previews/) | Previews SVG generados para la documentación visual del shell y los componentes. |
| [`previews/generate_previews.py`](previews/generate_previews.py) | Generador reproducible de los previews. |

## Previews

Los archivos `00-indice.svg` a `11-plymouth.svg` son referencias generadas para la etapa 1.0 Beta. Algunos pueden mostrar componentes o flujos que ya cambiaron (por ejemplo, referencias a Calamares, sustituidas por el instalador propio). No se usan como prueba del estado actual.

Para regenerarlos:

```bash
python3 recursos/previews/generate_previews.py
```

El script escribe los SVG en su propio directorio y no modifica el sistema.

## Recursos oficiales

- Paleta y definición técnica: [`branding/README.md`](../branding/README.md)
- Código y recursos de marca: [branding en DylanOS](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/tree/development/branding)
- Licencias y procedencia: [Licencias de recursos](../licencias/assets.md)
