# Modelización de las clases del Ajedrez

## Juego (Partida)

### Atributos

    - tablero: Tablero
    - turno: Color
    - partida: Estado

### Métodos

    + inicia()
    + jugada(Cadena)
    - mover(Movimiento)
    - cambiaTurno()
    + dameTablero(): Tablero
    + dameTurno(): Color
    + dameEstado(): Estado

## Jugador (Oponente, Adversario)

## Pieza

### Atributos

    - color: Color

### Métodos

    + ctor(color: Color)
    + dameColor(): Color
    # ponColor(color: Color)
    + mover(Movimiento, Tablero)
    # <<abtract>> esValido(Movimiento, Tablero): booleano

## Rey -> Pieza

### Métodos

    # <<override>> esValido(Movimiento, Tablero): booleano

## Reina (Dama) -> Pieza

### Métodos

    # <<override>> esValido(Movimiento, Tablero): booleano

## Alfil -> Pieza

### Métodos

    # <<override>> esValido(Movimiento, Tablero): booleano

## Caballo -> Pieza

### Métodos

    # <<override>> esValido(Movimiento, Tablero): booleano

## Torre -> Pieza

### Métodos

    # <<override>> esValido(Movimiento, Tablero): booleano

## Peon -> Pieza

### Métodos

    # <<override>> esValido(Movimiento, Tablero): booleano
    + <<override>> mover(Movimiento, Tablero)
    - enPosiciónInicial(Movimiento): booleano
    - avanza(Movimiento): booleano
    - puedeComer(Movimiento): booleano

### Eventos

    NecesitoPromoción(PromocionArgs)

## Color (Turno) \<\<enum>>

- Blanco
- Negro

## Tablero

### Atributos

    - piezas[8,8]: Escaque

### Métodos

    + ponPieza(Posición, Pieza)
    + ponPieza(fila: entero, columna: entero, Pieza)
    + damePieza(Posición): Pieza
    + quitaPieza(Posición)
    + hayPieza(Posición): booleano
    + hayPiezaEntre(Movimiento): booleano
    + hayPiezaEntre(inicial: Posición, final: Posición): booleano
    + mover(Movimiento)
    + mover(inicial: Posición, final: Posición)
    + clonar(): Tablero
    + <<clase>> dameColorEscaque(Posición): Color

## Escaque (cuadrado)

### Atributos

    - pieza: Pieza
  
### Métodos

    + ponPieza(Posición, Pieza)
    + damePieza(Posición): Pieza
    + quitaPieza(Posición)

## Posición

### Atributos

    - fila: Entero
    - columna: Entero
  
### Métodos

    + ctor(fila: entero, columna: entero)
    + ctor(fila: letra, columna: letra)
    + dameFila(): Entero
    + dameColumna(): Entero
    + igual(Posición)

## Movimiento

### Atributos

    - inicial: Posición
    - final: Posición
  
### Métodos

    + ctor(cadena)
    + damePosicionInicial(): Posición
    + damePosicionFinal(): Posición
    + esVertical(): booleano
    + esHorizontal(): booleano
    + esDiagonal(): booleano
    + saltoVertical(): entero
    + saltoHorizontal(): entero
    + deltaVertical(): entero
    + deltaHorizontal(): entero

## Estado \<\<enum>>

- Inicial
- Jugando
- Jaque
- Jaque Mate
- Tablas
- Cancelada

## JuegoException

### Atributos

    - mensaje: cadena
  
### Métodos

    + ctor(cadena)
    + dameMensaje(): cadena

## Descartes

Tiempo

Enroque

Promoción

Jaque


