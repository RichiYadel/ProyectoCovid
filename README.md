Matemáticas para entender la pandemia

Objetivos.
El objetivo de este proyecto es implementar la solución numérica del modelo epidemiológico SIR. La solución que se implementa tiene como partida los datos reales que se recopilaron y se mostraron como públicos sobre el número de contagios registrados por día. El resultado nos mostrará la tendencia inicial de cada "ola de contagio" que se vivió. La tendencia inicial se puede contrastar con el comportamiento real de los datos y evaluar la efectividad de las medidas por parte del gobierno para mitigar los efectos del COVID-19. 

Problema que resuelve:
El desarrollo de las enfermedades es un asunto de importancia capital para los gobiernos de todo el mundo. Entender la dispersión y comportamiento de una enfermedad nos permite ser previsores y tomar decisiones estratégicas para afrontar cuestiones de salud pública. En los años recientes, el mundo entero se conmocionó ante la aparición del COVID-19. Para afrontar y entender el desarrollo de la pandemia se recurrió a los modelos matemáticos para predecir su comportamiento.

Uno de los modelos matemáticos más sencillos para predecir el desarrollo de una enfermedad los encontramos en el modelo SIR. Las siglas SIR hacen referencia a los tres grandes grupos en los que se divide la población para desarrollar el modelo. Estos grupos son:

•	S(t): Número de individuos susceptibles de enfermarse en el tiempo t 
•	I(t): Número de individuos infectados en el tiempo t 
•	R(t): Número de individuos removidos de las categorías S e I.

El modelo SIR, a pesar de su sencillez, tiene gran potencial predictivo y es eficaz en la descripción de la dinámica de la dispersión en enfermedades infecciosas. Debido a su sencillez, resulta altamente atractivo como recurso educativo.

El modelo SIR consiste de un sistema de tres ecuaciones diferenciales no lineal donde las primeras dos están acopladas.

S^\prime=-\beta SI
I^\prime=\beta SI-\gamma I
R^\prime=-\gamma I

Para resolver el sistema se echa mano de los métodos numéricos de soluciones de ecuaciones diferenciales. Utilizando el método “Forward Euler” podemos construir el siguiente sistema de ecuaciones en diferencias.

S^{n+1}=-\beta hS^nI^n+S^n
I^{n+1}=\beta hS^nI^n-\gamma hI^n+I^n
R^{n+1}=\gamma hI^n+R^n

Las ecuaciones en diferencias resultantes son un caso particular de sucesiones recursivas. Debido a que las sucesiones son objetos matemáticos que se trabajan en la primera Unidad de Cálculo Diferencial e Integral I, podemos llevar este modelo al aula.


Lenguajes utilizados y argumentación sobre la utilización de este lenguaje:
El lenguaje en el que se realizó la progrmación fue en el lenguaje Python por su versatilidad y conveniencia para desarrollar cómputo científico


Descripción de lo que está simulando, analizando o demostrando.
Para construir las soluciones del modelo SIR con base en el sistema de ecuaciones en diferencias resultante al implementar el método “Forward Euler” se deben resolver una serie de problemas asociados.

En primer lugar, necesitamos determinar las constantes \beta y \gamma. Para determinar las constantes es necesario recurrir a los datos reales que se recopilaron durante la pandemia. Las constantes \beta y \gamma dependen del tipo de enfermedad con la que se trabaje. Sin embargo, debido a las medidas que se implementaron para atenuar los efectos en la población del COVID-19, se espera que los valores de \beta y \gamma cambien en cada etapa que se desee analizar.

Un segundo problema consiste en decidir el punto de partida o las “condiciones iniciales” que se deben utilizar. También se debe decidir un “tamaño de salto h adecuado”. Una vez teniendo en cuenta las condiciones iniciales y las constantes a utilizar en el modelo, se debe implementar en la computadora un bucle con el número de iteraciones necesarias para construir una aproximación adecuada a la solución. La información obtenida nos debe permitir realizar una gráfica para analizar los resultados. 

Para determinar las contantes \beta y \gamma se necesita tener acceso a los datos del COVID-19. Los datos del COVID-19 son datos abiertos y se pueden consultar en internet. Una vez teniendo los datos se podría calcular las constantes para un tiempo de partida que se desee analizar o se podría construir una función que actualice los valores de las constantes para cada etapa.

Las condiciones iniciales se deben tomar al inicio de un “pico de contagio”. Las predicciones importantes durante la pandemia fueron para identificar y medir la magnitud de los picos de contagio para construir estrategias para atenuar su crecimiento.

El tamaño de salto se debe tomar como una unidad de medida del tiempo, dependiendo de la unidad temporal que se decida analizar. Finalmente, para implementar la simulación se necesita construir un bucle con una instrucción “while” o “for” para iterar y obtener una cantidad de resultados adecuada.

S[n+1] = S[n] - h*beta*S[n]*I[n] 
I[n+1] = I[n] + h*beta*S[n]*I[n] - h*gamma*I[n] 
R[n+1] = R[n] + h*gamma*I[n] 
Los resultados se almacenarán en listas y finalmente se graficarán.


Ejemplo básico de funcionamiento general. Instrucciones de ejecución y uso
Al correr el programa, se toman datos de los primeros días que precedieron a una ola de contagio. Con base en esos datos se pueden calcular los parametros beta y gamma presentes en el modelo. Posteriormente se va calculando poco a poco para cada punto en el dominio el valor de las tres funciones implicadas S,I y R. Finalmente graficamos y observamos que la curva de S es decreciente, la curva de I sube y luego baja creando un pico y la curva de R es ceciente y asintótica.

Tema que ayuda a comprender:
El tema que ayuda a comprender el proyecto es el de "Procesos infinitos" comprendido en la Unidad 1 del programa de estudios de Cálculo Diferencial e Integral 1 oficial del Colegio de Ciencias y Humanidades de la UNAM.

Justificación de cómo ayuda al alumno a comprender el tema.
El estudio de los procesos infinitos se realiza construyendo ejemplos que avanzan paso a paso formando secuencias de números. El proyecto que se propone desarrolla un ejemplo de una secuencia que tiene aplicaciones pácticas y muy importantes. Más aún, la cercanía en el tiempo con la pandemia lo vuelve sumamente interesante y motivador en el aula.

