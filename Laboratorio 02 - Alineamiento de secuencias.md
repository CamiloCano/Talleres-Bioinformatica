# Laboratorio 02 - Alineamiento de secuencias

### Bioinformática BIOL350

### Camilo Cano Salazar

----
_**Parte 1:**_ Colectar genes homólogos

_Preguntas 1.1_

- ¿Qué función cumple el gen SRY?

El gen, encontrado en el cromosoma Y, codifica para la proteína _sex-determining region Y protein_, la cual está involucrada en la determinación del sexo masculino. La proteína siendo un factor de transcripción, cuenta con la funcionalidad de regular el perfil génico de expresión celular uniéndose a sitios específicos del DNA, logrando así, estimular procesos vinculados con la formación de testículos, e inhibir aquellos relacionados con el desarrollo de estructuras reproductivas femeninas, por ejemplo [1](https://www.ncbi.nlm.nih.gov/gene/6736) [2](http://omim.org/entry/480000) [3](https://ghr.nlm.nih.gov/gene/SRY).

- ¿Cuántos genes ortólogos están anotados en esa base de datos?

*Gene* reporta un total de 27 genes ortólogos [4](https://www.ncbi.nlm.nih.gov/gene/?Term=ortholog_gene_6736%5Bgroup%5D). 

----


_**Parte 2:**_ Alineamiento múltiple 


_Preguntas 2.1_

- ¿Qué es el EMBL-EBI?

Haciendo parte del _Laboratorio Europeo de Biología Molecular_, este es un instituto encargado de, además de realizar investigación en biología computacional, ofrecer servicios relacionados con herramientas bioinformáticas, masificar tecnologías vanguardistas, brindar programas para capacitación de usuarios, y compartir información de experimentos en ciencias biológicas; todo lo anterior con el objetivo de apoyar la industria y la academia [5](https://www.ebi.ac.uk/) [6](https://www.ebi.ac.uk/about).

- ¿Cuántos tipos de alineamiento múltiple se pueden realizar en EMBL-EBI?

Los tipos de alineamiento múltiple que se pueden realizar son [7](https://www.ebi.ac.uk/Tools/msa/):
		
	Clustal Omega
	Kalign	
	MAFFT
	MUSCLE
	T-Coffee
	WebPRANK
			
	

- ¿Cuál es el programa que ellos ofrecen que funciona mejor para secuencias de proteínas?

Según la página, MUSCLE es el mejor programa para secuencias proteicas [8](https://www.ebi.ac.uk/Tools/msa/). 

- ¿Qué otros tipos de herramientas ofrece EMBL-EBI?

Los tipos de herramientas que ofrece el instituto son [9](https://www.ebi.ac.uk/services/all):

	DNA & RNA
	Gene Expression
	Proteins
	Structures
	Systems
	Chemical biology
	Ontologies
	Literature
	Cross domain 



----

_Preguntas 2.2_

- ¿Cuál es el costo de abrir un _gap_?

El costo de abrir un _gap_ es 1.53 [10](https://www.ebi.ac.uk/Tools/msa/mafft/).

- ¿Cuál es el costo de extender un _gap_?

Extender un _gap_ cuesta 0.123 [11](https://www.ebi.ac.uk/Tools/msa/mafft/).


----


_Pregunta 2.3_ 

- ¿Cuál es la longitud total del alineamiento?

Según la secuencia consenso obtenida, la longitud total del alineamiento es de 1905 pb.

-----
_Preguntas 2.4_ 

- 	¿Cuál es la especie cuyo gen SRY está más relacionado con el gen SRY de humanos?

A partir del árbol filogenético obtenido, se puede evidenciar que el gen SRY de *Homo sapiens* está más relacionado al gen SRY de *Pan troglodytes* (siendo este, clado hermano).
 
- ¿Cuál es el más lejano?

Es evidente que el árbol filogenético resultante cuenta con una inconsistencia. El evento de especiación del ancestro común de todas las taxas resulta en tres líneas independientes; por tanto, es claro que la información suministrada no es suficiente para determinar las relaciones ancestro-descendientes del gen dado a tal nivel. Por lo anterior es correcto afirmar que los respectivos genes SRY de todas las terminales de los clados S y D (ver figura anexa) son los más lejanos al gen SRY de *Homo sapiens*. 


![screen shot 2018-03-24 at 2 38 46 pm](https://user-images.githubusercontent.com/37593827/37867007-3f9152de-2f71-11e8-8bc9-ff1d9cd88cce.png)

**Anexo 1.** *Árbol filogenético del gen SRY*. Las terminales agrupadas en los caldos S y D corresponden a las especies más alejadas evolutivamente de *Homo sapiens* con respecto al gen SRY.


- ¿Cuál es la especie cuyo gen SRY es más cercana a la del burro? 

Reconociendo las relaciones ancestro-descendientes del gen SRY, se puede afirmar que la especie *Equus asinus* (burro) está más cercana a *Equus przewalskii* (caballo salvaje mongol) que a cualquier otra taxa (esto es, en el anexo 1 del punto anterior, el clado D).

------

_Preguntas 2.5_ 

- ¿Cómo esperas que sea el alineamiento si el costo de abrir un _gap_ aumenta? ¿Y si disminuye?

Teóricamente, el objetivo final del alineamiento, incluyendo además el estado del resultado, es aquel que tienda a maximizar el beneficio o a minimizar el costo, obedeciendo a los valores de penalización de una matriz dada (Rosenberg, 2009). Según la premisa anterior, creo que aumentar el costo de abrir un _gap_ supondría que el alineamiento se construyera con pocos _gaps_; por el contrario, en el caso donde la penalización por abrir sea menor, esperaría encontrar más _gaps_.

- ¿Cómo esperas que sea el alineamiento si el costo de extender un _gap_ aumenta? ¿Y si disminuye?

Manteniendo el mismo concepto teórico anterior, al realizar un alineamiento de secuencias con un valor de extensión grande, creería que habría una tendencia de los _gaps_ a ser más cortos. Si la modificación es contraria, ahora con una penalización baja, esperaría que no hubiera restricciones para construir _gaps_ de longitud considerablemente alta.

______

**Nota:** la justificación de las dos respuestas anteriores no incluye lo que se cree que puede suceder a la longitud total de la secuencia consenso, ya que después de considerar varios escenarios posibles, producto de la combinación de distintos valores de penalización, no se identifica un patrón de cambio o correlación con el número de nucleótidos. Aquí hay una prueba de ello:


Para un valor de _Gap open penalty_ fijo (siendo este, 1.53) se obtuvieron los resultados de longitud de secuencia consenso a medida que el _Gap extension penalty_ aumenta.
 
| Gap extension penalty    | Lenght (pb)    |       
| ------------- | ------------- | 
|  0  | 1973 |          
| 0.1 | 1927                
| 0.2 | 1957              
| 0.3 | 1948 
| 0.4 | 1893
| 0.5 | 1851
| 0.6 | 1861
| 0.7 | 1846
| 0.8 | 1846
| 0.9 | 1846
| 1   | 1846

Es evidente que para el caso anterior no se puede establecer una correlación entre el aumento de la penalización y el cambio de longitud. Aunque se puede ver que este último tiende a estabilizarse, considerar esta afirmación como verdadera sería una tanto apresurado, ya que se requieren evaluar más variables.

--------

_Preguntas 2.6_

- ¿Cuál fue el efecto de aumentar el costo de abrir un _gap_ en la longitud total del alineamiento?
	prueba lo mismo pero esta vez disminuyendo al mínimo el costo de extender un _gap_. Describe cómo cambia el alineamiento. 
	
_Resultados para los tres casos_:


| Case     | Open penalty     |   Extension penalty | Length|     
| ------------- | ------------- | ---------| ----------|
| 1 | 1.53 |     0.123      | 1905 pb
|  2| 2 |       0.123    |        1957 pb    
| 3 |  1.53             |     0      |   1973 pb
		
Teniendo en cuenta que los valores del caso 1 arrojaron una longitud de 1905 pb, al aumentar el costo de abrir un _gap_ a 2 (siendo antes, 1.53) para el caso 2, se puede evidenciar en la secuencia consenso un aumento de su longitud total a 1957 pb. Por otro lado, manteniendo el valor predeterminado de apertura de un _gap_, disminuir el costo de extensión a 0 para el caso 3 (siendo antes, 0.123) resulta en una longitud total de alineamiento de 1973 pb. 

----


_**Parte 3:**_ Diseño de partidores

- Partidores encontrados:
	
		Forward: 5' CCGCCGTTCAACAAaayathccngc 3'
		Reverse: 3' tacstygtrgtTGATCCGGTGGATGGG 5'

**Nota**: las letras mayúsculas de ambos partidores corresponden a nucleótidos. Las letras minúsculas son aminoácidos, donde quieren significar que cualquier codón que los codifique puede ser ubicado en ese lugar.
 
 
_Ventana arrojada por el programa:_


![pprimers](https://user-images.githubusercontent.com/37593827/37870035-cee90856-2fa2-11e8-83e4-02c33da09a7d.png)

-----


**Referencias**  

Rosenberg, M. S., (2009), _Sequence Alignment Methods, Models, Concepts, and Strategies_, Los Angeles, California: University of California Press. 







