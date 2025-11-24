---
tags: [unity, game]
---

# Bowling

Este script controla una bola de bolos en Unity mediante tres funciones principales. Define variables serializadas que permiten ajustar desde el Inspector la fuerza de lanzamiento, los límites laterales del área de juego, el incremento de movimiento y una referencia al componente Rigidbody. Al iniciar, el método Awake obtiene automáticamente el Rigidbody del objeto para manejar su física.

![Bowling Game](https://play.unity.com/_next/image?url=https%3A%2F%2Fplay.unity.com%2Fapi%2Fv1%2Ffiles%2Ffile%2F11a5cf40-e98d-4d4c-bae9-ce6cc9a2ab7f%2Fcontent&w=1080&q=75)

El método Bowl es responsable de lanzar la bola hacia adelante aplicando una fuerza instantánea mediante AddForce. Multiplica Vector3.forward por la fuerza configurada y usa ForceMode.Impulse para crear un empuje inmediato, simulando el lanzamiento característico del boliche. Este método registra la acción en la consola para propósitos de depuración.

Los métodos MoveLeft y MoveRight permiten posicionar lateralmente la bola antes del lanzamiento, verificando que no sobrepase las barreras definidas. Si la posición actual está dentro de los límites, incrementan o decrementan la posición en el eje X según el valor de moveIncrement. Estos métodos públicos están diseñados para ser invocados desde botones de interfaz o sistemas de input, permitiendo al jugador apuntar antes de ejecutar el lanzamiento.

Click [here](https://play.unity.com/en/games/ef6de1c6-631e-4d5b-ba3c-8a35bda1a41f/aprendiendo-c-para-unity-bolos) to play the game.
