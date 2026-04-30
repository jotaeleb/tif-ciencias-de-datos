# 📖 Diccionario de Datos

Este dataset contiene **78 variables numéricas** y **1 variable categórica** (Label).

### **CARACTERÍSTICAS GENERALES DEL FLUJO**

| # | Nombre de variable | Descripción | Tipo de dato | Valores aceptados | ¿Acepta faltantes? |
| --- | --- | --- | --- | --- | --- |
| 1 | Destination Port | Puerto de destino del flujo de red. Identifica el servicio al que se dirige la conexión (ej: 80=HTTP, 443=HTTPS, 22=SSH, 21=FTP). | Numérico entero | 0 – 65535 | ❌  No |
| 2 | Flow Duration | Duración total del flujo de red, expresada en microsegundos. Desde el primer paquete hasta el último del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 3 | Total Fwd Packets | Cantidad total de paquetes enviados en la dirección forward (del origen al destino) durante el flujo. | Numérico entero | ≥ 0 | ❌  No |
| 4 | Total Backward Packets | Cantidad total de paquetes enviados en la dirección backward (del destino al origen) durante el flujo. | Numérico entero | ≥ 0 | ❌  No |
| 5 | Total Length of Fwd Packets | Suma total de bytes de todos los paquetes en dirección forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 6 | Total Length of Bwd Packets | Suma total de bytes de todos los paquetes en dirección backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 7 | Flow Bytes/s | Tasa de transferencia del flujo expresada en bytes por segundo. Se calcula como total de bytes / duración del flujo. | Numérico continuo (float64) | ≥ 0 (puede contener inf si Flow Duration = 0) | ⚠  Sí (contiene inf) |
| 8 | Flow Packets/s | Tasa de paquetes del flujo por segundo. Se calcula como total de paquetes / duración del flujo. | Numérico continuo (float64) | ≥ 0 (puede contener inf si Flow Duration = 0) | ⚠  Sí (contiene inf) |
| 9 | Flow IAT Mean | Tiempo inter-arribo medio entre paquetes consecutivos del flujo (en ambas direcciones). IAT = Inter-Arrival Time. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 10 | Flow IAT Std | Desviación estándar del tiempo inter-arribo entre paquetes del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 11 | Flow IAT Max | Valor máximo del tiempo inter-arribo entre paquetes del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 12 | Flow IAT Min | Valor mínimo del tiempo inter-arribo entre paquetes del flujo. | Numérico continuo (float64) | ≥ 0 (puede ser negativo por error de reloj) | ❌  No |

### **CARACTERÍSTICAS DE PAQUETES Y LONGITUDES**

| # | Nombre de variable | Descripción | Tipo de dato | Valores aceptados | ¿Acepta faltantes? |
| --- | --- | --- | --- | --- | --- |
| 13 | Fwd IAT Total | Suma total de los tiempos inter-arribo entre paquetes en dirección forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 14 | Fwd IAT Mean | Tiempo inter-arribo medio entre paquetes en dirección forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 15 | Fwd IAT Std | Desviación estándar del tiempo inter-arribo entre paquetes forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 16 | Fwd IAT Max | Valor máximo del tiempo inter-arribo entre paquetes forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 17 | Fwd IAT Min | Valor mínimo del tiempo inter-arribo entre paquetes forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 18 | Bwd IAT Total | Suma total de los tiempos inter-arribo entre paquetes en dirección backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 19 | Bwd IAT Mean | Tiempo inter-arribo medio entre paquetes en dirección backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 20 | Bwd IAT Std | Desviación estándar del tiempo inter-arribo entre paquetes backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 21 | Bwd IAT Max | Valor máximo del tiempo inter-arribo entre paquetes backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 22 | Bwd IAT Min | Valor mínimo del tiempo inter-arribo entre paquetes backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 23 | Fwd Packet Length Max | Longitud máxima (en bytes) de los paquetes en dirección forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 24 | Fwd Packet Length Min | Longitud mínima (en bytes) de los paquetes en dirección forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 25 | Fwd Packet Length Mean | Longitud media (en bytes) de los paquetes en dirección forward. Feature altamente discriminante para detección de ataques. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 26 | Fwd Packet Length Std | Desviación estándar de la longitud de los paquetes en dirección forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 27 | Bwd Packet Length Max | Longitud máxima (en bytes) de los paquetes en dirección backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 28 | Bwd Packet Length Min | Longitud mínima (en bytes) de los paquetes en dirección backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 29 | Bwd Packet Length Mean | Longitud media (en bytes) de los paquetes en dirección backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 30 | Bwd Packet Length Std | Desviación estándar de la longitud de los paquetes en dirección backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 31 | Min Packet Length | Longitud mínima de todos los paquetes del flujo (forward y backward combinados). | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 32 | Max Packet Length | Longitud máxima de todos los paquetes del flujo (forward y backward combinados). | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 33 | Packet Length Mean | Longitud media de todos los paquetes del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 34 | Packet Length Std | Desviación estándar de la longitud de todos los paquetes del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 35 | Packet Length Variance | Varianza de la longitud de todos los paquetes del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 36 | Average Packet Size | Tamaño promedio de los paquetes del flujo. Similar a Packet Length Mean pero calculado de forma diferente por CICFlowMeter. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 37 | Avg Fwd Segment Size | Tamaño promedio de los segmentos en dirección forward. Equivale a Fwd Packet Length Mean en la mayoría de los casos. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 38 | Avg Bwd Segment Size | Tamaño promedio de los segmentos en dirección backward. Equivale a Bwd Packet Length Mean en la mayoría de los casos. | Numérico continuo (float64) | ≥ 0 | ❌  No |


