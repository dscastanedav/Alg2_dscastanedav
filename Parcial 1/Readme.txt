Jhon Eduar Santofimio Medina  |  Alejandro Ramos Pérez  |  Nicolas La Rotta Mosquera  |  David Santiago Castañeda Vargas


Algoritmo que calcule la multiplicación de dos números enteros implementando el método “La russe”:

	- No acepta números enteros de tamaño mayor a 5.
	- No debe aceptar números negativos.




a = int(input("ingrese su primer numero")) ------------------------ O(1)
b = int(input("ingrese su segundo numero")) ----------------------- O(1)
respuesta = 0     ------------------------------------------------- O(1)
longcheck = 0     ------------------------------------------------- O(1)


if (len(str(a)) <= 5 and len(str(b)) <= 5 and a>0 and b>0):  ------ O(1)
  longcheck = 1   ------------------------------------------------- O(1)        
  print ("longitud valida")   ------------------------------------- O(1)
else:      -------------------------------------------------------- O(1)
  longcheck = 0 --------------------------------------------------- O(1)


def laRusse(a, b, respuesta):
  while (longcheck == 1): ----------------------------------------- O(log(longcheck))
    if (b%2 != 0):        ----------------------------------------- O(1)
      respuesta = respuesta + a  ---------------------------------- O(1)
      a = a*2             ----------------------------------------- O(1)
      b = b//2            ----------------------------------------- O(1)
    if (b%2 == 0):        ----------------------------------------- O(1)
      a = a*2             ----------------------------------------- O(1)
      b = b//2            ----------------------------------------- O(1)
    if (b != 0):          ----------------------------------------- O(1)
      return laRusse(a, b, respuesta) ----------------------------- O(1)
    return respuesta ---------------------------------------------- O(1)

Calculo de complejidad del tiempo: 

O(n)=+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(log(n))*[O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)] = O(log(longcheck))


Algoritmo que calcule el número de la serie Fibonacci:

	- Tamaño máximo aceptado  n <= 100.
	




a = int(input('¿Cuántos numeros desea en su secuencia?'))   -------- O(1)


def secuenciaFibonacci(n):
    a, b = 0, 1     ------------------------------------------------ O(1)
    for i in range(n): --------------------------------------------- O(n)
        yield a  --------------------------------------------------- O(1)
        a, b = b, a + b -------------------------------------------- O(1)


if a<=100 and a>=0: ------------------------------------------------ O(1)
    print(list(secuenciaFibonacci(a))) ----------------------------- O(1)
else:  ------------------------------------------------------------- O(1)
    print("Solo se puede imprimir entre los primeros 100 números de la serie") ---------------- O(1)
    print("Ejecute de nuevo el código y asegurese que su número sea menor o igual a '100'") ------ O(1)

O(n)= O(1)+O(1)+O(n)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)= O(n)