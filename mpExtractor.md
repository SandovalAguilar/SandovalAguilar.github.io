# mpExtractor

[Ver proyecto en GitHub](https://github.com/SandovalAguilar/mpExtractor)

"mpExtractor" es un conjunto de scripts, escritos en python, que permiten obtener las calificaciones de maestros del sitio web "MisProfesores.com" en un dataframe o archivo csv.

## Instalación

Para utilizar los scripts "htmlToDataframe.py" y "dataAnalyzer" es necesario instalar las siguientes librerías a traves del gestor de paquetes [pip](https://pip.pypa.io/en/stable/).

```bash
pip install requests 
pip install beautifulsoup4
pip install pandas 
```

Si se desea exportar los resultados a un archivo PDF, es necesario instalar las siguientes librerías.

```bash
pip install dataframe-image
pip install fpdf
```

También es necesario tener [Google Chrome](https://www.google.com/intl/es-419/chrome/) instalado. 

## Uso

Únicamente ejecutar el script "mpExtractor" e introducir una URL válida del sitio MisProfesores.com que corresponda a una facultad o escuela. Por ejemplo:

```
https://www.misprofesores.com/escuelas/UANL-FCFM_2263
```

Posteriormente se desplegarán una serie de opciones como:

- Generar un archivo CSV con todas las valoraciones.
- Generar un archivo CSV con todas las valoraciones más altas.
- Generar un archivo CSV con todas las valoraciones más bajas.
- Generar un reporte en PDF con el top de profesores con mejores y peores valoraciones.

El orden toma en cuenta el número de reseñas de cada maestro: es decir, tiene más peso un maestro con 9 de calificación pero (por ejemplo) 20 reseñas, que uno con la misma calificación pero solo con 5 reseñas. Además, tambien se encuentra en una de las carpetas una Jupyter Notebook, por si se desea experimentar directamente con el dataset. 

## Ejemplo

Al ingresar la [URL](https://www.misprofesores.com/escuelas/UANL-FCFM_2263) se obtiene la siguiente tabla que muestra el top de profesores con mejores puntuaciones y mayor número de reseñas:

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Apellido, Nombre</th>
      <th># de calif.</th>
      <th>Promedio</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Gómez Pérez , Diego Gerardo</td>
      <td>46</td>
      <td>9.9</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Guajardo , Elizabeth</td>
      <td>43</td>
      <td>9.6</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Guerrero Ceja , Yazmany Jahaziel</td>
      <td>60</td>
      <td>9.4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>arias , adriana</td>
      <td>40</td>
      <td>9.3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Barragan Amigón , Abraham Benito</td>
      <td>37</td>
      <td>9.1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Tlahuice Flores , Alfredo</td>
      <td>38</td>
      <td>9.1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Garza Garza , Luis Gerardo</td>
      <td>31</td>
      <td>8.6</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Rodríguez , rodrigo</td>
      <td>30</td>
      <td>8.5</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Rodriguez , Victoria Celeste</td>
      <td>42</td>
      <td>8.3</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Contreras Mendoza , Abigail</td>
      <td>47</td>
      <td>8.2</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Moller Garza , Jonathan Ricardo</td>
      <td>72</td>
      <td>8.1</td>
    </tr>
  </tbody>
</table>
</div>

## Notas adicionales

Este proyecto es un prototipo y podría contener errores. Además, también podría modificarse completamente en el futuro.

