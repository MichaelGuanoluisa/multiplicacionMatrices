# Multiplicación de Matrices
Multiplicación de matrices en python

Código realizado en python
Se acepta la longitud de las matrices, recibiendo los datos por teclados y de igual forma se ingresan los datos de las matrices por teclados.
Y al final se realiza el calculo correcto.

![Captura de pantalla (106)](https://user-images.githubusercontent.com/66236038/122299208-4ebebe00-cec3-11eb-9ddd-42b9b46f3a0f.png)


/* CÓDIGO */

def crearMatriz(n,m):
 matriz = []
 for i in range(n):
     a = [0]*m
     matriz.append(a)
 return matriz

print("MULTIPLICACION DE MATRICES")
n1=int(input("Ingrese el tamaño de la fila de la primera matriz: "))
m1=int(input("Ingrese el tamaño de la columna de la primera matriz: "))
matriz1 = crearMatriz(n1,m1)

for i in range(0,n1,1):
    for j in range(0,m1,1):
        matriz1[i][j]=int(input("ingrese el numero en la posicion ["+str(i)+"] ["+str(j)+"] : "))
        
print(matriz1)

n2=int(input("Ingrese el tamaño de la fila de la segunda matriz: "))
m2=int(input("Ingrese el tamaño de la columna de la segunda matriz: "))
matriz2 = crearMatriz(n2,m2)

for i in range(0,n2,1):
    for j in range(0,m2,1):
        matriz2[i][j]=int(input("ingrese el numero en la posicion ["+str(i)+"] ["+str(j)+"] : "))
        
print(matriz2)

matriz3 = crearMatriz(n1,m2)

#multiplicacion
for i in range(0,n1,1):
    for j in range(0,m2,1):
        for k in range(0,m1,1):
            matriz3[i][j] += matriz1[i][k] * matriz2[k][j]
            
print("La matriz resultante de la multiplicación de las dos matrices es la siguiente: ")
print(matriz3)
