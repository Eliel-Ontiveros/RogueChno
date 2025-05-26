# RogueChno

RogueChno es un juego de disparos lateral en 2D (shoot 'em up) desarrollado en C++ utilizando la biblioteca SDL. El jugador controla una nave espacial, esquiva enemigos y proyectiles, y trata de sobrevivir el mayor tiempo posible mientras acumula puntos.

## Descripción del Juego

En RogueChno, te enfrentarás a oleadas de naves enemigas con diferentes patrones de ataque. Deberás demostrar tus reflejos y habilidad para esquivar sus disparos y eliminarlos antes de que te destruyan. Recoge power-ups para mejorar tu nave y aumentar tus posibilidades de supervivencia. ¡Compite por la puntuación más alta! El juego se ejecuta en una ventana de 1024x500 píxeles.

## Características Principales

* **Acción Frenética:** Combate contra múltiples enemigos y esquiva una lluvia de balas.
* **Movimiento del Jugador:** Control total de la nave con movimiento en todas las direcciones (W/A/S/D o Flechas) y capacidad de "boost" (Shift Izquierdo) para mayor velocidad.
* **Sistema de Disparo:** Dispara proyectiles (Espacio) para destruir a los enemigos.
* **Power-ups:**
    * **Bonus de Salud (HP):** Recupera puntos de vida.
    * **Mejora de Ataque (Shootgun):** Dispara múltiples proyectiles a la vez.
* **Tipos de Enemigos:**
    * Enemigos con patrones de movimiento y disparo simples.
    * Enemigos que pueden cambiar su patrón de ataque y disparar ráfagas.
* **Sistema de Puntuación:** Gana puntos por destruir enemigos y recoger power-ups.
* **Puntuación Más Alta (High Score):** El juego guarda la puntuación más alta alcanzada en `resources/docs/scores.txt`.
* **Efectos Visuales:** Explosiones y efectos de partículas para una experiencia más inmersiva.
* **Sonido y Música:** Efectos de sonido para disparos, explosiones y música de fondo.
* **Pantallas de Juego:** Pantalla de título, pantalla de juego principal y pantalla de fin de juego.
* **Animación de Entrada:** Una breve animación cuando el jugador entra en la pantalla de juego.

## Requisitos

* Un compilador de C++ (como g++).
* Biblioteca SDL2 instalada.
* Biblioteca SDL2\_image instalada.
* Biblioteca SDL2\_ttf instalada.
* Biblioteca SDL2\_mixer instalada.

## Cómo Compilar (Ejemplo General)

Dado que no se proporcionan archivos de compilación específicos (Makefile, CMakeLists.txt), aquí hay un ejemplo general de cómo podrías compilar los archivos fuente utilizando g++ en un sistema Linux o similar. Deberás ajustar los paths y los nombres de los archivos según tu configuración.

```bash
g++ src/main.cpp src/Game.cpp src/Player.cpp src/Enemy.cpp src/Entity.cpp src/Effect.cpp -o RogueChno \
-I/ruta/a/tus/includes/SDL2 \
-L/ruta/a/tus/libs/SDL2 \
-lSDL2 -lSDL2_image -lSDL2_ttf -lSDL2_mixer
```

**Nota:** Reemplaza `/ruta/a/tus/includes/SDL2` y `/ruta/a/tus/libs/SDL2` con las rutas correctas donde tienes instaladas las bibliotecas SDL2 en tu sistema. En Windows, el proceso de compilación puede variar. El archivo de log `RogueChno.log` indica que se usó Visual Studio para compilar (`RogueChno.vcxproj -> C:\SDL\Proyectos\RogueChno\x64\Debug\RogueChno.exe`).

## Cómo Jugar

* **Menú Principal:**
    * Presiona `ESPACIO` para comenzar el juego.
    * Presiona `ESC` para salir del juego.
* **Controles en el Juego:**
    * **Movimiento:** `W` o `Flecha Arriba` (Mover hacia arriba), `S` o `Flecha Abajo` (Mover hacia abajo), `A` o `Flecha Izquierda` (Mover hacia la izquierda), `D` o `Flecha Derecha` (Mover hacia la derecha).
    * **Disparar:** `ESPACIO`.
    * **Boost (Aumento de Velocidad):** `SHIFT Izquierdo` (mantener presionado).
* **Objetivo:**
    * Sobrevive el mayor tiempo posible.
    * Destruye naves enemigas para obtener puntos.
    * Recoge power-ups para mejorar tu nave.
    * Evita colisionar con naves enemigas y sus proyectiles.
* **Fin del Juego:**
    * El juego termina cuando la salud de tu nave llega a cero.
    * Se mostrará tu puntuación final y la puntuación más alta.
    * Desde la pantalla de fin de juego, puedes presionar `ESPACIO` para volver a jugar o `ESC` para salir.

## Estructura de Carpetas (Basada en los archivos)

```
RogueChno/
├── resources/
│   ├── docs/
│   │   └── scores.txt       # Almacena la puntuación más alta
│   ├── fonts/
│   │   └── myriadProRegular.ttf # Fuente utilizada en el juego
│   ├── sprites/             # Contiene las imágenes y texturas
│   │   ├── playerShip.png
│   │   ├── enemyShip.png
│   │   ├── blueLaser.png
│   │   ├── shootGunBullet.png
│   │   ├── redLaser.png
│   │   ├── bonusHP.png
│   │   ├── enchanceATK.png
│   │   ├── explosion.png
│   │   ├── menu.png
│   │   ├── ending.png
│   │   ├── icono.png
│   │   └── background2.jpg
│   └── sound/               # Contiene los archivos de audio
│       ├── laser.ogg
│       ├── explosion.ogg
│       ├── background.mp3
│       └── button.ogg
├── src/                     # Código fuente del juego
│   ├── Effect.cpp
│   ├── Effect.h
│   ├── Enemy.cpp
│   ├── Enemy.h
│   ├── Entity.cpp
│   ├── Entity.h
│   ├── Game.cpp
│   ├── Game.h
│   ├── Player.cpp
│   ├── Player.h
│   ├── defs.h               # Definiciones y constantes globales
│   └── main.cpp             # Punto de entrada del programa
├── x64/Debug/               # Archivos de compilación (ej. RogueChno.log, RogueChno.exe)
└── README.md                # Este archivo
```

## Créditos

* **Desarrollador:** Eliel Ontiveros
```
