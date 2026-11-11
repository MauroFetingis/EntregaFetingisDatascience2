# Ventas de videojuegos: patrones de éxito comercial

**Mauro Fetingis · Data Science II · Coderhouse**  
Primera entrega: obtención de insights a partir de visualizaciones.

## Problema y audiencia
¿Qué patrones históricos por género, plataforma y región pueden orientar la evaluación comercial de un catálogo? El análisis está dirigido a responsables de publicación, marketing y planificación comercial.

## Entregables
- `PrimeraEntrega_DSII_Fetingis.ipynb`: notebook ejecutado con resultados, gráficos y conclusiones.
- `dataset data science.csv`: base original, 16.598 filas y 11 columnas. Conservar exactamente este nombre.
- `Presentacion_DSII_Fetingis.pdf`: presentación ejecutiva de 11 diapositivas.
- `Presentacion_DSII_Fetingis.pptx`: versión editable de la presentación.
- `graficos/`: seis figuras generadas por el notebook.
- `resultados/`: base enriquecida, tablas de análisis, métricas y manifiesto de descarga.
- `requirements.txt`: dependencias para ejecución local.
- `GUIA_ENTREGA.md`: instrucciones para Colab, GitHub y entrega en el curso.

## Fuente
[Video Game Sales, Gregor Gregory, Kaggle](https://www.kaggle.com/datasets/gregorut/videogamesales).

El notebook usa el endpoint público `https://www.kaggle.com/api/v1/datasets/download/gregorut/videogamesales`, guarda una copia local y compara los valores con la base original. La descarga se verificó el 10 de noviembre de 2026 y coincidió con el CSV aportado. La fecha de descarga no actualiza los datos históricos. La fuente original mantiene sus propios términos de uso.

## Ejecución en Google Colab
1. Abrir [Google Colab](https://colab.research.google.com/).
2. Subir `PrimeraEntrega_DSII_Fetingis.ipynb`.
3. En el panel Archivos del entorno, subir `dataset data science.csv`.
4. Ejecutar todas las celdas en orden. La descarga de la fuente está activada.
5. Si se trabaja sin internet y el CSV ya está presente, cambiar `DESCARGAR_FUENTE = False`.
6. Descargar el notebook luego de ejecutar para conservar sus salidas.

La base local se utiliza para mantener la versión analizada. La celda informa si falla la descarga o si una versión futura de la fuente es diferente. El proyecto no necesita claves de API.

## Ejecución local
Con Python 3.10 o superior y una terminal en la carpeta del proyecto:

```bash
python -m pip install -r requirements.txt
python -m jupyterlab
```

Abrir el notebook y ejecutar las celdas de principio a fin. Las carpetas de resultados y gráficos se crean automáticamente.

## Metodología
Adquisición pública y control de procedencia, inspección de metadata, normalización de tipos y textos, revisión de duplicados y faltantes, enriquecimiento con variables derivadas y EDA univariado, bivariado y multivariado. No se imputan años para el análisis temporal. El editor desconocido se etiqueta explícitamente. Los valores extremos se conservan y se analizan con medianas y escala logarítmica.

## Resultados principales
- Action y Sports lideran en volumen total; Platform tiene la mayor mediana por registro.
- PS2 lidera plataformas; Nintendo representa aproximadamente 20.0 % de las ventas globales de la base.
- Role-Playing representa 27.3 % de las ventas de Japón, frente a 7.5 % en Norteamérica.
- Los lanzamientos de 2000–2009 concentran 52.06 % del total de ventas registrado.
- 12.54 % de los registros alcanza al menos 1 millón de unidades; el 10 % superior concentra 58.9 % del volumen.

## Limitaciones
La unidad de análisis es el registro por juego y plataforma. Las ventas se expresan en millones de unidades, no dólares. La muestra histórica no representa el mercado actual. Las ventas agrupadas por año de lanzamiento son acumuladas por cohorte y no ventas del año calendario. No se observan costos ni márgenes. Las asociaciones no demuestran causalidad.

## Alcance de esta entrega
El trabajo cubre adquisición, limpieza, visualizaciones e insights. La consigna general menciona Machine Learning, pero los requisitos base de esta primera entrega se centran en EDA. El notebook plantea el siguiente paso predictivo y los controles contra fuga de información, sin presentar modelos como entrenados.
