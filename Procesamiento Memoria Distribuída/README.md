# Ecuación de calor bidimensional en mpi con C

En este proyecto se trabajará con la solución de un programa en C que involucra la Ecuación del Calor en un dominio 2D.
para esto se utiliza la programación paralela MPI. 
todos los códigos fueron proporcionados en un repositorio por el docente.

## Códigos contenidos en el repositorio

En el repositorio podemos encontrar varios archivos y son los siguientes:

- `core.c`: este código se ocupa de la comunicación entre procesos MPI, y luego utiliza el método de diferencia finita para calcular la evolución de la temperatura.
- `heat.h`: Este archivo es esencial para organizar y definir las estructuras de datos y funciones necesarias para implementar la solución de la ecuación de calor bidimensional con MPI.
- `io.c`:  permiten la inicialización, visualización y recuperación de datos, así como la capacidad de continuar una simulación desde un punto de control.
- `main.c`: Tiene la lógica principal para la simulación del solucionador de la ecuación de calor en 2D, incluyendo la paralelización MPI, la administración de campos de temperatura y la generación de salidas visuales.
- `pngwriter.c` y `pngwriter.h`: este código está diseñado para tomar un conjunto de datos bidimensionales que representan temperaturas y convertirlos en una imagen PNG.
- `setup.c`: es esencial para la inicialización y configuración de la simulación del solucionador de la ecuación de calor, incluyendo la generación de datos iniciales, la gestión de la comunicación entre procesadores y la definición de las dimensiones del campo de temperatura.
- `utilities.c`: son esenciales para la gestión de memoria y la manipulación de campos de temperatura en el solucionador de la ecuación de calor.

RECORDAR QUE EL CÓDIGO PRINCIPAL ES `main.c`

## CÓDIGO MAIN

El archivo "main.c" contiene la función principal que controla la simulación del solucionador de la ecuación de calor en 2D. Comienza definiendo variables esenciales, como la constante de difusión, campos para la temperatura actual y previa, pasos de tiempo, intervalos de salida y la información de paralelización MPI. Luego, inicializa el entorno MPI y configura los campos de temperatura iniciales. Durante la simulación, calcula pasos de tiempo, realiza iteraciones para actualizar la temperatura en el dominio y gestiona la salida de imágenes y puntos de control. Finalmente, calcula el tiempo de ejecución, muestra resultados y libera la memoria utilizada antes de cerrar MPI. Este archivo abarca la lógica central para la simulación de la ecuación de calor 2D, incluyendo paralelización, campos de temperatura y generación de resultados visuales.

## Información hacerca del entorno
### Entrar 
Para poder entrar en necesario la siguiente linea: srun -n 24 --pty /bin/bash
### Cargar Módulos
La carga de los modulos se realiza mediante: module load devtools/mpi/openmpi/3.1.4
### Limpiar
Previamente a la ejecución es necesario realizar una limpieza para esto usamos: make clean
### Copilar
Por último para copilar se ejecuta: make

## Trabajo
Teniendo claro los conceptos y lineas de código anteriores se realizará el trabajo el cual está dividido en dos partes una primera que será una ejecución en modo interactivo, la segunda parte será en modo pasivo.

### Modo Ejecución Interactivo
para esta ejecución se tomarán los siguientes comandos:
* mpirun -np X ./heat_mpi  --> valores predeterminados
* mpirun -np X ./heat_mpi botella.dat --> desde un campo inicial en este caso botella.dat
* mpirun -np X ./heat_mpi botella.dat 1000 --> igual que el anterior pero agregando pasos de tiempo (1000)
* mpirun -np X ./heat_mpi 800 800 1000 --> acá se agregan dimensiones A, H (800,8000) y pasos de tiempo (1000)

en mi caso x tomará el valor de 4

### Modo Ejecución Pasiva

* Es necesario crear un archivo de scrip ejecutable.sh :
    
![ejecutable](https://github.com/SC3UIS/IntroPP2161594/assets/117324114/1b9312dc-005c-4cd6-a6d9-5ad1ed9bb06a)

y en consola se ejecuta con: sbatch ejecutable.sh

## Resultados

* Prueba 1 
![imagen_1](https://github.com/SC3UIS/IntroPP2161594/assets/117324114/ad4ac99f-ed5c-45a6-93d1-963988a40d97)

* Prueba 2
![imagen_2](https://github.com/SC3UIS/IntroPP2161594/assets/117324114/d9c85b75-f2d0-4674-806b-bcd31f122eb4)

* Prueba 3
![imagen_3](https://github.com/SC3UIS/IntroPP2161594/assets/117324114/abebe765-069d-4a40-b78a-0d7657306ccb)

* Prueba 4
![imagen_4](https://github.com/SC3UIS/IntroPP2161594/assets/117324114/0e5d4c52-4c62-4db3-9d0b-dfadfc12e170)




