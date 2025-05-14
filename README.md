# Food Delivery Time Prediction

Este proyecto tiene como objetivo predecir el tiempo de entrega de pedidos a domicilio en minutos, utilizando técnicas de análisis exploratorio de datos (EDA) y modelos de machine learning. 

---

## Estructura del Proyecto

├── data/ # Contiene los datos crudos y limpios (CSV)
├── notebooks/ # Notebooks Jupyter para EDA y modelado
│ ├── 01_EDA.ipynb
│ └── 02_Modelado_Predictivo.ipynb
└── README.md # Documentación del proyecto

---

## 1. Análisis Exploratorio (EDA)

Se realizó una exploración detallada del dataset que incluye:

- ✅ Limpieza de datos: imputación de valores nulos por media (numéricos) y moda (categóricos).
- ✅ Análisis de distribución y simetría.
- ✅ Visualizaciones: histogramas, boxplots, mapas de calor de correlación.
- ✅ Agrupaciones y orden por promedio de tiempo de entrega para variables categóricas:
  - **Weather:** “Clear” tiene menor tiempo de entrega, “Snowy” el mayor.
  - **Traffic_Level:** “Low” es el más rápido, “High” el más lento.
  - **Time_of_Day:** “Night” tiene mejores tiempos de entrega.
  - **Vehicle_Type:** diferencia leve entre scooter, bicicleta y auto.
- ✅ Gráficos por segmento para estudiar combinaciones de variables (por ejemplo, vehículo según clima).

---

## 2. Modelado Predictivo

Se implementaron dos modelos supervisados de regresión para predecir la variable `Delivery_Time_min`:

### 🔹 Regresión Lineal
- **MAE:** 5.89 min
- **RMSE:** 8.83 min
- **R²:** 0.82

### 🔹 Random Forest Regressor
- **MAE:** 7.09 min
- **RMSE:** 10.29 min
- **R²:** 0.76

> La **regresión lineal** mostró un mejor desempeño general, siendo seleccionada como modelo final.

---

## 3. Variables Importantes

A través de la importancia de las variables (gráfico de `feature_importance_` en Random Forest), se identificó:

- `Distance_km` como la variable más influyente (>70% de importancia)
- Seguido por `Preparation_Time_min` (~15%)
- El resto de variables tienen un peso bajo (<5%)

---

## 4. Predicción Individual

El modelo final permite realizar predicciones con un diccionario de entrada como este:

```python
entrada_ejemplo = {
    "Distance_km": 4.5,
    "Preparation_Time_min": 12,
    "Courier_Experience_yrs": 3,
    "Weather": "Clear",           # Clear, Rainy, Foggy, Windy, Snowy
    "Traffic_Level": "Medium",    # Low, Medium, High
    "Time_of_Day": "Afternoon",   # Morning, Afternoon, Evening, Night
    "Vehicle_Type": "Scooter"     # Scooter, Bike, Car
}

---

## 5. Comparación de Modelos
Se realizaron gráficos comparativos de errores (MAE, RMSE, R²) entre regresión lineal y Random Forest, permitiendo visualizar claramente el mejor desempeño de la regresión lineal en este caso.

---

 Conclusiones
El proyecto identificó patrones importantes como el impacto del clima, tráfico y experiencia del repartidor.

La distancia al cliente es el principal factor que determina el tiempo de entrega.

Un modelo de regresión lineal simple, pero bien preparado, puede ofrecer resultados altamente precisos y comprensibles.

La solución es fácilmente integrable en sistemas logísticos o plataformas de seguimiento.

---

 Herramientas utilizadas
Python, pandas, matplotlib, seaborn, scikit-learn

Jupyter Notebook

Dataset de Kaggle: https://www.kaggle.com/datasets/denkuznetz/food-delivery-time-prediction/data

Archivo: requirements.txt

---

Autor
José Luis Bolaños Herrera.