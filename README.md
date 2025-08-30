# COMSIGNS - Sistema de Reconocimiento de Lenguaje de Señas

## **📋 Descripción del Proyecto**

COMSIGNS es un sistema de reconocimiento de lenguaje de señas en tiempo real que utiliza visión por computadora y aprendizaje automático para traducir gestos de manos a texto. El sistema captura landmarks de la mano usando MediaPipe, los procesa con un modelo de red neuronal y puede enviar los resultados a un dispositivo Arduino para aplicaciones adicionales.

## **🎯 Características Principales**

- **Reconocimiento en tiempo real** de letras del alfabeto (A-Y, excluyendo J y Z)
- **Interfaz visual intuitiva** con predicciones en vivo
- **Comunicación con Arduino** para proyectos de hardware
- **Modelo de machine learning** entrenado con TensorFlow/Keras
- **Normalización de landmarks** para mayor precisión
- **Sistema de confianza** para filtrar predicciones inciertas

## **🛠️ Tecnologías Utilizadas**

- **Python 3.x**
- **OpenCV** - Procesamiento de video e imágenes
- **MediaPipe** - Detección y tracking de landmarks de manos
- **TensorFlow/Keras** - Modelo de aprendizaje automático
- **NumPy** - Operaciones numéricas
- **Scikit-learn** - División de datos y métricas
- **PySerial** - Comunicación con Arduino

## **📁 Estructura del Proyecto**

- **COMSIGNS-main/** - Directorio raíz del proyecto
  - **dataset/** - Datos de entrenamiento
    - `hand_data.npy` - Datos de entrenamiento (landmarks)
    - `hand_labels.npy` - Etiquetas correspondientes
  - **modelo/** - Modelo entrenado
    - `model.h5` - Modelo entrenado de Keras
  - **src/** - Código fuente principal
    - **generacion_modelo/** - Scripts para generar y entrenar modelo
      - `generacion_dataset.py` - Generación del dataset
      - `generacion_modelo.py` - Entrenamiento del modelo
    - **modules/** - Módulos del sistema
      - `arduino_com.py` - Comunicación con Arduino
      - `capturar_landmarks.py` - Captura de landmarks
      - `funcioness_modelo.py` - Funciones del modelo
    - `main.py` - Aplicación principal
    - `requirements.txt` - Dependencias
  - `README.md` - Documentación del proyecto

## **⚙️ Instalación y Configuración**

### **Prerrequisitos**

- Python 3.7 o superior
- Cámara web funcional
- (Opcional) Arduino para comunicación serial

### **Instalación de Dependencias**

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/COMSIGNS.git
cd COMSIGNS-main/src



# Instalar dependencias
pip install -r requirements.txt

# Dependencias Especificas
opencv-python
mediapipe
numpy
tensorflow
scikit-learn
pyserial  # Para comunicación con Arduino

