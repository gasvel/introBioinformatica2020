# TP4 - Introducción a la bioinformática

### Trabajaremos con las secuencias del citocromo c de nueve organismos, listados en la tabla de abajo. Además de su denominación taxonómica, deberíamos conocer su nombre común: intentemos completar la tabla.

| Secuencia      | Nombre taxonómico        | Nombre común        |
|----------------|--------------------------|---------------------|
| NP_061820.1    | Homo sapiens             | Humano              |
| NP_001072946.1 | Gallus gallus            | Gallina             |
| NP_001065289.1 | Pan troglodytes          | Chimancé común      |
| NP_001157486.1 | Equus caballus           | Caballo             |
| NP_001183974.1 | Canis lupus familiaris   | Lobo                |
| AEP27192.1     | Gorilla gorilla          | Gorila              |
| XP_024245566.1 | Oncorhynchus tshawytscha | Salmón real         |
| NP_001086101.1 | Xenopus laevis           | Conejo              |
| NP_477164.1    | Drosophila melanogaster  | Mosca de la fruta   |


### 2.-¿Cuán sencillo será alinear dos o más secuencias a mano? ¿Cuánto influirá en el número de secuencias a alinear, su longitud, y la similitud entre ellas?

Como no existe un metodo mecanico para realizarlo, si son mas de dos secuencias y son largas o completamente distintas se vuelve casi imposible de hacer a mano.

### 3.-¿Son parecidos los citocromos c de humano y gallo?

La suma de residuos idénticos están en posiciones equivalentes al alinear las dos secuencias, eso nos hace pensar que son similares.

### 4.-¿Qué teorías subyacen a este análisis?

    Por lo que el término homología se usa solo cuando el antepasado común es lo suficientemente reciente como para que la información de la secuencia haya retenido suficiente similitud como para hacer inferencias evolutivas (Park et al. 1998)


### 5.-¿Cómo nos ayuda la evolución a explicar sus similitudes y diferencias?

La evolución indica que las poblaciones van diferenciándose debido a las variaciones random y el ambiente que determinan el grado en el que los organismos se reproducen y sobreviven, esto lleva a una acumulacion de cambios.

### 6.-Podemos elegir verlo en colores (Show Color ). ¿Qué indican los colores?

| Residue  | Colour  | Property                                     |
|----------|---------|----------------------------------------------|
| AVFPMILW | Red     | Small(small+ hydrophobic (incl.aromatic -Y)) |
| DE       | Blue    | Acidic                                       |
| RK       | Magenta | Basic - H                                    |
| STYHCNGQ | Green   | Hydroxyl + sulfhydryl + amine + G            |
| Others   | Grey    | Unusual amino/imino acids etc                |


### 7.-¿Qué indican el guión (-), los dos puntos (:) y el asterisco (*)?

El “-” significa un GAP, que es un corrimiento de la cadena.
El “*”  significa que el residuo analizado se conserva en la posición analizada.
El “:” significa que el residuo analizado en esa posición tiene una conservación fuerte.
El “.”  es una conservación débil.

### 8.- A simple vista, ¿se conserva la secuencia del citocromo c en los organismos?

Hay una gran cantidad de asteriscos, guiandonos en la respuesta del punto anterior, esto indica que hay gran conservación.



### 9.- ¿Creeríamos que todos los organismos se asemejan por igual al resto, o se pueden identificar grupos de mayor similitud? Si es así, ¿tienen sentido? ¿Qué evidencias nos aportaría este análisis, a la luz de la evolución?

Hay grupos de mayor similitud.
La evolución nos muestra que las similitudes anatómicas y fisiológicas se ven en el análisis de las secuencias.

### 10.- A juzgar por los organismos participantes, ¿cuáles creería que deberían estar más agrupados en el árbol filogenético?

Deberían estar agrupados por especies y descendencia:

Humano, Gorila occidental, chimpancé común
Salmón, Rana
Caballo
Gallo

### 11.- Observemos el árbol filogenético. ¿Concuerda con lo esperado? ¿De qué organismos son los citocromos c más parecidos? ¿Cómo se explica?

Los citocromos c más parecidos son del Salmón y la Rana, y del Humano y el Chimpancé. Concuerda con lo esperado y también agrega información sobre ancestros comunes.
