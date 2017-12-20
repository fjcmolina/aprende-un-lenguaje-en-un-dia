## Aprende un lenguaje de programación en un día (ejercicio voluntario para subir nota).

## Introducción

Cuando te sacaste el carnet de conducir, aprendiste las normas de circulación así como los fundamentos básicos para manejar un coche: volante, marchas, freno, acelerador, embrague, retrovisores... Seguramente, el coche que conduces ahora es diferente al que utilizaste para aprender a conducir, no obstante, lo puedes llevar sin problema. Cada coche tiene sus peculiaridades, pero quien sabe manejar un automóvil, puede adaptarse a las medidas, tacto y comportamiento de un vehículo en cuestión de horas.

Aprender a programar es como aprender a conducir. Si tienes una base sólida de programación y sabes manejar con soltura los tipos de datos, bucles, arrays, clases, métodos, etc. podrás pasar de un lenguaje a otro en un período relativamente corto, simplemente tendrás que adaptarte a la sintaxis y a las peculiaridades del nuevo lenguaje.

Con este ejercicio se pretende despertar el interés por otros lenguajes de programación distintos al que el alumno está estudiando como primer lenguaje.

Sigue los pasos que se indican a continuación.

## Creación del equipo

Este ejercicio se debe hacer en grupos de 3 alumnos. Uno de ellos será el representante del grupo.

## Forkea forkea

El representante del grupo debe hacer un *fork* de este repositorio para utilizarlo como base.

## Añadiendo colaboradores

El encargado del grupo deberá añadir como colaboradores del repositorio *forkeado* a los otros dos miembros, para trabajar todos sobre los mismos archivos. Cuando alguien es colaborador en un repositorio, puede hacer *push* a él sin necesidad de pedir permiso o hacer *pull request*.

Para añadir colaboradores hay que hacer click en la pestaña *Settings* y seleccionar luego *Collaborators* en el menú.

## Miembros del grupo

Escribe aquí los miembros del grupo. El primero es el representante o encargado.

* Francisco Jesús Caballero Molina
* Adán Estebanez Villarrubia
* Alejandro Puche Velasco

## Lenguaje de programación

El profesor llevará una cajita llena de papelitos con los nombres de distintos lenguajes de programación. Los encargados de cada grupo meterán la mano en la caja y sacarán dos papelitos, de los cuales el grupo elegirá uno. Se permite hacer intercambio de papelitos entre grupos.

Escribe el lenguaje de programación elegido por el grupo.

* TCL

Los papelitos se han recortado de este [documento](lenguajes_de_programacion.pdf).

## Información sobre el lenguaje

Es un lenguaje de script que aparecio en 1988 creado por John Ousterhout.
Este lenguaje se utiliza principalmente para el desarrollo rapido de prototipos, aplicaciones "script", interfaces graficas y pruebas.

Una de las características más usadas de Tcl es si en una aplicación requiere algo de funcionalidad no ofrecida por el Tcl estándar, los nuevos comandos de Tcl pueden ser implementados usando el lenguaje C. Tambien se caracteriza porque los daos son manejados como cadenas de caracteres Unicode.
## Herramientas de desarrollo

Para el desarrollo de los programas hemos usado eclipse que mediante la instalacion de un plugin solo necesitamos activar el interprete mediante un ejecutable que descargamos de [aqui.](https://www.activestate.com/activetcl/downloads/thank-you?dl=http://downloads.activestate.com/ActiveTcl/releases/8.6.7.0/ActiveTcl-8.6.7.0-MSWin32-x64-404764.exe)

Una vez activado solo tenemos que añadir el interprete tclsh en eclipse y esta listo para ejecutar el programa realizado.

## Poniendo en práctica el lenguaje

Pon en práctica el lenguaje de programación realizando los siguientes ejercicios. Para cada uno de los ejercicios, pega el código fuente de la solución y una captura de pantalla.

### 1. ¡Hola mundo!

Realiza un programa que muestre por pantalla la frase **¡Hola mundo!**.
```tcl
puts "Hola mundo"
```

### 2. Pirámide

Dada una altura introducida por el usuario, realiza un programa que pinte una pirámide a base de asteriscos con la altura indicada.
```tcl
puts "Introduce la altura: "
gets stdin alturaIntroducida
puts "Introduce el caracter: "
gets stdin caracter
set altura 1
set espacio [expr {($alturaIntroducida - 1)}]

while {$altura <= $alturaIntroducida} {
    for {set i 1} {$i <= ($espacio)} {incr i} {
	    puts -nonewline " "
	    
	    
	  }
	
    for {set i 1} {$i <= ($altura * 2) - 1} {incr i} { 
	    puts -nonewline $caracter
	  }
    puts " "
    incr altura
    incr espacio -1
}

```

### 3. Arrays y números aleatorios

Realiza un programa que rellene un array (o una estructura similar) con 20 números enteros aleatorios entre 1 y 100 y que seguidamente los muestre por pantalla. A continuación, se deben pasar los números primos a las primeras posiciones del array y los no primos a las posiciones restantes. Muestra finalmente el array resultado.
```tcl
array set numero {}
array set primo {}
array set noPrimo {}
set contadorPrimo 0
set contadorNoPrimo 0

for {set i 0}{$i < 10}{incr i}{
	puts "Introduce un numero: "
	gets stdin numero{i}
	set esPrimo false
	
	for{set j 2}{j < numero{}-1}{incr j}{
		if{{numero{i} % j} == 0}
		set esPrimo false
	}
	
	set esPrimo true
	if{$esPrimo}{
	 	primo{incr contadorPrimo}  numero{i}
	      }else{
		noPrimo{incr contadorNoPrimo}  numero{i}
	      }
for {set i 0}{$i < 10}{incr i}{
	puts numero{i}
}
for{set i 0}{i < $contadoPrimo}{incr i}{
	numero{i} noPrimo{$i -$contadorPrimo}
}
}
```

## Presentación de resultados

Cada equipo explicará al resto de la clase lo aprendido durante la realización del ejercicio. Todos los miembros de cada equipo deben participar en la explicación. Se puede utilizar como material de base para la presentación el repositorio de GitHub.

## Recompensa

* Todos los alumnos que realicen correctamente la actividad tendrán 0'25 puntos extra en la nota del trimestre.

* Los miembros del equipo más votado ganarán un premio.

:star: Si te ha gustado este ejercicio, dale una estrellita al [repositorio original](https://github.com/LuisJoseSanchez/aprende-un-lenguaje-en-un-dia).

