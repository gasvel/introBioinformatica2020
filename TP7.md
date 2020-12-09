
## TP 7 - Estructura de proteínas

1- ¿Cómo describís la estructura de esta proteína? ¿Cómo podrías describir la estructura de esta proteína? Realizá la misma descripción pero para la proteína 1THJ, 3OGB.
Las estructuras de las proteínas se pueden clasificar por su contenido en estructuras secundarias y según su cantidad de dominios. 

- 1THJ: alfa-hélices ; loops ; beta-plegadas
- 3OGB: alfa hélices y loops

3- Estudiá la proteína 2CPE. 
a) ¿Qué tipo de proteína es? 

- Tiene un núcleo concentrado con diferentes ramificaciones
			
b) ¿Cómo la describirías? Utilizá el comando “setall_states, on” para ver todos los estados conformacionales estimados para esa estructura. 

- No se ven túneles
- 2 alfa-hélices, 4 beta-plegadas y 7 loops.


c) Compará el espacio conformacional de la 2CPE con la de la estructura de la mioglobina (1MYF). 

- La mioglobina no tiene estructura beta-plegada, sólo 7 alfa-hélices y 8 loops

d) Utilizando el modo secuencia, seleccioná la HIS64. Mostrala en formato stick o lines. ¿Qué función podría llegar a tener?
 
- Se debría unir con otro aminoácido catión estabilizando el ligando ya que la proteína 2CPE se relaciona con el ARN (anion)

e) ¿Y la HIS93? 

- Une la HEM con la proteína

5- Cálculo de la distancia promedio de un puente de hidrógeno

- La medición entre el hidrógeno y el nitrógeno es de 1.0. La medición entre el oxígeno y el hidrógeno es de 3.2.Para ILE , la medición entre el oxígeno y el hidrógeno es de 2.6 y la medición entre el hidrógeno y el nitrógeno es de 0.9 Para PHE, la medición entre el hidrógeno y el nitrógeno es de 1 y la medición entre el oxígeno y el hidrógeno es de 2.6 

6- Identificación de interacciones π-π y π-catión 
- Y, F y W forman los residuos aromáticos la proteína 1A7E


7- Sitio activo de la anhidrasa carbónica. Utilizado la estructura de la anhidrasa carbónica 1THJ y la opción Select en el Menú Edit :
a) ¿Cuántas subunidades tiene la estructura nativa?

- 3 estructuras definidas

b) ¿Tiene heteroátomos esta molécula? ¿Cuáles?

- Zinc y oxígeno

d) ¿Los residuos que unen el Zinc pertenecen a la misma subunidad?
- No. El zinc actúa como ligando entre las estructuras de la proteína

9- Utilizando el programa Pymol estudiá la estructura terciaria y cuaternaria de la proteína 4AUI.
Determiná la superficie, localizá ligandos e identifícalos. Si querés obtener más información visitá el sitio https://www.rcsb.org/ y buscá por el ID: 4AUI.
Para seleccionar los ligandos podés usar el comando: select ligandos, organic
Para seleccionar grupos inorgánicos podés usar el comando: select inorganicos, inorganic

- Estructura terciaria: 31 átomos con ligandos inorgánicos y 93 átomos con ligandos orgánicos

- Estructura cuaternaria: 3 subestructuras
		
10- Estudio de túneles
Utilizando el programa (o servidor https://mole.upol.cz/) MOLE estudiá los túneles asociados al sitio activo de las estructuras 1THJ y 1F90. Este programa te pedirá que indiques a partir de qué regiones de la proteína debe comenzar la exploración en búsqueda de túneles. El punto de inicio puede ser a partir de cavidades, átomos o residuos seleccionados manualmente, o a partir de la base de datos CSA ( Catalytic site atlas ).

- 1THJ: 8 cavidades - 20 túneles
- 1F90: 6 cavidades - 10 túneles
		
11- Estudio de pockets en EGFR
El EGFR es uno de los principales marcadores de cáncer de pulmón. Utilizando la sesión de Pymol estudiá los pockets. 1M14 es un confórmero activo y 3W32 uno inactivo. Compará el sitio activo de ambos confórmeros así como también los tamaños de los pockets.
La determinación de las cavidades se puede realizar mediante el servidor fpocket: https://mobyle.rpbs.univ-paris-diderot.fr/cgi-bin/portal.py#forms::fpocket

Desactivar la opción de demo: “ Test the service with server sample data (input parameters will be discarded” .
Una vez que termina podés bajarte el Pymol visualization script [TGZ] para ver los resultados. Descomprimir (con 7zip u otro) y abrir el archivo .pml con Pymol…. Lo que vas a ver es para cada cavidad un conjunto de esferas. Primero para la molécula H → cartoon, H → spheres, S → Surface. Luego para cada ‘pocket’ S → dots !!

- Los pockets de la proteina 1M14 ocupan más espacio de la superficie. Los pockets de la proteina 3W32 tienen mayor superficie por dentro de la proteina.

- 1M14 = 25 pockets

- 3W32 = 22 pockets

12- Tomando como base la estructura PDB 3GPC, estudiá sus túneles utilizando el Fpocket 
a) ¿Encontrás algún/os túnel/es en la proteína donde pueda unirse algún fármaco? 
- 23 túneles

b) ¿Qué residuos se encuentran en dicha cavidad?

