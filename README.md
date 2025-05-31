# 🧠 Detección de Objetos en Video con YOLOv8

![License](https://img.shields.io/github/license/yourusername/deteccion-yolo)  
![Python](https://img.shields.io/badge/python-3.8%2B-blue)  
![Ultralytics](https://img.shields.io/badge/ultralytics-YOLOv8-green)  
![OpenCV](https://img.shields.io/badge/opencv-python-red)

Este proyecto utiliza **YOLOv8** (You Only Look Once) de [Ultralytics](https://github.com/ultralytics/ultralytics) para realizar inferencia sobre un video local. El script procesa el video, detecta objetos según un modelo entrenado previamente y guarda el resultado con las detecciones dibujadas.

---

## 📁 Estructura del Proyecto

```
Deteccion/
│
├── best.pt                          # Modelo entrenado YOLOv8 (.pt)
├── GH012372_no_audio.mp4            # Ejemplo de video de entrada
├── main.py                          # Script principal de detección
└── README.md                        # Este archivo
```

---

## 🚀 Funcionalidad del Código

El script hace lo siguiente:

1. **Importa librerías necesarias**, incluyendo OpenCV y Ultralytics.
2. **Configura rutas** para el modelo y el video de entrada.
3. **Carga el modelo YOLOv8** desde el archivo `.pt`.
4. **Verifica que el video exista** y obtiene sus propiedades (FPS, resolución, duración).
5. **Ejecuta la predicción** sobre el video usando `model.predict()` con parámetros configurables.
6. **Guarda el video procesado** con las detecciones dibujadas.
7. **Busca automáticamente el video de salida** y muestra información sobre él.

---

## 📦 Requisitos

Asegúrate de tener instalados los siguientes paquetes:

```bash
pip install opencv-python ultralytics
```

---

## ⚙️ Configuración

Antes de ejecutar el script, asegúrate de actualizar las siguientes variables en `main.py`:

```python
MODEL_PATH = 'ruta/a/tu/modelo/best.pt'
VIDEO_INPUT_PATH = 'ruta/a/tu/video.mp4'
```

También puedes ajustar los umbrales de confianza y de IoU si es necesario:

```python
CONF_ORIG = 0.3   # Umbral de confianza
IOU_ORIG = 0.5    # Umbral de IoU (Intersección sobre Unión)
```

---

## ▶️ Cómo Ejecutar

Desde la terminal, simplemente ejecuta:

```bash
python main.py
```

El video procesado se guardará en:

```
runs_original_working_structure/detect_video/<nombre_del_video>_processed_original/
```

---

## 📎 Salida del Programa

Una vez completado, el programa mostrará por consola:

- Información del modelo cargado
- Detalles del video de entrada
- Ruta del video procesado
- Verificación del video de salida (FPS, frames, duración)

---

## ✅ Resultado Esperado

Un nuevo video con las detecciones realizadas por el modelo YOLOv8 será creado en la carpeta de salida. Puedes abrir este video con cualquier reproductor compatible.

---

## 📌 Notas Adicionales

- Si deseas limpiar carpetas antiguas antes de ejecutar, descomenta la sección de limpieza en el código.
- Asegúrate de usar una GPU si es posible para acelerar el proceso de inferencia.
- Puedes añadir más parámetros como `imgsz`, `show`, o `save_frames` según tus necesidades.

---

## 🛡️ Licencia

MIT License - Consulta el archivo `LICENSE` para más información.
![License](https://img.shields.io/github/license/ocjorgeoc/DeteccionObjetos) 

---

🎉 ¡Esperamos que este script te sea útil para realizar detección de objetos en videos de manera sencilla!

