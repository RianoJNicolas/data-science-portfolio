# ¿Cuál es la mejor tarifa? — Megaline

## Pregunta de negocio

El operador de telecomunicaciones Megaline ofrece dos planes de prepago, **Surf** y **Ultimate**. El área comercial quiere saber cuál genera más ingresos para decidir dónde invertir el presupuesto de publicidad. Se analizan 500 clientes durante 2018.

## Proceso

1. **Limpieza y corrección de tipos** en 5 tablas: usuarios, planes, llamadas, mensajes e internet.
2. **Enriquecimiento:** extracción del mes, redondeo de minutos por llamada y conversión de MB a GB según las reglas de facturación.
3. **Agregación por usuario y mes** de minutos, mensajes y datos, y **cálculo del ingreso mensual** de cada usuario (cuota fija más excedentes).
4. **Análisis descriptivo:** medias, varianzas, desviaciones estándar, histogramas y diagramas de caja por plan.
5. **Pruebas de hipótesis** (α = 0.05):
   - Ingreso promedio Surf vs. Ultimate: prueba t de Welch (`equal_var=False`) → **p ≈ 3.2e-15**, se rechaza H₀.
   - Ingreso promedio NY-NJ vs. otras regiones: prueba de Levene (p ≈ 0.126) y luego prueba t (`equal_var=True`) → **p ≈ 0.044**, se rechaza H₀ con evidencia débil.

## Resultados y recomendaciones

- **Por usuario, Ultimate genera más** (72.31 USD/mes frente a 60.71 USD) y su ingreso es más estable (σ = 11.40 frente a 55.39).
- **En total, Surf aporta casi el doble** (95,491 USD frente a 52,066 USD) porque tiene más del doble de usuarios y más de la mitad de sus registros supera los 15 GB incluidos.
- Los usuarios de Ultimate casi no aprovechan lo que pagan: cerca del 95 % de sus registros paga solo la cuota base.
- **Recomendaciones:** priorizar Ultimate en la publicidad para captar clientes nuevos, ofrecer el cambio a Ultimate a los usuarios de Surf con facturas altas (retención) y evaluar un plan intermedio.

## Notebook

[`megaline_tarifas.ipynb`](megaline_tarifas.ipynb)

**Herramientas:** Python, pandas, NumPy, Matplotlib, Seaborn, SciPy
