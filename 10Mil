lista_nombres = []

def ingresar_nombres():
    seguir = "S"
    while seguir.upper() == "S":
        nombre = input('Ingrese un nombre: ')
        lista_nombres.append([nombre, 0])
        seguir = input("Desea agregar otro nombre? (S/N): ")
        if seguir.upper() == "N":
            break


def lista_top():
    lista_nombres.sort(key=lambda x: x[1], reverse=True)
    for i, jugador in enumerate(lista_nombres, start=1):
        print('Posicion {}: {}, con {} puntos.'.format(i, jugador[0], jugador[1]))


def sumar_puntos():
    turnos = 0
    while True:
        for nombres in lista_nombres:
            nombre = nombres[0]
            puntaje = nombres[1]

            suma = int(input('Ingrese el puntaje obtenido: '))
            puntaje += suma
            nombres[1] = puntaje

            print('El jugador: {}, tiene {} puntos. '.format(nombre, puntaje))

            if puntaje == 10000:
                print("El jugador {} gano!".format(nombre))
                return

        turnos += 1
        if turnos == 5:
            print('Top: ')
            lista_top()
            turnos = 0



if __name__ == '__main__':
    print('Bienvenido al 10000.')
    ingresar_nombres()
    sumar_puntos()
    print('Puntaje final: ')
    lista_top()