### **FLAGS TCP, VENTANAS Y TASAS**

| # | Nombre de variable | Descripción | Tipo de dato | Valores aceptados | ¿Acepta faltantes? |
| --- | --- | --- | --- | --- | --- |
| 39 | Fwd PSH Flags | Número de veces que el flag PSH (Push) está activado en los paquetes forward. PSH indica que los datos deben enviarse de inmediato al nivel de aplicación. | Numérico entero binario | 0 o 1 | ❌  No |
| 40 | Bwd PSH Flags | Número de veces que el flag PSH está activado en los paquetes backward. | Numérico entero binario | 0 o 1 | ❌  No |
| 41 | Fwd URG Flags | Número de veces que el flag URG (Urgent) está activado en los paquetes forward. Indica datos urgentes. | Numérico entero binario | 0 o 1 | ❌  No |
| 42 | Bwd URG Flags | Número de veces que el flag URG está activado en los paquetes backward. | Numérico entero binario | 0 o 1 | ❌  No |
| 43 | FIN Flag Count | Cantidad de paquetes con flag FIN activado en el flujo. FIN indica el cierre de la conexión TCP. | Numérico entero | ≥ 0 | ❌  No |
| 44 | SYN Flag Count | Cantidad de paquetes con flag SYN activado. SYN inicia una conexión TCP. Alta en ataques SYN Flood. | Numérico entero | ≥ 0 | ❌  No |
| 45 | RST Flag Count | Cantidad de paquetes con flag RST (Reset) activado. RST indica un reseteo abrupto de la conexión. | Numérico entero | ≥ 0 | ❌  No |
| 46 | PSH Flag Count | Cantidad total de paquetes con flag PSH activado en el flujo completo (forward + backward). | Numérico entero | ≥ 0 | ❌  No |
| 47 | ACK Flag Count | Cantidad de paquetes con flag ACK activado. ACK confirma recepción. Muy frecuente en tráfico normal. | Numérico entero | ≥ 0 | ❌  No |
| 48 | URG Flag Count | Cantidad total de paquetes con flag URG activado en el flujo completo. | Numérico entero | ≥ 0 | ❌  No |
| 49 | CWE Flag Count | Cantidad de paquetes con flag CWE (Congestion Window Reduced Echo) activado. | Numérico entero | ≥ 0 | ❌  No |
| 50 | ECE Flag Count | Cantidad de paquetes con flag ECE (ECN-Echo) activado. Relacionado con el control de congestión. | Numérico entero | ≥ 0 | ❌  No |
| 51 | Fwd Header Length | Longitud total del header (cabecera) de los paquetes forward en bytes. | Numérico entero | ≥ 0 | ❌  No |
| 52 | Bwd Header Length | Longitud total del header (cabecera) de los paquetes backward en bytes. | Numérico entero | ≥ 0 | ❌  No |
| 53 | Fwd Packets/s | Tasa de paquetes por segundo en dirección forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 54 | Bwd Packets/s | Tasa de paquetes por segundo en dirección backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 55 | Down/Up Ratio | Razón entre paquetes backward (download) y forward (upload). Ratio > 1 indica más tráfico de descarga. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 56 | Fwd Avg Bytes/Bulk | Promedio de bytes por bulk en dirección forward. Bulk = transferencias masivas de datos. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 57 | Fwd Avg Packets/Bulk | Promedio de paquetes por bulk en dirección forward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 58 | Fwd Avg Bulk Rate | Tasa promedio de transferencia bulk en dirección forward (bytes/s). | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 59 | Bwd Avg Bytes/Bulk | Promedio de bytes por bulk en dirección backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 60 | Bwd Avg Packets/Bulk | Promedio de paquetes por bulk en dirección backward. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 61 | Bwd Avg Bulk Rate | Tasa promedio de transferencia bulk en dirección backward (bytes/s). | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 62 | Init_Win_bytes_forward | Número de bytes enviados en la ventana inicial de TCP en dirección forward. Valor de la ventana en el handshake SYN. | Numérico entero | -1 a 65535 | ❌  No |
| 63 | Init_Win_bytes_backward | Número de bytes enviados en la ventana inicial de TCP en dirección backward. Valor en SYN-ACK. | Numérico entero | -1 a 65535 | ❌  No |
| 64 | act_data_pkt_fwd | Cantidad de paquetes con al menos 1 byte de payload (datos reales) en dirección forward. Excluye paquetes de control puro. | Numérico entero | ≥ 0 | ❌  No |
| 65 | min_seg_size_forward | Tamaño mínimo de segmento observado en la dirección forward (en bytes). | Numérico entero | ≥ 0 | ❌  No |

