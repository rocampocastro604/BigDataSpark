# Proyecto 4 sobre Big Data con Spark

### Autores
El equipo está conformado por:

Daniel Enrique Hernández Stalhuth :shipit:
- dehernands@eafit.edu.co  
- hsdaniele95@gmail.com  

Ricardo Ocampo Castro :goat:
- rocampo3@eafit.edu.co 
- rocampocastro604@gmail.com  

Alejandro Gil Maya :trollface:
- ggilmay@eafit.edu.co 
- lordbluebanana@gmail.com
______

El desarrollo del proyecto se dividio en tres(3) grandes partes:
-Ingesta de datos
-Preparacion de datos
-Procesamiento de los datos

La primera parte consistia en obtener los datos de la base de datos all-news en formato csv (Esto es un formato en el que la estructura se encuentra separada por comas (,).
Ademas este dataset se encontraba separado en varios datasets, por lo que fue necesario recurrir a funciones de SQL para lograr unirlos en uno solo, que resulto en uno consolidado de alrededor de 100000 registros.

Luego se paso a la parte de preparacion y limpieza de datos donde se aplicaron tecnicas como eliminacion de signos de puntuacion y stopWords, para esto se convirtio el Spark Datafrrame en un Pandas Dataframe, pues para esta tarea no se encontraba tanta informacion y parecia mas sencillo hacerlo en Pandas.

Sucesivamente, para el procesamiento de los datos se volvio a convertir el Pandas Dataframe en un Spark Dataframe para asi aplicar un algoritmo de Analisis de sentimientos, pues lo que se busca es analizar si una noticia es buena o mala dependiendo de su descripcion (En este caso la descripcion estaba dada por la columna 'content' del Dataframe(dfSpark)), adicionalmente el equipo convirtio ese resultado que es tipo String en un Booleano para asi usar un modelo donde al aplicarle una Regresion logistica logre predecir si una noticia futura sera positiva o negativa.
