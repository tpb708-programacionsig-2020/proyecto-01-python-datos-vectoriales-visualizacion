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

Se recomienda desarrollar el proyecto en un ambiente Conda, de manera similar a como se ha hecho en las lecciones. Los datos de COVID-19 en formato CSV y el archivo GeoJSON de cantones de Costa Rica están disponibles en [este enlace](https://github.com/tpb708-programacionsig-2020/leccion-10-folium/tree/main/datos).
