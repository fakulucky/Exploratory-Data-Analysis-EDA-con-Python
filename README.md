# 🧠 Exploratory Data Analysis (EDA) con Python
Este proyecto forma parte de mi portfolio profesional como ingeniero consultor, enfocado en análisis de datos e ingeniería y gestión de proyectos.  Se realiza un **Análisis Exploratorio de Datos (EDA)** utilizando Python, orientado a comprender el comportamiento financiero de los clientes de una institución emisora de tarjetas de crédito.


 
### Proyecto de Portfolio | Consultoría en Ingeniería y Datos
---
## 📌 Descripción

Este proyecto forma parte del portfolio profesional de la consultora **[Nombre de tu startup]**, enfocada en análisis de datos, ingeniería y gestión de proyectos. Se realiza un **Análisis Exploratorio de Datos (EDA)** utilizando Python, orientado a comprender el comportamiento financiero de los clientes de una institución emisora de tarjetas de crédito.

---

## 🎯 Objetivos

- Realizar un análisis estadístico y visual completo de los datos.
- Detectar patrones de comportamiento financiero, consumo y pago.
- Identificar posibles segmentos de clientes para campañas o control de riesgo.
- Generar insights relevantes para la toma de decisiones en empresas del sector financiero o IT.

---

## 📂 Dataset

**🔗 Fuente**: Kaggle  
**Título**: [Credit Card Dataset for Clustering](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)  
**Registros**: 8950  
**Columnas**: 18 (variables de compras, saldos, pagos, límites de crédito y duración de relación)

---

## 🛠️ Herramientas utilizadas

- Python 3.x
- Pandas
- Seaborn & Matplotlib
- NumPy
- Jupyter Notebook

---

## 📊 Proceso de Análisis

### 1️⃣ Carga y limpieza de datos  
- Se imputaron valores faltantes con la mediana de cada variable.
- Se crearon columnas derivadas para enriquecer el análisis.

### 2️⃣ Análisis Univariado  
- Distribuciones de variables clave como `BALANCE`, `PURCHASES`, `PAYMENTS`.

### 3️⃣ Análisis Bivariado y Correlacional  
- Se utilizó un **heatmap** para evaluar relaciones entre variables financieras.

![Heatmap](img/heatmap.png)

### 4️⃣ Feature Engineering  
- Variables creadas:  
  - `Balance_to_Limit` → Relación entre saldo y límite.
  - `Dominant_Purchase` → Tipo de compra predominante.
  - `MinPay_ratio` → Proporción del pago mínimo respecto al saldo.

---

## 📈 Insights clave

### 📌 1. Uso elevado del crédito
> El 28% de los clientes utiliza más del 80% de su límite disponible.

![Pie chart](img/uso_credito.png)
   
---

### 📌 2. Comportamiento de compra dominante
> El 63% de los clientes tiene compras en cuotas como su principal tipo de compra.

![Countplot](img/dominant_purchase.png)

---

### 📌 3. Riesgo potencial por pagos mínimos bajos
> Una parte significativa de los clientes mantiene pagos mínimos muy bajos respecto a sus saldos, lo cual puede ser indicio de riesgo crediticio.

![Histograma pagos mínimos](img/minpay_ratio.png)

---

## 📦 Estructura del proyecto

EDA-CreditCard-Portfolio/
│
├── notebooks/
│ └── EDA_credit_card.ipynb
│
├── img/
│ ├── heatmap.png
│ ├── uso_credito.png
│ ├── dominant_purchase.png
│ └── minpay_ratio.png
│
└── README.md


---

## 💼 Aplicabilidad

Este análisis puede ser reutilizado o adaptado para:

- Fintechs que deseen comprender a sus clientes.
- PYMEs con sistemas de crédito interno o programas de fidelización.
- Empresas IT que implementan soluciones de scoring o customer segmentation.

---

## 👨‍💼 Autor

**Ing. Facundo Reta**  
Consultor en Ingeniería, Gestión de Proyectos y Análisis de Datos  
📧 contacto: [freta@sanluis.edu.ar]  
🌐 [www.tusitio.com](https://www.tusitio.com)

---

## ✅ Próximos pasos

- Aplicar clustering no supervisado a los segmentos identificados.
- Comparar comportamiento mensual vs anual.
- Desarrollar dashboard interactivo en Power BI como complemento visual.


