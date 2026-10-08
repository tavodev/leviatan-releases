# Leviatán · versiones

Versiones publicadas de [Leviatán](https://github.com/tavodev/leviatan), un cliente Git para macOS 26.

- **Descargas**: cada versión está en [Releases](https://github.com/tavodev/leviatan-releases/releases) como un `.zip` firmado con Developer ID y notarizado por Apple.
- **Actualizaciones automáticas**: la app consulta [`appcast.xml`](appcast.xml) con [Sparkle](https://sparkle-project.org). Cada entrada lleva la firma EdDSA del zip y la app rechaza cualquier archivo que no coincida.
- **Cambios**: [`CHANGELOG.md`](CHANGELOG.md).

Este repositorio no contiene código: `./scripts/release.sh` del repositorio principal lo actualiza al publicar. No lo edites a mano.
