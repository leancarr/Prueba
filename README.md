# Donkey Kong - RTM32 v0.5

Este repositorio contiene la adaptación de **Donkey Kong** para la arquitectura de CPU **RTM32 v0.5**.

## ✨ Sprites Extraídos (32x32 píxeles)

Se han extraído, adaptado y escalado todos los sprites principales del juego a una resolución de 32x32 píxeles, utilizando una interpolación *Nearest Neighbor* para mantener la nitidez perfecta del *pixel art* original.

Entre los assets disponibles en la carpeta `assets/` se encuentran:
- **Personajes**: Donkey Kong (`kong.png`), Mario (`jumpman.png`), Pauline (`pauline.png`)
- **Enemigos y Objetos**: Barril (`barrel.png`), Fuego (`fireelemental.png`), Martillo (`hammer.png`), Barril de Fuego (`firebarrel.png`)
- **Escenario**: Plataformas (`platform.png`), Escaleras (`ladder.png`), Mapa de tiles (`tilemap.png`)

> **Nota de versión**: Estos sprites están preparados específicamente para ser cargados en la memoria de video y dibujados en consola/pantalla por la nueva CPU RTM32.

## 🚀 Cómo jugar (Próximamente)

*(El código ensamblador para Donkey Kong está en desarrollo. Estará disponible aquí cuando finalice su implementación utilizando el nuevo set de instrucciones y los snapshots binarios con cabecera de la versión 0.5).*

