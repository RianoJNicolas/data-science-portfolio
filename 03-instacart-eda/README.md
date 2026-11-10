# Análisis exploratorio de pedidos de Instacart

## Contexto

Instacart es una plataforma de entrega de supermercado. El conjunto de datos (una versión modificada del dataset público de Instacart, con ausentes y duplicados introducidos a propósito) tiene **5 tablas**: pedidos, productos, pasillos, departamentos y productos por pedido (~4.5 millones de filas).

## Proceso

1. **Descripción de los datos:** carga con el separador correcto e inspección de tipos, volúmenes y ausentes.
2. **Preprocesamiento:**
   - Eliminación de pedidos duplicados y análisis de duplicados en nombres de producto.
   - Validación de la clave compuesta (`order_id`, `product_id`) en la tabla de relación muchos a muchos.
   - Diagnóstico de ausentes: los productos sin nombre pertenecen al pasillo 100 y al departamento 21 (*missing*); los ausentes en `days_since_prior_order` son primeros pedidos, y los de `add_to_cart_order` aparecen en pedidos de más de 64 artículos.
   - Decisiones de imputación justificadas y conversión de tipos.
3. **Análisis exploratorio:** distribuciones por hora y día, tiempo entre pedidos, comparación miércoles/sábado, pedidos por cliente, productos más populares, tasas de recompra por producto y por cliente, y primeros artículos añadidos al carrito.

## Hallazgos principales

- **Horas pico entre las 10:00 y las 16:00**, y mayor actividad los **domingos y lunes**.
- Picos en el tiempo entre pedidos cada **7 días** (compra semanal) y a los **30 días** (posible tope del sistema).
- La mayoría de los clientes hace **entre 1 y 10 pedidos**, con un grupo grande que compra una sola vez.
- **Frutas y verduras dominan**: la banana es el producto más pedido, el más recomprado y el que más se añade primero al carrito.
- Las tasas de recompra por cliente se concentran en los extremos (cercanas a 0 y a 1), lo que permite segmentar clientes ocasionales y leales.

## Notebook

[`instacart_eda.ipynb`](instacart_eda.ipynb)

**Herramientas:** Python, pandas, Matplotlib
