# Examen Unidad 2 
Preguntas y programa .s agrabado con asciinema
<pre>

	<p align=center>

Tecnológico Nacional de México
Instituto Tecnológico de Tijuana

Departamento de Sistemas y Computación
Ingeniería en Sistemas Computacionales

Semestre:
Agosto - Diciembre 2023

Materia:
Lenguajes de interfaz

Docente:
M.C. Rene Solis Reyes 

Unidad:
2

Título del trabajo:
EXAMEN DE ÚNICA OPORTUNIDAD 

Estudiante:
García Cerillo Angel Albino

	</p>
-----------------------------------------------------------------------------------------------------------------
---CAPITULO 2---
Preguntas
	Como se accede a memoria en ARM?
En la arquitectura ARM los accesos a memoria se hacen mediante instrucciones
específicas ldr y str

---CAPITULO 3---
	Que es una pila?
Se denomina pila de programa a aquella zona de memoria, organizada de forma
LIFO (Last In, First Out)

	Que operaciones tiene asociadas la pila?
La pila tiene asociadas dos operaciones: push (meter un elemento en la pila) y
pop (sacar un elemento de la pila)

	Que funcion tiene el AAPCS (Procedure Call Standard for the ARM Architecture?
Si queremos interactuar con las librerías del sistema, tanto para llamar a funciones como para crear nuestras propias funciones y que éstas sean invocadas desde un lenguaje de alto nivel

	Para que se usa un .eq?
Para facilitar la legibilidad del código (asignandoo nombres  a variables locales)
	
---CAPITULO 4---
	Donde se encuentra la primera capa?
En la librería runtime que acompaña al ejecutable, la cual incluye sólamente el fragmento de código de la función que necesitemos, en este caso en printf.
	
	Donde se encuentra la segunda capa?
Desde que hacemos la llamada al sistema (System Call o Syscall) hasta que se produce la transferencia de datos al periférico, retornando desde la llamada al sistema y volviendo a la primera capa, que a su vez retornará el control a la llamada a librería que hicimos en nuestro programa inicialmente.

	Caracteristica de Bare Metal?
Sólo tenemos una sección de código (la sección .text), y no estamos obligados a crear la función main

	Como es el proceso de arranque de la Raspberry Pi?
	☸Cuando la encendemos, el núcleo ARM está desactivado. Lo primero que se activa es el núcleo GPU.
	☸El procesador GPU empieza a ejecutar la primera etapa del bootloader
	☸En la segunda etapa se activa la SDRAM y se carga la tercera parte del bootloader, cuyo código está repartido entre loader.bin (opcional) y start.elf
	☸En tercera y última etapa del bootloader se accede opcionalmente a dos archivos ASCII de configuración llamados config.txt y cmdline.txt. 

</pre>