### **TIEMPOS ACTIVOS / INACTIVOS Y SUBFLUJOS**

| # | Nombre de variable | Descripción | Tipo de dato | Valores aceptados | ¿Acepta faltantes? |
| --- | --- | --- | --- | --- | --- |
| 66 | Active Mean | Tiempo medio (en microsegundos) durante el que el flujo estuvo activo antes de entrar en un período de inactividad. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 67 | Active Std | Desviación estándar del tiempo activo del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 68 | Active Max | Tiempo máximo de actividad continua del flujo antes de una pausa. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 69 | Active Min | Tiempo mínimo de actividad continua del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 70 | Idle Mean | Tiempo medio (en microsegundos) durante el que el flujo estuvo inactivo (sin enviar/recibir paquetes). | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 71 | Idle Std | Desviación estándar del tiempo de inactividad del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 72 | Idle Max | Tiempo máximo de inactividad del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 73 | Idle Min | Tiempo mínimo de inactividad del flujo. | Numérico continuo (float64) | ≥ 0 | ❌  No |
| 74 | Subflow Fwd Packets | Promedio de paquetes en subflujos en dirección forward. Un subflujo es una subdivisión del flujo principal. | Numérico entero | ≥ 0 | ❌  No |
| 75 | Subflow Fwd Bytes | Promedio de bytes en subflujos en dirección forward. | Numérico entero | ≥ 0 | ❌  No |
| 76 | Subflow Bwd Packets | Promedio de paquetes en subflujos en dirección backward. | Numérico entero | ≥ 0 | ❌  No |
| 77 | Subflow Bwd Bytes | Promedio de bytes en subflujos en dirección backward. | Numérico entero | ≥ 0 | ❌  No |
| 78 | Fwd Header Length.1 | Duplicado técnico de Fwd Header Length generado por CICFlowMeter en algunos archivos. Misma semántica: longitud del header forward en bytes. | Numérico entero | ≥ 0 | ❌  No |

### **VARIABLE OBJETIVO**

| # | Nombre de variable | Descripción | Tipo de dato | Valores aceptados | ¿Acepta faltantes? |
| --- | --- | --- | --- | --- | --- |
| 79 |  Label | Variable objetivo (target). Etiqueta que indica si el flujo corresponde a tráfico normal (BENIGN) o a un tipo específico de ataque. ⚠ El nombre real en el CSV tiene un espacio al inicio: ' Label'. Usar df.columns.str.strip() al cargar. | Categórico nominal (object) | 15 valores: BENIGN, DoS Hulk, PortScan, DDoS, DoS GoldenEye, FTP-Patator, SSH-Patator, DoS slowloris, DoS Slowhttptest, Bot, Web Attack–Brute Force, Web Attack–XSS, Infiltration, Web Attack–SQL Injection, Heartbleed | ❌  No |