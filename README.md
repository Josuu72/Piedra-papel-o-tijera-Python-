# Piedra-papel-o-tijera-Python-
Juego clásico y simple "piedra, papel o tijera" contra un oponente con 3 oportunidades de intentos durante la partida.-

El objetivo de por qué hice este primer proyecto es para ejercitar la lógica de la programación.

```# ¡Piedra, papel o tijera! (finalizado en 🗓️ 20/08/2026) - Proyecto 01

import random

# Datos característico
vida_jugador = 3
vida_oponente = 3

# Datos de las listas
opciones = ["piedra", "papel", "tijera"]

# Intro de bienvenida (ignorar) ///
print("\n¡Bienvenido!, tienen 3 oportunidades para enfrentarse.")

# Definiendo Terminado al finalizar la partida
def Terminado(v_jugador, v_oponente):
    # Si tal jugador conquistó contra su rival/oponente:
    if v_jugador > v_oponente:
        print("\n¡Has ganado en esta partida, felicidades!")
    else:
        print("\nHas perdido... suerte para la próxima partida.")

# Mientras que la vida del jugador y/u oponente sean mayor a 0
while (vida_jugador > 0 and vida_oponente > 0):
    eleccion_jugador = input("\n¿Piedra, papel o tijera?: ").lower()

    # Cancelar las otras rutas de códigos en caso de error
    if eleccion_jugador not in opciones:
        print("❌ ERROR - respuesta no válida.\n\n   -----\n")
        continue

    eleccion_oponente = random.choice(opciones)
    print(f"> El oponente eligió: {eleccion_oponente}\n")

    if eleccion_jugador == eleccion_oponente:
        print(f"🟡 Eligieron {eleccion_oponente}, así que, es empate.")

    elif eleccion_jugador == "piedra" and eleccion_oponente == "tijera":
        vida_oponente -= 1
        print(f"🟢 Al oponente le queda {vida_oponente} de vida.")
    elif eleccion_jugador == "papel" and eleccion_oponente == "piedra":
        vida_oponente -= 1
        print(f"🟢 Al oponente le queda {vida_oponente} de vida.")
    elif eleccion_jugador == "tijera" and eleccion_oponente == "papel":
        vida_oponente -= 1
        print(f"🟢 Al oponente le queda {vida_oponente} de vida.")

    else:
        vida_jugador -= 1
        print(f"🔴 Te queda {vida_jugador} de vida.")

Terminado(vida_jugador, vida_oponente)```
