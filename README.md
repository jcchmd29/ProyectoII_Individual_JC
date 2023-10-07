# Análisis de Datos de Siniestros Viales en Buenos Aires


## Descripción del Problema y Contexto
<p align="center">
  <img src="https://github.com/jcchmd29/ProyectoII_Individual_JC/assets/118317736/840fccfc-f8d2-4fa6-891e-d9b3b2bcb4bc" alt="9 julio">
</p>

Los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, son eventos que involucran vehículos en las vías públicas y que pueden tener diversas causas, como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, choques con objetos fijos o caídas de vehículos. Estos incidentes pueden tener consecuencias que van desde daños materiales hasta lesiones graves o fatales para los involucrados.

En el contexto de una ciudad como Buenos Aires, los siniestros viales pueden ser una preocupación importante debido al alto volumen de tráfico y la densidad poblacional. Estos incidentes pueden tener un impacto significativo en la seguridad de los residentes y visitantes de la ciudad, así como en la infraestructura vial y los servicios de emergencia.

Las tasas de mortalidad relacionadas con siniestros viales suelen ser un indicador crítico de la seguridad vial en una región. Estas tasas se calculan, generalmente, como el número de muertes por cada cierto número de habitantes o por cada cierta cantidad de vehículos registrados. Reducir estas tasas es un objetivo clave para mejorar la seguridad vial y proteger la vida de las personas en la ciudad.

Es importante destacar que la prevención de siniestros viales involucra medidas como la educación vial, el cumplimiento de las normas de tráfico, la infraestructura segura de carreteras y calles, así como la promoción de vehículos más seguros. El seguimiento de las estadísticas y la implementación de políticas efectivas son esenciales para abordar este problema de manera adecuada.

## Rol a Desarrollar

El Observatorio de Movilidad y Seguridad Vial (OMSV), centro de estudios que se encuentra bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires, nos solicita la elaboración de un proyecto de análisis de datos. El objetivo es generar información que permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales. Para ello, se nos proporciona un dataset sobre homicidios en siniestros viales acaecidos en la Ciudad de Buenos Aires durante el periodo 2016-2021.

### Contenido en el repositorio  ![mochila](https://github.com/jcchmd29/ProyectoII_Individual_JC/assets/118317736/4ccd9f9c-c4d2-45d2-bd8f-6ef55df6c7df)

* Archivo xlsx.(Dataset)
* ETL y EDA del dataset (formato Jupyter notebook)
* Archivo CSV. (Data Frame creado para ser utilizado en el analisis)
* Archivo SQL. (llamado: datapowerbi) que contiene la Base de Datos creada para cargar en Power BI.
* Carpeta picture ( Contine las imagenes incluidas aca en este readme)



### Análisis Exploratorio de Datos (EDA) ![lupa](https://github.com/jcchmd29/ProyectoII_Individual_JC/assets/118317736/9bc74d8f-a127-4442-8c97-283ff480bb9d)



En este proyecto, realizaremos un análisis exploratorio de datos (EDA) para comprender mejor la información proporcionada en el dataset. A continuación, se resumen los aspectos clave a abordar durante el EDA:

- Búsqueda de valores faltantes en el dataset.
	
	En este aspecto encontramos valores faltantes en algunas columnas las cuales segun el caso decidi:
	
	* Rellenar con un valor como *'Sin cruce'*, la columna *'Cruce'* ya que no era necesario porque estos casos 	  eran suceos ocurridos dentro de una misma Calles o Avenidas.
	* Se decidio color valor *'0'* en la columna de *'Altura'*, ya que en este caso se trataba de una 	  	  interseccion en la cual no era clara la altura numerica.


- Identificación de valores atípicos/extremos (outliers) y registros duplicados.

	En relacion a los valores duplicados en el dataset de *'Hechos'* asumimi que la unica columna que no debia presentar valores repetidos o duplicados debia ser la de *'ID'*, al revisar no existian valores duplicados. 

En el data set de *'Victimas'* existe una columna *'ID_Hechos'* que contiene la misma informacion quer la *'ID'* del data set *'Hechos'*, que si presentaba 21 registros duplicados. Sin embargo procedia  dejarlos tal cual ya que al inspeccionar las filas duplicadas enteras se trataban de registros de victimas diferentes afectadas en ese mismo numero de *'ID_Hechos'*. Por lo tanto se perservo la informacion intacta.


- La verificacion de los niveles y subniveles de los valores dentro de las columnas asi como posibles errores o diferencia de tipografias se realizo a traves de gráficos adecuados según el tipo de variable para visualizar la información.

