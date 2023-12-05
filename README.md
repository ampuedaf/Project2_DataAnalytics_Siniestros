### PROYECTO INDIVIDUAL Nº2
 ##Siniestros Viales en las 15 Comunas de Buenos Aires  con víctimas       fatales -(2016-2021).
<p align="center">
<a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/Kck0nx1D/ampcont2.jpg' border='0' alt='ampcont2'/></a>
</p>
<p align="center">
<a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/6p5j4Rny/siniestro.jpg' border='0' alt='siniestro' width="550" height="150"/></a>
</p>
#Indice.

- Introducción.
- Contenido del repositorio.
- Contexto de los datos.
- Flujo de trabajo.
- ETL.
- EDA.
- Propuesta de negocio.
- Herramientas utilizadas.
- Colaboradores.


# Introducción.
Consideraciones generales acerca de los siniestros de tránsito

Argentina ostenta uno de los índices más altos de mortalidad por siniestros de tránsito.

19 personas mueren por día; hay 6.627 víctimas fatales por año (2019) y unos 120 mil heridos de distinto grado y miles de discapacitados. Las pérdidas económicas del tránsito caótico y accidentes de tránsito superan los U$S 10.000 millones anuales.

Pero no se trata de números, sino de vidas humanas. De hombres, mujeres, jóvenes y niños, que vieron truncadas sus vidas a causa de un accidente de tránsito.

Son proyectos, sueños, ilusiones y esperanzas muertas. Familias destrozadas. Luchar para transformar esta realidad es el objetivo de Luchemos por la Vida.

Es como si un avión de pasajeros cayera todas las semanas muriendo unas 130 personas cada vez. Y si así ocurriera, seguramente, no estaríamos tan tranquilos. Las autoridades tomarían graves y urgentísimas medidas de seguridad.

No sucede lo mismo con los siniestros de tránsito. Tal vez, porque las muertes se producen de a una, de a dos, o de a tres. Los muertos en el tránsito no nos "llegan" tanto. Se los considera lejanos, creyendo que son cosas que les ocurren "a otros". Difícilmente se cree que cualquiera puede sufrir uno en el momento menos pensado. Nadie al subir a un automóvil experimenta el miedo que muchas veces se siente al despegar dentro de un avión.

Sin embargo, los siniestros de tránsito en la Argentina, son la primera causa de muerte en menores de 35 años, y la tercera sobre la totalidad de los argentinos.

Las cifras de muertos son elevadísimas, comparadas con las de otros países (ver cuadro), llegando a tener 8 o 10 veces más víctimas fatales que en la mayoría de los países desarrollados, en relación al número de vehículos circulantes.

Al momento de los hechos, se dan muchas explicaciones (algunas reales, otras no tanto) pero que suelen poner siempre el acento -la culpa- del accidente en "los otros". Rara vez se analiza la conducta en el tránsito en primera persona.

 Para este  proyecto de análisis de datos estudiaremos  los  siniestros viales en la Ciudad de Buenos Aires.

Objetivo: Identificar los principales factores y patrones asociados a los siniestros viales en la Ciudad de Buenos Aires , con el fin de proponer medidas y políticas efectivas para reducir la incidencia de accidentes de tránsito y mejorar la seguridad vial.

Este proyecto de análisis de datos nos enfocamos en recopilar y analizar información relevante sobre los siniestros viales en la Ciudad de Buenos Aires, incluyendo datos sobre ubicación (especificamente las **15 comunas centrales de Buenos Aires**), tipo de accidente,  Tipo se siniestros, factores humanos y vehiculares, entre otros. A partir de este análisis, se buscaría identificar los principales factores que contribuyen a los accidentes de tránsito y entender los patrones de incidencia.

Algunas  acciones que se  derivaron en  este proyecto incluyen:

Identificación de  zonas de la ciudad con mayor incidencia de siniestros viales y proponer medidas específicas para mejorar la seguridad vial en esas áreas.
Analizar los factores humanos involucrados en los accidentes de tránsito, como el exceso de velocidad, el consumo de alcohol, el uso de dispositivos móviles, entre otros, y proponer campañas de concientización y educación para abordar estos problemas.
Evaluar la infraestructura vial y proponer mejoras en la señalización, diseño de calles y cruces, y otros aspectos que puedan contribuir a la reducción de los accidentes de tránsito.
Analizar la efectividad de las políticas y regulaciones existentes en materia de seguridad vial y proponer ajustes o nuevas medidas en base a los resultados obtenidos.
Es importante destacar que este objetivo es solo una propuesta y que un proyecto real de análisis de datos sobre siniestros viales en la Ciudad de Buenos Aires  requeriría una planificación más detallada y la definición de indicadores específicos para medir el éxito del proyecto.
 
 ##Contenido del Repositorio.

 - En la carpeta src se encuentran los recursos (imágenes) utilizadas para la elaboración del presente Readme.
 - En el archivo ETL se encuentra la documentación y el paso a paso del ETL.
 - En el archivo EDA se encuentra la documentación y el paso a paso del EDA.
 - En el archivo Dashboard se encuentra la presentación de Power Bi correspondiente al proyecto, la cual muestra el estado actual de los KPI´s.

