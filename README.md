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

## 🔧 Configuración

1. Define tu **API Key** de OpenAI en el archivo `.env` o directamente en el código.
2. Ajusta el **path de ChromeDriver** según tu entorno local.
3. Configura el **remitente y la contraseña del correo** (preferiblemente utilizando variables de entorno o almacenamiento seguro).

## 🧠 Clasificación Legal

El sistema es capaz de reconocer y clasificar automáticamente documentos en las siguientes categorías legales:

- Litigios
- Contratos
- Propiedad Intelectual
- Cumplimiento Normativo
- Recursos Humanos
- Corporativo
- Penal
- Tributario
- Ambiental

## 📤 Salidas

El sistema genera los siguientes archivos y reportes:

- **Excel**: con la estructura tabular y resumen de los documentos procesados.
- **Gráficos**: de distribución por fecha y categoría.
- **Correo electrónico**: con el archivo Excel adjunto.

## 🧪 Ejecución

Para ejecutar el flujo completo (desde la descarga de PDFs hasta el envío del correo con el reporte), simplemente corre el siguiente comando:

```bash
python prabstract.py
```

## 📈 Resultados Esperados

- Mayor eficiencia en el análisis de documentos judiciales, procesando grandes volúmenes de información en menor tiempo.
- Reducción de errores humanos en la clasificación de los documentos.
- Visualización de patrones judiciales y fechas clave a través de los gráficos generados.
- Mejora en la toma de decisiones basada en análisis de datos claros y precisos.

## 🛡️ Seguridad

Este proyecto es una **prueba de concepto académica**. Se recomienda implementar mecanismos adicionales de autenticación y protección de credenciales antes de usarlo en un entorno de producción. Además, se debe garantizar el cumplimiento de normativas de privacidad y seguridad de la información.

