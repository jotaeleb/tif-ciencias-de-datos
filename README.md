# 🛡️ TIF — Análisis de Detección de Intrusiones en Red (CIC-IDS-2017)

| | |
|---|---|
| **Institución** | UPATECO — Tecnicatura Universitaria en Ciencia de Datos e IA Aplicada |
| **Módulo** | Ciencia de Datos y Optimización de Modelos |
| **Docente** | Amalia Guaymás Canavire |
| **Año** | 2026 |

Este repositorio contiene el desarrollo del Trabajo Integrador Final (TIF). El objetivo es desarrollar un modelo de clasificación capaz de identificar flujos de tráfico de red maliciosos utilizando técnicas de Machine Learning.

## 📊 Sobre el Dataset

El dataset fue diseñado por el **Canadian Institute for Cybersecurity (CIC)**. Contiene más de 2,8 millones de instancias capturadas durante 5 días de tráfico de red, abarcando escenarios de tráfico benigno y ataques comunes (DDoS, Fuerza Bruta, XSS, etc.).

- **Fuente original:** [UNB — CIC-IDS-2017](https://www.unb.ca/cic/datasets/ids-2017.html)
- **Formato de almacenamiento:** Los datos fueron procesados y convertidos de CSV a **Parquet** para optimizar el rendimiento y el almacenamiento.

## 🚀 Ejecución en Google Colab

- **Eda**   [![Eda en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jotaeleb/tif-ciencias-de-datos/blob/main/proyecto_eda.ipynb)

- **Entrenamiento**   [![Entrenamiento en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jotaeleb/tif-ciencias-de-datos/blob/main/proyecto_entrenamiento.ipynb)

## 🗂️ Estructura del Proyecto

```text
├── dataset/
│   ├── dataset_parte_1.parquet
│   ├── dataset_parte_2.parquet
│   ├── dataset_parte_3.parquet
│   ├── dataset_parte_4.parquet
│   └── df_muestra.parquet
├── notebooks/                   # Jupyter Notebooks del desarrollo
│   ├── proyecto_eda.ipynb
│   ├── proyecto_clean.ipynb
│   └── proyecto_entrenamiento.ipynb
├── resources/                   # Archivos complementarios
│   ├── diccionario_de_datos.md
│   └── clase_label.md
├── README.md                    # Descripción general del proyecto
└── .gitignore                   # Archivos excluidos de Git
```

## 👥 Integrantes — Grupo N° 1

| Apellido y Nombre | DNI |
|---|---|
| Alvarado, Marcelo Daniel | 39.781.697 |
| Biazutti, Jorge Luciano | 23.584.366 |
| Casasola, Hernán Guido Gustavo | 29.976.458 |
| Gonza, Gabriela Guadalupe | 31.173.807 |
| Lera, Aníbal Iván | 18.229.630 |