- Se procedioa renombrar los titulos de gran parte de las columnas para hacerme mas facil su contenido.

- Se creo un Df unificado de ambos dataset a fin de recabar en un solo lugar toda la informacion necesraia para su manipulacion. la union de realizo con *marge rigth* a traves de las columnas *'ID'* y *'ID_Hechos'*. Postrerior mente se creo un archivo CSV

- Con el archivo CSV que se creo pocredimos a crear un Base de Datos en MySQL Workbench.
  


### Dashboard  ![graficos](https://github.com/jcchmd29/ProyectoII_Individual_JC/assets/118317736/49bfa7e2-a398-4fb1-9ebc-691c9e56c047)


Crearemos un dashboard interactivo que incluirá filtros para explorar los datos en detalle. El diseño del dashboard facilitará la interpretación de la información y contendrá gráficos pertinentes para una presentación clara de los datos.

La creacion del Dashboard se eligio hacer en Power Bi Desktop, el ingreso de la informacion se ejecuto a traves de una base de datos en MySQL Workbench llamada *'DataPowerBI'*.

Para ello se utilizaron los siguientes datos:
	
![Captura de pantalla bd powerbI](https://github.com/jcchmd29/ProyectoII_Individual_JC/assets/118317736/643d6b86-fd71-4f78-ab98-bbee10161316)




### KPIs (Indicadores Clave de Desempeño)  ![KPI](https://github.com/jcchmd29/ProyectoII_Individual_JC/assets/118317736/6894b625-f636-4fc8-9289-dd1d612da8ec)


Mediremos y graficaremos los siguientes KPIs:

1. Reducción en un 10% de la tasa de homicidios en siniestros viales de los últimos seis meses, en comparación con la tasa del semestre anterior.


![acc viales](https://github.com/jcchmd29/ProyectoII_Individual_JC/assets/118317736/6ec22ac2-5153-42ee-8fdd-9b35559c3c13)

 
2. Reducción en un 7% de la cantidad de accidentes mortales de motociclistas en el último año, en comparación con el año anterior.

![motorizado](https://github.com/jcchmd29/ProyectoII_Individual_JC/assets/118317736/61f68a02-99bf-45a4-abae-948d3bdf4c53)

3. Propuesta y medición de un tercer KPI Propia relevante para la seguridad vial.




### Conclusion

En este proyecto, se analizaron datos de siniestros viales en Buenos Aires entre 2016 y 2021 con el propósito de proporcionar información valiosa para mejorar la seguridad vial. Se realizó un análisis de datos exploratorio (EDA), se creó un dashboard interactivo en Power BI y se establecieron KPIs para medir el progreso en la seguridad vial. El proyecto destaca la importancia de utilizar análisis de datos para abordar problemas de seguridad en las carreteras.

Este análisis de datos puede ayudar a tomar decisiones informadas y reducir la cantidad de víctimas en siniestros viales en la ciudad.

Nuestra atención se ha centrado en el análisis exhaustivo de las tendencias de los KPIs (Indicadores Clave de Desempeño). Este análisis involucra la observación detallada de cómo evolucionan los KPIs a lo largo del tiempo, así como su relación con otras variables cruciales, como la franja horaria, el tipo de calles, el género y la edad, entre otras. Este enfoque nos ha permitido identificar patrones, fluctuaciones y posibles factores que podrían estar contribuyendo a las causas subyacentes de los problemas que estamos investigando.

Hemos diseñado una estrategia de visualización que comienza con una vista panorámica, reflejada en los gráficos seleccionados, lo que facilita la ubicación de información específica en el contexto temporal. Esta lógica nos ayuda a mantener una comprensión global de los datos mientras exploramos detalles específicos. Además, hemos enriquecido la visualización de los KPIs con los insights obtenidos a partir del análisis de métricas realizadas mediante Python.

Este enfoque combinado de análisis y visualización nos brinda una comprensión profunda de cómo se desarrollan los KPIs a lo largo del tiempo y cómo se relacionan con diversas variables. Estamos comprometidos en identificar las oportunidades de mejora y las posibles soluciones a los desafíos que enfrentamos.

### Agradecimientos

Agradecemos la oportunidad de trabajar en este proyecto y esperamos que los resultados contribuyan a mejorar la seguridad vial en Buenos Aires.

Feliz de haber llegado hasta esta instancia del BootCamp.



![agradecimiento-1-684x384](https://github.com/jcchmd29/ProyectoII_Individual_JC/assets/118317736/3696d156-cf7f-49ec-8846-410bf9fda4a3)

### Enlaces relacionados 

