# Protocolos IoT (Streamlit, 100% web)
 
Práctica de la asignatura **Blockchain y IoT** (4º curso).  
Compararemos **WiFi, Zigbee, LoRaWAN y NB-IoT** en consumo, latencia, cobertura y vida de batería, usando **Streamlit Community Cloud**.  
No hace falta instalar nada en local. Todo se hace online.
 
---
 
## 🚀 Objetivo
- Entender diferencias entre protocolos IoT.  
- Ajustar parámetros (nº sensores, mensajes, payload, batería).  
- Ver cómo cambian consumo, latencia, cobertura y duración de batería.  
- Defender un protocolo para un caso real (hogar, parking o riego).  
 
---
 
## 📝 Pasos rápidos
 
### 1. Crea tu repositorio
1. Entra en [GitHub](https://github.com/).  
2. **New Repository** → Nombre: `sesion3-iot-streamlit`.  
3. Marca *Add a README file* y crea el repo.  
4. Añade dos archivos:  
   - `app.py` → copia el código que te da el profesor.  
   - `requirements.txt` → pega las dependencias:
     ```
     streamlit==1.37.1
     pandas==2.2.2
     numpy==1.26.4
     matplotlib==3.8.4
     ```
5. Commit en la rama `main`.
 
---
 
### 2. Despliega la app
1. Entra en [Streamlit Community Cloud](https://streamlit.io).  
2. Sign in con GitHub.  
3. **Deploy an app** → selecciona tu repo.  
4. Main file path: `app.py`.  
5. Pulsa **Deploy**.  
6. Abre la URL de tu app (se comparte con tu equipo).
 
---
 
### 3. Actividad guiada (40 min)
 
#### Parte A (exploración de parámetros, 10 min)
- Cambia en la barra lateral:  
  - `Nº sensores`: 50 → 500  
  - `Mensajes/día`: 6 → 96  
  - `Payload`: 20 → 200  
  - `Ratio downlink`: 0.0 → 0.3  
  - `Batería`: 1000 → 5000  
- Observa: ¿quién gana en consumo, latencia, cobertura y días de batería?
 
#### Parte B (mini-experimentos, 8 min)
1. **Tráfico:** fija payload=64 y batería=2400.  
   - Cambia msgs/día: 6 → 24 → 96.  
   - ¿Cuándo Zigbee deja de ser competitivo frente a NB-IoT?  
2. **Overhead:** fija msgs/día=24, payload=32, rx_ratio=0.05.  
   - Cambia overhead 1.0 → 2.0.  
   - ¿Quién sufre más: LoRaWAN o WiFi? Explica por qué.  
 
#### Parte C (caso aplicado, 8 min)
Elige 1 caso:
- Smart Home → Zigbee vs WiFi  
- Parking urbano → NB-IoT vs LoRaWAN  
- Riego agrícola → LoRaWAN vs NB-IoT  
 
Tarea:
- Ajusta parámetros para tu caso.  
- En el panel *Caso aplicado*, escribe justificación (2–3 frases).  
- Exporta CSV con resultados.
 
---
 
### 4. Entrega (5 min)
Sube a tu repositorio o al LMS:
1. `resultados_protocolos.csv` (exportado).  
2. `justificacion.md` (2–3 frases de defensa).  
3. Captura de pantalla de tu tabla o gráfica principal.
 
---
 
## ✅ Checklist rápido
- [ ] App desplegada en Streamlit Cloud.  
- [ ] Parámetros modificados y gráficos revisados.  
- [ ] Mini-experimentos A y B completados.  
- [ ] Caso aplicado defendido en 2–3 frases.  
- [ ] Entregables subidos (CSV + justificación + captura).  
 
---
 
## 📊 Rúbrica (evaluación rápida)
| Criterio | Excelente (2) | Adecuado (1) | Insuficiente (0) |
|----------|---------------|---------------|------------------|
| Ejecución técnica | App desplegada y usada | App desplegada pero exploración mínima | No desplegada |
| Análisis de métricas | Conecta datos con conclusiones | Menciona datos sin analizarlos | Vago o incorrecto |
| Defensa del caso | Justificación clara con evidencia | Justificación parcial | Sin justificación |
| Entregables | CSV + justificación + captura | Parcial | Faltan entregables |
 
---
 
## 📌 Nota
El modelo es **didáctico y simplificado**: no sustituye a un diseño industrial de red IoT.  
Sirve para **aprender compromisos** entre consumo, latencia, cobertura y duración de batería.
