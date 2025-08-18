# ChallengeONE
# 📊 Análisis de Cancelación de Clientes (Churn Prediction)

Este proyecto tiene como objetivo **identificar los factores que influyen en la cancelación de clientes** de la empresa Telecom X, utilizando diferentes modelos de Machine Learning y técnicas de interpretación de variables.  

---

## 🚀 Flujo del Proyecto

1. **Carga y preparación de datos**  
   - Limpieza y codificación de variables categóricas.  
   - Estandarización de variables numéricas.  

2. **Modelos utilizados**  
   - **Regresión Logística** → análisis de coeficientes e interpretación del impacto directo.  
   - **Árboles de Decisión / Random Forest** → importancia de variables en base a reducción de impureza.  
   - **KNN (K-Nearest Neighbors)** → impacto indirecto por escala y distancia.  
   - **SVM (Support Vector Machine)** → interpretación de coeficientes del hiperplano.  

3. **Métricas de evaluación**  
   - Se utilizó **F1 Score** como métrica principal debido al desbalance de clases (clientes que cancelan vs. no cancelan).  
   - Ejemplo: F1 score base con KNN = `0.5122`.  

4. **Análisis de importancia de variables**  
   - Se evaluó el peso de cada variable en la predicción de cancelación.  
   - Se integró la visión de KNN (variables más discriminantes) con Regresión Logística y SVM (dirección del efecto).  

---

## 🔑 Principales Factores de Cancelación

1. **Mayor riesgo de cancelación (efecto positivo):**
   - Uso de **Fibra óptica** (`internet.InternetService_Fiber optic`).  
   - **Altos cargos totales** (`account.Charges.Total`).  
   - **Facturación sin papel** (`account.PaperlessBilling_Yes`).  
   - **Pago con electronic check** (`account.PaymentMethod_Electronic check`).  

2. **Menor riesgo de cancelación (efecto negativo):**
   - **Mayor antigüedad (tenure)** → clientes nuevos son más propensos a cancelar.  
   - **Servicios adicionales** como `OnlineSecurity` o `TechSupport`.  
   - **Contratos de uno o dos años** → reducen la rotación.  

---

## 🎯 Estrategias de Retención

- **Onboarding y retención temprana:** programas de bienvenida para clientes con baja antigüedad.  
- **Clientes de fibra óptica:** revisar percepción de valor y ofrecer bundles con otros servicios.  
- **Servicios de valor agregado:** promover seguridad online y soporte técnico.  
- **Gestión de precios:** planes escalonados y descuentos para clientes con cargos altos.  
- **Métodos de pago:** incentivar débito automático o tarjeta.  
- **Contratos largos:** ofrecer beneficios a quienes acepten contratos de 1 o 2 años.  

---

## 📈 Conclusión

El análisis muestra que la **antigüedad del cliente (tenure)** es el factor más determinante en la cancelación, mientras que los servicios contratados, el método de pago y el tipo de contrato también influyen significativamente.  
Las estrategias de fidelización deben enfocarse en **clientes nuevos**, **usuarios de fibra óptica** y **clientes con métodos de pago inestables**, promoviendo la adopción de contratos largos y servicios adicionales que aumenten la permanencia.  
