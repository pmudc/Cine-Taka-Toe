Cine Taka Toe es un juego inspirado en el Tiki Taka Toe de fútbol, pero llevado al cine: un tablero 3×3 donde cada casilla representa la intersección entre una condición de fila y una condición de columna.  
En tu turno, eliges una casilla y buscas una película que cumpla ambas condiciones. Si aciertas, colocas tu jugada. Si fallas, pierdes el turno y la casilla continúa vacía.

> El proyecto fue hecho por dos estudiantes de primer año:
> - **Pablo Muradas Santa María** — Doble Grado en Ingeniería Informática y Ciencia de Datos  
> - **Gonzalo Simón López** — Ingeniería Informática

---

Instrucciones de juego.

1. El botón "Nueva partida" genera 3 condiciones para filas y otras 3 para columnas (estas condiciones pueden ser un actor que aparezca en la película, quién fue el director, de qué género es, o la década en que se estrenó).
2. En tu turno:
   - Seleccionas una casilla
   - Buscas una película
   - Pulsas "usar esta película"
3. El juego valida automáticamente si la película cumple ambas condiciones usando la API de TMDB.
4. El turno cambia tanto si aciertas como si fallas.
5. Si un jugador consigue 3 en raya, gana la partida.
6. Al acabar, salen 3 opciones:
   - Nueva partida
   - Seguir jugando (para intentar completar las casillas vacías)
   - Completar (rellena automáticamente las casillas vacías con ejemplos válidos)

---

Características

- ✅ Modo 1v1: jugador azul vs jugador rojo  
- ✅ Turnos alternos
- ✅ Victoria por 3 en raya
- ✅ Selector de iempo por turno (sin tiempo / 15s / 30s / 60s)
- ✅ Botón Saltar turno
- ✅ Botón Completar tablero automático
- ✅ Marcador de partidas ganadas (persistente con `localStorage`)
- ✅ Fondo dinámico que cambia según el turno (azul/rojo)
- ✅ Validación real con TMDB

---

Cómo valida una jugada (API de TMDB)

Cuando eliges una película:
1. Se consulta su ficha completa en TMDB con `append_to_response=credits`  
2. Se comprueba:
   - Actor/actriz en reparto  
   - Director/a en crew  
   - Género  
   - Década (año de estreno)  
3. Si cumple fila + columna, se coloca la película en la casilla.

Nota sobre licencia TMDB: tras revisar el GitHub de TMDB, no hemos encontrado ninguna licencia, por lo que nuestro proyecto es totalmente independiente y no está limitado por TMDB. Además, queremos que nuestro proyecto sea totalmente libre y que cualquiera pueda utilizarlo.

Nota sobre la API Key: para conseguir la API Key que debes colocar en el codigo en app.js, simplemente creamos una cuenta en TMDB, y en ajustes buscamos la opción que nos permite solicitar la API Key v3.
---

Cómo ejecutarlo.

Nosotros escogimos utilizar Live Server en Visual Studio Code:
1. Abre la carpeta del proyecto en VSCode
2. Click derecho en `index.html` → **Open with Live Server**
3. Se abre en el navegador y ya puedes jugar

Contacto: (estaremos encantados de resolver cualquier consulta o propuesta)
cinetakatoe@proton.me
pablo.muradas@udc.es
gonzalo.simon.lopez@udc.es
