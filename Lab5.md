

# Laboratorio 05 - Metagenómica

### Bioinformática BIOL350

### Camilo Cano Salazar

----

_**Parte 1:**_ Plataforma MG-RAST y exploración de metagenomas

_Preguntas 1.1_

- ¿Cuántas secuencias fueron subidas? 

Según la información reportada, un total de 120,671 secuencias fueron subidas por el estudio [1](http://www.mg-rast.org/mgmain.html?mgpage=overview&metagenome=mgm4441593.3).

- ¿Qué tipo de plataforma de secuenciamiento fue usada para producir estos datos?

Revisando el artículo publicado, _AB3730xl sequencer_ es el nombre de la plataforma de secuenciamiento empleada (siendo su marca, _Applied Biosystems_) (Dereeper _et al_, 2008).

- ¿Cuántas secuencias pasaron el control de calidad? ¿A qué crees que se refiere esto?

Partiendo de lo encontrado en la página, un total de 0 secuencias pasaron el control de calidad [2](http://www.mg-rast.org/mgmain.html?mgpage=overview&metagenome=mgm4441593.3). Lo anterior no indica que no se realizó el control o que ninguna secuencia lo pasó, simplemente da a entender que el proceso de filtración se hizo previamente y la información resultante no fue reportada en la plataforma.

_Quality Control_ es básicamente una estrategia empleada para filtrar aquellas secuencias que cuentan con una poca confiabilidad por bajos valores de calidad en sus posiciones nucleotídicas (normalmente encontrados hacia el extremo 3'). El método de filtración podrá cortar aquellos nucleótidos de baja calidad si es que son pocos, o eliminará la secuencia directamente si estos superan el 50% del total de la longitud.

- ¿Cuántos otros metagenomas están disponibles para el bioma “marine habitat”?

Empleando los filtros de búsqueda, el bioma _marine habitat_ cuenta con otros 6,968 metagenomas disponibles.

- ¿Cuántas reads fueron asignadas a eucariontes según MG-RAST?

A partir de la gráfica de _Taxonomic Category Hits Distribution_ para dominio, 9,207 _reads_ (13.03% del total) fueron asignadas a eucariontes [3](http://www.mg-rast.org/mgmain.html?mgpage=overview&metagenome=mgm4441593.3). 

- ¿Cuál es el filo (Phylum) más abundante en la muestra?

Según la gráfica de _Taxonomic Category Hits Distribution_ para filo, Cyanobacteria es el más abundante de la muestra contando con un total de 22,956 secuencias (37.03% del total) [4](http://www.mg-rast.org/mgmain.html?mgpage=overview&metagenome=mgm4441593.3).

- ¿A cuántas secuencias se les asignó una función de acuerdo a la base de datos KEGG con un e-value entre -10 y -20?

Según _MG-RAST_, 7,960 son el total de secuencias a las cuales se les asignó una función de acuerdo con la base de datos _KEGG_ en el intervalo de _e-value_ especificado [5](http://www.mg-rast.org/mgmain.html?mgpage=overview&metagenome=mgm4441593.3).

- ¿Por qué hay tan pocas secuencias con funciones asignadas según SwissProt?

_SwissProt_, partiendo de lo comentado en clase, es una base de datos curada, es decir, la información depositada está respaldada por varios niveles de evidencia; por tanto, el número de secuencias, a pesar de contar con alta calidad en su información, es bajo comparado con otras bases no curadas. 

Según el proceso de biocuración de _Uniprot Consortium_, _Swiss-Prot_ (siendo esta, una de sus dos secciones) posee una curación donde se pretende revisar los registros con anotaciones obtenidas de la literatura y evaluar el análisis computacional [6](http://www.uniprot.org/help/biocuration). Todo lo anterior se hace de forma manual (esto es contrario a lo realizado con la otra sección, _TrEMBL_, donde la curación es automática), lo que explica las pocas secuencias disponibles para poder hacer transferencias funcionales (solo hay 557,275) [7](http://www.uniprot.org) [8](http://www.uniprot.org/help/biocuration).



--------
_Preguntas 1.2_

- ¿Cuántas secuencias mapearon en contra de Proteobacteria?

Un total de 24,194 secuencias mapearon en contra de Proteobacteria.

- ¿Cuántas secuencias de Salmonella (Proteobacteria; Gammaproteobacteria; Enterobacteriales; Enterobacteriaceae) fueron identificadas? (Pista: level - genus)

Fueron identificadas 72 secuencias para el género _Salmonella_.

-------

**Referencias**

- Dereeper, A., Guignon, V., Blanc, G., Audic, S., Buffet, S., Chevenet, F., … Gascuel, O. (2008). Phylogeny.fr: robust phylogenetic analysis for the non-specialist. Nucleic Acids Research, 36(Web Server issue), 465–469. https://doi.org/10.1093/nar/gkn180


