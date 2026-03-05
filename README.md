# TelecomX_LATAM
Challenge de Alura sobre ETL

https://github.com/yansiercaro/TelecomX_LATAM/issues/1#issue-4031071300

# 📊 Análisis de Evasión de Clientes (Churn) - Telecom X

Este proyecto tiene como objetivo identificar los factores principales que influyen en la salida de clientes de la empresa Telecom X, utilizando técnicas de limpieza, transformación y análisis exploratorio de datos (EDA) para generar recomendaciones estratégicas.

## 🚀 Resumen del Proyecto

El análisis se centra en transformar datos crudos provenientes de una API en un formato estructurado para detectar patrones de comportamiento. Se identificó que la antigüedad del cliente, el tipo de contrato y los cargos mensuales son los predictores más fuertes de la evasión.

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** Python 3.x
* **Librerías:** * `Pandas`: Manipulación y limpieza de datos.
    * `Requests`: Extracción de datos desde la API.
    * `Matplotlib` & `Seaborn`: Visualización estadística.
    * `Warnings`: Gestión de alertas de compatibilidad.

## 📋 Flujo de Trabajo

### 1. Extracción y Normalización
Se procesó un archivo JSON con estructuras anidadas, normalizando las columnas `customer`, `phone`, `internet` y `account` para crear un DataFrame plano unificado.

### 2. Limpieza de Datos
* Conversión de la columna `TotalCharges` a tipo numérico.
* Eliminación de valores nulos y registros inconsistentes.
* Creación de la métrica **`Cuentas_Diarias`** para analizar el impacto del costo diario en la fuga.

### 3. Estandarización y Transformación
* **Traducción:** Columnas renombradas al español para mayor claridad de los stakeholders.
* **Binarización:** Conversión de variables categóricas (Sí/No, Género) a formato binario (1/0).
* **One-Hot Encoding:** Transformación de variables multiclase como `Tipo_Contrato` e `InternetService`.

### 4. Análisis Exploratorio (EDA)
Se generaron visualizaciones para comparar la distribución de la fuga según:
* **Variables Categóricas:** Contratos mensuales vs. anuales y métodos de pago.
* **Variables Numéricas:** Relación entre cargos mensuales y meses de antigüedad.



## 💡 Hallazgos Principales (Insights)

* **Riesgo por Contrato:** Los clientes con contratos "Mes a Mes" tienen la tasa de fuga más alta.
* **Sensibilidad al Precio:** Los clientes que cancelan pagan, en promedio, un 20% más por mes que los clientes retenidos.
* **Periodo Crítico:** El mayor volumen de evasión ocurre durante el primer año de servicio (específicamente entre los meses 1 y 12).

## 📈 Recomendaciones

1. **Incentivos de Permanencia:** Migrar clientes de contratos mensuales a anuales mediante descuentos.
2. **Optimización de Fibra Óptica:** Revisar la estabilidad y precio del servicio de fibra, dado que presenta mayor rotación que el DSL.
3. **Campañas de Onboarding:** Reforzar el soporte técnico durante los primeros 6 meses del cliente.

## 📦 Cómo Ejecutar el Proyecto

1. Clonar el repositorio.
2. Instalar dependencias: `pip install pandas seaborn matplotlib requests`.
3. Ejecutar el notebook principal para replicar el análisis.

## Para soporte técnico

joseyansiercarovarona@gmail.com
