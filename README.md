#  Juego de Lucha en Java - Patrón Decorator

##  Descripción

Este proyecto consiste en el desarrollo de un juego de lucha por turnos en Java, donde dos personajes se enfrentan hasta que uno de ellos pierde todos sus puntos de vida (HP).

El proyecto está basado en el enunciado del taller propuesto, pero se mejora aplicando el **patrón de diseño Decorator**, permitiendo agregar habilidades especiales a los personajes como escudo y veneno sin modificar la clase base.

---

##  Objetivo

Implementar un sistema de combate entre personajes utilizando:

* Programación Orientada a Objetos (POO)
* Herencia y polimorfismo
* Patrón de diseño **Decorator**

---

##  Funcionamiento del Juego

* Cada personaje inicia con **100 puntos de vida (HP)**.
* En cada turno, un jugador ataca al otro.
* El daño de cada ataque es aleatorio entre **10 y 30 puntos**.
* El juego continúa por turnos hasta que uno de los personajes llega a **0 HP**.
* El último personaje en pie es el ganador.

---

##  Estructura del Proyecto

El proyecto está compuesto por las siguientes clases:

### 🔹 `Personaje` (Interfaz)

Define el comportamiento básico:

* `atacar()`
* `recibirDano()`
* `estaVivo()`
* `getNombre()`
* `getPuntosDeVida()`

---

### 🔹 `PersonajeBase`

Implementa la lógica principal del personaje:

* Vida inicial de 100 HP
* Ataques aleatorios
* Recepción de daño

---

### 🔹 `PersonajeDecorador` (Abstracta)

Clase base para los decoradores:

* Permite añadir funcionalidades sin modificar la clase original

---

### 🔹 `EscudoDecorador`

Agrega una defensa adicional:

* Absorbe hasta **20 puntos de daño**
* Reduce el daño recibido

---

### 🔹 `VenenoDecorador`

Agrega daño extra:

* Inflige **5 puntos adicionales** después de cada ataque

---

### 🔹 `JuegoLucha`

Controla el flujo del juego:

* Maneja los turnos
* Determina el ganador

---

### 🔹 `Main`

Clase principal:

* Solicita nombres de jugadores
* Inicializa personajes
* Inicia la pelea

---

##  Patrón de Diseño Utilizado

###  Decorator

El patrón **Decorator** permite agregar nuevas funcionalidades a un objeto de forma dinámica sin alterar su estructura original.

###  Ventajas en este proyecto:

* Se pueden combinar habilidades (ej: escudo + veneno)
* Código flexible y escalable
* Fácil de extender con nuevos poderes

---

##  Ejecución del Proyecto

###  Compilación

```bash
javac *.java
```

###  Ejecución

```bash
java Main
```

---

##  Ejemplo de Ejecución

```text
Nombre jugador 1: Juan
Nombre jugador 2: Pedro

=== PELEA: Juan [Escudo] [Veneno] vs Pedro ===

Turno de Juan [Escudo] [Veneno] | HP def: 100
Juan ataca causando 25 pts.
[Veneno inflige 5 pts extra]
Pedro: 70 HP
...
>>> GANADOR: Juan <<<
```

---

##  Relación con el Taller

Este proyecto cumple con los requisitos del taller:

✔ Clase `Personaje` con los métodos requeridos
✔ Clase `JuegoLucha` con control del flujo
✔ Ataques aleatorios entre 10 y 30
✔ Sistema de turnos
✔ Determinación del ganador

🔹 **Mejora adicional:** Implementación del patrón Decorator para enriquecer la solución.

---

##  Posibles Mejoras

* Agregar nuevos poderes (fuego, curación, crítico)
* Implementar interfaz gráfica
* Añadir más tipos de personajes
* Guardar historial de combates

---

##  Autores

Anderson Garcia Amu - Ferney Mauricio Montes - Exenover Diaz

---


