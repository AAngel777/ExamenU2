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
_ _ ---CAPITULO 2--- _ _
	**¿Como se accede a memoria en ARM?**
En la arquitectura ARM los accesos a memoria se hacen mediante instrucciones
específicas ldr y str
	
	**¿Que es el direccionamiento inmediato?**
El operando fuente es una constante, formando parte de la instrucción.

	**¿Que es el direccionamiento inmediato con desplazamiento o rotacion?**
Es una variante del anterior en la cual se permiten operaciones intermedias sobre los registros.

	**¿Que es Direccionamiento a memoria, sin actualizar registro puntero?**
Es la forma más sencilla y admite 4 variantes. Después del acceso a memoria ningún registro implicado en el cálculo de la dirección se modifica.Simplemente añade (o sustrae) un valor inmediato al registro dado para calcular la dirección.

	**¿Que es Direccionamiento a memoria, actualizando registro puntero?**
En este modo de direccionamiento, el registro que genera la dirección se actualiza con la propia dirección. De esta forma podemos recorrer un array con un sólo registro
sin necesidad de hacer el incremento del puntero en una instrucción aparte.

	**¿Cuales son los tipos de datos basicos?**
.byte , .hword , .short , .word , .int ,.quad

	**¿Que espacio ocupa un puntero?**
Un puntero siempre ocupa 32 bits y contiene una dirección de memoria.

	**¿Donde se almacenan los vectores?**
Todos los elementos de un vector se almacenan en un único bloque de
memoria a partir de una dirección determinada. Los diferentes elementos se almacenan en posiciones consecutivas, de manera que el elemento i está entre los i-1 e
i+1. 
	**¿Donde se almacenan las matrices bidimensionales?**
Una matriz bidimensional de N×M elementos se almacena en un único bloque de memoria. Interpretaremos una matriz de N×M como una matriz con N filas de M elementos cada una. Si cada elemento de la matriz ocupa B bytes, la matriz ocupará un bloque de M ×N ×B bytes.
	
	**¿Método para determinar si una constante entra o no en una instrucción mov?**
Pasar la constante a binario y quitar los ceros de la izquierda y de la derecha y contar el número de bits resultante
	
**---CAPITULO 3---**
	¿Que es una pila?
Se denomina pila de programa a aquella zona de memoria, organizada de forma
LIFO (Last In, First Out)

	¿Que operaciones tiene asociadas la pila?
La pila tiene asociadas dos operaciones: push (meter un elemento en la pila) y
pop (sacar un elemento de la pila)

	¿Que funcion tiene el AAPCS (Procedure Call Standard for the ARM Architecture?
Si queremos interactuar con las librerías del sistema, tanto para llamar a funciones como para crear nuestras propias funciones y que éstas sean invocadas desde un lenguaje de alto nivel

	¿Para que se usa un .eq?
Para facilitar la legibilidad del código (asignandoo nombres  a variables locales)
	
---CAPITULO 4---
	¿Donde se encuentra la primera capa?
En la librería runtime que acompaña al ejecutable, la cual incluye sólamente el fragmento de código de la función que necesitemos, en este caso en printf.
	
	¿Donde se encuentra la segunda capa?
Desde que hacemos la llamada al sistema (System Call o Syscall) hasta que se produce la transferencia de datos al periférico, retornando desde la llamada al sistema y volviendo a la primera capa, que a su vez retornará el control a la llamada a librería que hicimos en nuestro programa inicialmente.

	¿Caracteristica de Bare Metal?
Sólo tenemos una sección de código (la sección .text), y no estamos obligados a crear la función main

	¿Como es el proceso de arranque de la Raspberry Pi?
	☸Cuando la encendemos, el núcleo ARM está desactivado. Lo primero que se activa es el núcleo GPU.
	☸El procesador GPU empieza a ejecutar la primera etapa del bootloader
	☸En la segunda etapa se activa la SDRAM y se carga la tercera parte del bootloader, cuyo código está repartido entre loader.bin (opcional) y start.elf
	☸En tercera y última etapa del bootloader se accede opcionalmente a dos archivos ASCII de configuración llamados config.txt y cmdline.txt. 
	
	¿Que es el GPIO?
Conjunto de señales mediante las cuales la CPU se comunica con
distintas partes de la Rasberry tanto internamente (audio analógico, tarjeta SD o
LEDs internos) como externamente a través de los conectores P1 y P5.
	
	¿¿Que direccion tienen en memoria los puertos del GPIO?
Toman como base la dirección 0x20200000

	¿Cuantos grupos fncionales tiene el puerto GPFSEL0?
Diez grupos funcionales llamados FSELx (del 0 al 9) de 3 bits cada uno, quedando los dos bits más altos sin usar

	¿Para que sirven los puertos GPEDSn?
Sirven para detectar qué pin ha provocado una interrupción en caso de usarlo como lectura.

	¿Para que sirven los puertos GPRENn?
Con estos puertos enmascaramos los pines que queremos que provoquen una interrupción en flanco de subida, esto es cuando hay una transición
de 0 a 1 en el pin de entrada.


	
</pre>


