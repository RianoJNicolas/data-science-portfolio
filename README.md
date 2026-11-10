# Portafolio de Ciencia de Datos — TripleTen

Proyectos desarrollados durante el bootcamp de **Data Science de TripleTen**. Cada proyecto parte de una pregunta de negocio y recorre el flujo completo: carga, limpieza, análisis exploratorio, visualización, pruebas estadísticas y conclusiones con recomendaciones.

**Autor:** Johan Nicolás Riaño

## Proyectos

| # | Proyecto | Pregunta de negocio | Habilidades principales |
|---|----------|---------------------|-------------------------|
| 01 | [Limpieza y segmentación de clientes con Python](01-python-limpieza-clientes/) | ¿Cómo preparar una base de clientes cruda para campañas de fidelización? | Python puro: strings, listas anidadas, bucles, condicionales, funciones, manejo de errores |
| 02 | [Comportamiento musical por ciudad y día](02-analisis-musica-ciudades/) | ¿Varía lo que escuchan los usuarios según la ciudad y el día de la semana? | pandas, limpieza de encabezados, valores ausentes, duplicados implícitos, agrupaciones |
| 03 | [Análisis exploratorio de pedidos de Instacart](03-instacart-eda/) | ¿Cuáles son los hábitos de compra de los clientes de una app de supermercado? | EDA con 5 tablas (~4.5 M filas), *merge*, tratamiento de ausentes, histogramas y barras con matplotlib |
| 04 | [¿Cuál es la mejor tarifa? — Megaline](04-megaline-pruebas-hipotesis/) | ¿Qué plan de prepago genera más ingresos y dónde invertir en publicidad? | Agregación por usuario/mes, ingeniería de variables, estadística descriptiva, pruebas t de Student y de Levene (SciPy) |
| 05 | [Tienda de videojuegos Ice](05-ice-videojuegos/) *(en progreso)* | ¿Qué patrones determinan si un videojuego tiene éxito? | Exploración inicial con pandas: estructura, nulos, duplicados y valores únicos |

## Tecnologías

Python · pandas · NumPy · Matplotlib · Seaborn · SciPy · Jupyter Notebook

## Cómo ejecutar los notebooks

Los notebooks ya incluyen sus resultados y gráficos, por lo que pueden leerse directamente en GitHub. Para ejecutarlos localmente:

```bash
git clone <url-de-este-repositorio>
cd data-science-portfolio
python -m venv .venv
# Windows: .venv\Scripts\activate   |   macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

Los datos están incluidos en la carpeta `data/` de cada proyecto, así que los notebooks se pueden ejecutar directamente después de clonar el repositorio. Los datasets fueron proporcionados por TripleTen con fines educativos; cada `data/README.md` describe sus archivos.

## Estructura

```
.
├── 01-python-limpieza-clientes/
├── 02-analisis-musica-ciudades/
├── 03-instacart-eda/
├── 04-megaline-pruebas-hipotesis/
├── 05-ice-videojuegos/
├── requirements.txt
└── README.md
```
