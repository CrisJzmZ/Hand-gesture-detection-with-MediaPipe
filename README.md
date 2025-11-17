# 🖐️ Detección de Gestos y Conteo de Dedos con MediaPipe

Este es un proyecto de visión por computadora en Python que utiliza **OpenCV** y **MediaPipe** para detectar y rastrear manos en tiempo real. La aplicación puede contar el número de dedos levantados (hasta 10, usando ambas manos) y reconocer gestos específicos como "Like" 👍, "Dislike" 👎, y "OK" 👌.



## 🌟 Características

* **Detección de Manos en Tiempo Real:** Utiliza MediaPipe Hands para un seguimiento rápido y preciso de los 21 puntos de referencia de la mano.
* **Soporte para Múltiples Manos:** Capaz de detectar y procesar hasta dos manos simultáneamente.
* **Conteo de Dedos:** Cuenta el número total de dedos levantados (de 0 a 10).
* **Reconocimiento de Gestos:** Identifica gestos estáticos específicos (Like, Dislike, OK).
* **Visualización Completa:** Dibuja el esqueleto de la mano, los puntos de referencia (landmarks) y muestra la información del gesto y el conteo en pantalla.

## 🛠️ Instalación y Requisitos

Este proyecto fue desarrollado en Python (se recomienda 3.9 - 3.11) y requiere varias bibliotecas específicas. La instalación puede ser compleja debido a conflictos de dependencias entre `tensorflow` y `mediapipe`.

Se recomienda encarecidamente usar un **entorno virtual** (`venv`) para este proyecto.

### 1. Clonar el repositorio

```bash
git clone [https://github.com/CrisJzmZ/Hand-gesture-detection-with-MediaPipe.git](https://github.com/CrisJzmZ/Hand-gesture-detection-with-MediaPipe.git)
cd Hand-gesture-detection-with-MediaPipe
```

### 2. Crear y activar un Entorno Virtual

```bash
# Crear el entorno
python -m venv .venv

# Activar en Windows (PowerShell)
.\.venv\Scripts\Activate.ps1

# Activar en Windows (Git Bash / CMD)
.venv\Scripts\activate
```

### 3. Instalar las dependencias

El orden de instalación y las versiones son importantes para evitar conflictos.

```bash
# 1. Instala OpenCV y MediaPipe
pip install opencv-python mediapipe

# 2. Instala TensorFlow completo
# (Necesario para los modelos .tflite y para evitar conflictos)
pip install tensorflow

# 3. Asegúrate de que protobuf esté actualizado
# (Resuelve conflictos entre tensorflow y mediapipe)
pip install --upgrade protobuf
```

## Cómo Ejecutar

Una vez que tu entorno virtual esté activado y todas las dependencias estén instaladas, simplemente ejecuta el script principal:

```bash
python app.py
```

La aplicación abrirá una ventana mostrando la captura de tu cámara web.

### Controles

* **ESC**: Presiona la tecla `ESC` para cerrar la aplicación.
