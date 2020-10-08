# TPB708 Programación de aplicaciones en sistemas de información geográfica
## Proyecto 01 - Visualización de datos vectoriales

### Fecha de entrega y entregables
La fecha y hora límite para la entrega es **jueves 15 de octubre de 2020 a las 5:00 p.m.**

Debe enviarle al profesor por correo electrónico la dirección del notebook resultante. Puede trabajar en grupos de un máximo de tres estudiantes. Solo debe enviarse un mensaje por grupo, con los nombres de los integrantes.

### Desarrollo
Desarrolle un notebook de Jupyter que muestre un mapa Folium con las siguientes características:

1. (5%) Tres capas base (puede elegirlas).
2. Cuatro capas sobrepuestas (*overlay*):  
    a. (20%) Mapa de coropletas de casos positivos de COVID-19 en cantones de Costa Rica.  
    b. (20%) Mapa de coropletas de casos activos de COVID-19 en cantones de Costa Rica.  
    c. (20%) Mapa de coropletas de casos recuperados de COVID-19 en cantones de Costa Rica.  
    d. (20%) Mapa de coropletas de casos fallecidos de COVID-19 en cantones de Costa Rica.  
3. (10%) Control de capas para activar y desactivar las capas base y sobrepuestas.
4. (5%) Control de escala.
5. (5% extra) Al hacer clic sobre el polígono de un cantón, debe mostrarse el nombre del cantón y la cantidad de casos correspondiente a la capa (positivos, activos, recuperados o fallecidos).


Se recomienda ejecutar estos comandos en un ambiente Conda que contenga el paquete GDAL.

Descargue la capa de cantones del Sistema Nacional de Información Territorial (SNIT, [https://www.snitcr.go.cr/](https://www.snitcr.go.cr/)) en un archivo GeoJSON llamado "cantones.geojson": 
```shell
# Descarga de la capa de cantones del IGN en el SNIT
ogr2ogr -f GeoJSON -s_srs EPSG:5367 -t_srs EPSG:4326 -makevalid cantones.geojson WFS:"http://geos.snitcr.go.cr/be/IGN_5/wfs" "IGN_5:limitecantonal_5k"

# Información sobre la capa descargada
ogrinfo -al -so cantones.geojson
```

Utilice el comando ```ogr2ogr``` y el archivo "cantones.geojson" para realizar los siguientes ejercicios. El valor porcentual de cada uno se muestra entre paréntesis.

1. (25%) Extraiga en un shapefile los cantones de la provincia de Heredia con área menor o igual que 20 km2.
2. (25%) Extraiga en un archivo GeoPackage los campos de provincia, cantón y área de los cantones de la provincia de San José con área menor o igual que 20 km2.
3. (25%) Extraiga en un archivo KML los campos de provincia, cantón y área de los cantones con área menor o igual que 20 km2 de las provincia de San José o Heredia.
4. (25%) Extraiga en un archivo GeoJSON los campos de provincia, cantón y área de los cantones con área menor o igual que 20 km2 de la provincia de San José o con área mayor o igual que 2000 km2 de la provincia de Limón.

Debe enviarle al profesor por correo electrónico un archivo de texto con los comandos utilizados en los ejercicios del 1 al 4.
