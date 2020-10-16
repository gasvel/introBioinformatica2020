
## TP 5 - Introducción a la bioinformática
 
#### RETO I: Intentemos, entonces alinear estas dos palabras, para comprender mejor el problema. Alinea en la tabla interactiva las palabras "BANANA" y "MANZANA".
 
  B  A  N  -  A  N  A
 
M  -  A  N  Z  A  N  A
 
#### RETO II: En la siguiente tabla interactiva distintos alineamientos para las palabras "ANA" y "ANANÁ". Verás que en el margen superior izquierdo aparece un valor de identidad calculado para cada alineamiento que intentes. Tomá nota de los valores de identidad observados y de las conclusiones que se desprendan de estas observaciones.
 
 
A  N  A
A  N  A  N  A
 
Penalidad: 0 - Identidad: 0.6
Penalidad: 2 - Identidad: -0.2
 
`-  -  A  N  A
A  N  A  N  A
 
Penalidad: 0 - Identidad: 0.6
Penalidad: 2 - Identidad: -0.2
 
A  N  -  -  A
A  N  A  N  A
 
Penalidad: 0 - Identidad: 0.6
Penalidad: 2 - Identidad: -0.2
 
Parece ser que la posición o la cantidad de igualdades continuas no alteran el valor de la identidad c.
 
#### RETO IV: En la siguiente tabla probá distintos alineamientos para las secuencias nucleotídicas. Podrás ver las traducciones para cada secuencia. Probá varias combinaciones, tomá nota de las observaciones y de las conclusiones que se desprendan de estas.
 
T  G  C  -  G  -  A  G  G
 
`.  C  .  .  -  .  .  R  .`
 
T  G  C  C  G  A  A  G  G
 
`.  C  .  .  R  .  .  R  .`
 
---
 
 
`-  -  A  G  -  G  G  G  A`
 
`.  -  .  .  -  .  .  G  .`
 
T  G  A  G  A  G  G  G  -
 
`.  X  .  .  E  .  .  -  .`
 
Para alinear estas secuencias cada tripla debe quedar igual arriba y abajo
 
 
#### RETO V: Estuvimos viendo que el alineamiento de secuencias no es trivial y requiere contemplar los múltiples caminos posibles, teniendo en cuenta al mismo tiempo la información biológica que restringe ese universo de posibilidades.
 
#### ¡Es momento de llevar entonces estos conceptos a lo concreto! Te proponemos pensar los pasos a seguir en un alineamiento de dos secuencias cortas, teniendo en cuenta una matriz genérica de scoring (puntuación) que contemple las complejidades que estuvimos viendo, es decir que penalice de distinto modo una inserción o deleción, que una discordancia (mismatch) o una coincidencia (match). Escribirlos o esquematizarlos en un diagrama de flujo.
 
Si tenemos en cada paso la mejor alineación posible de la sub-alineación , debemos elegir la opción que nos permita maximizar el puntaje:
 
 - sub-solucion + gap izq
 - sub-solucion + gap der
 - sub-solucion + coincidencia
 
#### RETO VI: Utilizando la herramienta interactiva desarrolladas por el Grupo de Bioinformática de Freiburg probá distintos Gap penalties para el ejemplo propuesto y observa lo que ocurre. Interpretando la recursión, explica con tus palabras de dónde salen los valores de la matriz que se construye. ¡Esquematiza tus conclusiones!
 
Los valores de la matriz se obtienen aplicando los valores de match, mismatch y gap. Moverse una celda hacia la derecha o una celda hacia abajo implica hacer el valor actual sumado al valor del gap. Si los índices son iguales, hay que sumar el valor de match o mismatch dependiendo de los valores en esa posición.
 
 Pseudo python
```python
def crear_matriz(seq_a, seq_b, match, mismatch, gap):
 matriz =[[0]]
 gaps_y = 0
 gaps_x = 0
 
 for m_y, y in matriz:
   for _,x in m_y:
     if x == 0 & y == 0:
       next
 
     if y >= 1 & x == 0:
       gaps_y += gap
       m_y[x] = gaps_y
     elif x >= 1 & y == 0:
       gaps_x += gap
       m_y[x] = gaps_x
     else :
        if seq_a[y-1] == seq_b[x-1]: 
         score_comparacion = match
        else:
          mismatch
      
       gap_izq = matriz[y-1][x] + gap
       gap_der = matriz[y][x-1] + gap
       comp = matriz[y-1][x-1] + score_comparacion
    
       m_y[x] = [gap_izq, gap_der, comp].max
     end
   end

 
 matriz
end
```
 
#### RETO VII: calculá el E-value y % identidad utilizando el programa Blast de la siguiente secuencia input usando 20000 hits, un e-value de 100 y tomando aquellos hits con un mínimo de 70% cobertura. Observe y discuta el comportamiento de : E-value vs. % id, Score vs %id, Score vs E-value
 
> E-value vs. % id
 
Mientras que un porcentaje alto de identidad indica que un gran conjunto de valor fueron alineados de la misma forma, un E-value alto indica que esto es de casualidad y no demuestra que haya una relación biológica real.
 
> Score vs %id
 
Valores altos de ambos muestran que tenemos una muestra significativa. El score se calcula mediante una fórmula
 
> Score vs E-value
 
Idem E-value vs % id. Un E-value bajo con un score alto indica que la muestra es significativa.
 
#### RETO VIII: Realizar nuevas búsquedas usando la mitad de la secuencia problema y para un cuarto de la secuencia original. Compara los gráficos obtenidos.¿Qué conclusiones puede sacar?
 
El E-value es ás alto ya que la posibilidad de que los match sean de casualidad aumentan, también tenemos un score y un max score mas bajo.
 
#### RETO IX: Utilizando BLAST utilice búsquedas de similitud secuencial para identificar a la siguiente proteína:
 
>MIDKSAFVHPTAIVEEGASIGANAHIGPFCIVGPHVEIGEGTVLKSHVVVNGHTKIGRDNEIYQFASIGEVNQDLKYAGEPTRVEIGDRNRIRESVTIHRGTVQGGGLTKVGSDNLLMINAHIAHDCTVGNRCILANNATLAGHVSVDDFAIIGGMTAVHQFCIIGAHVMVGGCSGVAQDVPPYVIAQGNHATPFGVNIEGLKRRGFSREAITAIRNAYKLIYRSGKTLDEVKPEIAELAETYPEVKAFTDFFARSTRGLIR
 
La proteína es "Acetylglucosamine O-acyltransferase [Escherichia coli]".
 
#### RETO X: Realiza una nueva corrida del BLASTp, utilizando la misma secuencia , pero ahora contra la base de datos PDB. ¿Se obtienen los mismo resultados? ¿Qué tipo de resultados(hits) se recuperan? ¿Cuándo nos podría ser útil este modo de corrida?
 
Obtuvimos resultados diferentes, también obtuvimos otros organismos (Proteus mirabilis HI4320, Acinetobacter baumannii, etc) donde aparece la misma proteína y también otras proteínas similares.