# Laboratorio 04 - Filogenética Molecular

### Bioinformática BIOL350

### Camilo Cano Salazar

----

_**Parte 1:**_ Plataforma phylogeny.fr y preparación de datos

_Preguntas 1.1_

- ¿Qué cosas ofrece este portal? 

Siendo una plataforma que pretende integrar diversos programas con oficio en el análisis filogenético, Phylogeny.fr ofrece la posibilidad de emplear diferentes herramientas de forma simple como optimización combinatoria, modelos probabilísticos, métodos de estimación de parámetros, entre otros. Todo esto con el objetivo de identificar secuencias homólogas, realizar alineamientos múltiples, reconstruir filogenias, y representar de forma gráfica los árboles inferidos (Dereeper, 2008) [1](http://www.lirmm.fr/recherche/equipes/mab) [2](http://www.phylogeny.fr/documentation.cgi). 

- ¿Para qué tipo de usuario está diseñado?

Según los indicado en la página de documentación, esta herramienta tiene como premisa principal ofrecer una plataforma de alto rendimiento que pueda ser empleada por biólogos o cualquier otra persona que tenga interés en el análisis de información para la reconstrucción de filogenias, sin la necesidad de que posea alta experticia en estos temas; además, al ser una interfaz gráfica da la posibilidad de prescindir de _scripting_. "One Click Mode" es uno de los tres modos que ofrece la página que puede ser utilizado por personal no capacitado. Este permite esclarecer las relaciones genealógicas de un conjunto de secuencias sin realizar ninguna intervención o modificación en los parámetros o programas, debido a que la configuración ya viene predeterminada (Dereeper, 2008) [3](http://www.phylogeny.fr/documentation.cgi).

- Menciona 5 tipos de análisis que se pueden realizar en el portal de acuerdo con la documentación.

Según la pestaña de documentación, estos son algunos de los tipos de análisis que se pueden realizar [4](http://www.phylogeny.fr/documentation.cgi#moreinfo): 

_Para alineamiento múltiple:_ MUSCLE, T-Coffee/ 3D-Coffee, ClustalW, y ProbCons.

_Para reconstrucción de filogenia:_ PhyML, TNT, ProtDist/FastDist + BioNJ, ProtDist/FastDist + Neighbor, y MrBayes.
	
_Para refinar alineamiento:_ Gblocks.

-------

_Preguntas 2.2_

- ¿A qué se refiere el paso de *Alignment curation* y para qué sirve?

Es una opción que permite eliminar regiones poco informativas o de baja calidad después de hacer el alineamiento [5](http://molevol.cmima.csic.es/castresana/Gblocks/Gblocks_documentation.html). Estas por lo general representarían regiones que no son homólogas y no dan cuenta de un proceso biológico; por tanto, sería coherente ignorarlas pues de lo contrario se introduciría ruido al resultado final y la filogenia sería menos resolutiva [6](http://molevol.cmima.csic.es/castresana/Gblocks/Gblocks_documentation.html).


- ¿Cuál es la diferencia entre BioNJ y Neighbor? (Pista: revisa la documentación)

Aunque ambos son algoritmos de reconstrucción para estimar las distancias entre secuencias de DNA o proteínas, BioNJ es una versión mejorada de Neighbor-joining, la cual cuenta con una mayor precisión topológica e importancia cuando se trata de resolver casos con altas tasas de sustitución y con gran variación entre las taxa.  Otra de las diferencias más relevantes está relacionada con las limitantes que tiene cada algoritmo para analizar determinado número de taxa (Gascuel, 1997) [7](http://www.phylogeny.fr/documentation.cgi#moreinfo). Mientras BioNJ puede ser aplicado hasta para 5000 taxa, Neighbor puede aceptar un máximo de 500 [8](http://www.phylogeny.fr/documentation.cgi#moreinfo) [9](http://www.atgc-montpellier.fr/bionj/).
_____________________________________________

**Comparación entre árboles inferidos**

_Los órdenes identificados para el análisis de filogenias inferidas fueron:_

|      Orden     |                                                                            Especies                                                                            |
|:--------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Chiroptera     | Miniopterus natalensis y Pteropus alecto                                                                                                                       |
| Artiodactyla   | Bos taurus, Bos indicus, Bison bison bison, Odocoileus virginianus, Capra hircus, y Camelus ferus                                                              |
| Perissodactyla | Equus asinus y Equus przewalskii                                                                                                                               |
| Rodentia       | Marmota marmota y Fukomys damarensis                                                                                                                           |
| Carnivora      | Odobenus rosmarus, Ursus maritimus, Neomonachus schauinslandi                                                                                                  |
| Primates       | Macaca mulatta, Chlorocebus sabaeus, Rhinopithecus roxellana, Rhinopithecus bieti, Piliocolobus tephrosceles, Pan troglodites, Homo sapiens, y Cebus capucinus |

-----
- **Árbol 1** (ProbCons, GBlocks, MrBayes, y TreeDyn)

![1](https://user-images.githubusercontent.com/37593827/38618167-32b16f5c-3d6f-11e8-9112-b57b385a5f5e.png)


- **Árbol 2** (ClustalW, "Remove positions with gaps", TNT, y TreeDyn)

![2](https://user-images.githubusercontent.com/37593827/38618166-3295c9d2-3d6f-11e8-91c0-d3d877b75b27.png)

**_Descripción_**

No entrando mucho al detalle sobre el efecto de cada uno de los métodos empleados para inferir los árboles, es evidente, sin tener en cuenta el estado de las agrupaciones, que la filogenia inferida por parsimonia (_árbol 2_) resuelve más las relaciones genealógicas de las secuencias SRY, pues las politomías presentadas (siendo esto, nodos sin resolver) no son tantas comparadas con el árbol obtenido por inferencia bayesiana (_árbol 1_). Por otro lado, también es relevante considerar que la hipótesis de evolución para algunos de los órdenes en términos de sus agrupaciones tiende a cambiar al compararlos. A continuación, se expondrán algunas de las similitudes y diferencias más relevantes (solo se considerarán los órdenes que posean más de dos especies) en agrupación:

- Todos los ortólogos del gen SRY evaluados para construir los árboles pertenecen a organismos de la clase Mammalia, a excepción de la especie _Gavia stellata_ (colimbo chico) que es de la clase Aves. Aunque el ave derivó del mismo ancestro, es posible afirmar que la relación que posee con los demás organismos no es muy cercana como la que pueden mantener los mamíferos entre sí, por lo que es flagrante que este sería el grupo externo (esta afirmación solo es válida si es un ortólogo verdadero). El _árbol 1_ es el único que obedece a la discusión anterior, mientras que el árbol inferido por parsimonia ubica al ave como clado hermano del orden Perissodactyla; por tanto, esta filogenia puede ser considerada en su totalidad como un clado parafilético.

- En ambos árboles inferidos, los dos mayores órdenes (siendo estos, Primates y Artiodactyla) son monofiléticos. Este es el mismo caso de Perissodactyla.

- El orden Chiroptera para el _árbol 1_ es un clado parafilético. Por otro lado, en el _árbol 2_ es monofilético.

- Rodentia para el _árbol 1_ no se resuelve como un clado natural, mientras que para el _árbol 2_ es polifilético.

- Carnivora es parafilético para el _árbol 1_ y monofilético para el _árbol 2_.

---------

**Comparación entre árboles inferidos y su modificación sin _Alignment curation_**

- **Árbol 1** (ProbCons, GBlocks, MrBayes, y TreeDyn)

![1](https://user-images.githubusercontent.com/37593827/38618167-32b16f5c-3d6f-11e8-9112-b57b385a5f5e.png)

- **Árbol 1.1** (ProbCons, sin _Alignment curation_, MrBayes, y TreeDyn)

![1 1](https://user-images.githubusercontent.com/37593827/38618165-3278997a-3d6f-11e8-955d-802c690446cb.png)

**_Descripción_**

Al comparar las dos filogenias inferidas, se puede afirmar que la obtenida para el caso sin _alignment curation_ logró resolver más relaciones entre las secuencias del gen SRY, ya que solo se pueden identificar dos politomías correspondientes a los órdenes Chiroptera y Artiodactyla (para este último específicamente con las especies _Bos indicus_, _Bos taurus_, y _Bison bison bison_), las cuales siguen siendo menos que para el árbol al que se le aplicó la curación. 

En términos de las posibles agrupaciones que se pueden establecer para los órdenes, la mayor parte de los casos no presenta modificaciones. Los órdenes Primates, Artiodactyla, y Carnivora continúan siendo grupos monofiléticos (agrupaciones naturales). No obstante, uno de los cambios más relevantes después de eliminar el _alignment curation_, corresponde al caso de Rodentia, ya que para esta nueva inferencia el clado conformado por sus dos especies se pudo resolver, y ahora se dispone en la filogenia como una agrupación monofilética y grupo hermano de la especie _Tupaia chinensis_ (orden Scandentia). También es importante resaltar que el orden Chiroptera (representado aquí por las especies _Pteropus alecto_ y _Miniopterus natalensis_) sigue sin resolverse, y que la secuencia correspondiente al ave continúa siendo el grupo externo.


----------

- **Árbol 2** (ClustalW, "Remove positions with gaps", TNT, y TreeDyn)

![2](https://user-images.githubusercontent.com/37593827/38618166-3295c9d2-3d6f-11e8-91c0-d3d877b75b27.png)

- **Árbol 2.1** (ClustalW, sin _Alignment curation_, TNT, y TreeDyn)

![2 1](https://user-images.githubusercontent.com/37593827/38618164-3256aef0-3d6f-11e8-9e38-31ab7c8ffc90.png)

**_Descripción_**
	
Con respecto a las demás descripciones de comparación de árboles inferidos, esta es, por lejos, la que más diferencias posee. Inicialmente, igual que para el caso anterior, la filogenia obtenida sin _alignment curation_ alcanza una mayor resolución de las relaciones genealógicas, pues las politomias del orden Artiodactyla, y el orden Rodentia con las especies _Tupaia chinensis_ y _Galeopterus variegatus_ fueron resueltas (algo no alcanzado por el árbol al que sí se le aplicó la curación). Es relevante comentar, solo como observación, que esta es la única de todas las filogenias inferidas que cuenta con una gran cantidad de ancestros comunes; además, el árbol inferido tiene como clados externos a especies del orden Carnivora, lo que indica, al igual que para el caso que si se obtuvo con _alignment curation_, que toda la filogenia es un clado parafilético (el ave está relacionada con el murciélago _Pteropus alecto_).

Al evaluar las agrupaciones de los órdenes se encuentra que muchas de ellas han cambiado al no realizar el _alignment curation_. Las dos especies de Perissodactyla ya no son clados hermanos, lo que las lleva a ser un grupo artificial (polifilético en este caso). Rodentia dejó de ser un clado polifilético, y pasó a ser grupo hermano de _Miniopterus natalensis_ como grupo monofilético. Por su lado, Chiroptera pasó a ser una agrupación polifilética cuando era monofilética. En el caso del orden Primates, la característica de clado natural se perdió al inferir la filogenia sin _alignment curation_, ya que al establecerse _Equus asinus_ y _Tupaia chinensis_ como grupos hermanos de especies del clado que derivaron recientemente, los primates ahora son parafiléticos. Finalmente, Artiodactyla y Carnivora continuaron siendo clados monofilético y parafilético, respectivamente. 


------
**Respaldo de árboles inferidos**

![1](https://user-images.githubusercontent.com/37593827/38492485-70f86032-3bc5-11e8-89a6-e53d5e333f23.png)
![1 1](https://user-images.githubusercontent.com/37593827/38492488-72f61104-3bc5-11e8-879f-eb78dd34aa1e.png)
![2](https://user-images.githubusercontent.com/37593827/38492491-75fbe5f4-3bc5-11e8-87bc-cccafeeddd55.png)
![2 1](https://user-images.githubusercontent.com/37593827/38492494-7795bde0-3bc5-11e8-937f-e2f76a557cb6.png)

-----
**Referencias**

- Dereeper, A., Guignon, V., Blanc, G., Audic, S., Buffet, S., Chevenet, F., … Gascuel, O. (2008). Phylogeny.fr: robust phylogenetic analysis for the non-specialist. Nucleic Acids Research, 36(Web Server issue), 465–469.  

- Gascuel, O. (1997). BIONJ: an improved version of the NJ algorithm based on a simple model of sequence data. Molecular Biology and Evolution, 14(7), 685–695. 
