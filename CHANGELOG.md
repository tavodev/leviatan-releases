# Cambios

Los cambios relevantes de cada versión de Leviatán. El formato sigue [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) y las versiones siguen el [versionado semántico](https://semver.org/lang/es/). Ver «Publicar una versión» en [`docs/desarrollo.md`](docs/desarrollo.md).

`./scripts/release.sh` mueve la sección «Sin publicar» a la versión nueva. Si está vacía, la genera a partir de los commits desde la versión anterior, agrupados por su gitmoji.

## [Sin publicar]

## [0.2.2] - 2026-10-09

### Correcciones

- La app deja de congelarse al mostrar la descripción de un issue.

## [0.2.1] - 2026-10-08

### Novedades

- Ajustes › General › Actualizaciones muestra cuándo buscó la app actualizaciones por última vez.

## [0.2.0] - 2026-10-08

### Novedades

- Actualizaciones automáticas con Sparkle: Leviatán busca versiones nuevas una vez al día, comprueba su firma (EdDSA y Developer ID), las instala y se relanza.
- «Buscar actualizaciones…» en el menú de la app.
- Sección «Actualizaciones» en Ajustes › General: búsqueda automática, descarga e instalación automáticas y versión instalada.

### Correcciones

- El panel de contexto deja de anidar una lista perezosa por carpeta dentro de la suya.

## [0.1.0] - 2026-10-07

Primera versión empaquetada: firmada con Developer ID, notarizada y distribuida a mano, sin actualizador. Incluye el grafo de historia, el panel de contexto con diff y blame, ramas, stashes, etiquetas, rebase interactivo, editor de conflictos, varias cuentas de GitHub y GitLab, revisión de pull requests e issues.