##Contexto de los datos.
Los datos fueron suminstrados directamente por  estos enlaces:
Buenos Aires Data: **Homicidios**
Complementarios:
Buenos Aires Data:  dataset de **Lesiones**
Buenos Aires Data: Complementarios: usamos un datesets de las especificaciones de nombre y ubicación geografica de las distintas 15 comunas de Buenos Aires.  **comunas.xlsx**

 ##Diccionario de datos.
  Se tiene toda una documentación para el diccionario de datos. [ Diccionario](http://https://cdn.buenosaires.gob.ar/datosabiertos/datasets/transporte-y-obras-publicas/victimas-siniestros-viales/NOTAS_HOMICIDIOS_SINIESTRO_VIAL.pdf " Diccionario")

##Flujo de trabajo.

# ETL.
- Cambio de tipos de datos, así como extracción de puntos en variables numéricas.
- Unión de dataframes relacionadosy elección de columnas relevantes.  Caso especifico de  el dataframe de las comunas.
- Detección de valores con errores y noormalización de los mismos.
- Detección de nulos e imputación de los mismos. Los nulos  pudimos percibir que estan representados como SD (sin dato),   Nombrando  un caso particular en las coordenadas de los distintos siniestros ocurridos en las diversas comunas de buenos aires,  tuvimos que  buscar cada una de las coordenadas a traves de ciertas bibiliotecas de Python.

- Detección de duplicados. Las diferentes etapas de transformación se - - -  llevaron a cabo con el propósito de obtener un conjunto de datos de excelente calidad, coherente y pertinente para su posterior análisis. Al asegurar la limpieza y estandarización de los datos, se establece una base sólida para obtener conclusiones fiables y tomar decisiones fundamentadas.

- Creamos una columna nueva denomina "semestre" por año para  la ralización de los KPI. 

##EDA.



##Estudio de los Accidentes por mes  observando las distintas variaciones por cada uno de los años  (2016-2021).
<a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/hGStvLSf/victimas-mes.jpg' border='0' alt='victimas-mes'/></a>

###Conclusion:
- Podemos observar que  los años  2016, 2017 y 2019 en  el primer trimestre tienen un incremento proporcional. 
- En el año 2018 podemos corroborar que es el año donde hubo mas accidentes. teniendo como punto de inflexión el mes de agosto.
- El año 2020 es sumamente interesate, ya que hubo una gran disminución por la llegada del COVID 19, la cual fue decretada el 11 de marzo de ese año. observamos una disminución sucesiva, llegando a valores minimos en el mes de julio. Sin embago en el mes de diciembre fue el evento donde hubo maw siniestro en todo el estudio que realizamos, para un total de 26 victimas fatales.
### Estudio de   siniestros por sexo y victimas a traves de un grafico de dispersion.

<a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/gJM0hnMm/Dispe-Sexo.jpg' border='0' alt='Dispe-Sexo'/></a>

###Conclusión:
- Aca observamos que el numero de accidente ocurren en  los siguientes horarios: 2 am hasta la 10 am  y vuelve un aumento 17 hasta las 22 de la noche.
- Se Observa que en su gran mayoria  los fallecidos son hombres.

### Estudio georeferencial por cada uno de los  siniestros ocurridos en las distintas comunas de  Buenos Aires.
<a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/qRZ3TbHs/mapa.jpg' border='0' alt='mapa'/></a><br /><a href='https://postimages.org/es/'>free image hosting</a><br />

 Este mapa interactivo de la ciudad de Buenos Aires con sus respectivas comunas, se muestra  la información de los accidentes ocurridos en un periodo de tiempo desde 2016 hasta 2021. Este mapa permite visualizar de manera clara y precisa la distribución de los accidentes en las diferentes zonas de la ciudad.

El mapa interactivo ha sido diseñado utilizando tecnología utilizando  la libreria  **folium** que permite una experiencia de navegación fluida y amigable.  Se explorar las comunas y acceder a información detallada sobre cada accidente registrado en el periodo de tiempo mencionado.

Cada comuna estará representada en el mapa por un marcador, el cual contendrá información relevante sobre los accidentes ocurridos en esa zona específica. Al hacer clic en cada marcador, se desplegará una ventana emergente con detalles como la fecha, hora, tipo de accidente y número de víctimas involucradas.

Además, el mapa interactivo lo  podemos ver tambien en el dashborad de la presentación, donde  cuenta con  opciones de filtrado para que se puede   seleccionar un rango de fechas específico y visualizar únicamente los accidentes ocurridos en ese periodo. Esto permite  realizar análisis comparativos y observar posibles patrones o tendencias a lo largo del tiempo.



<a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/rm08dcPP/comunas.jpg' border='0' alt='comunas'/></a><br /><a href='https://postimages.org/es/'>photo sharing</a><br />
###Conclusión:
- Podemos afirmar que la mayor cantidad d victimas fatales están en las comunas 1: llamada CONSTITUCIÓN-MONSTERRAT-PUERTO MADERO, seguido de la comuna  numero 4; llamada BARRACAS-BOCA-NUEVA POMPETA, le sigue la comuna numero 9 llamada LINIERS-MATADORES-PARQUE AVELLANEDA Y LA COMUNA 8  conformada por: VILLALUGENO-VILLARIACHUELO-VILLA SOLDATI. y asi sucesivamente.
- Estos numeros pueden ser atribuidos a varios fenómenos. Uno de los factores que contribuye a estos altos números de accidentes es la congestión del tráfico urbano. La limitada capacidad vial en espacios fijos a corto plazo puede llevar a una acumulación de vehículos y aumentar el riesgo de accidentes 

- Otro factor es que estas comunas es donde esta el casco central de la ciudad,  hacer todas las diligencias adminitrativas se encuentra en dichas comunas, el turismo es otro factor de alta demanda de transito  de autobuses.

- Para  salir de  Buenos Aires y tomar todas las rutas costeras tambien se debe cruzar estas importantes comunas. por tal motivo incrementa el numero de accidente en todas estas arterias viales.

<a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/xTyz5D0Z/Acusados.jpg' border='0' alt='Acusados'/></a>

###Conclusion:
-Podemos observar   que la mayor cantidad de victimas por Acusados esta en AUTO, PASAJERSO Y CARGAS.

```