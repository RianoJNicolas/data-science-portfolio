# Limpieza y segmentación de clientes con Python

## Contexto

La tienda en línea *Store 1* guarda la información de sus clientes en listas anidadas con errores de formato: espacios sobrantes, guiones bajos en los nombres, edades como `float` o texto, y categorías en mayúsculas. El objetivo es dejar los datos listos para un programa de fidelización y responder preguntas de segmentación, **sin usar librerías externas**.

## Notebooks

- [`parte1_fundamentos.ipynb`](parte1_fundamentos.ipynb): limpieza de un registro paso a paso: `strip()`, `replace()`, `split()`, conversión de tipos, `try/except` para entradas no válidas, ordenamiento y f-strings para generar resúmenes.
- [`parte2_funciones_y_segmentacion.ipynb`](parte2_funciones_y_segmentacion.ipynb): la limpieza se convierte en una función reutilizable (`clean_user`) que se aplica a toda la base. Después se calculan los ingresos totales y se segmenta a los clientes (menores de 30 años, jóvenes con alto gasto, compradores por categoría) con bucles, condicionales y funciones con filtros.

## Habilidades demostradas

- Manipulación de cadenas y listas anidadas
- Conversión y validación de tipos de datos
- Control de flujo (`for`, `if`, `try/except`)
- Diseño de funciones reutilizables
- Segmentación simple de clientes

> Este proyecto no necesita archivos de datos externos: los datos de ejemplo están definidos dentro de los notebooks.
