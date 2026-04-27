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

# 📖 Diccionario de Variables

Este dataset contiene **78 variables numéricas** y **1 variable categórica** (Label). 

### 1. Identificadores y Puertos
| Variable | Descripción |
| :--- | :--- |
| `Destination Port` | Puerto de destino del flujo. |

### 2. Estadísticas de Tiempo y Duración (IAT - Inter-Arrival Time)
| Variable | Descripción |
| :--- | :--- |
| `Flow Duration` | Duración total del flujo en microsegundos. |
| `Flow IAT Mean` | Media del tiempo entre la llegada de dos paquetes en el flujo. |
| `Flow IAT Std` | Desviación estándar del tiempo entre paquetes. |
| `Flow IAT Max` | Tiempo máximo entre la llegada de dos paquetes. |
| `Flow IAT Min` | Tiempo mínimo entre la llegada de dos paquetes. |
| `Fwd IAT Total` | Tiempo total entre paquetes en dirección forward. |
| `Fwd IAT Mean` | Media del tiempo entre paquetes forward. |
| `Fwd IAT Std` | Desviación estándar del tiempo entre paquetes forward. |
| `Fwd IAT Max` | Tiempo máximo entre paquetes forward. |
| `Fwd IAT Min` | Tiempo mínimo entre paquetes forward. |
| `Bwd IAT Total` | Tiempo total entre paquetes en dirección backward. |
| `Bwd IAT Mean` | Media del tiempo entre paquetes backward. |
| `Bwd IAT Std` | Desviación estándar del tiempo entre paquetes backward. |
| `Bwd IAT Max` | Tiempo máximo entre paquetes backward. |
| `Bwd IAT Min` | Tiempo mínimo entre paquetes backward. |

### 3. Estadísticas de Longitud y Tamaño de Paquetes
| Variable | Descripción |
| :--- | :--- |
| `Total Fwd Packets` | Número total de paquetes en dirección forward. |
| `Total Backward Packets` | Número total de paquetes en dirección backward. |
| `Total Length of Fwd Packets` | Tamaño total de los paquetes forward (bytes). |
| `Total Length of Bwd Packets` | Tamaño total de los paquetes backward (bytes). |
| `Fwd Packet Length Max` | Longitud máxima de un paquete forward. |
| `Fwd Packet Length Min` | Longitud mínima de un paquete forward. |
| `Fwd Packet Length Mean` | Longitud media de los paquetes forward. |
| `Fwd Packet Length Std` | Desviación estándar de la longitud de paquetes forward. |
| `Bwd Packet Length Max` | Longitud máxima de un paquete backward. |
| `Bwd Packet Length Min` | Longitud mínima de un paquete backward. |
| `Bwd Packet Length Mean` | Longitud media de los paquetes backward. |
| `Bwd Packet Length Std` | Desviación estándar de la longitud de paquetes backward. |
| `Flow Bytes/s` | Tasa de transferencia de bytes por segundo. |
| `Flow Packets/s` | Tasa de transferencia de paquetes por segundo. |
| `Min Packet Length` | Longitud mínima observada en todo el flujo. |
| `Max Packet Length` | Longitud máxima observada en todo el flujo. |
| `Packet Length Mean` | Media de la longitud de todos los paquetes. |
| `Packet Length Std` | Desviación estándar de la longitud de paquetes. |
| `Packet Length Variance` | Varianza de la longitud de los paquetes. |
| `Average Packet Size` | Tamaño promedio de los paquetes en el flujo. |
| `Avg Fwd Segment Size` | Tamaño promedio de segmento en dirección forward. |
| `Avg Bwd Segment Size` | Tamaño promedio de segmento en dirección backward. |

