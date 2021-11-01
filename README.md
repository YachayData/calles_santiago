# calles_santiago

Reproducción y continuación del trabajo de: 
https://github.com/Mjrovai/Python4DS/tree/master/Streets_Santiago.

Para más información, ver el árticulo de Marcelo Rovai [[1]](https://towardsdatascience.com/how-safe-are-the-streets-of-santiago-e01ba483ce4b).

Cambios menores:
- Se utilizaron los últimos datos de siniestros del CONASET [[2]](https://mapas-conaset.opendata.arcgis.com/datasets/3a084373b58b45d0ae01d9c14a231cf8_0); 
- Se usó un GeoPackage para dismunuir el peso de los datos espaciales;
- Se agregó la infraestructura necesaria para que el código sea 100% distribuible. Para esto, se creó una imagen Docker. 

Requerimientos: [Docker](https://docs.docker.com/get-docker/).

Para reproducir el código, correr: 

```
docker run -p 8888:8888 pescapil/geostreet
```

Para construir la imagen Docker desde cero:
```
git clone https://github.com/YachayData/calles_santiago.git
cd calles_santiago
docker build -f Dockerfile . -t geostreet
docker run -p 8888:8888 geostreet
```
