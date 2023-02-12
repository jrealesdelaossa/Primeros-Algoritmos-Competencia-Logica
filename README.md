# Primer proyecto competencia Nuevas tecnologías, Vue.js

Proyecto personal para practicar desarrollo Frontend usando el Framework Vue.js en su versión 2

Para eso desarrolle los siguientes algoritmos en mi proyecto.
## Primer algoritmo

Escribir un algoritmo que realize la suma de dos números.

```
Algoritmo suma_de_dos_numeros
	Escribir "Digite dos números cualquiera.";
	leer num1;
	Leer num2;
	Escribir "El resultado de la suma es: ", num1 + num2;
FinAlgoritmo

```

## Segundo algoritmo

Se deben pedir dos números, se debe obtener la *multiplicación* de esos dos número, *menos* el primer número.

```
Algoritmo segundo_problema
	Escribir "Digite el primer número";
	leer num1;
	Escribir "Digite el primer número";
	Leer num2;
	Escribir "El resultado de la suma es: ", (num1 * num2) - num1;
FinAlgoritmo

```

## Tercer algoritmo

En un cine *x* solo pueden entrar personas mayores de edad, si es mayor de edad mostrar *Usted puede entrar al cine* si no *Usted no puede entrar al cine*.

```
Algoritmo problema_cine
	Escribir "Digite su edad:";
	Leer age;
	
	Si age >= 18 Entonces
		Escribir "Usted puede entrar al cine";
	SiNo
		Escribir "Usted no puede entrar al cine";
	Fin Si
FinAlgoritmo
```

## Cuarto algoritmo

Solicitar tres números *diferentes* y mostrar cual número es el mayor.

Posibles casos:

| num1 | num2 | num3 | 
|:----:|:----:|:----:|
|  5   |  2   |  1   |
|  2   |  5   |  1   |
|  1   |  4   |  5   |


```
Algoritmo numero_mayor
	Escribir "--- DIGITE NÚMEROS DIFERENTES ---"
	Escribir "Digite primer número:";
	Leer num1;
	Escribir "Digite segundo número:";
	Leer num2;
	Escribir "Digite tercer número:";
	Leer num3;
	
	Si num1 > num2 Entonces
		si num1 > num3 Entonces
			Escribir "El numero mayor es: ", num1;
		SiNo
			Escribir "El número mayor es; ", num3;
		FinSi
	SiNo
		si num2 > num3 Entonces
			Escribir "El número mayor es: ", num2;
		SiNo
			Escribir "El número mayor es: ", num3
		FinSi
	Fin Si
FinAlgoritmo

```

### Quinto algoritmo

Dado una hora en formato *23*, unos minutos *60*, determinar cuantos segundos hay.

```
Algoritmo determinar_segundos
	Escribir "Digite la hora";
	Leer hora;
	Escribir "Digite los minutos";
	Leer min;
	
	seg <- ((hora * 60) * 60) + (min * 60);
	
	Escribir "Los segundos totales son: ", seg;
FinAlgoritmo

```

### Sexto algoritmo

Dada _n_ cantidad de horas, retornar los segundos totales.

```:Arreglar
Algoritmo determinar_segundos
    Escribir "Para terminar el programa digite 0";
    Escribir "Digite la hora";
    Leer hora;
    Sumador <- hora;
    
    Mientras hora <> 0 Hacer
        Escribir "Digite la hora";
        Leer hora;
		Sumador <- Sumador + hora;
        Escribir Sumador;
    FinMientras
     
    
    seg <- (Sumador * 60) * 60;
    Escribir "Los segundos totales son: ", seg;
FinAlgoritmo

```
