# Datos

Versión modificada por TripleTen del dataset público [Instacart Market Basket Analysis](https://www.kaggle.com/c/instacart-market-basket-analysis). Los archivos usan `;` como separador.

- `instacart_orders.csv`
- `products.csv`
- `aisles.csv`
- `departments.csv`
- `order_products.csv.gz`: comprimido porque pesa ~90 MB sin comprimir. pandas lo lee directamente con `pd.read_csv()`.
