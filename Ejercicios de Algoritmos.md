# Ejercicios de Algoritmos

1.  Hola Mundo

```
Algoritmo hola_mundo
	Escribir "Hola mundo"
FinAlgoritmo
```
Entrada: -    
Salida: Hola mundo

2.  A partir de un número ingresado diga si es mayor, menor o igual a 9.

```
Algoritmo MayoresIgualesMenoresA9 (INICIO)
	N<-0
	Escribir "Escribir el numero"
	Leer N
	Si N Es Igual A 9 Entonces
		Escribir "El numero es igual a 9"
	Si no
		Si N Es Mayor Que 9 Entonces
			Escribir "El numero es mayor a 9"
		Si no
			Escribir "El numero es menor a 9"
		Fin Si
	Fin Si
FinAlgoritmo (FIN)
```
Entrada: N      
Salidas: 3, Escribir...      
El paso 2 sirve para inicializar la variable N

![](img\alg1.PNG)

Comprobación:
N: 0     
Escribir: "Escribir el numero" (entonces escribimos un numero que elegimos, p.ej. el 5)   
N: 5         
saltamos paso 5 porque no cumple la condicion       
pasamos al paso 7        
pasamos al paso 8          
como no cumple la condicion, pasamos al 10.      cumple la condicion y se escribe "El numero es menor a 9"        
el paso 12 pone fin a lo que empieza en 8      
el paso 13 pone fin a lo que empieza en 5         
paso 14 pone fin al algoritmo completo



3.  A partir de un número ingresado diga si el mismo es par o impar.

```
Algoritmo ParidadNumeros
	Leer nro
	Si (nro mod 2) = 0 entonces
		Escribir "es par"
	Sino
		Escribir "es impar"
	Fin Si
FinAlgoritmo
```
las palabras reservadas del algortimo son: Leer, si, sino, Escribir, Fin Si, entonces, FinAlgoritmo, =

![](img\alg2.PNG)

Comprobacion:        
nro: 7         
mod: es el resto de la division. como el resto no es 0, no cumple la condicion y salta a la linea 5.
pasa a la 6 y escirbe 'es impar'          
linea 7 pone fin a lo que empieza en la linea3    
linea 8 pone fin al algoritmo

4.  ingresar dos números y devuelva el resultado de la suma entre ambos.

```
Algoritmo SumaDosNumeros
    Num1<-0
    Num2<-0
    Escribir "Escribir el numero 1"
    	Leer Num1
    Escribir "Escribir el numero 2"
    	Leer Num2
    	Rta<-Num1+Num2
    Escribir "El resultado es:" Rta
FinAlgoritmo
```
Comprobacion
num1: 0        
num2: 0        
aparece en pantalla: "Escribir el numero 1"     
linea 5-> num1: 3      
aparece en pantalla: "Escribir el numero 2"          
linea 7-> num2: 4      
linea 8-> se asigna a la variable Rta, la suma entre num1 y num2      
Rta: 7      
linea 9-> escribe: El resultado es 7       
linea 10 finaliza el algoritmo


5. Sumar todos los números pares entre 2 y 100.

```
Algoritmo SumaDePares
	suma <- 0
	nro <- 2
	Mientras nro<=100 hacer
		si nro mod 2 = 0 Entonces
			suma= suma+nro			
		FinSi
		nro=nro+1
	FinMientras
	Escribir "la suma de los pares entre 2 y 100 es " suma
FinAlgoritmo
```
![](img\alg3.PNG)
Prueba de escritorio     
linea 2-> sum:0         
linea 3-> nro: 2        
linea 4-> condicion, se repite el bucle mientras que nro sea menor o igual a 100        
linea 5-> si el resto de dividir el nro en 2 es 0 (es decir, si el numero es par)         
linea 6-> se suma el numero a la suma global. sum: 2         
linea 7-> fin de lo que empieza en 5         
linea 8 -> nro: 3        
linea 9-> como se sigue cumpliendo la condicion, vuelve a 4. se repite hasta que nro = 100. entonces se acaba el bucle y pasa a 10       
linea 10 -> escribe 'la suma de los pares entre 2 y 100 es ...'

Algoritmo mejorado

![](img\alg4.PNG)


6. Ingresar un número y muestre todos los divisores del mismo.

```
Algoritmo divisores_de_numero
	Escribir "Ingrese Numero"
	Leer Num
	div<-1
	Mientras Div<=Num Hacer
		Si Num MOD div = 0 
			Escribir div
		Fin Si
		div<-div+1
	Fin Mientras
FinAlgoritmo
```
![](img\alg5.PNG)
Comprobacion   
linea 2-> Ingrese Numero     
linea 3-> Num: 6    
linea 4-> div: 1    
linea 5-> cumple la condicion, asi que pasa a la 6     
linea 6-> condicion de ser divisor. se cumple, asi que se escribe el 1 (linea 7)        
linea 8-> div: 2. se vuelve a la linea 5 y se sigue cumpliendo la condicion. repetimos el proceso.    
el 2 es divisor (el resto de dividir 6 entre 2 es 0), por lo que se escribe. div pasa a ser 3 y se repite el bucle (div es menor a num:6). 3 tambien es divisor. tambien se escribe y pasa a 4. se repite el bucle por cumplir la condicion. Sin embargo, en este caso, el resto de dividir num:6 entre div:4, no es 0, por lo que no se escribe. SE suma 1 a div y pasa a ser 5. Se repite el bucle. 5 tampoco es divisor. No se escribe. div:6. SE repite el bucle. El resto es 0 y se escribe. div:7. Ya no cumple la condicion y se pasa a linea 10.      
linea 11-> fin algoritmo.     
Asi, quedarian escritos 1, 2, 3, 6





