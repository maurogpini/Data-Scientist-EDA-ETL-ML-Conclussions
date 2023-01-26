 <h1 align=center> MAURO GONZALO PINI
 <h1 align=center> HENRY LABS - DATA SCIENCE COHORTE 06
 <h1 align=center> PROYECTO INDIVIDUAL º2
  
 




## **Contexto**
El escenario simula una petición sobre una base de datos de 346.479 filas y 22 columnas con diversos datos del mercado inmobiliario de USA. Pueden leer la consigna en detalle en el archivo CONSIGNA.md, pero en síntesis lo requerido fue realizar un modelo de Machine Learning en el cual se pueda predecir si una propiedad pertenece a una categoría dada por un rango de precio.

## **Documentación y descripción del proceso**
Inicialmente realicé un profundo trabajo de análisis exploratorio y transformación de los datos, el cual se puede ver en detalle en la versión 1 del trabajo, dada por el archivo V1_EDA_ETL. Siendo extremadamente minucioso en la detección y eliminación de registros repetidos, reduje la cantidad de los mismos desde 346.479 a 63297, lo cual representa el 18,26% del total inicial. Acto seguido decidí implementar varios modelos de aprendizaje supervisado, no logrando superar un accuracy del 80% al testear el modelo contra un dataset de test. 
Fue entonces cuando me planteé la hipótesis de que, al entrenar con pocos registros al modelo, eso hizo que problemas de predicción posteriores. Entonces generé un EDA y ETL totalmente distinto, modificando el criterio, siendo mucho más laxo y dejando en la base 251639 registros (72.62%). 
Para comparar los resultados, decidí limitarme solo a evaluar el rendimiento de un modelo de árbol de decisión con parámetros dados y aplicado a una misma estructura de columnas de datos. En este caso logré un accuracy vs el dataset de testeo del 91%, lo cual representa una mejora sustancial.
El tercer escenario es un escenario intermedio en el cual trabajo con 147404 registros, lo cual representa un 42.5% de los datos originales y alcanzo un accuracy del 84%.

## **Conclusiones **
En principio podría inferirse que, a mayor cantidad de datos a analizar, mejor es el resultado obtenido. Una fácilmente tendería a estar de acuerdo con esa afirmación. Sin embargo, surgen varios interrogantes cuando se reflexiona sobre la cuestión. Si una gran parte del espacio muestral está sesgado o repleto de inconsistencias, ¿mis conclusiones serán acertadas? Si la naturaleza de la pregunta es responder a qué categoría de precio pertenece una propiedad, ¿me conviene que para el entrenamiento del modelo haya registros que se repiten hasta 380 veces?
Mucho tendrá que ver a la hora de responder estos y otros interrogantes la naturaleza de la pregunta que se quiere responder y el tipo de información que nos es requerida. Más allá de los pormenores del caso puntual, lo que estos notebooks y su desarrollo muestran, es que el criterio del analista, las decisiones que toma y el orden en que las toma, afectan directa y enormemente en resultado final, pudiendo una decisión puntual en la etapa del ETL determinar todo el futuro de un proyecto.