### 4. Banderas TCP (Flags) y Conteo de Control
| Variable | Descripción |
| :--- | :--- |
| `Fwd PSH Flags` | Conteo de banderas PSH en paquetes forward. |
| `Bwd PSH Flags` | Conteo de banderas PSH en paquetes backward. |
| `Fwd URG Flags` | Conteo de banderas URG en paquetes forward. |
| `Bwd URG Flags` | Conteo de banderas URG en paquetes backward. |
| `Fwd Header Length` | Longitud total de las cabeceras en dirección forward. |
| `Bwd Header Length` | Longitud total de las cabeceras en dirección backward. |
| `FIN Flag Count` | Número de paquetes con bandera FIN. |
| `SYN Flag Count` | Número de paquetes con bandera SYN. |
| `RST Flag Count` | Número de paquetes con bandera RST. |
| `PSH Flag Count` | Número de paquetes con bandera PSH. |
| `ACK Flag Count` | Número de paquetes con bandera ACK. |
| `URG Flag Count` | Número de paquetes con bandera URG. |
| `CWE Flag Count` | Número de paquetes con bandera CWE. |
| `ECE Flag Count` | Número de paquetes con bandera ECE. |
| `Down/Up Ratio` | Relación de descarga frente a subida. |

### 5. Estadísticas de Bulk (Ráfagas)
| Variable | Descripción |
| :--- | :--- |
| `Fwd Avg Bytes/Bulk` | Promedio de bytes por ráfaga en forward. |
| `Fwd Avg Packets/Bulk` | Promedio de paquetes por ráfaga en forward. |
| `Fwd Avg Bulk Rate` | Tasa promedio de ráfaga en forward. |
| `Bwd Avg Bytes/Bulk` | Promedio de bytes por ráfaga en backward. |
| `Bwd Avg Packets/Bulk` | Promedio de paquetes por ráfaga en backward. |
| `Bwd Avg Bulk Rate` | Tasa promedio de ráfaga en backward. |

### 6. Subflujos y Ventanas
| Variable | Descripción |
| :--- | :--- |
| `Subflow Fwd Packets` | Número promedio de paquetes en subflujos forward. |
| `Subflow Fwd Bytes` | Número promedio de bytes en subflujos forward. |
| `Subflow Bwd Packets` | Número promedio de paquetes en subflujos backward. |
| `Subflow Bwd Bytes` | Número promedio de bytes en subflujos backward. |
| `Init_Win_bytes_forward` | Bytes enviados en la ventana inicial (forward). |
| `Init_Win_bytes_backward` | Bytes enviados en la ventana inicial (backward). |
| `act_data_pkt_fwd` | Paquetes con al menos 1 byte de carga útil de TCP en forward. |
| `min_seg_size_forward` | Tamaño mínimo de segmento observado en forward. |

### 7. Estados Active e Idle (Actividad de Red)
| Variable | Descripción |
| :--- | :--- |
| `Active Mean` | Tiempo medio que el flujo estuvo activo antes de quedar inactivo. |
| `Active Std` | Desviación estándar del tiempo activo. |
| `Active Max` | Tiempo máximo que el flujo estuvo activo. |
| `Active Min` | Tiempo mínimo que el flujo estuvo activo. |
| `Idle Mean` | Tiempo medio que el flujo estuvo inactivo antes de activarse. |
| `Idle Std` | Desviación estándar del tiempo inactivo. |
| `Idle Max` | Tiempo máximo que el flujo estuvo inactivo. |
| `Idle Min` | Tiempo mínimo que el flujo estuvo inactivo. |

### 8. Variable Objetivo
| Variable | Descripción |
| :--- | :--- |
| `Label` | Clase del tráfico (BENIGN o el nombre del ataque específico). |

# 🛡️ Clases y Tipos de Ataque

| Clase | Tipo de ataque |
| :--- | :--- |
| **BENIGN** | Tráfico normal (~80% del dataset) |
| **DoS Hulk** | Denegación de servicio — Hulk |
| **DoS GoldenEye** | Denegación de servicio — GoldenEye |
| **DoS slowloris** | Denegación de servicio — Slowloris |
| **DoS Slowhttptest** | Denegación de servicio — Slowhttptest |
| **DDoS** | Ataque distribuido de denegación de servicio |
| **PortScan** | Escaneo de puertos |
| **FTP-Patator** | Fuerza bruta sobre FTP |
| **SSH-Patator** | Fuerza bruta sobre SSH |
| **Bot** | Tráfico de botnet |
| **Web Attack - Brute Force** | Ataque web por fuerza bruta |
| **Web Attack - XSS** | Cross-site scripting |
| **Web Attack - SQL Injection** | Inyección SQL |
| **Infiltration** | Infiltración de red |
| **Heartbleed** | Explotación de vulnerabilidad Heartbleed |