7. Determinar si un alumno aprueba o suspende un curso, sabiendo que aprobará si su promedio de tres calificaciones es mayor o igual a 4.0; supsende en caso contrario. Deberá permitir ingresar las tres calificaciones y luego calcular su promedio.

```
Algoritmo aprueba_reprueba //1
	Escribir "Ingrese calificacion 1" //2
		Leer Cal1 //3
	Escribir "Ingrese calificacion 2" //4
		Leer Cal2 //5
	Escribir "Ingrese calificacion 3" //6
		Leer Cal3 //7
	Prom<-(Cal1+Cal2+Cal3)/3  //8	                           
        Si Prom>=4 Entonces //9
		Escribir "Aprueba" //10
	Sino //11
		Escribir "Reprueba" //12
	Fin Si //13
	Escribir Prom //14
FinAlgoritmo //15
```

Comprobacion
linea 2-> Ingrese calificacion 1
linea 3-> Cal1: 5
linea 4-> Ingrese calificacion 2
linea 5-> Cal2: 3
linea 6-> Ingrese calificacion 3
linea 7-> Cal3: 2
linea 8-> Prom: 3.33
linea 9-> no cumple condicion, pasa a 11
linea 12-> Reprueba
linea 14-> 3.33
linea 15-> fin del algoritmo




8. Crear un algoritmo que permita ingresar un nombre y una cantidad numérica para escribir este nombre tantas veces como su cantidad ingresada. 

```
Algoritmo Cantidad_nombre
	Escribir "Ingresar Nombre"
	Leer nombre
	Escribir "Ingresar Cantidad"
	Leer num
	Mientras Num>0 Hacer
		Escribir nombre
	Num<-Num - 1
	Fin Mientras
FinAlgoritmo
```

9. Sumar todos los números naturales comprendidos entre 1 y 50.

```
Algoritmo suma_numerosnaturales_1y50 
	Num<-1
	Resul<-0
	Repetir
	    Resul<-Resul+Num
	    Num<-Num+1 	                           
        Hasta Que Num>50
	Escribir Resul
Fin algoritmo
```

10. Leer tres números; si el primero es negativo, debe imprimir la multiplicación de los tres y si no lo es, imprimirá la suma.

```
Algoritmo tresnumeros
	Escribir "Ingrese numero 1"
		Leer Num1
	Escribir "Ingrese numero 2"
		Leer Num2
	Escribir "Ingrese numero 3"
		Leer Num3
	Si Num1<0 Entonces
		Resul<-Num1 * Num2 * Num3
	Sino
		Resul<-Num1+Num2+Num3
	Fin Si
	Escribir Resul
FinAlgoritmo
```

11. Si un número ingresado es primo o no. (Un número es primo si es divisible únicamente por 1 y por sí mismo).

```
Algoritmo NumerosPrimos
	Escribir "Ingrese un número: "
	Leer nro
	div <- 2
	band <- Verdadero 	         
        Si nro=1 Entonces 		            
             Escribir "Es primo" 	         
        Sino 		             
             Mientras band=Verdadero y nro>div Hacer
		Si nro MOD div = 0 Entonces
		    band <- Falso
		FinSi
		    div <- div +1
	     FinMientras
	     si band= Verdadero Entonces
		Escribir "Es primo"
	     Sino
		Escribir "No es primo"
	     FinSi
	FinSi
FinAlgoritmo
```

12 . Sumar los dígitos de un número ingresado. Ejemplo: Si se ingresa 123, debería devolver 6.

```
Algoritmo SumaDigitos
	Escribir "Ingrese un nro: "
	Leer nro
	resul <- 0
	Mientras nro <> 0 Hacer
		resul <- resul + nro MOD 10
		nro <- trunc(nro/10)
	FinMientras
	Escribir "El resultado es: " resul
FinAlgoritmo
```

13. Ejercicios Propuestos
    1. Calcular y mostrar el cuadrado de los números del 1 a 30.
    2. Números primos
    3. Construir un avión de papel
    4. Realizar las cuatro operaciones básicas (Suma, Resta, Multiplicación, División)
    5. Volumen y Area de un Cilindro
    6. Pedir un libro en una biblioteca
    7. Encontrar el mayor número de tres números
    8. Factorial de cualquier número
    9. Encontrar si un numero en mayor o menor a un número dado.
    10. Adivinar una palabra.