# UFC Fight Predictor - Deep Learning Project

Este proyecto utiliza redes neuronales para predecir las probabilidades de victoria en combates de la UFC, utilizando datos históricos de peleadores y resultados de eventos.

## 📊 Diccionario de Datos

### 1. Dataset de Peleadores (`df_peleadores`)
Este archivo contiene el perfil físico y las estadísticas promedio de por vida de cada peleador.

| Columna | Descripción |
| :--- | :--- |
| **Fighter_Name** | Nombre completo del peleador (ID principal). |
| **Height** | Altura del peleador (habitualmente en pies y pulgadas). |
| **Weight** | Peso del peleador (en libras). |
| **Reach** | Envergadura/alcance de los brazos (en pulgadas). |
| **Stance** | Posición de combate (Orthodox, Southpaw, Switch). |
| **DOB** | Fecha de nacimiento (*Date of Birth*). |
| **Wins / Losses / Draws** | Récord histórico de victorias, derrotas y empates. |
| **SLpM** | Golpes significativos conectados por minuto. |
| **Str_Acc** | Precisión de golpeo (*Striking Accuracy*). |
| **SApM** | Golpes significativos absorbidos por minuto. |
| **Str_Def** | Defensa de golpeo (% de golpes rivales evitados). |
| **TD_Avg** | Promedio de derribos (*Takedowns*) cada 15 minutos. |
| **TD_Acc** | Precisión de derribos. |
| **TD_Def** | Defensa de derribos (% de intentos rivales evitados). |
| **Sub_Avg** | Promedio de intentos de sumisión cada 15 minutos. |

---

### 2. Dataset de Peleas (`df_peleas`)
Contiene los resultados y estadísticas específicas de cada combate individual realizado.

| Columna | Descripción |
| :--- | :--- |
| **Fighter_1 / Fighter_2** | Nombres de los contendientes. |
| **Winner** | Nombre del ganador del encuentro. |
| **Weight_Class** | Categoría de peso en la que se realizó la pelea. |
| **Method** | Método de victoria (KO, TKO, Submission, Decision, etc.). |
| **End_Round** | Asalto en el que terminó la pelea. |
| **Total_Fight_Time_Sec** | Duración total del combate en segundos. |
| **F1_KD / F2_KD** | *Knockdowns* anotados por cada peleador. |
| **F1_Sig_Landed / Att** | Golpes significativos conectados e intentados. |
| **F1_TD_Landed / Att** | Derribos conseguidos e intentados. |
| **F1_Sub_Att** | Intentos de sumisión realizados durante la pelea. |
| **F1_Ctrl_Sec** | Tiempo total de control (en el suelo o clínica) en segundos. |
| **F1_Head / Body / Leg** | Golpes significativos conectados por zona del cuerpo. |
| **F1_Distance / Clinch / Ground** | Golpes conectados según la posición (distancia, clínica o suelo). |
| **Event_Date** | Fecha en la que ocurrió el evento. |

## 🛠️ Tecnologías Utilizadas
- **Python 3.11**
- **TensorFlow / Keras** (Redes Neuronales)
- **Pandas / NumPy** (Procesamiento de datos)
- **Scikit-learn** (Escalado y métricas)