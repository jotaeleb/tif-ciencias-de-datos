# Análisis de Detección de Intrusiones en Red (CIC-IDS-2017) 🛡️🔍

Este proyecto es parte del **Trabajo Integrador Final (TIF)** de la materia **Ciencia de Datos y Optimización de Modelos** perteneciente a la carrera de **Ciberseguridad 2026** . El objetivo es desarrollar un modelo de clasificación capaz de identificar flujos de tráfico de red maliciosos utilizando técnicas de Machine Learning.

## 📊 Sobre el Dataset
El dataset utilizado fue diseñado por el **Canadian Institute for Cybersecurity (CIC)**. Contiene más de **2.8 millones de instancias** capturadas durante 5 días de tráfico de red, abarcando escenarios de tráfico benigno y ataques comunes (DDoS, Brute Force, XSS, etc.).

* **Fuente original:** [UNB - CIC-IDS-2017](https://www.unb.ca/cic/datasets/ids-2017.html)
* **Formato de almacenamiento:** Los datos se han procesado y convertido de CSV a **Parquet** para optimizar el rendimiento y el almacenamiento.

## 🗂️ Estructura del Proyecto

```text
├── dataset/ 
│   ├── dataset_parte_1.parquet
│   ├── dataset_parte_2.parquet
│   ├── dataset_parte_3.parquet
│   └── dataset_parte_4.parquet
├── notebooks/              # Jupyter Notebook principal del desarrollo
├── resources/               # Archivos complementarios como Ficha del proyecto
├── README.md               # Descripción general del proyecto
└── .gitignore              # Archivos excluidos de Git
