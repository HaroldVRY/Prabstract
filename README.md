📄 Prabstract – Automatización de Documentos Judiciales en Perú
Prabstract es una solución de Automatización Robótica de Procesos (RPA) desarrollada para facilitar la recopilación, análisis y categorización de documentos judiciales del portal del Poder Judicial del Perú. El sistema automatiza la descarga de PDFs, extrae datos relevantes usando IA y genera reportes gráficos, todo de forma autónoma cada 5 minutos.

🚀 Características
🔍 Extracción automática de documentos desde el sitio oficial del Poder Judicial.

🧠 Procesamiento de texto con OpenAI para extraer:

Nombre del caso

Ponente

Fecha

Lugar

Resumen

Categoría legal

📊 Análisis visual: generación de gráficos de frecuencia por fecha y categoría.

📈 Reportes en Excel con tablas y visualizaciones incrustadas.

📧 Envío automático por correo electrónico del reporte generado.

🏗️ Arquitectura
El flujo automatizado se compone de los siguientes pasos:

Acceso web al portal del Poder Judicial.

Descarga de archivos PDF con decisiones judiciales.

Extracción de texto con pdfplumber.

Clasificación y resumen usando la API de OpenAI.

Organización de datos en Excel usando pandas y openpyxl.

Visualización de datos mediante gráficos (matplotlib).

Envío de los resultados por correo electrónico (smtplib).

📦 Requisitos
Python 3.10+

ChromeDriver (compatible con tu versión de Chrome)

Cuenta de OpenAI con API Key activa

Instalación de dependencias
bash
Copiar
Editar
pip install -r requirements.txt
requirements.txt sugerido:

txt
Copiar
Editar
pdfplumber
openai
pandas
matplotlib
openpyxl
selenium
🔧 Configuración
Define tu API Key de OpenAI en el archivo .env o directamente en el código.

Ajusta el path de chromedriver a tu entorno local.

Configura el remitente y la contraseña de correo (preferiblemente con variables de entorno o almacenamiento seguro).

🧠 Clasificación Legal
El sistema reconoce automáticamente categorías legales como:

Litigios

Contratos

Propiedad Intelectual

Cumplimiento Normativo

Recursos Humanos

Corporativo

Penal

Tributario

Ambiental

📤 Salidas
Excel con estructura tabular y resumen de documentos.

Gráficos de distribución por fecha y categoría.

Correo con reporte adjunto.

🧪 Ejecución
python
Copiar
Editar
python prabstract.py
Esto ejecutará el flujo completo, desde la descarga hasta el envío del correo.

📈 Resultados Esperados
Mayor eficiencia en el análisis de documentos judiciales.

Reducción de errores humanos en la clasificación.

Visualización de patrones judiciales y fechas clave.

Mejora en la toma de decisiones basada en datos.

🛡️ Seguridad
Este proyecto es una prueba de concepto académica. No se recomienda su uso en producción sin antes aplicar mecanismos robustos de autenticación, protección de credenciales y cumplimiento normativo.
