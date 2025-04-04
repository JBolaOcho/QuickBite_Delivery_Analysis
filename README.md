# QuickBite_Delivery_Analysis# QuickBite Delivery Analysis 🛵📊

Análisis integral de datos y modelado predictivo para optimizar el servicio de entregas de comida a domicilio de **QuickBite Delivery**.

---

## 🧠 Objetivo del Proyecto

Este proyecto tiene como propósito mejorar la eficiencia operativa y la experiencia del cliente en QuickBite Delivery, combinando técnicas de **Business Intelligence (BI)** y **Machine Learning (ML)** para:

- Analizar patrones en los tiempos de entrega considerando variables como tráfico, clima y tipo de vehículo.
- Predecir con mayor precisión el tiempo de entrega esperado para cada pedido.
- Visualizar métricas clave del servicio en dashboards interactivos.
- Proponer mejoras en la gestión logística y la asignación de recursos.

---

## 📦 Estructura del Proyecto

QuickBite_Delivery_Analysis/ 
├── data/ # Datos crudos y procesados 

├── notebooks/ # Análisis exploratorio, visualizaciones, modelado 

├── src/ # Scripts reutilizables (preprocesamiento, predicción) 

├── dashboards/ # Archivos de visualización (Power BI, notebooks) 

├── reports/ # Presentaciones, resúmenes ejecutivos 

├── models/ # Modelos entrenados guardados 

├── docs/ # README, requerimientos, documentación técnica

---

## 🧾 Variables del Dataset

| Variable                | Tipo   | Descripción |
|-------------------------|--------|-------------|
| `Order_ID`              | str    | Identificador único del pedido |
| `Distance_km`           | int    | Distancia en kilómetros entre restaurante y cliente |
| `Weather`               | str    | Condiciones climáticas (Clear, Rainy, Snowy, etc.) |
| `Traffic_Level`         | str    | Nivel de tráfico (Low, Medium, High) |
| `Time_of_Day`           | str    | Momento del día (Morning, Afternoon, Evening, Night) |
| `Vehicle_Type`          | str    | Medio de transporte (Bike, Scooter, Car) |
| `Preparation_Time_min`  | int    | Tiempo de preparación del pedido (min) |
| `Courier_Experience_yrs`| int    | Años de experiencia del repartidor |
| `Delivery_Time_min`     | int    | Tiempo total de entrega (min) - **variable objetivo** |

---

## 🔧 Herramientas Utilizadas

- Python (pandas, numpy, matplotlib, seaborn, scikit-learn)
- Jupyter Notebooks
- Power BI (dashboards)
- Git & GitHub

---

## 📈 Resultados Esperados

- Predicción precisa del tiempo de entrega.
- Paneles BI interactivos para visualizar el rendimiento de la operación.
- Recomendaciones de mejora basadas en datos.

---

## 🚀 En Desarrollo

Este proyecto se encuentra en curso. Próximamente se incluirán:
- Scripts funcionales para preprocesamiento y predicción.
- Dashboards finales.
- Documentación técnica completa.

---

## 🧑‍💻 Autor

Desarrollado por José Luis Bolaños Herrera (JBolaOcho). Proyecto personal para demostrar habilidades en análisis de datos, BI y machine learning.

---

## 📄 Licencia

MIT License. Consulta el archivo LICENSE para más detalles.