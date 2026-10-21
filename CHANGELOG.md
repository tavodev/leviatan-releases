# Cambios

Los cambios relevantes de cada versión de Leviatán. El formato sigue [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) y las versiones siguen el [versionado semántico](https://semver.org/lang/es/). Ver «Publicar una versión» en [`docs/desarrollo.md`](docs/desarrollo.md).

`./scripts/release.sh` mueve la sección «Sin publicar» a la versión nueva. Si está vacía, la genera a partir de los commits desde la versión anterior, agrupados por su gitmoji.

## [Sin publicar]

## [0.5.0] - 2026-10-21

### Novedades

- La pestaña CI de las pull requests de GitHub permite seguir las ejecuciones de GitHub Actions, consultar sus trabajos y pasos, y leer sus logs dentro de Leviatán. Los estados se actualizan automáticamente y los logs aparecen cuando GitHub los publica.

### Mejoras

- La pantalla sin repositorios abiertos muestra accesos a los grupos y a los repositorios recientes, con sus colores y pertenencia a grupos. También permite volver a abrir el grupo activo tras cerrar su última pestaña.
- El desplazamiento es más fluido en listas grandes de archivos de la copia de trabajo, commits, stashes y pull requests.

### Correcciones

- La clonación por SSH usa el alias configurado para la cuenta elegida. Se puede guardar un alias por cuenta desde Ajustes o al clonar; el remoto del repositorio conserva ese alias para las operaciones posteriores.
- Se corrigen bloqueos al mostrar el detalle de un commit y al cerrar el registro de actividad.

## [0.4.0] - 2026-10-14

### Novedades

- Los grupos de repositorios funcionan como espacios de trabajo: cada grupo recuerda sus pestañas y la pestaña activa. Se puede cambiar de grupo desde la barra de pestañas o con ⌥⌘0…⌥⌘9, y crear uno a partir de las pestañas abiertas.
- Se puede asignar un color a cada grupo y a la pestaña de cada repositorio.

### Mejoras

- El espacio de issues facilita la búsqueda y la lectura con tarjetas rediseñadas, mejor contraste y menos elementos decorativos.
- La barra de pestañas deja más espacio al mostrar Repositorios como icono y la cuenta en la tarjeta lateral.

### Correcciones

- Se puede volver al historial desde una vista de issues vacía.
- Se evita un bucle de cálculo de alturas en el panel de carpetas.

## [0.3.0] - 2026-10-09

### Novedades

- Al abrir una carpeta que no es un repositorio Git, Leviatán propone inicializar uno en ella.

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
