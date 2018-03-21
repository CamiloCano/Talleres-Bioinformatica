## Laboratorio 01 - Bases de datos biológicas
### Bioinformática - BIOL350
#### Camilo Cano Salazar
-----
_**Parte uno:**_	Enfermedades genéticas y genes

### Síndrome de Meckel 1
- **Descripción**

Es un grave desorden genético hereditario que se caracteriza por ser una enfermedad autosómica recesiva letal, donde mutaciones en el gen MKS1 que produzcan la enfermedad, pueden alterar la estructuralidad de cuerpos basales (cilios, más que todo) en células epiteliales, ocasionando comúnmente: aumento del tamaño de los riñones, encefalocele occipital, anormalidades en el sistema nervioso central, polidactilia, entre otras. [1](https://ghr.nlm.nih.gov/condition/meckel-syndrome#genes) [2](http://www.omim.org/entry/249000?search=meckel%20syndrome&highlight=meckel%20syndrome%20syndromic).

- **Gen relacionado:** MKS1 [3](http://www.omim.org/entry/249000?search=meckel%20syndrome&highlight=meckel%20syndrome%20syndromic
 ). 
 
 ---
 
*Preguntas 1.1*

- ¿Tiene nombres alternativos el gen? 
 
Según la base de datos *Gene*, los alias reportados son: BBS13, JBTS28, 	MES, 
	MKS, y POC12 [4](https://www.ncbi.nlm.nih.gov/gene/54903#variation).

- ¿En qué cromosoma está? ¿Cuántos exones tiene? ¿Cuántas isoformas de transcritos?  

El gen MKS1 se encuentra en el brazo q del cromosoma 17, región 2, banda 2 (siendo su nomenclatura, 17q22) [5](https://www.ncbi.nlm.nih.gov/gene/54903#variation). 

GRCh38.p7 (actual) y GRCh37.p13 (anterior) son los dos ensambles reportados por *Gene* con nueve y cinco isoformas, respectivamente. Ambos poseen 20 exones [6](https://www.ncbi.nlm.nih.gov/gene/54903#variation).

- ¿Qué tipo de proteína es codificada por este gen? ¿Cuál es su número EC?  

EL gen MKS1, según la base de datos *Uniprot*, codifica para la proteína estructural **Meckel syndrome type 1 protein** [7](http://www.uniprot.org/uniprot/Q9NXB0). Esta proteína realiza varias funciones estructurales donde resalta su participación como componente del complejo tipo tectónico (siendo este una barrera que impide el escape de proteínas transmembrana entre cilios y membranas), intervención en el desplazamiento del centrosoma en la cilogenésis, y aporte a la morfología de ramificación celular [8](http://www.uniprot.org/uniprot/Q9NXB0). No posee número EC en *Gene*, pues no es una enzima [9](https://www.ncbi.nlm.nih.gov/gene/54903#variation).

- ¿Qué genes están inmediatamente río arriba/abajo?

Teniendo en cuenta que, según *Genome Data Viewer* y la base de datos *Gene*, el gen MKS1 está orientado 3' a 5', estos son los dos genes inmediatamente cercanos [10](https://www.ncbi.nlm.nih.gov/gene/54903#variation) [11](https://www.ncbi.nlm.nih.gov/genome/gdv/browser/?context=gene&acc=54903): 

	Río arriba: LOC105371841 (se sobrepone con MKS1).
	Río abajo: EPX (no se sobrepone con MKS1).
---
*Preguntas 1.2*

- ¿Cuál es la longitud de tu gen?

La longitud reportada en *Nucleotide* es de 14170 pb [12](https://www.ncbi.nlm.nih.gov/nuccore/NC_000017.11?report=genbank&from=58205436&to=58219605&strand=true).

- ¿Cuántas variantes de tu gen hay descritas y en qué posiciones?  

En *Clinvar* hay descritas un total de 144 variantes del gen. Debido a que es una gran cantidad, es imposible reportar cada una de las posiciones relacionadas; sin embargo, aquí están los tipos a los que corresponden [13](https://www.ncbi.nlm.nih.gov/clinvar/?term=MKS1%5Bgene%5D):

	Deletion (13)
	Duplication (13)
	Indel (0)
	Insertion (7)
	Single nucleotide (117)
	
Es importante resaltar que, al buscar en otras bases de datos, por ejemplo, *Variation Viewer*, lo reportado tiende a ser diferente. Aquí se encuentran 2253 variantes del gen clasificadas así [14](https://www.ncbi.nlm.nih.gov/variation/view/?q=54903%5Bgeneid%5D):

	Single nucleotide variant (2,013)
	Copy number variation (74)
	Deletion (81)
	Insertion (47)
	Short tandem repeat variation (4)
	Inversion (7)
	
- ¿Las sustituciones corresponden a cambios sinónimos o no sinónimos?  

320 de las variantes del gen encontradas en *Variation Viewer* de *NCBI* corresponden a cambios no sinónimos, y 151 a cambios sinónimos [15](https://www.ncbi.nlm.nih.gov/variation/view/?q=54903%5Bgeneid%5D).

- ¿Existen ortólogos de tu gen en otras especies? ¿Cuántos?  
	¿Y paralógos? ¿Hay pseudogenes? ¿Cuántos?  
	
*Kegg* reporta 391 ortólogos del gen MKS1 [16](http://www.kegg.jp/ssdb-bin/ssdb_best?org_gene=hsa:54903). Por otro lado, según misma base de datos, existen 5 parálogos [17](http://www.kegg.jp/ssdb-bin/ssdb_paralog?org_gene=hsa:54903). No hay pseudogenes reportados en *Kegg*, ni en otras bases revisadas.

----
_**Parte dos:**_ Rutas y procesos metabólicos

*Preguntas 2.1* **Kegg**

- Anteriormente encontraste nombres alternativos de tu gen ¿Existen otros reportados por Kegg? ¿Cuáles?

Los nombres alternativos reportados por *Kegg* para el gen MKS1 son los mismos que se encontraron en *Gene* (siendo estos, BBS13, JBTS28, MES, MKS, y POC12) [18](http://www.genome.jp/dbget-bin/www_bget?hsa:mks1).

- ¿En qué rutas metabólicas participa la proteína codificada por tu gen?  

**Meckel syndrome type 1 protein** no participa en ninguna ruta metabólica según *Kegg* [19](http://www.genome.jp/dbget-bin/www_bget?hsa:mks1).

- ¿Cuál es el número de identificación de tu gen (entry number)?  

**54903** es el número de identificación (es igual al de la base de datos *Gene*) [20](http://www.genome.jp/dbget-bin/www_bget?hsa:mks1).

- En general, cada unidad dentro de una base de datos tiene un número o código de identificación único. De esta forma, uno puede obtener exactamente lo que quiere dentro de un océano de otras cosas ¿En qué otras bases de datos está tu gen presente y cuáles son sus números de acceso?  

Las bases de datos con su número de acceso para el gen MKS1, encontradas en *Kegg*, son las siguientes [21](http://www.genome.jp/dbget-bin/www_bget?hsa:mks1):

	NCBI-GeneID: 54903
	NCBI-ProteinID: NP_060247
	OMIM: 609883
	HGNC: 7121
	Ensembl: ENSG00000011143
	Vega: OTTHUMG00000133714
	Pharos: Q9NXB0 (Tbio)
	UniProt: Q9NXB0
-----
*Preguntas 2.2* **Kegg**

- ¿En qué otras rutas metabólicas están involucrado tu gen?

EL gen MKS1, según *Kegg*, no está involucrado en ninguna ruta metabólica [22](http://www.genome.jp/dbget-bin/www_bget?hsa:mks1).


- ¿Qué significan los cuadros verdes en el diagrama?

No es posible resolver esta pregunta para el gen MKS1; no obstante, leyendo las guías de *Kegg*, los cuadros verdes representan rutas específicas del organismo (procesos identificados, en este caso, para humanos) [23](http://www.genome.jp/kegg/kegg3a.html).

- ¿Con qué rutas se cruza la ruta metabólica?

Esta pregunta no es del caso para el gen MKS1 [24](http://www.genome.jp/dbget-bin/www_bget?hsa:mks1).

----
*Preguntas 2.3* **GO (Gene ontology)**

- ¿Cuántos "dominios" forman la anotación GO?

Los dominios que forman *GO* son tres principalmente [25](http://geneontology.org/page/ontology-documentation) [26](http://geneontology.org/page/ontology-structure):

	Componente celular
	Función molecular
	Proceso biológico

- Ve a "Tools" --> "AmiGO 2" y escribe en la casilla de búsqueda GO:0006096  
¿A qué corresponde este término y qué información te entrega la página?

El término GO:0006096 corresponde al Proceso Glucolítico. Al buscarlo, *GO* nos entrega ciertos links con los cuales podemos acceder a información precisa que necesitemos del proceso (siendo estos, información detallada, anotaciones directas e indirectas, y genes y productos asociados al proceso) [27](http://amigo.geneontology.org/amigo/medial_search?q=GO%3A0006096). Por otro lado, aunque un tanto similar a lo ya expuesto, también aparecen las pestañas *Ontology*, *Genes and genes products*, y *Annotations*, las cuales tienen información un tanto similar, para algunos casos, con la encontrada en los links [28](http://amigo.geneontology.org/amigo/medial_search?q=GO%3A0006096).

- Haz clic en "Graph Views" y examina el gráfico. Anota 10 sub-categorías GO a la cual GO:0006096 pertenece.

Las sub-categorías seleccionadas son [29](https://www.ebi.ac.uk/QuickGO/GTerm?id=GO:0006096): 

	GO:0009152 (purine ribonucleotide biosynthetic)
	GO:0046034 (ATP metabolic process)
	GO:0009166 (nucleotide catabolic process)
	GO:0046031 (ADP metabolic process)
	GO:0042866 (pyruvate biosynthetic process)
	GO:0009179 (purine ribonucleoside diphosphate)
	GO:0046496 (nicotinamide nucleotide metabolic)
	GO:0009150 (purine ribonucleotide metabolic)
	GO:0009205 (purine ribonucleoside triphosphate)
	GO:0019363 (pyridine nucleotide biosynthetic)

------
_**Parte tres:**_ Descargando secuencias, convirtiendo formatos.

*Preguntas 3.1* **Nucleotide**

- ¿Cuántos items fueron encontrados? ¿cuántos en animales?

En *Nucleotide* fueron encontrados un total de 70748 items para GAPDH, donde 13419 son de animales [30](https://www.ncbi.nlm.nih.gov/nuccore/?term=GAPDH).

- Probablemente tus resultados fueron una mezcla de fragmentos de genes, regiones codificantes parciales, genes completos, etc. Filtra tus datos por mRNA, animales, RefSeq.
	Haz clic en la entrada para la secuencia de GAPDH de gallina. 
	¿Cuál es la longitud del gen? 
	
El gen GAPDH para *Gallus gallus* tiene una longitud de 1288 pb según *Nucleotide* [31](https://www.ncbi.nlm.nih.gov/nuccore/NM_204305.1).

- ¿Cuál es la referencia bibliográfica más reciente? 

La más reciente de las referencias bibliográficas reportada en *Nucleotide* es del 2 de diciembre de 2015 [32](https://www.ncbi.nlm.nih.gov/nuccore/NM_204305.1). Su referencia completa es [33](https://www.sciencedirect.com/science/article/pii/S0168170215300289?via%3Dihub):

Ren, Xiangang, Zhang, Lizhou, Gao, Yulong, Gao, Honglei, Wang, Yongqiang, Liu, Changjun, Cui, Hongyu, Zhang, Yanping, Jiang, Lili, Qi, Xiaole, Wang, Xiaomei, Binding chicken Anx2 is beneficial for infection with infectious bursal disease virus.Virus Research http://dx.doi.org/10.1016/j.virusres.2015.07.024 

- ¿Cuál es el número de acceso?

**NM_204305** es el número de acceso para mRNA de GAPDH de *Gallus gallus* en *Nucleotide* [34](https://www.ncbi.nlm.nih.gov/nuccore/NM_204305.1).

-  Secuencia de nucleótidos (mRNA) de GAPDH para *Gallus gallus*.

Formato FASTA

![gapdh_fasta](https://user-images.githubusercontent.com/37593827/37691280-683316bc-2c8f-11e8-84ab-f2401a88348b.png)



Formato NEXUS/ non-interleaved

![gapdh_nexus](https://user-images.githubusercontent.com/37593827/37691279-67650006-2c8f-11e8-9267-85bc1f2c3aa4.png)


---

_**Parte cuatro:**_ Buscando artículos científicos en línea.

- Alerta *NCBI PubMed*

![alert_pubmed](https://user-images.githubusercontent.com/37593827/37693436-6e34e13a-2c9e-11e8-8bc3-69722856b587.png)

![alerta_ncbi](https://user-images.githubusercontent.com/37593827/37708511-b73877e2-2ce5-11e8-99bb-a4ee22e81dae.png)

- Alerta *Google Scholar*

![alerta_scholar](https://user-images.githubusercontent.com/37593827/37691284-6a985106-2c8f-11e8-885a-5aafd9ddd5b8.png)

- Confirmación de suscripción a *Nature*

![confirmacion](https://user-images.githubusercontent.com/37593827/37691282-694acfd6-2c8f-11e8-9012-130309fdaf20.png)

![confirmacion de suscripcion](https://user-images.githubusercontent.com/37593827/37707533-34ac521a-2ce2-11e8-8379-47232e1b1360.png)


---
*Preguntas 4.1* **Google Scholar**

Búsqueda de la palabra *Hedychium coronarium*.

- Ahora usa comillas para realizar tu búsqueda.
	¿Son los resultados idénticos o no?
	
Los resultados no son idénticos, ya que para el caso sin comillas el número de resultados obtenidos es mayor con respecto a la búsqueda realizada con comillas (siendo, 3540 y 3300 resultados para *Hedychium coronarium* y "*Hedychium coronarium*", respectivamente) [35](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=%22Hedychium+coronarium%22&btnG=) [36](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Hedychium+coronarium&btnG=	).

Según los sitios encontrados en las últimas páginas de búsqueda, se puede afirmar que escribir la palabra sin comillas permite obtener resultados un tanto "flexibles", donde únicamente se encuentre el género (*Hedychium*), por ejemplo. Por otro lado, con el uso de comillas solo se encuentran resultados que incluyan las dos palabras (*Hedychium coronarium*).

- También puedes usar * para representar una palabra que falta ("*Hedychium* +").
¿En qué cambiaron los resultados de la búsqueda?.

Teniendo en cuenta el número de resultados de la pregunta anterior, los obtenidos para este caso corresponden a la máxima cantidad de sitios encontrados (siendo estos, un total de 8710) [37](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=%22Hedychium+*%22&btnG=). Esto es muy razonable, debido a que, por razón del asterisco (refleja palabra faltante), se añade a la búsqueda las demás especies de *Hedychium*, por ejemplo.

- También puedes condicionar tus búsquedas a rangos de números como precios, años, etc. Prueba con 14 inch...17 inch laptops en google.com
¿Qué encuentras en los resultados? Prueba sin el rango también.

Al establecer el rango, se obtuvieron un total de 3.800.000 resultados, donde se pueden identificar páginas que dan cuenta del intervalo de pulgadas establecido [38](https://www.google.cl/search?q=14+inch...17+inch+laptops&rlz=1C5CHFA_enCO779CO779&ei=kWSxWqbCN8uswgTX9KWIDA&start=40&sa=N&biw=1366&bih=694). Por otro lado, al buscar solamente laptops, el número de resultados asciende hasta 235.000.000, y el número de pulgadas anterior ya no es la única característica del común de las páginas [39](https://www.google.cl/search?rlz=1C5CHFA_enCO779CO779&ei=0mSxWs3_K8GkwAS9n7WwAg&q=+laptops&oq=+laptops&gs_l=psy-ab.3..35i39k1j0i7i30k1l9.3526.3526.0.3679.1.1.0.0.0.0.59.59.1.1.0....0...1c.1.64.psy-ab..0.1.59....0.ZTjr3JP8MoQ).

- Para buscar artículos científicos también es útil restringir los resultados de búsqueda a tipos de archivo. Prueba con "*Hedychium coronarium*" filetype:pdf.
Describe tus resultados.

Solo se obtuvieron 924 resultados, donde la mayoría conducen a un archivo en formato pdf o a sitios web que lo contienen (es coherente que el número de resultados haya disminuido tanto con respecto a *Hedychium coronarium*, ya que ahora hay una condición altamente limitante) [40](https://scholar.google.com/scholar?start=0&q=%22Hedychium+coronarium%22+filetype:pdf&hl=en&as_sdt=0,5) [41](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Hedychium+coronarium&btnG=&oq=he).

- Otro truco útil es usar signos - y +. Por ejemplo, trata buscar "PCR amplification" +temperature, y luego "PCR amplification" -temperature.
¿En qué cambian los resultados de la búsqueda?

Para el caso del signo "+", todos los resultados de la búsqueda contienen la palabra "temperature" [42](https://scholar.google.cl/scholar?q=%22PCR+amplification%22+%2Btemperature&hl=en&as_sdt=0&as_vis=1&oi=scholart&sa=X&ved=0ahUKEwjiycGw1vvZAhXEHJAKHbRdCqAQgQMIJjAA). Por el contrario, con el signo "-", el criterio  "temperature" no aparece en ellos [43](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=%22PCR+amplification%22+-temperature&btnG=).

- Finalmente, prueba los operadores Boolean que representan opciones de inclusión. Por ejemplo, trata con Soil OR Human pathogens y luego trata con Soil AND Human pathogens.
	De nuevo, ¿en qué cambian los resultados de la búsqueda?

La búsqueda con el operador OR resultó en sitios web que contienen uno de los dos elementos o los dos; por el contrario, con el operador AND, solo se obtienen resultados que contienen ambos elementos. Las razones anteriormente expuestas, justifican el porqué hay más resultados al utilizar OR [44](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Soil+OR+Human+pathogens+&btnG=) [45](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Soil+AND+Human+pathogens&btnG=). 








