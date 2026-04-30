# 📋 Información del dataset

| Campo | Descripción |
| :--- | :--- |
| **Nombre** | CICIDS2017 — Network Intrusion Dataset |
| **Institución creadora** | Canadian Institute for Cybersecurity (CIC) — University of New Brunswick |
| **Propósito** | Desarrollo y evaluación de sistemas de detección de intrusiones (IDS/NIDS) |
| **Mecanismo de recolección** | Captura de tráfico de red real durante 5 días con **CICFlowMeter** (extrae features de flujos TCP/UDP) |
| **Registros** | 2.830.743 |
| **Variables** | 78 variables numéricas + 1 variable categórica `Label` |
| **Documentación de cada variable** | La descripción técnica de cada una de las 78-79 columnas (como *Flow Duration*, *Total Fwd Packets*, *Init_Win_bytes_forward*, etc.) está disponible en el repositorio de **CICFlowMeter**, que es el software que extrajo las características de los archivos de tráfico original (pcap). <br> [CICFlowMeter ReadMe (Lista de Features)](https://github.com/ahlashkari/CICFlowMeter/blob/master/ReadMe.txt) |
| **Fuentes** | [Kaggle](https://www.kaggle.com/datasets/cicdataset/cicids2017) · [UNB oficial](https://www.unb.ca/cic/datasets/ids-2017.html) |
| **Restricciones** | Libre para uso académico e investigación |