- 22 STP

Analizando la proteina 3GPC post procesada con FPocket encontramos que el pocket 61 es un buen candidato para la unión con un fármaco. En dicho pocket intervienen los aminoácidos del 75 al 81 en la cadena.


Ahora analicemos los resultados de los investigadores de la UBA y UNQ (https://doi.org/10.1007/s00018-020-03679-5 ), que mediante una técnica de acoplamiento molecular (docking) diseñaron un inhibidor para esta proteína, capaz de unirse a la misma y reducir entonces la proliferación de células tumorales.

	
Descargá la estructura de la proteína y la del inhibidor y visualizalas en Pymol (abrí ambos archivos en la misma sesión) 
a)¿Dónde se une el inhibidor? 

- En un túnel

b) ¿Coincide con el túnel que propusiste anteriormente?

- Si

c ) ¿Dada esta inspección ocular cómo creés que actúa el inhibidor? Usando el play de la botonera, observá las distintas conformaciones del ligando o inhibidor.

- El ligando "gira" dentro del tunel sin salirse

13- Asignación de estructura secundaria basado DSSP
Para inferir estructura secundaria utilizaremos el servidor 2StrucCompare con la Endolisina de bacteriófago en dos variantes (3F8V y 4LMZ).
1) Primero determiná la estructura secundaria de ambas conformaciones por separado usando el sevidor https://2struccompare.cryst.bbk.ac.uk/index.php
a) Corré el análisis por separado de cada estructura (recuadro derecho), cargando su código PDB y haciendo click en submit

b) Observá las distintas regiones de estructura secundaria, 

¿todas son de igual cantidad de residuos? 

- 3F8V tiene más residuo helicoidal que 4LMZ


¿Se requieren más o menos residuos para formar una alfa hélice que un loop? ¿Por qué?

- Una estructura secundaria de alfa hélice necesita 3.6 residuos de AA por vuelta.
					
					
### RETO I: Estas estructuras difieren de las estructuras sobre las que venimos trabajando en su determinación. Como habrás notado estas fueron obtenidas mediante la técnica de MNR, ¿Pero en qué consiste esta técnica?
La técnica de MNR (Nuclear Magnetic Resonance) somete a una molécula a un campo electromagnético y sus átomos
empiezan a actuar como imanes. Este campo magnético permite el estudio detallado de estructuras más complejas ayudando a responder preguntas vitales de la actualidad.

### RETO II: Investigá en qué consisten las interacciones puentes de hidrógeno,π-π y π-catión y qué aminoácidos podrían intervenir en dichas interacciones.
- Puentes de hidrógeno: Son enlaces que se producen a partir de la atracción
existente entre un átomo de hidrógeno y un átomo de oxígeno, flúor o
nitrógeno con carga negativa.


- Interacciones π-π: Las interacciones π-π son interacciones débiles que tienen lugar entre dos sistemas π, generalmente uno π deficiente y otro π excedente. Estas interacciones son combinación de fuerzas electrostáticas, efectos hidrofóbicos, dipolo-dipolo o transferencia de carga entre un dador y un aceptor de electrones

- Interacciones π-catión: Se producen entre un catión y un sistema aromático, principalmente mediante fuerzas electrostáticas. Esta interacción se produce, por ejemplo, entre el ion K+ y el benceno


### RETO III: Investigá en qué consiste el docking, en qué ideas basa su funcionamiento.
El docking o acoplamiento molecular es una técnica de mecánica molecular
usada para predecir energías y modos de enlace entre proteínas y ligandos. Este método tiene un rol muy importante en el diseño racional de
fármacos. Para tal fin entran en juego una serie de procesos químicos
gobernados por leyes físicas, entre ellas las que tienen que ver con la
energía que se consume o libera en tal proceso.
En la actualidad contamos con sofisticadas técnicas experimentales de cuyos resultados se extrae información tridimensional tanto de las proteínas como de los ligandos

