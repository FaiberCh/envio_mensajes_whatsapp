# Envío de Mensajes por WhatsApp con Python
Este proyecto permite enviar mensajes personalizados a través de WhatsApp Web utilizando Python. La funcionalidad principal incluye la validación de números de teléfono, la medición de la duración de la ejecución y la capacidad de adjuntar archivos, como videos, al mensaje.

## Funciones Principales
**1. Validación de Números de Teléfono**

  La función is_valid_number(number) verifica que el número de teléfono tenga 10 dígitos, sea numérico y comience con '3'. Esto asegura que solo se envíen mensajes a números válidos.

**2. Envío de Mensajes**

  La función send_whatsapp_messages(df, var, ruta_video) permite enviar mensajes a una lista de números de teléfono almacenados en un DataFrame. Esta incluye:
  - Validación del número antes de enviar el mensaje.
  - Opciones para adjuntar un archivo (como un video) a los mensajes.
  - Selección aleatoria de mensajes promocionales para hacer la comunicación más dinámica.

**3. Manejo de Errores**

El sistema captura y registra errores durante el envío, permitiendo identificar problemas con números inválidos o fallos en la conexión.

## Requisitos
- `Python 3.x`
  
- Bibliotecas:
  - `pandas`
  - `re`
  - `io`
  - `sys`
  - `time`
  - `webbrowser`
  - `pyautogui`
  - `pyperclip`

    
## Cómo Usar
- Asegúrate de tener instaladas las bibliotecas necesarias.
- Prepara un DataFrame con los números de teléfono que deseas contactar.
- Llama a la función send_whatsapp_messages() con el DataFrame, la columna que contiene los números y la ruta del video que deseas adjuntar.

## Ejemplo de Uso

```python
import pandas as pd

# Crear un DataFrame de ejemplo
df = pd.DataFrame({'número': ['3123456789', '3134567890']})

# Llamar a la función para enviar mensajes
send_whatsapp_messages(df, 'número', '/ruta/al/video.mp4')
```

## Notas
- Este script abre WhatsApp Web en tu navegador, por lo que debes asegurarte de que estés conectado y que el chat esté disponible.
- Las coordenadas para hacer clic en los elementos de la interfaz de WhatsApp pueden necesitar ajustes según la resolución de tu pantalla.
