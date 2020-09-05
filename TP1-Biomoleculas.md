# TP 1 - Biomoléculas - Introducción a la bioinformática

## RETO I
El ADN es un ácido nucleico, está compuesto de nucleótidos. Almacena información genética de cada ser vivo.

## RETO II
La estructura primaria se puede expresar usando un String ya que solo debemos listar en orden los aminoácidos que componen a la proteína.

## RETO III
La estructura terciaria podría representarse usando un grafo para indicar la forma en la que se va plegando la proteína.

## RETO IV
Sus investigaciones llevaron a la obtención de imágenes de la estructura del ADN con una gran nitidez mediante la técnica de difracción de rayos X. 
También realizó investigaciones sobre la estructura del ARN, utilización del carbón y el polio virus.

## RETO V
Si asumimos que la secuencia es una lista de los aminoácidos y un diccionario, donde las claves son los aminoácidos y los valores las preferencias, escribimos el siguiente código en el lenguaje Python:
```
  def estructuraSecundaria(secuencia,preferencias):
  estructura = {"h":0,"b":0,"l":0}
  for sec in secuencia:
    pref = preferencias[sec]
    estructura[pref] += 1
  
  return {max(estructura,key=estructura.get):max(estructura.values())}
```
## RETO VI
Se podría corroborar creando un programa que compare cadenas de ADN de los individuos.La diferencia se da por variaciones en la información genética
```
def esDiferente(adn_a, adn_b):
  for idx,elem_a in enumerate(adn_a):
    if(elem_a != adn_b[idx]):
      return True

  return False
```
