# BarChart

Plantilla de visualización tipo Bar chart.<br>
Descripción de archivos principales:

- `barchart.html` <br>- Archivo html en el que se importan principalmente:
  * Librería de la visualización
  * Archivo `js` con diversas funcionalidades (`js/barchart.js`)
  * **Contendor para la gráfica**, que en este caso se debe definir en el html como: `<div id="bar-chart"></div>`<br><br>
  
  
- `partials/barchart_example.json`<br>- **Json base** para definir los valores que mostrará la visualización, se debe respetar la **estructura** y los **nombres** o `keys` de los valores.<br><br>

- `js/barchart.js`<br>- Javascript que contiene las funcionalidades **necesarias** para dibujar la visualización.