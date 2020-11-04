## TP 6 Inferencias Evolutivas

#### RETO I: Detalla las tácticas y/o metodologías que deberían utilizarse para darles una respuesta a los padres del niño.

#### a) Dadas las secuencias de Mosca, humano y Moscahumano ¿Qué criterios se les ocurren para comparar las secuencias? ¿Qué resultados obtienen del análisis anterior?

Viendo los alineamientos de los 3 en Clustal, observamos que los tres comparten la mayoría de los elementos y esto es todavía mayor si comparamos solamente al humano y a bart mosca. Podríamos decir que bartmosca conserva mas del humano que de la mosca.

#### b) ¿Qué resultado esperaría obtener si utilizara el resto de las secuencias en el análisis? ¿Por qué?

Si se utilizan muchas secuencias de una misma especie, se puede generar un sesgo, y el resultado se vea más inclinado hacia dicha especie. Lo ideal sería tener una cantidad de secuencias parecidas entre diferentes especies.

#### RETO II: Mediante el uso del servidor de ​IQtree ​(Trifinopoulos et al. 2016)​, confecciona los árboles filogenéticos para los alineamientos obtenidos en el punto II.

#### a) Como vemos, el servidor nos permite elegir el modelo de sustitución ¿A qué se refiere?

Nos permite elegir la forma en la que se producen las sustituciones entre las secuencias a fin de "corregir" la distancia entre ellas y estimar el numero de sustituciones. Elegir un modelo lo mas cercano al verdadero comportamiento de la evolución de las secuencias es la clave para construir un buen árbol filogenético.


##### b) ¿Qué es el Bootstrap? ¿De qué manera nos habla de la calidad de nuestro árbol? ¿Cómo influye el número de Bootstraps en el resultado?

Bootstrap es un método para inferir que tan fiable es nuestro árbol. El bootstrap value nos muestra que tantas veces pudimos observar la misma rama del arbol al realizar la reconstrucción filogenética.

##### c) Interpreten los resultados obtenidos, mediante la visualización de los árboles con la herramienta ​FigTree​. ¿Es necesario realizar algún paso extra, previo a la interpretación del árbol? ¿Por qué?

Es necesario alinear las secuencias antes de generar el árbol filogenético para reconstruirlo correctamente.

`NP_061820.1_cytochrome_c_[Homo_sapiens]` es el ancestro mas cercano a `bartmosca` porque están en el mismo nivel en el árbol.
