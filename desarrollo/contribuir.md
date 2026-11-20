# Contribuir a DylanOS

Gracias por dedicar tiempo a mejorar DylanOS. El proyecto sigue un modelo de contribución centrado en cambios pequeños, revisión de arquitectura y validación real del comportamiento del sistema.

## Antes de empezar

Lee la documentación vigente antes de abrir un cambio:

- [Documentación de DylanOS](../README.md)
- [Visión general de la arquitectura](../arquitectura/vision-general.md)
- [Guía de uso y estado de las funciones](../guia/guia-de-uso.md)
- [Instalación, build y QA](../guia/instalacion.md)

Trabaja siempre contra el estado actual del código y la arquitectura, no contra informes históricos. Los documentos de [`auditorias/`](../auditorias/README.md), los planes cerrados y las bitácoras fechadas son contexto; no sustituyen las guías activas.

## Flujo recomendado

1. Haz un fork del repositorio [DylanOS](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS).
2. Crea una rama exclusiva para el cambio.
3. Mantén el alcance del PR pequeño, enfocado y documentado.
4. Ejecuta la validación mínima del repositorio.
5. Abre el Pull Request con resumen, contexto y pruebas.

```bash
git checkout -b feature/mi-cambio
```

## Estándares del proyecto

- Mantén la estructura del repositorio y los nombres actuales de los componentes.
- Prioriza cambios pequeños y bien documentados; evita refactorizaciones amplias sin necesidad.
- No subas artefactos de build ni contenido temporal de `work/` salvo que el proceso lo requiera explícitamente.
- Si tocas branding o diseño, revisa la paleta Crimson y el estado visual del proyecto.
- Evita referencias obsoletas a Calamares, Dolphin como producto final o Discover si el proyecto ya usa sus propias soluciones (instalador DylanOS, Explorer, Store).
- Si modificas comandos, controles, perfiles o límites conocidos, actualiza la guía de uso, el README del componente y el índice de documentación en el mismo cambio.
- Los enlaces internos deben ser relativos y resolver dentro del repositorio; los enlaces a código deben apuntar al repositorio DylanOS.

## Validación mínima

Desde la raíz del repositorio DylanOS:

```bash
python3 -m venv .venv
. .venv/bin/activate
python -m pip install -r apps/workspace/requirements-dev.txt
DYLANOS_PYTHON="$PWD/.venv/bin/python" bash scripts/check.sh
```

Si el cambio afecta a staging, instalación o scripts del sistema, valida también `scripts/build.sh` y `scripts/stage.py`. Las pruebas estáticas, de staging y de CI no sustituyen el arranque completo, la instalación en disco ni la validación en hardware real.

## Pull requests

Incluye en la descripción:

- problema o mejora, con contexto técnico;
- archivos tocados;
- pruebas ejecutadas y su resultado;
- impacto esperado en escritorio, branding, instalador o sistema;
- limitaciones conocidas o validaciones pendientes.

## Documentación

La documentación de este repositorio se organiza por tema:

- [`guia/`](../guia/README.md): uso, instalación, compilación y resolución de problemas.
- [`arquitectura/`](../arquitectura/README.md): diseño vigente del sistema y sus componentes.
- [`aplicaciones/`](../aplicaciones/README.md): documentación por aplicación y plasmoid.
- [`instalador/`](../instalador/README.md): arquitectura, API y límites del instalador.
- [`desarrollo/`](README.md): roadmap, RFC, planes, benchmarks y changelog.
- [`auditorias/`](../auditorias/README.md): informes fechados conservados como histórico.

Cuando una guía activa deje de ser exacta, corrígela o retírala del índice; no la dejes conviviendo con una afirmación contradictoria. Los informes históricos no se reescriben: se marcan como tales.

## Código de conducta

Se espera un entorno respetuoso, técnico y colaborativo. El foco es mejorar DylanOS sin generar ruido ni cambios no relacionados.
