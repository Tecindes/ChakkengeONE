# 📊 Telecom X - Parte 2: Predicción de Churn

## 🎯 Propósito del análisis
Este proyecto tiene como objetivo **predecir el churn (cancelación de clientes)** en una empresa de telecomunicaciones, utilizando variables de comportamiento, servicios contratados y características sociodemográficas.  
El análisis busca **identificar los principales factores de riesgo y protección** asociados a la cancelación, y a partir de ellos, proponer **estrategias de retención basadas en evidencia**.

---

## 📂 Estructura del proyecto
TelecomX-Parte2/

│── 📓 TelecomX_Parte2.ipynb # Cuaderno principal (Google Colab / Jupyter)

│── 📑 reporte.csv # Dataset procesado para modelado

│── 📄 README.md # Documentación del proyecto

---

## 🛠️ Preparación de datos

### 1. Clasificación de variables
- **Categóricas:** Tipo de contrato, método de pago, servicios de internet, soporte técnico, facturación electrónica, etc.  
- **Numéricas:** Tenure (antigüedad), cargos mensuales, cargos totales, edad, entre otras.

### 2. Transformaciones
- **Codificación One-Hot Encoding** para variables categóricas.  
- **Normalización (StandardScaler)** aplicada en modelos sensibles a la escala (p.ej., KNN, regresión logística).  

### 3. División de los datos
- **Entrenamiento:** 70%  
- **Prueba:** 30%  
Se mantuvo un balance adecuado entre churn y no churn para asegurar representatividad en ambos conjuntos.

---

## 🤖 Modelado y justificación
Se utilizaron distintos algoritmos para capturar diferentes patrones en los datos:

- **Regresión Logística:** Interpretable, útil para cuantificar impacto de cada variable.  
- **KNN:** Basado en distancias, sensible a la normalización, útil para identificar grupos de clientes similares.  
- **Otros modelos explorados:** (si los probaste, se listan aquí: Random Forest, XGBoost, etc.).

Las decisiones se tomaron en función de:  
- **Rendimiento (F1 Score, AUC).**  
- **Interpretabilidad de resultados.**  
- **Coherencia con el negocio.**

---

## 📈 Exploratory Data Analysis (EDA) – Principales insights

Algunos hallazgos destacados de la fase exploratoria y del modelado:  
- **Mayor riesgo de cancelación** en clientes con **fibra óptica**, facturación electrónica y pago por **e-check**.  
- **Mayor permanencia** y menor churn en clientes con contratos de **1-2 años** y métodos de pago automáticos (tarjeta/débito).  
- **Factores protectores:** soporte técnico, seguridad online y tenure largo.  

Ejemplos de visualizaciones:  
- Distribución de tenure vs churn.

  <img width="460" height="270" alt="image" src="https://github.com/user-attachments/assets/82320c9c-b92e-46d0-b27a-a74148fa1c28" />

- Correlaciones de variables con Churn.
  
  <img width="788" height="355" alt="image" src="https://github.com/user-attachments/assets/cb485997-8447-468b-b75c-79eecac253cd" />

- Importancia de variables por modelo (coeficientes, varianza, F1).

<img width="902" height="416" alt="image" src="https://github.com/user-attachments/assets/7c0c0e7a-423f-4331-bc3e-e5bd8953b9ac" />

<img width="906" height="418" alt="image" src="https://github.com/user-attachments/assets/dd8eb81c-fdbb-4687-b267-3eedb2c3c281" />

---

## 🛡️ Estrategias de retención basadas en evidencia

### 🔹 Reforzar factores protectores
- Incentivar contratos largos mediante descuentos o upgrades.  
- Promover servicios de soporte y seguridad como parte del valor agregado.  
- Ofrecer paquetes “combo” con beneficios adicionales al combinar contrato largo + pago automático.  

### 🔹 Mitigar factores de riesgo
- Revisar la experiencia de clientes con **fibra óptica** (soporte técnico proactivo, encuestas).  
- Segmentar clientes con **facturación electrónica** y ofrecerles un canal de contacto humano.  
- Monitorear clientes que usan **e-check** y recomendar alternativas más estables (tarjeta automática, débito).  

---

## ▶️ Instrucciones de ejecución

1. **Abrir el cuaderno:**  
   Ejecutar `TelecomX_Parte2.ipynb` en Google Colab o Jupyter.

2. **Instalar dependencias:**  
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
