# BarChart Responsive

Plantilla de visualización tipo Bar chart responsiva.<br>

Para esta versión se utiliza nvd3, un nuevo release de la librería js para gráficas.

Descripción de archivos principales:

- `barchart.html` <br>- Archivo html en el que se importan principalmente:
  * Librería de la visualización
  * Archivo `js` con diversas funcionalidades (`js/barchart.js`)
  * **Contendor para la gráfica**, que en este caso se debe definir en el html como:
  `<div id="bar-chart">
    <svg></svg>
  </div>`
  * **Contenedor para leyendas**, que debe tener la siguiente estrucutra html:<br>
  ```
  <div class="svgLegend4">
      <div class="legend4"></div>
  </div>
  ```
  <br>
  
- `partials/barchart_example.json`<br>- **Json base** para definir los valores que mostrará la visualización.<br><br>

- `js/barchart.js`<br>- Javascript que contiene las funcionalidades **necesarias** para dibujar la visualización.

##Json base

El Json que consumirá la visualización debe estar en todo momento dentro del folder `partials` y debe tener asignado el nombre `barchart_example.json`<br>

La **estructura** debe ser igual a la del archivo `barchart_example.json`, si exisite alguna diferencia, por mínima que sea, la gráfica no se visualizará en el navegador.

Además los **nombres** o `keys` de los valores deben ser iguales a los dej Json de ejemplo para que estos se puedan mostrar en la visualización.

**Estructura**
- Esta estructura cambia respecto a la plantilla de la gráfica de barras no responsiva

```
{
  "ejex": "Transporte",
  "ejey": "Personas",
  "valores": [
    {
      "key": "Chihuahua",
      "values": [
        {"x": "Coche", "y": 35650},
        {"x": "Coche compartido", "y": 18546},
        {"x": "Metro", "y": 12654},
        {"x": "Bicicleta", "y": 12654},
        {"x": "A pie", "y": 12654},
        {"x": "Motocicleta", "y": 12654},
        {"x": "Taxi", "y": 12654}
      ]
    }
  ]
}
```

- "ejex" //Legenda del Eje X en la gráfica
- "ejey" //Legenda del Eje Y en la gráfica
- "valores" //Son los valores que se muestran en las columnas de la gráfica
- "x" //Es el valor por el cual se agrupan las columnas
