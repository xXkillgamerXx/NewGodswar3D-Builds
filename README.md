# New Godswars — Builds

Repositorio de descargas del cliente Windows.

- Cada versión se publica aquí (y preferiblemente como GitHub Release)
- El aviso sale en Discord (`#descargas`)
- El código del juego está en otro repositorio
- El **launcher** lee [`version.json`](./version.json) y **pregunta** si hay update

## Versiones

| Versión | Archivo | Notas |
|---------|---------|--------|
| **0.2.2** (actual) | [NewGodswar-v0.2.2.zip](./NewGodswar-v0.2.2.zip) | Hitstun real, sin warp al atacar, windup, rango más justo |
| 0.2.1 | [NewGodswar-v0.2.1.zip](./NewGodswar-v0.2.1.zip) | Sync nombres/HP/movimiento, floaters locales, click-to-attack |
| 0.2.0 | [NewGodswar-v0.2.0.zip](./NewGodswar-v0.2.0.zip) | Red/ping estable, Prod VPS, autoridad de combate/movimiento |
| 0.1.0 | [NewGodswar-v0.1.0.zip](./NewGodswar-v0.1.0.zip) | Build inicial |

## Launcher (recomendado)

Descarga el launcher adaptado: [NewGodswarLauncher.zip](./NewGodswarLauncher.zip)

1. Extrae `NewGodswarLauncher.exe`
2. Ábrelo — lee `version.json`, descarga/actualiza el juego solo y pregunta si hay update
3. **Launch game** abre `NewGodswar3D.exe` desde `%LocalAppData%\NewGodswar\Game\`

## Cómo descargar (manual)

1. Baja el archivo de la versión más reciente (`.zip`)
2. Extrae la carpeta
3. Ejecuta `NewGodswar3D.exe`

En Login debe salir: `v0.2.2 | Env=Prod → 213.136.69.57:7777`

## Servidor (v0.2.2)

- Game (TCP): `213.136.69.57:7777` (el cliente sigue por IP)
- Admin / registro: http://newgodswar.online  (sin puerto)
- Admin directo (fallback): http://213.136.69.57:9080

## Changelog v0.2.2

### Combate (slime / IA)
- **Hitstun real** — Al pegarle al slime, el server también se pausa (~0.75s); ya no sigue atacando mientras hace GetHit
- **Sin teleporte al atacar** — Dejó de hacer Warp agresivo al entrar en Attack; el “salto pesado” debería desaparecer
- **Sin flinch falso** — Miss (FALLA) y golpe mortal ya no juegan GetHit; la muerte va directo a Die
- **Primer golpe con windup** — Al enganchar, espera ~0.45s antes del primer hit (menos ataque “de la nada”)
- **Rango más justo** — Menos daño a distancia absurda; camp assist un poco más corto (8u)
- **GetHit más largo** — Stun visual 0.85s, alineado con la animación

## Changelog v0.2.1

### Multijugador
- Nombres de personaje correctos (ya no “Guerrero” en ambos)
- Vida sincronizada al entrar (el otro jugador ve HP real)
- Movimiento remoto más estable (sin flotar)
- Textos de daño / FALLA / CRIT solo locales
- Barra táctica del enemigo solo si lo tienes en target

### Combate / UX
- Click izquierdo en enemigo → ir y atacar
- Click derecho corto → quitar target
- Mejoras de IA / camps en servidor

### UI
- Tamaño de daño/crit configurable en `config.ini` sección `[UI]`

## Changelog v0.2.0

- Ping local corregido (ya no sube a miles de ms al moverse)
- Cola de red + prioridad ping
- Validación de movimiento / cooldown de ataque / portales
- Cliente embebido con `Environment=Prod`
- Versión visible en Login y HUD

