# taller 1 Evaluación Curso de Introducción al Procesamiento en Paralelo 

Maximiliano Correa Pico - 2161594

# introducción 

La sucesión de Fibonacci es un concepto fundamental en matemáticas que ha inspirado una variedad de aplicaciones y representaciones visuales en el mundo de la geometría y la programación. Esta sucesión, que comienza con los números 0 y 1, se caracteriza por su propiedad única en la que cada término es la suma de los dos anteriores. Esta relación de recurrencia da lugar a una secuencia infinita de números naturales: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34 y así sucesivamente.

En este taller, nos enfocaremos en un aspecto práctico de la sucesión de Fibonacci. Proponemos la creación de un programa en lenguaje C que calcule la suma de los números de Fibonacci en índices pares de hasta N términos de la sucesión. Para abordar este desafío, proporcionaremos dos soluciones: una solución secuencial y otra solución paralela utilizando OpenMP (Open Multi-Processing). Esta última permitirá aprovechar al máximo los recursos de procesamiento disponibles y acelerar el cálculo de la suma de manera eficiente.

# Implementación

1) Solución Secuencial.

![image](https://github.com/Maxito06/IntroPP2161594/assets/117324114/51d4f020-3102-413a-a535-45b4ed874482)

2) Solución Paralela con OMP.

![image](https://github.com/Maxito06/IntroPP2161594/assets/117324114/0ddec32a-3898-47c9-8c9a-ae96bf283d7b)

# Conclusiones

* Rendimiento: De acuerdo a la teoría y las pruebas se puede concluir que la solución paralela toma la delantera, especialmente cuando se cuenta con un valor N grande. Esto se debe al aprovechamiento eficaz de los recusrsos de procesamiento disponibles para el aceleramiento de la ejcución de tareas.

* Escalabilidad: Se puede observar una clara diferencia en el tiempo de ejución, en especial una vez más en el momento en el que N se hace más grande, ya que en situaciones así la respuesta paralela y su alta escalabilidad se convierten en una clara opción para la reducción de tiempo de procesamiento.

* Overhead de paralelismo: Aunque la solución paralela ofrece mejoras en el rendimiento, también puede introducir un cierto grado de overhead debido a la gestión de hilos y la coordinación entre ellos. Esto significa que para problemas pequeños o cálculos simples, la solución secuencial podría ser más eficiente debido al costo adicional asociado con el paralelismo.

* Consistencia de resultados: Es importante verificar que ambas versiones (secuencial y paralela) produzcan resultados consistentes. Si los resultados son consistentes, esto sugiere que la implementación paralela es correcta y que no se han introducido errores en el proceso de paralelización.

* Uso de recursos: La solución paralela utilizará más recursos del sistema, como CPU y memoria, en comparación con la versión secuencial. Esto es especialmente relevante en sistemas con recursos limitados, y es importante considerar el equilibrio entre el rendimiento mejorado y el uso de recursos adicionales.

* Optimización y paralelización selectiva: La práctica también destaca la importancia de identificar las partes críticas del código que se beneficiarán más de la paralelización. No todos los problemas son adecuados para la programación paralela, y es fundamental seleccionar las secciones del código que justifiquen la introducción de paralelismo.


