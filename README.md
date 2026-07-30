# New Godswars — Builds

Repositorio de descargas del cliente Windows.

- Cada versión se publica aquí (y preferiblemente como GitHub Release)
- El aviso sale en Discord (`#descargas`)
- El código del juego está en otro repositorio

## Versiones

| Versión | Archivo | Notas |
|---------|---------|--------|
| **0.2.0** (actual) | [NewGodswar-v0.2.0.zip](./NewGodswar-v0.2.0.zip) | Red/ping estable, Prod VPS, autoridad de combate/movimiento |
| 0.1.0 | [NewGodswar-v0.1.0.zip](./NewGodswar-v0.1.0.zip) | Build inicial |

## Cómo descargar

1. Baja el `.zip` de la versión más reciente
2. Extrae la carpeta
3. Ejecuta `NewGodswar3D.exe`

## Servidor (v0.2.0)

- Game: `213.136.69.57:7777`
- Admin: http://213.136.69.57:9080

## Changelog v0.2.0

- Ping local corregido (ya no sube a miles de ms al moverse)
- Cola de red + prioridad ping
- Validación de movimiento / cooldown de ataque / portales
- Cliente embebido con `Environment=Prod`
- Versión visible en Login y HUD
