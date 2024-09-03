///_____convinatoria
Funcion res <- convinatoria ( n,k )
	res = factorial(n)/(factorial(k) * factorial(n-k))
Fin Funcion
Funcion fac <- factorial ( num )
si num > 1 Entonces
	f = 1
	para i = 1 Hasta num
		f = f * i
	FinPara
	fac = f
SiNo
	si num ==1 o num == 0  Entonces
		fac = 1
	SiNo
		fac= -1 
	FinSi
FinSi
Fin Funcion


Algoritmo calcularconvinatoria
	Escribir "ingrese el valor de n"
	leer n
	si n >= 0 Entonces
		escribir " ingrese el valor de k"
		leer k 
		si k >= 0 y n >= k Entonces
			Escribir "la convinatoria de n-k ", convinatoria( n, k )
		SiNo
			Escribir "error el numero k debe ser mayor o igual a 0"
		FinSi
	SiNo
		
		Escribir "error el numero n debe ser mayor o igual a 0"
	FinSi
	
FinAlgoritmo

///_____pasal

Funcion res <- convinatoria ( n,k )
	res = factorial(n)/(factorial(k) * factorial(n-k))
Fin Funcion


Funcion fac <- factorial ( num )
	si num > 1 Entonces
		f = 1
		para i = 1 Hasta num
			f = f * i
		FinPara
		fac = f
	SiNo
		si num ==1 o num == 0  Entonces
			fac = 1
		SiNo
			fac= -1 
		FinSi
	FinSi
Fin Funcion

Algoritmo pascal
	Escribir "ingresar n valor"
	leer n 
	Para i<-1 Hasta n-1 Hacer
		Para j<- 0 Hasta i  Hacer
			Escribir Sin Saltar convinatoria ( i,j) " " 
		Fin Para
		
	Fin Para
	
FinAlgoritmo


_factorial 
Funcion fac <- factorial ( num )
	si num > 1 Entonces
		f = 1
		para i = 1 Hasta num
			f = f * i
		FinPara
		fac = f
	SiNo
		si num ==1 o num == 0  Entonces
			fac = 1
		SiNo
				fac= -1 
		FinSi
	FinSi
Fin Funcion

Algoritmo calcular
	Escribir "ingrese un numero" 
	leer num
	
	si num >= 0 Entonces
		Escribir "el factorial es",factorial(num)
	SiNo
		Escribir "error el numero debe ser mayor o igual a 0"
	FinSi
	
FinAlgoritmo


//---menu 

Funcion result<- divicionsobrando( num, num2 )
//	si num2 <> 0 Entonces
	result = num % num2
//	SiNo
//		result = 0 
//		Escribir 	"el segundo numero no puede ser 0"
//		
	//FinSi
	
Fin Funcion
Funcion result<- divicion( num, num2 )
//	si num2 <> 0 Entonces
		result = num / num2
//	SiNo
//		result = 0 
//		Escribir 	"el segundo numero no puede ser 0"
		
//FinSi
Fin Funcion
	
Funcion result<- multiplicacion( num, num2 )
	result = num * num2
Fin Funcion

Funcion result<- resta( num, num2 )
	result = num - num2
Fin Funcion

Funcion result<- suma( num, num2 )
	result = num + num2
Fin Funcion
	
Funcion menu
	escribir " **menu**"
	Escribir "1: sumar"
	Escribir "2 restar"
	Escribir "3 multiplicar"
	Escribir "4 dividir"
	Escribir "5 divicion con resta"
	Escribir "6 salir"
	Escribir ">> opcion"
FinFuncion
		

Funcion clarscreen
	para i<-1 Hasta 40 
		escribir""

	FinPara
Fin Funcion


