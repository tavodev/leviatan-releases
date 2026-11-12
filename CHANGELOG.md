# Cambios

Los cambios relevantes de cada versión de Leviatán. El formato sigue [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) y las versiones siguen el [versionado semántico](https://semver.org/lang/es/). Ver «Publicar una versión» en [`docs/desarrollo.md`](docs/desarrollo.md).

`./scripts/release.sh` mueve la sección «Sin publicar» a la versión nueva. Si está vacía, la genera a partir de los commits desde la versión anterior, agrupados por su gitmoji.

## [Sin publicar]

## [0.9.2] - 2026-11-11

### Interfaz

- El historial, el panel de referencias, la barra de herramientas y el detalle del commit mejoran su jerarquía y aprovechan mejor el espacio. La rama activa resulta más visible.
- Los archivos muestran iconos de sus lenguajes y se incorporan iconos para repositorios y navegación.
- Las ayudas de los controles son más legibles, se animan con Leviatán y evitan solaparse con la ayuda del botón de commit.
- Ajustes y las hojas comparten la jerarquía visual de la ventana principal: secciones separadas por líneas, cabeceras compactas y botones con tamaños y estilos comunes.
- Las hojas de gestión, creación y recuperación separan el contenido de su barra de acciones. Los formularios largos permiten desplazarse sin perder los botones y conservan las etiquetas de sus campos.
- Merge, creación de PR/MR, clonación y sincronización usan el mismo marco. Ajustes mantiene visibles sus seis pestañas al ancho mínimo.

### Correcciones

- La ventana principal conserva su tamaño y posición.
- El repositorio muestra el historial cuando no hay cambios pendientes.
- La detección de cambios remotos también funciona en segundo plano.

## [0.9.1] - 2026-11-09

### Interfaz

- Historial, Cambios e Issues comparten una tipografía, colores y controles más uniformes, con menos tarjetas y separaciones más claras.
- La ventana gana espacio para el contenido: el selector de espacio y la rama actual pasan a la barra de herramientas, junto al estado compacto del repositorio. Los filtros del grafo se integran en la cabecera de columnas.
- En Cambios, la barra lateral reúne los archivos y el compositor de commits, y el diff aprovecha el centro de la ventana. Si se oculta la barra lateral, los archivos vuelven al panel de detalle.
- El botón de commit explica qué falta al pulsarlo; las acciones sobre líneas del diff aparecen cuando hay una selección. Aprobar destaca como acción principal cuando la cuenta puede revisar.
- Deshacer y Rehacer siguen visibles en la barra de herramientas. Las acciones de rama y stash se pueden recuperar desde «Personalizar barra de herramientas».

## [0.9.0] - 2026-11-09

### Novedades

- Soporte de Git LFS: estado de cada archivo (puntero, descargado o extraído), diff con el contenido real o el aviso «sin descargar», descargas de todo o de archivos concretos y bloqueos desde el menú del archivo. Sin `git-lfs` instalado, Leviatán lo indica sin errores.
- Firma de commits y tags con la configuración GPG o SSH que ya tienes, también en merge, revert, cherry-pick y rebase. El detalle de commits y tags muestra si la firma está verificada, y Ajustes de Git permite activar la firma global o por repositorio. Los errores de clave o de agente se explican con claridad.
- Submódulos: sincronizar sus URL, registrar el commit actual de un submódulo en el repositorio padre, ver los commits entre el puntero anterior y el nuevo en el diff y resolver conflictos de submódulo eligiendo un lado.

### Colaboración

- Comentarios de review en una línea o un rango del diff de una PR o MR, con respuestas y hilos que se pueden resolver o reabrir, en GitHub y GitLab.
- Desde el detalle de un issue se puede crear una rama con su número y título; la PR creada desde esa rama propone «Closes #n». El issue muestra también sus PR vinculadas.
- Antes de un push, un force push o una fusión, Leviatán lee las reglas de protección de la rama (rulesets y protección clásica de GitHub, ramas protegidas de GitLab) y avisa sin bloquear cuando el servidor probablemente rechazará la operación. El panel de fusión lista las aprobaciones y los checks exigidos. Sin permiso para leer reglas no se muestra nada.

### Interfaz

- El filtro de referencias se enfoca con ⌥⌘L; ⌥⌘F queda para abrir el repositorio en Finder.

## [0.8.2] - 2026-11-06

### Interfaz

- La sección de issues conserva las tarjetas de lista, título, descripción y metadatos, con filtros agrupados y una cabecera más clara.
- Los detalles se pueden plegar, se muestran por defecto en ventanas amplias y el modo de lectura permite concentrarse en el contenido del issue.
- Las descripciones aprovechan mejor el ancho disponible y mantienen una tipografía compacta.

### Correcciones

- Los comentarios HTML de las descripciones se ocultan sin alterar los ejemplos de código, los enlaces ni el énfasis del Markdown.
- Se eliminan los huecos que dejaban los comentarios HTML ocultos antes de la descripción.
- Actualizar los issues conserva la lista visible y su selección.

## [0.8.1] - 2026-11-05

### Interfaz

- Rediseña la hoja de Actividad con tarjetas, estado visible y salida de error destacada
- Rediseña la hoja de operación fallida con icono, salida de git destacada y botones al estilo macOS

### Correcciones

- Quita el chevrón duplicado de las secciones y permite abrir las carpetas de ramas
- Quita el progreso de git de los mensajes de error para que se vea la causa

## [0.8.0] - 2026-11-04

### Novedades

- Permite ampliar toda la interfaz con una escala persistente (#242)

### Interfaz

- Separa Historial y Cambios y simplifica el contexto del repositorio (#239)
- Mejora la legibilidad y la navegación de la barra lateral

### Correcciones

- Muestra códigos gitmoji como emojis en el historial

## [0.7.0] - 2026-10-29

### Novedades

- Se pueden inspeccionar los archivos modificados y sus diffs en otros worktrees desde el historial.

### Mejoras

- Se mejora la legibilidad de los filtros, formularios, paneles de issues, resolución de conflictos y avisos.
- Se conservan la búsqueda, la visibilidad y las pausas al alternar paneles.

### Correcciones

- El inspector evita recortar su contenido en ventanas estrechas.
- La ventana de Ajustes recuerda su tamaño y muestra correctamente el cursor en los controles interactivos.

## [0.6.0] - 2026-10-28

### Novedades

- La pestaña CI permite consultar los pipelines de GitLab, sus trabajos y logs, y cancelar o volver a ejecutar procesos de CI desde Leviatán.
- Las filas WIP de la copia de trabajo y de los worktrees aparecen junto a su commit base en el grafo.
- Al pulsar una etiqueta se selecciona y revela su commit. El historial también incluye los commits alcanzables desde etiquetas.

### Rendimiento

- La carga de páginas del historial precarga bloques y reutiliza el trabajo de Git; los refrescos automáticos comparten y reutilizan las consultas de worktrees.
- Los cambios en las filas WIP reutilizan los carriles del grafo ya calculados.
- Los cálculos de presentación y búsqueda de diffs se cancelan al cambiar de archivo, y las líneas demasiado largas se descartan antes de copiarlas completas para comparar palabras.
- El editor de conflictos deja de recomponer el archivo completo al escribir o navegar entre bloques.

### Correcciones

- Los diffs de más de 8 MiB se detienen antes de parsearse y muestran un aviso para abrir el archivo en un editor externo, evitando un consumo excesivo de memoria.

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
