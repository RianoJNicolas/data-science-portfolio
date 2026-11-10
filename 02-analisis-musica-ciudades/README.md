# Comportamiento musical por ciudad y día de la semana

## Pregunta

¿La actividad de los usuarios de un servicio de streaming musical varía según la ciudad (Springfield y Shelbyville) y el día de la semana (lunes, miércoles y viernes)?

## Proceso

1. **Exploración:** revisión de estructura, tipos y calidad de los datos con `info()` y `head()`.
2. **Preprocesamiento:**
   - Estandarización de los nombres de columnas (minúsculas, sin espacios, *snake_case*).
   - Imputación de valores ausentes en columnas categóricas con `'unknown'`.
   - Eliminación de duplicados explícitos y corrección de **duplicados implícitos** en los géneros (p. ej., variantes de *hip-hop*).
3. **Análisis:** conteo de reproducciones por ciudad y día con `groupby()` y una función de filtrado propia.

## Resultados principales

- En ambas ciudades la actividad **aumenta el viernes** frente al lunes (+205 reproducciones en Springfield y +281 en Shelbyville).
- Shelbyville registra alrededor de **un tercio** de las reproducciones de Springfield, probablemente porque tiene menos usuarios.
- Validar los resultados contra visualizaciones previas permitió detectar y corregir un error de filtrado con `query()`.

## Notebook

[`analisis_musica.ipynb`](analisis_musica.ipynb)

**Herramientas:** Python, pandas
