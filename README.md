# Hoopy_Days_2.0 - Udemy GoDot Course - 2º Project 
## Personal Upgrade Version 
Hoopy_Days is a platforms game. The 2.0 version change sprites and add behaviours for the player and enemies.

**Needs GoDot 3.1**
<br>**Status: Develop**<br>

- [Introduccion](#introduccion)
- [Casos de uso](#casos-de-uso)
  * [CU1. Level 1](#cu1-level-1)
  * [CU2. El jugador](#cu2-el-jugador)
  * [CU3. Enemigos](#cu3-enemigos)
  * [CU3.1. Enemigos Generico](#cu31-enemigos-generico)
  * [CU3.2. Enemigo - Germen](#cu32-enemigo---germen)
  * [CU3.3. Enemigo - Trasero Volador](#cu33-enemigo---trasero-volador)
  * [CU3.4. Enemigo - Mr Mojón](#cu34-enemigo---mr-moj-n)
  * [CU4. GUI](#cu4-gui)
  * [CU5. Música](#cu5-m-sica)

## Introduccion
El juego constará de una fase de plataformas con jefe final.
La fase uno consistirá en un mapa de plataformas con enemigos.
El personaje principal deberá evitar/acabar con los enemigos hasta llegar
al jefe final y derrotarlo para superar la fase. Ademas de soltear
las plataformas de la fase.
El personaje principal será un rollo de papel higiénico que tendrá que acabar
con enemigos de temática similar mientras supera plataformas hasta
 acabar el nivel

## Casos de uso
### CU1. Level 1
- El level 1 debe tener un diseño fijo (no aleatorio) determinado por 
el diseñador de niveles. Será una cloaca donde las tuberías (al estilo Super Mario) harán de plataforma.
- Las plataformas serán fijas, no móviles.
- Habrá elmentos hostiles como pinchos y fuego.
- Habrá items de recuperación de cargas de golpear (paquete de rollos de papel)
- Habrá un límite de tiempo en superarlo de 99 segundos
- Los enemigos estarán en sitios específicos y serán un número determinado 
por el diseñador de niveles
- Habrá dos tipos de enemigos:
    - El "Germen"
    - El "Trasero Volador"
- El jefe final será "Mr Mojón"

### CU2. El jugador
- El jugador será un rollo de papel higiénico. Sprite de rollo de papel
- El jugador tendrá 3 puntos de vida los cuales perderá en los siguientes
casos:
    - Si un enemigo le golpea/toca perdera 1 punto, por defecto.
    - Si es golpeado por algún elmento hostil (fuego, pinchos, etc)
    perderá 1 punto, por defecto.
    - Si cae al vacío perderá 1 punto y tendrá que comenzar la fase, por defecto.
- Al perder vida el jugador estará 2 segundos inmune a cualquier daño.
Esto se reflejará en que el jugador parpadea.
- Al perder vida debe emitir un sonido "ouch"
- El jugador puede golpear, cada vez que lo hace, gasta un poco de rollo.
Si lo gasta todo, no podrá golpear. Puede hacer uso de golpear 5 veces.
Estas cargas para golpear se pueden recuperar con items que hay en el escenario.
Cada vez que coja un item de recuperación, recuperará todas las cargas.
Cada vez que golpee y pierda una carga también se deberá reflejar graficamente,
haciendose cada vez más fino.
- Al recuperar carga de ataque debe emitir un sonido "ouh yeah mama"

### CU3. Enemigos
### CU3.1. Enemigos Generico
- Los enemigos podrán moverse o no por el mapa, según estén definidos.
- Los enemigos tendrán puntos de vida, según estén definidos.
- Cuando un enemigo muere parpadea 2 segundos y desaparece.
- Los enemigos no pueden tocarse entre si, no tienen collision
- Los enemigos al atacar pueden dañar al jugador y al tocarlo también. Por defecto     al tocarlo le quitan 1 punto de vida y al dañarlo con un ataque según estén definidos.  
### CU3.2. Enemigo - Germen
- Sprite de Germen (bola morada con pinchos al estidlo del pokemon kofkaf o como se llame)
- Enemigo en movimiento botando de izquierda a derecha por la plataforma sin llegar a caerse.
- Al botar debe emitir el sonido "boing"
- Si toca al jugador le quita 1 punto de vida.
- Tiene un punto de vida.
- Al ser golpeado emitirá un sonido "ahhhh"

### CU3.3. Enemigo - Trasero Volador
- Sprite de Trasero Volador (trasero con pelos que lanza ventosidades verdes)
- Enemigo en movimiento horizontal de izquierda a derecha por la plataforma sin llegar a caerse
- Si toca al jugador le quita 1 punto de vida
- Lanza una ventosidad cuando en su visión entra el jugador, con un timer de 2 segundos. La ventosidad quita 1 punto de vida.
- Al lanzar la ventosidad debe emitir el sonido "prr" de ventosidad reverberante
- Tiene un punto de vida.
- Al ser golpeado emitira un sonido "shh" de ventosidad silenciosa

### CU3.4. Enemigo - Mr Mojón
- Sprite de Mr Mojón (un mojón gigante como el de wassap)
- Enemigo en movimiento botando de izquierda derecha de manera lenta, cada 3 segundos da un salto.
- Al botar debe eimitr el sonido "chof"
- Cada vez que toca el suelo deja una mancha. Estas manchas si tocan al jugador lo dañan 1 punto.
    Se pueden eliminar si el jugador las golpea.
- Si toca al jugador le quita 1 punto de vida.
- Tiene 5 puntos de vida.
- Al ser golpeado debe emitir el sonido "au"
- Cuando le quede 1 punto de vida entrará en enrage y saltará cada 1.5 segundos. Esto se indicará
cambiando su color a un tono rojizo parpadeante.
- Cuando le quede un punto de vida debe emitir el sonido "madafakaaaaaaa"
- Al perder todos los puntos de vida debe emitir el sonido "noooo"

### CU4. GUI
- Se debe mostrar los puntos de vida del jugador a modo de mini rollos de papel como él.
- Se debe mostrar las cargas de ataqe como si fuese una barra de progresión.
- Se debe mostrar el contador de tiempo

### CU5. Música
- El tema principal será decidido por el diseñador
- En el jefe final la música cambiando
- Cuando el jefe final entra en enrage se escucha la música de psicosis a la vez
- Cuando quedan 20seg en el contador la música se hacelera un 50%