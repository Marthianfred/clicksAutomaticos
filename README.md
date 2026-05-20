# Clicks Automáticos - Automatizador Avanzado v2.0

Este proyecto es una herramienta de automatización de interfaz de usuario (GUI) desarrollada en Python. Permite grabar y ejecutar secuencias de acciones (clics, escritura, esperas) e incluye capacidades avanzadas de lógica condicional mediante Reconocimiento Óptico de Caracteres (OCR).

## Características principales

- **Interfaz Gráfica (Tkinter):** Panel de control intuitivo para gestionar acciones.
- **Acciones Simples:** Clics, doble clics, escritura de texto y tiempos de espera.
- **Acciones Condicionales (OCR):** Ejecución de acciones basada en la detección de texto en regiones específicas de la pantalla usando Tesseract.
- **Gestión de Configuraciones:** Guarda y carga tus secuencias de automatización en archivos JSON.
- **Seguridad (Failsafe):** Mueve el ratón a cualquier esquina de la pantalla para detener la ejecución inmediatamente.
- **Multihilo:** La ejecución se realiza en segundo plano para no bloquear la interfaz.

## Requisitos Previos

1. **Python 3.12+**
2. **Tesseract OCR:** Es necesario para las funciones de lectura de texto en pantalla.
   - Descarga el instalador para Windows desde [aquí](https://github.com/UB-Mannheim/tesseract/wiki).
   - Asegúrate de que esté instalado en `C:\Program Files\Tesseract-OCR\tesseract.exe` (ruta predeterminada).

## Instalación

Sigue estos pasos para configurar el entorno:

```powershell
# 1. Clonar el repositorio (o entrar a la carpeta)
cd clicksAutomaticos

# 2. Crear entorno virtual
python -m venv venv

# 3. Activar entorno virtual
# Windows:
.\venv\Scripts\activate

# 4. Instalar dependencias
pip install -r requirements.txt
```

## Uso

Para iniciar la aplicación principal:

```powershell
python automatizador_formularios.py
```

### Guía rápida:
1. **Agregar Acción:** Usa "Agregar Simple" para movimientos y clics básicos.
2. **Acción Condicional:** Selecciona una región de la pantalla y define qué texto debe buscar la aplicación para realizar la acción.
3. **Guardar:** No olvides guardar tu configuración para usarla en el futuro.
4. **Detener:** Presiona la tecla `SUPR` (Delete) o usa el mecanismo de seguridad (esquina de pantalla) para detener una ejecución en curso.

## Estructura del Proyecto

- `automatizador_formularios.py`: Aplicación principal con interfaz gráfica completa.
- `automatizador_no_close_session.py`: Versión simplificada para mantener sesiones activas.
- `requirements.txt`: Lista de librerías necesarias.
- `venv/`: Entorno virtual de Python (generado localmente).
