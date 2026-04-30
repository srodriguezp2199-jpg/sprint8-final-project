# sprint8-final-project

# 📊 Análisis de Comportamiento de Clientes - NovaRetail+

## 🎯 Objetivo del Proyecto

Analizar el comportamiento de los clientes de NovaRetail+, una plataforma de comercio electrónico en Latinoamérica, para responder la pregunta central del equipo de Crecimiento y Retención:

**¿Qué factores del comportamiento del cliente están más fuertemente asociados con el ingreso anual generado?**

Para ello, el análisis busca:

- Explorar y limpiar el dataset para garantizar la calidad de los datos
- Identificar relaciones entre variables numéricas, binarias y categóricas
- Calcular coeficientes de correlación adecuados según el tipo de variable
- Generar insights exploratorios que orienten decisiones comerciales

> Este proyecto es un análisis **correlacional** (exploratorio).
> **Correlación ≠ causalidad.**

---

## 📁 Dataset Utilizado

El proyecto trabaja con una fuente de datos precargada en el entorno de TripleTen:

**`novaretail_comportamiento_clientes_2024.csv`**: Comportamiento de 15,000 clientes durante 2024

| Variable | Descripción |
|---|---|
| `id_cliente` | Identificador único del cliente |
| `edad` | Edad del cliente |
| `nivel_ingreso` | Ingreso anual estimado del cliente |
| `visitas_mes` | Número de visitas mensuales a la plataforma |
| `compras_mes` | Número de compras realizadas en el mes |
| `gasto_publicidad_dirigida` | Gasto en anuncios asignado al usuario |
| `satisfaccion` | Calificación de satisfacción (escala 1–5) |
| `miembro_premium` | Suscripción premium: 1 = sí, 0 = no |
| `abandono` | Abandono de la plataforma: 1 = sí, 0 = no |
| `tipo_dispositivo` | Dispositivo utilizado (móvil, escritorio, tablet) |
| `region` | Región geográfica (norte, sur, este, oeste) |
| `ingreso_anual` | Ingreso anual generado por el cliente (**métrica principal**) |

---

## 🔄 Etapas del Análisis

### 1. Carga y Exploración Inicial
- Carga del dataset con `pd.read_csv()`
- Validación de estructura, tipos de datos y valores faltantes
- Identificación de variables numéricas, binarias y categóricas

### 2. Preparación de Datos
- Corrección de tipos de datos
- Diagnóstico descriptivo con `.describe()`
- Documentación de supuestos del análisis

### 3. Visualización de Relaciones
- Matriz de correlación (heatmap) para variables numéricas
- Scatterplots para pares con asociaciones relevantes

### 4. Coeficientes de Correlación
- **Pearson / Spearman** para variables numéricas
- **Punto-biserial** para variables numéricas vs binarias
- **V de Cramér** para variables categóricas

### 5. Interpretación para el Negocio
- Hallazgos estructurados con evidencia visual y numérica
- Lenguaje no causal, orientado a asociaciones exploratorias

### 6. Limitaciones y Próximos Pasos
- Reconocimiento de los límites del análisis correlacional
- Propuesta de análisis complementarios

---

## 🚀 Cómo Ejecutar el Notebook

Este proyecto está diseñado para ejecutarse en el entorno de **TripleTen JupyterHub**, donde el dataset ya se encuentra precargado en `/datasets/`.

1. Abre el archivo `S8_Student_Version_Project_NovaRetail_(2) (1).ipynb` en el entorno de TripleTen
2. Ejecuta las celdas secuencialmente
3. Cada sección está documentada con observaciones e interpretaciones

---

## 📋 Requisitos

- Python 3.7+
- Bibliotecas: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`
