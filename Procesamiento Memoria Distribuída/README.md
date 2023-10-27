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
- `utilities.c`: son esenciales para la gestión de memoria y la manipulación de campos de temperatura en el solucionador de la ecuación de calor,.



