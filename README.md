# 📄 Prabstract – Automatización de Documentos Judiciales en Perú

Prabstract es una solución de Automatización Robótica de Procesos (RPA) desarrollada para facilitar la recopilación, análisis y categorización de documentos judiciales del portal del Poder Judicial del Perú. El sistema automatiza la descarga de PDFs, extrae datos relevantes usando IA y genera reportes gráficos, todo de forma autónoma cada 5 minutos.

## 🚀 Características
- 🔍 **Extracción automática de documentos** desde el sitio oficial del Poder Judicial.
- 🧠 **Procesamiento de texto con OpenAI** para extraer:
  - Nombre del caso
  - Ponente
  - Fecha
  - Lugar
  - Resumen
  - Categoría legal
- 📊 **Análisis visual**: generación de gráficos de frecuencia por fecha y categoría.
- 📈 **Reportes en Excel** con tablas y visualizaciones incrustadas.
- 📧 **Envío automático por correo electrónico** del reporte generado.

## 🏗️ Arquitectura
El flujo automatizado se compone de los siguientes pasos:
1. **Acceso web** al portal del Poder Judicial.
2. **Descarga de archivos PDF** con decisiones judiciales.
3. **Extracción de texto** con `pdfplumber`.
4. **Clasificación y resumen** usando la API de OpenAI.
5. **Organización de datos en Excel** usando `pandas` y `openpyxl`.
6. **Visualización de datos** mediante gráficos (`matplotlib`).
7. **Envío de los resultados** por correo electrónico (`smtplib`).

## 📦 Requisitos
- Python 3.10+
- ChromeDriver (compatible con tu versión de Chrome)
- Cuenta de OpenAI con API Key activa

### Instalación de dependencias
```bash
pip install -r requirements.txt

