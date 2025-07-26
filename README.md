# Análisis y Segmentación de Clientes de Tarjetas de Crédito

Este proyecto combina **Análisis exploratorio de datos (EDA)** y técnicas de clustering para segmentar clientes de una entidad emisora de tarjetas de crédito. Utilizando Python, se identifican patrones de comportamiento financiero con el objetivo de comprender mejor a los distintos grupos de clientes y apoyar estrategias personalizadas orientadas a cada segmento.

Forma parte de mi portfolio profesional como ingeniero consultor, con foco en análisis de datos, ingeniería y gestión de proyectos.

 ---
## Resumen del Proyecto

Este proyecto comienza con un Análisis Exploratorio de Datos (EDA) para obtener una visión general del comportamiento financiero de los clientes. A continuación, se realiza la limpieza y el preprocesamiento de los datos, seguidos de una reducción de dimensionalidad mediante Análisis de Componentes Principales (PCA), con el fin de simplificar el modelo y minimizar el sobreajuste.

Finalmente, se aplica un algoritmo de clustering (K-Means) para identificar grupos de clientes con características similares. El análisis revela 3 clusters diferenciados, lo que permite comprender mejor sus perfiles y potencialmente orientar estrategias específicas para cada segmento.

---

## Objetivos

- Realizar un análisis estadístico y visual completo de los datos.
- Detectar patrones de comportamiento financiero, consumo y pago.
- Identificar posibles segmentos de clientes para campañas o controles de riesgo.
- Generar insights relevantes para la toma de decisiones en empresas del sector financiero o IT.

---

## Dataset

**🔗 Fuente**: Kaggle  
**Título**: [Credit Card Dataset for Clustering](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)  
**Registros**: 8950  
**Columnas**: 18 (variables de compras, saldos, pagos, límites de crédito y duración de relación)

---

## Estructura del proyecto
Contenido del repositorio:

- Credit-Card-Clustering-Analysis.ipynb
- images/ (graficas del proyecto)
- README.md

---

## Herramientas utilizadas

- Python 3.x
- Pandas
- Seaborn & Matplotlib
- NumPy
- Jupyter Notebook

---

## Aplicabilidad

Este análisis puede ser reutilizado y/o adaptado para:

- Fintechs que deseen comprender a sus clientes.
- PYMEs con sistemas de crédito interno o programas de fidelización.
- Empresas IT que implementan soluciones de scoring o segmentación de clientes.
---

## Proceso de Análisis y segmentación

### 1. Carga y descripción de datos  
- Se carga dataset, y se cargan las librerias necesarias para el proyecto

### 2. Tratamiento de datos faltantes
- Se imputaron valores faltantes con la mediana de cada variable.
- Se crearon columnas derivadas para enriquecer el análisis.

### 3. Análisis univariado  
- Distribuciones de variables clave como `BALANCE`, `PURCHASES`, `PAYMENTS`.

### 4. Análisis Bivariado y Correlacional  
- Se utilizó un **heatmap** para evaluar correlaciones entre variables financieras.

### 5. Ingenieria de variables 
- Variables creadas:  
  - `Balance_to_Limit` → Relación entre saldo y límite.
  - `Dominant_Purchase` → Tipo de compra predominante.
  - `MinPay_ratio` → Proporción del pago mínimo respecto al saldo.

---

### 6. Insights clave

  ### 6.1 Uso elevado del crédito
  > El 20.2% de los clientes utiliza más del 80% de su límite disponible.
---
  ### 6.2 Comportamiento de compra dominante
  > El 61% de los clientes tiene compras en cuotas como su principal tipo de compra.
---
  ### 6.3 Riesgo potencial por pagos mínimos bajos
  > Una parte significativa de los clientes mantiene pagos mínimos muy bajos respecto a sus saldos, lo cual puede ser indicio de riesgo crediticio.

### 7. Pipeline
  ### 7.1 Pre procesamiento de datos
  - Tratamiento de outliers
  - Escalamiento de datos
  ### 7.2 Análisis de componentes principales (PCA)
  - Descripcion de la varianza (Definicion de componentes)
  ### 7.3 Clustering
  - Método Elbow (Codo) (k=3)
  - Método Silhouette y Davies Bouldin score (k=3)
  - K-Means
  - Boxplot variables / Cluster

### 8. Conclusion final - Implicaciones estratégicas
Este proyecto aplica técnicas de análisis exploratorio y clustering sobre datos de clientes de una fintech emisora de tarjetas de crédito. Se identificaron tres segmentos bien diferenciados:

- **Clúster 0**: Clientes con bajo nivel de compras y saldos moderados. Se sugiere fomentar su actividad con incentivos específicos.
- **Clúster 1**: Clientes altamente activos, con altos saldos y límites de crédito. Representan un perfil valioso que requiere gestión estratégica.
- **Clúster 2**: Clientes conservadores con bajo uso del crédito. Recomendable fortalecer el vínculo con herramientas educativas o ajustes graduales de crédito.

El análisis se basó en visualizaciones (*boxplots*) de variables clave como `BALANCE`, `PURCHASES`, `PAYMENTS`, `CREDIT_LIMIT`, entre otras. El resultado brinda información útil para diseñar estrategias personalizadas orientadas a la retención, fidelización y control de riesgo.

---
- Implicaciones Estratégicas
Los resultados del clustering ofrecen una base sólida para la toma de decisiones estratégicas en la fintech:

  - Marketing Personalizado: La comprensión de los perfiles permite diseñar campañas específicas. Por ejemplo, el Clúster 1 podría recibir ofertas de productos premium, mientras que el Clúster 0 podría ser incentivado con promociones para aumentar su actividad de compra.
  - Gestión de Riesgos: El Clúster 1, con mayores saldos y pagos, requiere un seguimiento más cercano para mitigar riesgos crediticios, mientras que el Clúster 2, con un comportamiento conservador, implica un riesgo menor.
  - Desarrollo de Productos: Las necesidades de cada grupo sugieren oportunidades para nuevos productos, como herramientas de incentivo para el Clúster 0 o recursos educativos para el Clúster 2.

En resumen, este análisis ha segmentado con éxito la base de clientes en tres grupos diferenciados: clientes de alta actividad (Clúster 1), clientes de baja actividad (Clúster 0) y clientes conservadores (Clúster 2). Estas conclusiones proporcionan a la fintech una guía clara para optimizar sus estrategias de marketing, gestión de riesgos y desarrollo de productos, mejorando así la satisfacción del cliente y el desempeño general del negocio.

---
## Autor

**Ing. Facundo Reta**  
Data Analyst, Project Manager Engineer  
📧 contacto: [freta@sanluis.edu.ar]  
🌐 [www.tusitio.com](https://www.tusitio.com)