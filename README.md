# Proceso de Preprocesamiento de Datos
## Elaborado por
Marcos Ulises Sánchez.
## Docente
Msc. Arlen López.

## 1. Exploración Inicial
Se cargó el dataset, se identificaron las columnas clave y se realizó una exploración de las estadísticas descriptivas para entender mejor la estructura de los datos. Las columnas principales fueron:
- `Revenue`
- `Profit`
- `Order_Quantity`

## 2. Tratamiento de Outliers
Se eliminaron los outliers de las columnas `Revenue`, `Profit` y `Order_Quantity` utilizando el Z-score con un umbral de 3 desviaciones estándar. Este paso es importante para garantizar que los valores atípicos no afecten el análisis.

## 3. Transformación de Variables
Se aplicaron las siguientes transformaciones:
- **Estandarización (Z-score)**: Se escaló `Revenue`, `Profit` y `Order_Quantity` para que tengan una media de 0 y una desviación estándar de 1.
- **Normalización (Min-Max Scaling)**: Se escaló `Revenue`, `Profit` y `Order_Quantity` a un rango de [0,1].

## 4. Creación de Nuevas Características
Se crearon dos nuevas características:
- **Revenue_Diff**: Diferencia entre `Revenue` y el revenue esperado, que sería el producto de la cantidad y el precio unitario.
- **Profit_margin**: Margen de ganancia, calculado como `Profit` dividido por `Revenue`.

## 5. Codificación de Variables Categóricas
Se aplicó One-Hot Encoding a las variables categóricas más relevantes:
- `Product_Category`
- `Sub_Category`
- `Country`

## 6. Comparación de Distribuciones
Se compararon las distribuciones de `Revenue` y `Profit` en tres etapas:
- Antes del preprocesamiento
- Después de la estandarización (Z-score)
- Después de la normalización (Min-Max Scaling)

## 7. Gráficos Generados
Se generaron gráficos que muestran la distribución de `Revenue` y `Profit` antes y después del preprocesamiento. Estos gráficos ayudan a visualizar el impacto de las transformaciones en los datos.

## 8. Decisiones Tomadas
- Eliminamos outliers para garantizar que los valores extremos no influyan negativamente en el análisis.
- Se aplicó tanto la estandarización como la normalización para explorar diferentes enfoques de escalado.
- Se creó un conjunto de características adicionales para mejorar la capacidad de análisis y modelado posterior.

