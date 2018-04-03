# Laboratorio 03 - Ensamblaje de genomas y predicción de genes

### Bioinformática BIOL350

### Camilo Cano Salazar

----

**_Parte 1:_** El artículo genoma

_Preguntas 1.1_

- ¿Cuántos genomas han sido depositados en GOLD? ¿Son los mismos de GENBANK?

El total de genomas depositados en _GOLD_ corresponde a la suma del número de **proyectos completos** y el número **borradores permanentes**, siendo este, 125,471 [1](https://gold.jgi.doe.gov/). Al comparar con _GENBANK_, se puede identificar que este último cuenta con una cantidad superior de genomas reportados, alcanzando hasta la fecha 177,666 (este valor fue calculado por la suma del total de genomas reportados para todos los grupos taxonómicos definidos) [2](https://www.ncbi.nlm.nih.gov/genome/browse#!/overview/). 
	
- ¿Cuál es la distribución de procariontes y eucariontes secuenciados?

Obedeciendo a la categoría _organism_ de la página principal de _GOLD_, el número de organismos eucariontes cuyos genomas han sido secuenciados corresponde a 23,037 (representando esto, el 7.74% del total de organismos) [3](https://gold.jgi.doe.gov/). Por otro lado, para los procariontes el valor es de 265,346 (representando esto, el 89.23% del total de organismos) [4](https://gold.jgi.doe.gov/). 

----
	
_Preguntas 1.2_

- ¿Qué es el N50, L50, NG50?

**N50:** este equivale a la longitud en nucleótidos del _contig_ más corto, dentro del conjunto de los más largos que representan el 50% de la longitud total del ensamblaje [5](https://en.wikipedia.org/wiki/N50,_L50,_and_related_statistics).

**L50:** este equivale al número mínimo de _contigs_ necesarios para representar el 50% del tamaño del ensamblaje [6](https://en.wikipedia.org/wiki/N50,_L50,_and_related_statistics). 

**NG50:** este parámetro estadístico posee el mismo fundamento necesario para calcular el N50; sin embargo, este se define a partir de la longitud total del genoma conocido o estimado, no del tamaño del ensamblaje (pudiendo ser este una desviación del tamaño real del genoma estudiado) [7](https://en.wikipedia.org/wiki/N50,_L50,_and_related_statistics). 

- ¿Cuál es el propósito de calcular estas estadísticas?

Los parámetros **N50** y **L50** acuden al objetivo de identificar la calidad y estado final del ensamblaje, además de ser una medida indirecta de la posibilidad de encontrar genes completos [8](https://en.wikipedia.org/wiki/Contiguity). Los estadísticos anteriores, juntos, dan cuenta de la _contigüidad_ [9](https://en.wikipedia.org/wiki/Contiguity). Contar con un valor grande para el **N50** no es suficiente para concluir sobre la integridad del ensamblaje en términos de su fragmentación, pues los demás _contigs_ mayores en tamaño pueden ser muy cercanos en longitud; por tanto, saber el número mínimo de _contigs_ para alcanzar el 50% del ensamblaje (esto es, **L50**) es clave para no cometer errores tipo B (por ejemplo, falsos positivos). 

El cálculo del **NG50** tiene como propósito establecer un valor idóneo para poder comparar entre genomas de diferentes especies, por ejemplo [10](https://en.wikipedia.org/wiki/N50,_L50,_and_related_statistics). Esto es necesario ya que el **N50** puede ser muy variable entre los diferentes ensamblajes para un genoma dado; por tanto, esto supone un inconveniente a la hora de decidir cuál **N50** seleccionar para hacer la comparación (el uso de algunos podría dar resultados contrarios, incluso existe la posibilidad de que no sean informativos) [11](https://en.wikipedia.org/wiki/N50,_L50,_and_related_statistics). Que el **NG50** este construido basado en la longitud conocida o estimada del genoma, evita esta problemática [12](https://en.wikipedia.org/wiki/N50,_L50,_and_related_statistics).


- ¿Cuál es el genoma que escogiste? Adjunta la referencia.

Existe un único genoma de _Asparagus officinalis_ reportado en _Genome_ (siendo este, completo), cuya referencia es: **PRJNA317340** [13](https://gold.jgi.doe.gov/projects?id=Gp0235896) [14](https://www.ncbi.nlm.nih.gov/genome/?term=PRJNA317340). 

- ¿Cuál es el N50 del genoma que escogiste? ¿Y el NG50?

Según _Genome_, los valores para algunos parámetros estadísticos del genoma de _Asparagus officinalis_ (referencia, **PRJNA317340**) son [15](https://www.ncbi.nlm.nih.gov/assembly/GCF_001876935.1/): 

	
	Contig N50: 46,553
	Contig L50: 7,625
	NG50: no reportado. No se encontró ningún valor en la página web y en
	ninguno de los artículos referenciados en ella.
	
- ¿Qué tipo de tecnología se usó para secuenciar el genoma que escogiste?

Según _Assembly_, la tecnología de secuenciación empleada para ensamblar el genoma fue _Illumina HiSeq_ [16](https://www.ncbi.nlm.nih.gov/assembly/GCF_001876935.1/).

- ¿Qué organismo escogiste, cuántos cromosomas tiene tu organismo y cuál es su tamaño?

Esparraguera o espárrago común (_Asparagus officinalis_), según las bases de datos _Genome_ y _Assembly_, cuenta con un total de 10 cromosomas y su genoma tiene un tamaño de 1,187,538,024 pb [17](https://es.wikipedia.org/wiki/Asparagus_officinalis) [18](https://www.ncbi.nlm.nih.gov/assembly/GCF_001876935.1/) [19](https://www.ncbi.nlm.nih.gov/genome/?term=PRJNA317340).

El tamaño de cada uno de los 10 cromosomas es [20](https://www.ncbi.nlm.nih.gov/assembly/GCF_001876935.1/#/st): 


| Chromosome| Length (dp)|       
| ----- | ----- | 
| 1  | 132,393,784 |          
| 2  |     84,732,013                
| 3  | 113,259,003           
| 4  | 146,560,859 
| 5  | 131,469,567
| 6  | 78,779,235
| 7  | 151,357,931
| 8  | 131,339,754
| 9  | 68,543,460
| 10  | 73,452,336
| unplaced  | 75,650,082

----

**_Parte 2:_** Predicción de genes

_Preguntas 2.1_

- ¿Cuántos ORF o genes encontró ORFfinder?

_ORFdinder_ encontró un total de 7 ORF en la secuencia problema.

- ¿Cuántos ORF o genes encontró Glimmer?

_Glimmer_ encontró un total de 10 ORF en la secuencia problema.

- ¿Alguno de los genes predichos por estas herramientas coinciden?

Considerando que la palabra _coincidir_ alude a aquellos genes **individuales** cuyas posiciones de codones de inicio y de parada son similares y, por tanto, cuentan con una longitud de secuencia parecida, las parejas G2-ORF4, G3-ORF5, y G6-ORF7 coinciden.

Para _GLIMMER_:

| Label | Stand | Start | Stop | Length (nt) |
|:-----:|:-----:|:-----:|:----:|:------:|
|   G1  |   +   |  909  | 1884 |   924  |
|   G2  |   -   |  948  | 1436 |   486  |
|   G3  |   -   |  1391 | 1831 |   438  |
|   G4  |   -   |  455  |  823 |   366  |
|   G5  |   -   |  150  |  476 |   324  |
|   G6  |   +   |  434  |  709 |   273  |
|   G7  |   +   |  1587 | 1829 |   240  |
|   G8  |   -   |  1366 | 1587 |   219  |
|   G9  |   -   |  283  |  241 |   156  |
|  G10  |   +   |  1391 | 1531 |   138  |

Para _ORFinder_:

| Label | Stand | Start | Stop | Length (nt) |
|:-----:|:-----:|:-----:|:----:|:-----------:|
|  ORF1 |   +   |   1   |  909 |     909     |
|  ORF2 |   +   |  1304 | 1381 |      78     |
|  ORF3 |   +   |  1433 | 1531 |      99     |
|  ORF4 |   -   |  1388 |  948 |     441     |
|  ORF5 |   -   |  1795 | 1391 |     405     |
|  ORF6 |   -   |  1048 |  965 |      84     |
|  ORF7 |   -   |  598  |  455 |     144     |



- ¿En qué hebra están codificados?

Para _GLIMMER_:

| Label | Strand|       
| ----- | ----- | 
| ORF1  | + |          
| ORF2  | +                
| ORF3  | +             
| ORF4  | -
| ORF5  | -
| ORF6  | -
| ORF7  | -


Para _ORFfinder_:

| Label | Strand|    
| ----- | ----- | 
|  G1 | +|        
|  G2 |  -            
|  G3 |  -           
| G4  | -
|   G5| -
| G6  | +
|  G7 | +
|  G8 |-
|	G9 |- 
|  G10 |+
- ¿Qué tipo de programa es GLIMMER? ¿Ab initio o por homología?

Según los artículos referenciados, _GLIMMER_ es un tipo de programa _ab initio_ (Majoros, 2004; Aggarwal, 2002). Este es un método que pretende detectar o predecir regiones codificantes solo a partir de la información en la secuencia dada, sin ninguna referencia homóloga en bases de datos (Zhu, 2010).

-----
_Preguntas 2.2_

- Describe los resultados encontrados con respecto a los genes que encontraste con GLIMMER y ORFfinder.

_Resultados de búsqueda en BLAST para ORFfinder:_


| Label | Strand |                   Protein                   | Accession | Query cover | E value |
|:-----:|:------:|:-------------------------------------------:|:---------:|:-----------:|:-------:|
|  ORF1 |    +   |             Protein FdhE            |  P44452.1 |     100%    |    0    |
|  ORF2 |    +   |                      --                     |     --    |      --     |    --   |
|  ORF3 |    +   |                      --                     |     --    |      --     |    --   |
|  ORF4 |    -   | Ribosomal-protein-alanine acetyltransferase |  P44305.1 |     100%    |  1e-105 |
|  ORF5 |    -   |        DNA polymerase III subunit psi       |  P43750.1 |     100%    |  2e-95  |
|  ORF6 |    -   |                      --                     |     --    |      --     |    --   |
|  ORF7 |    -   |                      --                     |     --    |      --     |    --   |



**Nota:** la definición funcional se aceptó según el valor de los parámetros de _Query cover_ y _E value_. Aunque para ORF2 y ORF6 sí se reportaba una proteína producto del alineamiento, se decidió no considerarlas, pues para los dos casos los valores de los parámetros suponían que no era muy confiable tomar el resultado como verdadero. Los valores encontrados son:

|Label|Query cover|E value
|---|----|------|
|ORF2| 88%|5.8
|ORF6| 92%| 28

**Criterio de selección:** la transición funcional se tomará siempre y cuando el _Query cover_ sea igual o mayor a 90%, y se cuente con un _E value_ muy cercano a cero (este criterio no fue diseñado bajo ninguna referencia bibliográfica).


	Para ambos, el valor de Query cover se aleja en cierta medida del 100% 
	y los valores para E value son muy altos.

Por su lado, para los casos de ORF3 y ORF7, BLAST no encontró similitudes significativas.

----
 
_Resultados de búsqueda en BLAST para GLIMMER:_

| Label | Strand |                    Protein                   |    Accession   | Query cover | E value |
|:-----:|:------:|:--------------------------------------------:|:--------------:|-------------|---------|
|   G1  |    +   |                      --                      |       --       |      --     |    --   |
|   G2  |    -   |          Peptide N-acetyltransferase         |     D64042     |     95%     |  1e-96  |
|   G3  |    -   |        DNA polymerase III subunit psi        | WP_005663309.1 |     91%     |  2e-79  |
|   G4  |    -   | Formate dehydrogenase accessory protein FdhE | WP_048942786.1 |     99%     |  2e-86  |
|   G5  |    -   | Formate dehydrogenase accessory protein FdhE | WP_005693890.1 |     99%     |  4e-67  |
|   G6  |    +   | Formate dehydrogenase accessory protein FdhE | WP_105899619.1 |     98%     |  2e-61  |
|   G7  |    +   |                      --                      |       --       |      --     |    --   |
|   G8  |    -   |                      --                      |       --       |      --     |    --   |
|   G9  |    -   |                 Protein FdhE                 |   PRI29053.1   |     98%     |  4e-28  |
|  G10  |    +   |        DNA polymerase III subunit psi        | WP_065251658.1 |     97%     |  1e-24  ||

**Nota:** la definición funcional acá, fue tomada de las misma manera que para el caso de la herramienta _ORFfinder_ (se empleó el mismo criterio). Este es el detalle de los genes predichos cuyas proteínas no fueron tomadas:

|Label|Query cover|E value
|---|----|------|
|G1| 45%|1e-87
|G7| 85%| 2e-40
|G8| 86%| 2e-39

	Aunque los valores de E value son "acordes", el Query cover
	de los tres no es muy tendiente a 100%.

**Discusión**

Al comparar las definiciones funcionales aceptadas del alineamiento por BLAST para las dos herramientas, es evidente que los genes predichos, como conjunto, codifican para las mismas proteínas (siendo estas, _DNA polymerase III subunit psi_, _Protein FdhE_, y _Peptide N-acetyltransferase_). No obstante, es necesario hacer notar ciertos puntos.  Aunque ya se comentó que solo había tres parejas que coincidían (siendo esto a nivel de la estructura genómica), la definición funcional permite establecer más coincidencias. Por otro lado, los resultados arrojados por _GLIMMER_, además de ser más comparados con _ORFfinder_, son redundantes para algunos genes predichos. 
Identificar las razones puntuales por lo que esto sucede escapa de los objetivos de este taller, lo único que considero relevante para tomar como justificación es que cada herramienta emplea un método diferente para predecir (_GLIMMER_ es un programa _ab initio_, y _ORFfinder_ se basa en homología).

-----
**Referencias**  

- Aggarwal, G., & Ramaswamy, R. (2002). Ab initio gene identification: prokaryote genome annotation with GeneScan and GLIMMER. Journal of Biosciences, 27(1), 7–14. https://doi.org/10.1007/BF02703679

- Majoros, W. H., Pertea, M., & Salzberg, S. L. (2004). TigrScan and GlimmerHMM: Two open source ab initio eukaryotic gene-finders. Bioinformatics, 20(16), 2878–2879. https://doi.org/10.1093/bioinformatics/bth315

- Zhu, W., Lomsadze, A., & Borodovsky, M. (2010). Ab initio gene identification in metagenomic sequences. Nucleic Acids Research, 38(12), 1–15. https://doi.org/10.1093/nar/gkq275

 