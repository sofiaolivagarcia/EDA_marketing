# 📊 Proyecto EDA con Python  

## 📌 Descripción  
Este proyecto forma parte del curso y su objetivo ha sido poner en práctica todo lo aprendido sobre **Python, Pandas y análisis de datos**.  
El trabajo consiste en realizar un **Análisis Exploratorio de Datos (EDA)** a partir de dos conjuntos de datos relacionados con clientes de un banco y sus campañas de marketing telefónicas.  

La idea principal es **entender el perfil de los clientes y cómo responden a las campañas**, apoyándome en limpieza de datos, estadísticos básicos y visualizaciones.  

---

## 📂 Conjuntos de datos  
- **`bank-additional.csv`**  
  Contiene información sobre clientes y campañas de marketing (edad, ocupación, estado civil, educación, duración de las llamadas, canal de contacto, número de intentos, etc.), así como indicadores económicos y la variable objetivo (**y**) que indica si el cliente contrató o no un depósito a plazo.  

- **`customer-details.xlsx`**  
  Archivo Excel con tres hojas, cada una con clientes que entraron en el banco en distintos años. Incluye datos demográficos y de comportamiento: ingresos anuales, número de hijos/adolescentes en el hogar, fecha de alta como cliente, visitas web mensuales y un identificador único.  

Ambos datasets se unieron usando el identificador único para poder analizarlos de forma conjunta.  

---

## 🛠️ Herramientas utilizadas  
- **Python 3.13.0**  
- **Pandas** → limpieza y transformación de datos  
- **Matplotlib / Seaborn** → visualización de datos  
- **Visual Studio Code** → entorno de desarrollo  

---

## 🔎 Proceso seguido  

### 1. Análisis preliminar  
- Revisión de columnas y tipos de datos.  
- Exploración inicial de valores únicos en variables categóricas.  
- Identificación de nulos y duplicados.  

### 2. Limpieza y transformación  
- Conversión de columnas de fecha a formato `datetime`.  
- Cambio de tipos de datos numéricos y categóricos donde fue necesario.  
- Normalización de valores y nombres de columnas.  
- Creación de nuevas variables (ejemplo: **año de alta del cliente**).  
- Unión de datasets con `merge` en la columna de ID.  

### 3. Análisis descriptivo  
- Estadísticos básicos (media, mediana, desviación estándar, percentiles).  
- Distribución de variables clave: edad, ingresos, visitas web.  
- Comparaciones de características demográficas frente a la respuesta de campañas.  
- Relación entre **duration** (duración de la llamada) y el éxito de la campaña.  
- Revisión de indicadores macroeconómicos y variable objetivo.  

### 4. Visualizaciones  
- Histogramas de edad e ingresos.  
- Gráficos de barras (ocupación, estado civil, educación).  
- Boxplots (ingresos vs. número de hijos).  
- Evolución temporal de altas de clientes por año.  
- Dispersión: duración de llamada vs. probabilidad de éxito.  

### 5. Conclusiones principales  
- La **duración de la llamada** es un factor clave para el éxito de la campaña.  
- Algunos perfiles por profesión y educación muestran más probabilidad de aceptar.  
- Los **ingresos** y la **composición del hogar** influyen, pero no son determinantes por sí solos.  
- El canal de contacto y el momento de la campaña afectan la probabilidad de éxito.  
- El cruce de datasets permitió ver cómo los datos demográficos se relacionan con los resultados de marketing.  

---

## 📑 Estructura del repositorio  

├── data/
│   ├── processed/
│   │   ├── bank_clean.csv
│   │   ├── bank-additional.csv
│   │   ├── customer-details.xlsx
│   ├── raw/
│   │   ├── bank-additional.csv
│   │   ├── customer-details.xlsx
│
├── notebook/
│   ├── 01-Analisis_preliminar_bank.ipynb
│   ├── 02-Analisis_preliminar_customers.ipynb
│   ├── 03-EDA_bank.ipynb
│   ├── 04-EDA_customers.ipynb
│   ├── 05-Unión_bank_customers.ipynb
│
├── src/
├── .gitignore
├── README.md

## 👤 Autor  
Proyecto realizado por Sofía Oliva García. 
