# BarChart

Plantilla de visualización tipo Bar chart.<br>
Descripción de archivos principales:

- `barchart.html` <br>- Archivo html en el que se importan principalmente:
  * Librería de la visualización
  * Archivo `js` con diversas funcionalidades (`js/barchart.js`)
  * **Contendor para la gráfica**, que en este caso se debe definir en el html como: `<div id="bar-chart"></div>`
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

```
{
  "ejex": "Transporte",
  "ejey": "Personas",
  "valores": [
    {"label":"Coche", "Chihuahua":20325, "Coahuila":10834, "Sonora": 50926, "Nuevo León":20778},
    {"label":"Coche compartido", "Chihuahua":15643, "Coahuila":30726, "Sonora":40878, "Nuevo León":15352},
    {"label":"Autobus", "Chihuahua":20778, "Coahuila":15352, "Sonora":40878, "Nuevo León":20325},
    {"label":"Metro", "Chihuahua":50926, "Coahuila":20778, "Sonora":40522, "Nuevo León":10834},
    {"label":"Bicicleta", "Chihuahua":20325, "Coahuila":10834, "Sonora":25899, "Nuevo León":23987},
    {"label":"A pie", "Chihuahua":15352, "Coahuila":20325, "Sonora":30726, "Nuevo León":16335},
    {"label":"Motocicleta", "Chihuahua":40878, "Coahuila":15352, "Sonora":67854, "Nuevo León":20778},
    {"label":"Taxi", "Chihuahua":50926, "Coahuila":10834, "Sonora":20325, "Nuevo León":20778}
  ]
}
```

- "ejex" //Legenda del Eje X en la gráfica
- "ejey" //Legenda del Eje Y en la gráfica
- "valores" //Son los valores que se muestran en las columnas de la gráfica
- "label" //Es el valor por el cual se agrupan las columnas
