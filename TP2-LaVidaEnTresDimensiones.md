
## TP2 - La vida en tres dimensiones

#### ¿Por qué una célula querría destruir sus propias proteínas?

La célula busca degradar sus propias proteína para liberar los aminoácidos que la componen. Estos se utilizarán para formar otras proteínas o generar energía.

#### ¿Qué información nos provee esta página?

La pagina nos muestra información sobre la estructura tridimensional de las proteínas y los resultados de las investigaciones realizadas. Se incluye su clasificación,una vista en 3D de la estructura, la fecha de publicación, el autor,  etc.
#### ¿Cómo se determinó la estructura de esta proteína?

Se determinó mediante el método de difracción de rayos X.

#### A la izquierda vemos una representación de la estructura de ubiquitina. ¿Qué significan las cintas, las flechas y las regiones angostas?

Representan los distintos tipos de segunda estructuras

#### ¿Representa esa imagen a la realidad del sistema biológico?

No, ya que la proteína está en constante movimiento, y en la imagen no permite ver el mismo.

#### La estructura 1UBQ fue “refinada a una resolución de 1.8 Angstroms”. Éste es el error asociado al experimento: mientras mayor es la resolución, menor es la certeza al determinar la posición de cada átomo. ¿Cuál es la utilidad y los condicionamientos de usar un modelo científico que sabemos inexacto?

En este caso, tener una resolución más alta no sirve de nada porque permite determinar que las dos estructuras son diferentes. Con una resolución más alta, ni el cambio ni la distancia mínima son "obvios", y la resolución más baja hace que sea más fácil notar estas distancias. En la actualidad, es una de las mejores herramientas para este tipo de investigación hasta el momento, además, la información que puede extraer es suficiente para representar cómo se forma la proteína en cuestión y tiene suficiente información para realizar predicciones.

## 3D View

#### En la pantalla principal vemos una representación de la estructura de ubiquitina. ¿Qué significan las cintas, las flechas y las regiones angostas?

Representan las cadenas, combinación, rotaciones y traducciones necesarias para formar la representación biológica completa de la macromolécula.

#### ¿Qué diferencias y similitudes notamos respecto de la representación inicial?

Permite explorar desde otros ángulos la estructura, ver la estructura primaria 

#### ¿Podríamos extraer de este archivo información sobre la estructura primaria de la proteína en cuestión? ¿Cómo se presenta dicha información y qué significa la representación? Desde el punto de vista computacional:¿de qué tipo de dato se trata esta información?

Si, los valores SEQRES listan los aminoácidos unidos de formar lineal. La información se presenta de la siguiente manera:

> SEQRES 1 A 76 MET GLN ILE PHE VAL LYS THR LEU THR GLY LYS THR ILE

Siendo 1 el número de la cadena y A el identificador.

Esto se puede representar como un String (Cadena de caracteres) o un Array.

#### ¿Considera que el formato PDB es útil para presentar los resultados del experimento?

Si, ya que se trata de un archivo completo, esta vista nos permite rotar la macromolécula, ver distintas representaciones y los distintos aminoácidos que la componen.

#### En el menú de la izquierda hay opciones de distintos tipos de representación y formas de colorear la estructura tridimensional. ¿Para qué podría ser útil visualizar lo mismo de distintas maneras?

El coloreo es útil porque nos permite analizar la composición en base a distintos criterios: propiedades de los residuos, átomos, o cadenas hasta características como la simetría.

## PDB Format

#### ¿Qué información esperaría encontrar como resultado un experimento destinado a determinar la estructura terciaria de una molécula biológica?

Encontrar que átomos componen a la molécula y de qué forma están unidos entre si.

#### Podemos explorar el contenido del archivo que acabamos de descargar si lo observamos con un editor de texto. Haciendo clic con el botón derecho del mouse sobre el archivo descargado, usemos la opción ​Abrir con y seleccionemos el ​Bloc de Notas u otro editor de texto. ¿En qué consiste un archivo PDB?

El archivo PDB contiene la información necesaria para describir la estructura tridimensional de una molécula. Se incluye la descripción de la proteína y las estructuras de los ácidos nucleicos que incluyen las coordenadas atómicas, estructura secundaria y conectividad atómica.

#### Desplacémonos por el archivo hasta encontrar las líneas que comienzan con la palabra ATOM. ¿Qué tipo de información brinda esta sección?


La posición del átomo anterior se puede ver en el título "ATOM", que muestra el eje de coordenadas. Sus columnas muestra el número de átomos, el átomo en cuestión, su correspondiente aminoácido, coordenadas, etc. Es útil para almacenar y compartir rápidamente, pero no debería usarse para presentaciones. Es difícil comprender la información que muestra.

#### Observamos que la información respeta cierta estructura interna. ¿Cuáles son los beneficios y las limitaciones de imponer una estructura para comunicar los resultados de un experimento?

La principal limitación es la falta de flexibilidad a la hora de agregar contenido inesperado. La ventaja de estandarizar la información de esta manera es que se puede crear programas para usar este tipo de archivos y presentarlos a los lectores de una manera más entendible.

#### Hemos visto que las proteínas tienen estructura tridimensional y hemos podido observar algunas características de las mismas. ¿Será igual con los ácidos nucléicos?

Si, ya que se compondrían de lo visto previamente, en distinta escala y en una estructura agrupada de proteínas.

#### Rosalind Franklin es una científica muy relevante, que tuvo menos reconocimiento del merecido. Contanos sobre los procedimientos que puso a punto Rosalind.

Rosalind Franklin trabajaba para descubrir la estructura del ADN con la cristalografía de rayos X. Con este método, logró una imagen de la estructura de doble hélice del ADN, fotografía conocida como Fotografía 51.
