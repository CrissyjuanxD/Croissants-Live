# Croissants · datos en vivo

Los datos que la [web de Croissants Segunda Edición](https://crissyjuanxd.github.io/Croissants-Web/) lee en tiempo real.
Los sube **QuasoPlugin** desde el servidor; no se editan a mano.

| Archivo | Qué trae |
| --- | --- |
| `estado.json` | Día de la temporada, misiones activas, cambios activos (`/changes`), quién está conectado y la versión de los otros dos archivos |
| `catalogo.json` | Items, mobs, misiones, crafteos, trabajos y habilidades tal como están en el plugin |
| `jugadores.json` | Las estadísticas de cada jugador: misiones, DinoCoins, trabajos, habilidades, horas jugadas… |

Cada subida es un commit nuevo sin historia (la rama se mueve a la fuerza), así el repositorio no crece. Después del
commit el plugin avisa por [ntfy.sh](https://ntfy.sh) y las páginas abiertas se actualizan al instante.

En el servidor: `/web` muestra el estado de la conexión, `/web subir` sube todo al momento y `/web recargar` vuelve a
leer la sección `web:` de `plugins/QuasoPlugin/config.yml`.
