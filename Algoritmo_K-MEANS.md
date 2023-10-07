# Algoritmo K-MEANS

Resuelve un problema de optimización, siendo la funcion a optimizar la suma de las distancias cuadráticas de cada objeto al centroide de su cluster.

clave de la clase ***tnhgzoo***

## Ventajas
+ Facilidad para comprender su funcionamiento, asi como su implementacion
+ El algoritmo puede tomar diferentes caminos si se utilizan diferentes criterios como *Distancia, método de seleccion de centroides iniciales, etc*.

## Desventajas
+ Dificultades para detectar grupos con formas no esf+ericas y de tamaño diferente.
+ Sensible al ruido y a puntos atípicos (*OUTLIERS*).
+ Solo maneja varables numéricas.
+ Datos cuantitativos

## Variantes de K-MEANS
+ **K-modas**
+ **K-Medoids**
+ **Mini Batch K-Means**

## Cuando no es óptimo K-Means

- Separar 2 aros de diferentes tamaños, porque divide los aros no los separa.
- Divide datos concentrados de una misma agrupación.


[K-Means en Python](https://anderfernandez.com/blog/programar-kmeans-python/)
[Ejemplo de algoritmo K-Means](https://www.unioviedo.es/compnum/laboratorios_py/kmeans/kmeans.html)
 
 ```py
def initialize_centroids(k, data):

    n_dims = data.shape[1]
    centroid_min = data.min().min()
    centroid_max = data.max().max()
    centroids = []

    for centroid in range(k):
        centroid = np.random.uniform(centroid_min, centroid_max, n_dims)
        centroids.append(centroid)

    centroids = pd.DataFrame(centroids, columns = data.columns)

    return centroids

centroids = initialize_centroids(3, data)
centroids
 ```
