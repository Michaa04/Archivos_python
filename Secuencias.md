def ingresar_dato(mensaje):
    """"permite el ingreso de un dato y valida si es numerico"""
    while True:
        numero = input(mensaje)
        try:    
            numero = int(numero)
            break
        except:
            print("Tipo de datos incorrectos")
            continue
    return numero
def mostrar_secuencia(dato):
    for iterador in dato:
        print (iterador)
    return 

#Cuerpo principal del programa
valor_inicial = ingresar_dato("Ingrese el valor numerico inicial: ")
valor_final = ingresar_dato("Ingrese el valor numerico final: ")
salto         = ingresar_dato("Ingrese el salto: ")
secuencia = range(valor_inicial, valor_final, salto)
mostrar_secuencia(secuencia)
archivo = open("Secuencia.txt", "x") 
for valor in secuencia:
    archivo.write(secuencia)
archivo.close()
