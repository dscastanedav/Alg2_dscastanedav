David Santiago Castañeda Venegas
Alejandro Ramos Perez
Jhon Eduar Santofimio
Nicolás La Rotta Mosquera

Este programa es un algoritmo que se encarga de encontrar una subsecuencia llamada target en una cadena protéica llamada secuence.
Se trata de una simulación sobre cómo funciona el proceso para la detección del covid-19 en pacientes. 

j=0    --------------------------------------------------------------- O(1)
posicion = 0   ------------------------------------------------------- O(1)     
for i in range(len(secuence)):  -------------------------------------- O(N) 
  if j < len(target):   ---------------------------------------------- O(1)
    if secuence[i] == target[j]:  ------------------------------------ O(1)
      posicion=i     ------------------------------------------------- O(1)
      j=j+1    ------------------------------------------------------- O(1)
      if(j == len(target)): ------------------------------------------ O(1)
        print(posicion-len(target)+1,"termina en ",posicion+1) ------- O(1)
    else: ------------------------------------------------------------ O(1)
      j=0  ----------------------------------------------------------- O(1)
      posicion=0 ----------------------------------------------------- O(1)

O(1)+O(1)+O(N)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1) = O(N)