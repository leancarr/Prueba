# Donkey Kong - RTM32

<div align="center">
  <img src="preview/kong.png" alt="Donkey Kong Animaciones">
  <br>
  <img src="preview/jumpman.png" alt="Mario (Jumpman)">
  <img src="preview/pauline.png" alt="Pauline">
</div>

## Descripción del juego

Donkey Kong es una reinterpretación del clásico arcade de Nintendo para la arquitectura RTM32. El objetivo es controlar a Jumpman (Mario) y escalar una obra en construcción evadiendo obstáculos para rescatar a su novia Pauline de las garras del gorila gigante Donkey Kong.

## Historia

Jumpman es un carpintero valiente pero común y corriente. Su mascota, un enorme simio llamado **Donkey Kong**, se ha escapado, ha secuestrado a su novia **Pauline** y la ha llevado a lo más alto de una obra en construcción de la ciudad. 

En un acto de furia, Donkey Kong ha comenzado a lanzar barriles por las rampas y vigas metálicas para impedir que alguien se acerque. Jumpman debe armarse de valor, trepar por escaleras inestables, saltar obstáculos mortales y esquivar llamas vivientes para llegar a la cima y salvar al amor de su vida. 

Esto no es solo un trabajo de construcción. Es una misión de rescate en las alturas donde un solo paso en falso significa la derrota.

## Mecánicas del juego

### Controles
El jugador controla a Jumpman desde una vista lateral (plataformas). Se puede correr de izquierda a derecha, saltar para esquivar obstáculos o alcanzar plataformas, y subir o bajar por las escaleras que conectan los distintos niveles de vigas.

### Obstáculos y enemigos
La obra está llena de peligros que harán que tu ascenso sea una pesadilla:

- **Barriles (Barrels)**: Lanzados constantemente por Donkey Kong desde la cima. Ruedan por las rampas y, a veces, caen sorpresivamente por las escaleras. ¡Un toque y estás frito!
- **Llamas Vivientes (Fireballs)**: Enemigos impredecibles que nacen cuando los barriles azules chocan contra el barril de fuego en la base. Se mueven de forma errática por las plataformas y pueden subir escaleras.

Si Jumpman es golpeado por un barril, tocado por el fuego, o cae desde una altura demasiado grande, pierde una vida.

### El Martillo (Hammer)
El recurso más valioso para la defensa. 
- En la pista aparecen martillos flotantes. Si Jumpman salta y agarra uno, entrará en un modo de invencibilidad ofensiva por tiempo limitado.
- **Destrucción**: Con el martillo en mano, Jumpman no puede saltar ni subir escaleras, pero aplastará automáticamente cualquier barril o bola de fuego que se cruce en su camino, sumando jugosos puntos extra.

### Puntuación y progresión
- Los puntos se acumulan al saltar sobre los barriles, destruirlos con el martillo, agarrar los objetos perdidos de Pauline (paraguas, sombreros, bolsos) y al completar la etapa.
- Además de los puntos, hay un temporizador de bonus. Si el tiempo llega a cero, Jumpman pierde una vida. El tiempo restante al terminar la etapa se suma como puntos.
- La dificultad aumenta en cada nivel con barriles más rápidos y más bolas de fuego.

## Las 4 Etapas del Rescate

El ascenso a la cima se divide en 4 etapas clásicas (niveles de altura), cada una con un diseño arquitectónico distinto y desafíos únicos.

### Etapa 1: "25m" (Las Rampas)
El nivel icónico que lo empezó todo. Una estructura en zig-zag de vigas rojas.

### Etapa 2: "50m" (La Fábrica de Cemento / Cintas Transportadoras)
El nivel de las plataformas móviles (a menudo omitido en versiones de consola, pero presente en el arcade original).

### Etapa 3: "75m" (Los Ascensores)
Un salto al vacío. Ascensores mecánicos que suben y bajan constantemente.

### Etapa 4: "100m" (Los Remaches)
El enfrentamiento final para derrotar a Donkey Kong quitando los soportes de la estructura.

<div align="center">
  <img src="preview/tilemap.png" alt="Tileset de los Niveles">
  <p><i>Tileset (Bloques de construcción) para renderizar los niveles</i></p>
</div>

## Hoja de Sprites (Animaciones completas)

| Elemento | Animaciones completas (Vista previa ampliada) | Dimensiones Originales |
|--------|-------------|--------|
| **Jumpman (Mario)** | <img src="preview/jumpman.png" width="150"> | 16x16 por frame |
| **Donkey Kong** | <img src="preview/kong.png" width="250"> | 40x32 por frame |
| **Pauline** | <img src="preview/pauline.png" width="100"> | 16x24 por frame |
| **Barriles** | <img src="preview/barrel.png" width="150"> | 16x16 por frame |
| **Fuego (Enemigo)** | <img src="preview/fireelemental.png" width="100"> | 16x16 por frame |
| **Martillo** | <img src="preview/hammer.png" width="100"> | 10x14 por frame |

> **Nota:** En la carpeta `assets/` se encuentran las imágenes en su **resolución original 1x** (Pixel Perfect) idéntica a la del Arcade original, listas para cargarse en memoria y ser renderizadas por la GPU/CPU de la arquitectura RTM32. En el README se muestran escaladas (Zoom 3x) para mejor visualización.

## Características visuales

- Paleta de colores vibrantes sobre un fondo negro profundo para resaltar la obra nocturna.
- Animaciones clásicas en pixel-art de 8 bits.
- Vista lateral de plataformas estáticas de una sola pantalla (Single-screen platformer).
