# Detección de Anomalias en Auditorías

Este es un repositorio con el código utilizado para una pipeline de detección de outliers en datos de auditorías. La mayor parte de funciones pueden utilizarse para la detección de anomalías en cualquier otros datos numéricos.

En este caso, las variables eran principalmente categóricas, por lo que se crearon variables numéricas nuevas a partir de la variable con la media del importe de los contratos analizados, el número de apariciones de cada categoría y las "relaciones" entre categorías (el número de veces que coincide una categoría con otra, por ejemplo un proveedor con un aprobador). Sin embargo, toda esta fase puede saltarse y pasar directamente a la detección propiamente dicha. Aún así, lo he incluido por si le resulta útil a alguien :)

El código incluye funciones para aplicar MCD, One-Class SVM, LOF y Isolation Forest con las funciones de Scikit-Learn y unos parámetros prefijados. Sin embargo, es fácil modificar cualquier parámetro (porque la estructura es sencilla) o añadir la posibilidad de pasarlos en un diccionario. Además, se realizan varios gráficos con la distribución de las puntuaciones, pues en este caso se realizó una ordenación en función de las scores de los métodos, sin realizar una clasificación binaria entre «anomalía» o «no anomalía».