Algoritmo calculadora
	Repetir
		Limpiar Pantalla
		menu
		leer opc
		Segun opc Hacer
			1:
				Limpiar Pantalla
				Escribir "sumar ----*"
				Escribir "ingrese el otro numero "
				leer num
				Escribir "ingrese el otro numero "
				leer num2
				Escribir suma(num,num2)
				Escribir "presione cualquier tecla para volver al menu"
				Esperar Tecla
			2: 
				Limpiar Pantalla
				Escribir "Resta ----*"
				Escribir "ingrese el otro numero "
				leer num
				Escribir "ingrese el otro numero "
				leer num2
				Escribir resta(num,num2)
				Escribir "presione cualquier tecla para volver al menu"
				Esperar Tecla
			3: 
				Limpiar Pantalla
				Escribir "Multiplicacion ----*"
				Escribir "ingrese el otro numero "
				leer num
				Escribir "ingrese el otro numero "
				leer num2
				Escribir multiplicacion(num,num2)
				Escribir "presione cualquier tecla para volver al menu"
				Esperar Tecla
			4:
				Limpiar Pantalla
				Escribir "divicion ----*"
				Escribir "ingrese el otro numero "
				leer num
				Escribir "ingrese el otro numero "
				leer num2
				Escribir divicion(num,num2)
				
				si num2 <> 0 Entonces
					Escribir "el resultado de la divicion es:", divicion(num,num2)
				sino 	
					Escribir "el error no se puede dividir en 0"
				FinSi
				Escribir "presione cualquier tecla para volver al menu"
				Esperar Tecla
			5: 
				Limpiar Pantalla
				Escribir "divivcion con sobrante ----*"
				Escribir "ingrese el otro numero "
				leer num
				Escribir "ingrese el otro numero "
				leer num2
				Escribir divicionsobrando(num,num2)
				si num2 <> 0 Entonces
					Escribir "el resultado de la divicion es:", divicionsobrando(num,num2)
				sino 	
					Escribir "el error no se puede dividir en 0"
				FinSi
				
				Escribir "presione cualquier tecla para volver al menu"
				Esperar Tecla
			6:
				Limpiar Pantalla
				Escribir "dejame descansar, gracias :3"
			De Otro Modo:
				Escribir "opccion invalida"
				Escribir "presione cualquier tecla para volver al menu"
				Esperar Tecla
		Fin Segun
		
	Hasta Que opc == 6
	

FinAlgoritmo
____________________for sumatoria de multiplos
for
Algoritmo sumatoria_de_0_a_30
	sum = 0
	Para i<- 0 Hasta 30 Con Paso 3 Hacer
		sum = sum + i
		
	Fin Para
	Escribir "la sumatroia de los multiplos de 3 es ", sum
FinAlgoritmo
___________________for serie de nuemros
Algoritmo numbers
	Para i<-2 Hasta 20 Con Paso 2 Hacer
		escribir i
	Fin Para
FinAlgoritmo
______________________--factorial de un numero
Funcion fac <- factorial(num)
	si num > 1 Entonces
		f = 1
		para i = 1 Hasta num
			f = f * i
		FinPara
		fac = f
	SiNo
		si num ==1 o num == 0  Entonces
			fac = 1
		SiNo
			fac= -1 
		FinSi
	FinSi
Fin Funcion
Algoritmo fact
	Escribir "ingrese el valor para hallar su factorial"
	leer num
	Escribir factorial(num)
	
FinAlgoritmo


_______________________--convinatoria 
Funcion fac <- factorial ( num )
	si num > 1 Entonces
		f = 1
		para i = 1 Hasta num
			f = f * i
		FinPara
		fac = f
	SiNo
		si num == 1 o num == 0 Entonces
			fac = 1
		SiNo
			fac = -1
		FinSi
	FinSi
Fin Funcion

funcion res <- combinatoria(n, k)
	res = factorial(n) / (factorial(k) * factorial(n-k))
FinFuncion

Algoritmo calcular_combinatoria
	Escribir "Ingrese el valor de n: "
	leer n
	
	si n >= 0 Entonces
		Escribir "Ingrese el valor de k: "
		leer k
		
		si k >= 0 y n >= k Entonces
			Escribir "C(",n, ", ",k, ") = ",combinatoria(n,k)
		SiNo
			Escribir ">> Error. El valor de k debe ser mayor o igual a cero."
		FinSi
	SiNo
		Escribir ">> Error. El valor de n debe ser mayor o igual a cero."
	FinSi
	
FinAlgoritmo
______________validar contraseña 


