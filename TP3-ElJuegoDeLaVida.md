
## Reto I
- Las procariotas son más pequeñas.
- Las células procariotas no tienen un núcleo definido y su material genético se encuentra disperso en el citoplasma
- Las células eucariotas tienen membrana nuclear.
- Las eucariotas tienen reproducción sexual y asexual, en cambio las procariotas solo asexual.
- La división celular procariota es directa.
- Las células eucariotas tienen citoesqueleto.

## Reto II
    def print_arn(peptido, tabla):
	    validos = 'UCAG'
	    cadena = []
	    elemento = []
	    for p in peptido:
		    if(validos.find(p) != -1):
			    elemento.append(p)
		    if(elemento.size == 3):
			    cadena.append(tabla[elemento])
			    elemento = []    
	    return cadena

  
## Reto III
    def print_index(peptido):
	    valida = 'TATA'
	    regiones = []
	    index_region = []
	    caja = ''
	    for idx,p in enumerate(peptido):
		    caja += p
		    if((len(caja) == 4) and (caja == valida)):
			    if(len(index_region) == 0):
				    index_region.append(idx +1)
			    else:
					index_region.append(idx - 3)
				    regiones.append(index_region)
				    index_region = []
			    caja = ''
    
	    return index_region
    
      
