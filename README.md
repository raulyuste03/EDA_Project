# Proyecto EDA - Análisis Exploratorio de Datos Bancarios

## Objetivo

El objetivo de este proyecto es realizar un análisis exploratorio de datos (EDA) para entender el comportamiento de los clientes y el impacto de las campañas de marketing telefónicas de una institución bancaria portuguesa. Se busca identificar patrones y relaciones relevantes que ayuden a optimizar futuras campañas y mejorar la toma de decisiones.

---

## Descripción de los Datos

Se utilizaron dos conjuntos de datos principales:

- **bank-additional.csv**: Contiene información sobre las campañas telefónicas realizadas, datos demográficos y socioeconómicos de los clientes, detalles de las interacciones y el resultado de suscripción al producto (depósito a plazo).
  
- **customer-details.xlsx**: Contiene datos demográficos y comportamiento de clientes para los años 2012, 2013 y 2014. Incluye ingresos, número de hijos, visitas mensuales al sitio web y fecha en la que el cliente se unió al banco.

---

## Herramientas Utilizadas

- Python 3.8+
- Librerías: pandas, numpy, matplotlib, seaborn, openpyxl
- Entorno de desarrollo: Visual Studio Code con soporte para Jupyter Notebooks

---

## Metodología

1. **Carga y exploración inicial**  
   Se importaron los datasets y se verificaron tipos de datos, estructura, valores faltantes y duplicados.

2. **Limpieza y transformación**  
   Se eliminaron columnas innecesarias, se convirtieron tipos de datos (fechas, numéricos con coma decimal) y se imputaron valores faltantes utilizando mediana para variables numéricas y moda para variables categóricas.

3. **Análisis estadístico descriptivo**  
   Se calcularon medidas como media, mediana, desviación estándar y distribuciones para variables numéricas y categóricas clave.

4. **Visualización**  
   Se generaron histogramas, boxplots, mapas de calor de correlaciones, gráficos de barras y scatterplots para identificar distribuciones, outliers y relaciones entre variables.

5. **Análisis segmentado**  
   Se analizaron las tasas de suscripción al producto según variables categóricas importantes como profesión, nivel educativo y estado civil.

---

## Resultados Principales

- El dataset `bank-additional` consta de 43,000 registros, con varias columnas que contenían valores nulos, destacando:  
  - `euribor3m` con ~21.5% nulos  
  - `default` con ~20.9% nulos  
  - `age` con ~11.9% nulos  
- Después de la limpieza, los valores faltantes fueron imputados correctamente sin eliminar columnas relevantes.
- La tasa global de suscripción al producto es aproximadamente **11.27%**.
- Las tasas de suscripción varían significativamente según el perfil del cliente:  
  - Por profesión, los estudiantes tienen la tasa más alta (~31.3%), seguidos de jubilados (~25.2%) y desempleados (~14.4%).  
  - Por nivel educativo, las personas analfabetas (illiterate) muestran una tasa alta (~22.2%), aunque con pocos casos, y los universitarios alcanzan cerca del 13.8%.  
  - Por estado civil, los solteros presentan una tasa de suscripción más alta (~13.9%) comparado con casados y divorciados (~10%).
- Estos insights pueden orientar campañas personalizadas para mejorar la conversión.

---

## Uso del Dataset Customer-Details

- Se exploraron las hojas para los años 2012, 2013 y 2014, con datos limpios y sin valores nulos relevantes.
- Contienen información sobre ingresos anuales, composición familiar y visitas web, útiles para enriquecer análisis futuros o modelos predictivos.

---

## Instrucciones para ejecutar el proyecto

1. Clonar o descargar este repositorio.
2. Instalar las dependencias con:

   ```bash
   pip install -r requirements.txt
