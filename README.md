# VO - RPE (Registre de Parelles Estables)

ESBORRANY

Versió	Data	Autor	Comentaris
V1.0	01/03/2022	Roger Noguera i Arnau	Creació del document
| | | | | | | | | | | | | | | | | | | | | | | | | | | | | |

Índex

[1Introducció 1](# RefHeading_ Toc97198252)

[2Transmissions de dades disponibles 1](# RefHeading_ Toc97198253)

[3Missatgeria dels serveis 1](# RefHeading_ Toc97198254)

[3.1Situació d'un titular al Registre de Parelles Estables (RPE_CONSULTA) 1](# RefHeading_ Toc97198255)

[3.1.1Petició – dades genèriques 1](# RefHeading_ Toc97198256)

[3.1.2Petició – dades específiques 2](# RefHeading_ Toc97198257)

[3.1.3Resposta – dades específiques 2](# RefHeading_ Toc97198258)

[3.2Verificació d'un titular al Registre de Parelles Estables (RPE_CONSULTA) 3](# RefHeading_ Toc97198259)

[3.2.1Petició – dades específiques 3](# RefHeading_ Toc97198260)

[3.2.2Resposta – dades específiques 3](# RefHeading_ Toc97198261)

1Introducció
Aquest document detalla la missatgeria associada al servei de consulta del Registre de Parelles Estables (en endavant RPE) del Departament de Justícia.

Per poder realitzar la integració cal conèixer prèviament la següent documentació:

Document de Missatgeria Genèrica de la PCI del Consorci AOC.
2Transmissions de dades disponibles
Les dades disponibles a través del servei són les que es presenten a continuació:

EMISSOR
Departament de Justícia (Generalitat de Catalunya)
PRODUCTE
RPE
| | --- | --- | --- | | RPE_VERIFICACIO | Consulta de situació d'un titular al Registre de Parelles Estables en un moment donat a partir d'un o dels dos membres de la parella. |

Totes les consultes del producte tenen disponible la versió imprimible del resultat de la consulta en format PDF. Per més detalls adreceu-vos a l'apartat Extensions de missatgeria del document de missatgeria genèrica.

3Missatgeria dels serveis
A continuació es detalla la missatgeria corresponent al bloc de dades específiques de les modalitats de consum del producte RPE.

3.1Situació d'un titular al Registre de Parelles Estables (RPE_CONSULTA)
3.1.1Petició – dades genèriques
Element	Descripció
//DatosGenericos/Titular/TipoDocumentacion	Tipus de document identificador (cal informar l'element però el servei no el té en compte).
| | --- | --- | | //DatosGenericos/Titular/Documentacion | Document identificador del titular a consultar. |

3.1.2Petició – dades específiques
Element	Descripció
peticioConsultaParellesEstables/data	
Bloc de dades opcional. Data en la que es vol conèixer la situació del titular al registre.	
| | --- | --- |



3.1.3Resposta – dades específiques


Element	Descripció
respostaConsultaParellesEstables/peticioConsultaParellesEstables	
| Bloc de dades corresponent a la petició que genera la resposta. | | --- | --- | | //resposta/dataInscripcio | Data d'inscripció de la parella (AA/MM/DDDD). | | //resposta/dataExtincio | Data d'extinció de la parella (AA/MM/DDDD). | | //resposta/estat | Estat en el que consta al registre:

Inscrit
No inscrit
| | //resposta/membre1 | Nom i cognoms del primer membre de la parella. | | //resposta/membre2 | Nom i cognoms del segon membre de la parella. | | respostaConsultaParellesEstables/resultat/codiResultat | Codi de resultat de la consulta:

0: consulta realitzada correctament.
0502: error realitzant la consulta.
| | respostaConsultaPrestacions/resultat/descripció | Descripció del resultat. |

3.2Verificació d'un titular al Registre de Parelles Estables (RPE_CONSULTA)
3.2.1Petició – dades específiques


Element	Descripció
peticioVerificacioParellesEstables/document1	
Document identificador d'un membre de la parella a consultar (no es té en compte el tipus de document).	
| | --- | --- | | peticioVerificacioParellesEstables/document2 | Document identificador d'un membre de la parella a consultar (no es té en compte el tipus de document). | | peticioVerificacioParellesEstables/data | Data en la que es vol conèixer la situació dels titulars al registre. |

3.2.2Resposta – dades específiques
Element	Descripció
respostaVerificacioParellesEstables/peticioVerificacioParellesEstables	
| Bloc de dades corresponent a la petició que genera la resposta. | | --- | --- | | //resposta/dataInscripcio | Data d'inscripció de la parella (AA/MM/DDDD). | | //resposta/dataExtincio | Data d'extinció de la parella (AA/MM/DDDD). | | //resposta/estat | Estat en el que consta al registre:

Inscrit
No inscrit
| | respostaVerificacioParellesEstables/resultat/codiResultat | Codi de resultat de la consulta:

0: consulta realitzada correctament.
0502: error realitzant la consulta.
| | respostaVerificacioPrestacions/resultat/descripció | Descripció del resultat. |

