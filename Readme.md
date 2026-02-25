# Análisis de Retención de Clientes (Telco Churn) 🚀

Este proyecto utiliza Ciencia de Datos para identificar por qué los clientes de una empresa de telecomunicaciones cancelan sus servicios y propone estrategias basadas en datos para mejorar la retención.

## 📊 Hallazgos Principales (Insights)
Basado en el Análisis Exploratorio de Datos (EDA) realizado:
- **Contratos Críticos:** Los clientes con contratos **mes a mes** representan el mayor foco de fuga (más del 40% de abandono).
- **Servicios de Apoyo:** La falta de **Soporte Técnico** y **Seguridad Online** está fuertemente correlacionada con la salida de clientes.
- **Fidelización:** Existe una relación inversa entre la antigüedad (`tenure`) y la fuga; los primeros 6 meses son críticos para asegurar la lealtad del cliente.
- **Métodos de Pago:** Los clientes que utilizan cheque electrónico tienen una tasa de abandono significativamente mayor que aquellos con pagos automatizados.

## 🛠️ Stack Tecnológico
- **Sistema Operativo:** Arch Linux 🐧
- **Lenguaje:** Python 3.14
- **Entorno:** Virtualenv (venv)
- **Librerías Principales:** Pandas, Seaborn, Matplotlib, Kagglehub.

## 📂 Estructura del Proyecto
- `analisis_churn.ipynb`: Notebook principal con el análisis visual y limpieza de datos.
- `requirements.txt`: Lista de dependencias para replicar el entorno.
- `.gitignore`: Configuración para mantener el repositorio limpio de archivos innecesarios.

## 🚀 Cómo ejecutarlo
1. Clonar el repositorio.
2. Crear entorno virtual: `python -m venv venv`.
3. Activar entorno: `source venv/bin/activate`.
4. Instalar dependencias: `pip install -r requirements.txt`.
5. Ejecutar el notebook en VS Code.

---
*Proyecto en desarrollo - Siguiente paso: Implementación de Modelos de Machine Learning para predicción de fuga.*
